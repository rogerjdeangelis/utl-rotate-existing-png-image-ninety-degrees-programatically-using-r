# utl-rotate-existing-png-image-ninety-degrees-programatically-using-r
Rotate existing png image ninety degrees programatically using r
    %let pgm=utl-rotate-existing-png-image-ninety-degrees-programatically-using-r;

    Rotate existing png image ninety degrees programatically using r

    Input landscape
    http://tinyurl.com/mwm7tnvn
    https://github.com/rogerjdeangelis/utl-rotate-existing-png-image-ninety-degrees-programatically-using-r/blob/main/landscape.png

    output portrait
    http://tinyurl.com/mr3x2tj2
    https://github.com/rogerjdeangelis/utl-rotate-existing-png-image-ninety-degrees-programatically-using-r/blob/main/portrait.png

    github
    http://tinyurl.com/5f5txdrj
    https://github.com/rogerjdeangelis/utl-rotate-existing-png-image-ninety-degrees-programatically-using-r

    /**************************************************************************************************************************/
    /*                              |                                                                  |                      */
    /*                              |                                                                  |                      */
    /*                              |                                                                  |                      */
    /*            INPUT             |                 PROCESS                                          |      OUTPUT          */
    /*                              |                                                                  |                      */
    /*       d:/png/lanscape.png    |                                                                  |  d:/png/portrait.png */
    /*                              |                                                                  |                      */
    /*                              |                                                                  |                      */
    /*   |   |  -----  |      ----- | newlogo <- image_read("d:/png/landscape.png");                   |   -------------      */
    /*   |   |    |    |        |   | newlogo <- image_scale(newlogo, "1280x800");                     |         |            */
    /*   |   |    |    |        |   | image_rotate(newlogo, 90) %>% image_write("d:/png/portrait.png") |         |            */
    /*   |---|    |    |        |   |                                                                  |         |            */
    /*   |   |    |    |        |   |                                                                  |   -------------      */
    /*   |   |    |    |        |   |                                                                  |                      */
    /*   |   |  -----  -----    |   |                                                                  |   |           |      */
    /*                              |                                                                  |   |-----------|      */
    /*                              |                                                                  |   |           |      */
    /*                              |                                                                  |                      */
    /*                              |                                                                  |   ------------       */
    /*                              |                                                                  |   |                  */
    /*                              |                                                                  |   |                  */
    /*                              |                                                                  |               |      */
    /*                              |                                                                  |               |      */
    /*                              |                                                                  |   |-----------|      */
    /*                              |                                                                  |               |      */
    /*                              |                                                                  |               |      */
    /*                              |                                                                  |                      */
    /**************************************************************************************************************************/

    /*                   _
    (_)_ __  _ __  _   _| |_
    | | `_ \| `_ \| | | | __|
    | | | | | |_) | |_| | |_
    |_|_| |_| .__/ \__,_|\__|
            |_|
    */

    %utl_rbegin;
    parmcards4;
    library(ggplot2)
    library(ggtext)
       landscape <- data.frame(
          x = 1
         ,y = 1
         ,label = "<span style='font-size: 100pt'>HILT</span>"
         );
       png("d:/png/landscape.png");
       ggplot(landscape) +
         ggtext::geom_textbox(aes(x = x, y = y ,label = label)
           ,box.colour = NA
           ,width = unit(10, "cm")) + theme_void();
    ;;;;
    %utl_rend;

    /**************************************************************************************************************************/
    /*                                                                                                                        */
    /*            INPUT                                                                                                       */
    /*                                                                                                                        */
    /*       d:/png/lanscape.png                                                                                              */
    /*                                                                                                                        */
    /*                                                                                                                        */
    /*   |   |  -----  |      -----                                                                                           */
    /*   |   |    |    |        |                                                                                             */
    /*   |   |    |    |        |                                                                                             */
    /*   |---|    |    |        |                                                                                             */
    /*   |   |    |    |        |                                                                                             */
    /*   |   |    |    |        |                                                                                             */
    /*   |   |  -----  -----    |                                                                                             */
    /*                                                                                                                        */
    /**************************************************************************************************************************/

    /*
     _ __  _ __ ___   ___ ___  ___ ___
    | `_ \| `__/ _ \ / __/ _ \/ __/ __|
    | |_) | | | (_) | (_|  __/\__ \__ \
    | .__/|_|  \___/ \___\___||___/___/
    |_|
    */

    %utl_rbegin;
    parmcards4;
    library(magick);
    library(dplyr);
    newlogo <- image_read("d:/png/landscape.png");
    newlogo <- image_scale(newlogo, "1280x800");
    image_rotate(newlogo, 90) %>% image_write("d:/png/portrait.png");
    ;;;;
    %utl_rend;

    /**************************************************************************************************************************/
    /*                                                                                                                        */
    /*                                                                                                                        */
    /*                                                                                                                        */
    /*      OUTPUT                                                                                                            */
    /*                                                                                                                        */
    /*  d:/png/portrait.png                                                                                                   */
    /*                                                                                                                        */
    /*                                                                                                                        */
    /*   -------------                                                                                                        */
    /*         |                                                                                                              */
    /*;        |                                                                                                              */
    /*         |                                                                                                              */
    /*   -------------                                                                                                        */
    /*                                                                                                                        */
    /*   |           |                                                                                                        */
    /*   |-----------|                                                                                                        */
    /*   |           |                                                                                                        */
    /*                                                                                                                        */
    /*   ------------                                                                                                         */
    /*   |                                                                                                                    */
    /*   |                                                                                                                    */
    /*               |                                                                                                        */
    /*               |                                                                                                        */
    /*   |-----------|                                                                                                        */
    /*               |                                                                                                        */
    /*               |                                                                                                        */
    /*                                                                                                                        */
    /**************************************************************************************************************************/

    /*              _
      ___ _ __   __| |
     / _ \ `_ \ / _` |
    |  __/ | | | (_| |
     \___|_| |_|\__,_|

    */
