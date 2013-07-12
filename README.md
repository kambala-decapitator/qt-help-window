qt-help-window
==============

A C++/Qt class to show simple window with HTML help.

Usage example:

    QDialogButtonBox *buttonBox = new QDialogButtonBox(QDialogButtonBox::Ok | QDialogButtonBox::Help, Qt::Horizontal, this);
    HelpWindowDisplayManager *helpDislplayManager = new HelpWindowDisplayManager(this, tr("My help title"),
        tr(
        "My <b><i>bold italic help text</i></b>"
        "<h3>My heading</h3>"
        "<a href=\"https://github.com/kambala-decapitator/qt-help-window\">My URL</a>"
        ));
    connect(buttonBox, SIGNAL(helpRequested()), helpDislplayManager, SLOT(showHelp()));
    connect(buttonBox, SIGNAL(accepted()),      helpDislplayManager, SLOT(closeHelp()));

Result:

![](http://i1125.photobucket.com/albums/l592/kambala_decapitator/qt_help_window.png)
