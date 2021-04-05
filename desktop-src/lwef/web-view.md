---
title: Anpassen der Webansicht eines Ordners
description: Eine Webansicht ist eine leistungsstarke und flexible Möglichkeit, den Windows-Explorer zu verwenden, um Informationen zum Inhalt eines shellordners anzuzeigen.
ms.assetid: a894df21-bcc6-4760-b7d7-9bf95a0dba7f
keywords:
- Webansichten
- Klassisches Format
- Webstil
- Banner
- FileList-Region
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e364551d461eff6ae17a780bafc0b69182a1f16f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724696"
---
# <a name="customizing-a-folders-web-view"></a>Anpassen der Webansicht eines Ordners

\[Dieses Feature wird nur unter Windows XP oder früher unterstützt. \]

Eine Webansicht ist eine leistungsstarke und flexible Möglichkeit, den Windows-Explorer zu verwenden, um Informationen zum Inhalt eines shellordners anzuzeigen.

-   [Introduction (Einführung)](#introduction)
-   [Verwenden der webansichts Vorlage](#using-the-web-view-template)
    -   [Der Vorlagen Text](#the-template-body)
    -   [Der Vorlagen Kopf](#the-template-head)
-   [Zusammenfassung](#summary)

## <a name="introduction"></a>Einführung

Windows bietet Benutzern zwei Hauptmöglichkeiten, den Shellnamespace anzuzeigen und zu navigieren. Die am häufigsten vertrauten, der klassischen Stil, ähneln dem vertrauten Windows-Datei-Manager. Im rechten Bereich wird der Inhalt des aktuell ausgewählten Ordners in einem von fünf Formaten aufgelistet: großes Symbol, kleines Symbol, Liste, Details und Miniaturansicht. Der Hauptunterschied zwischen dem Windows-Datei-Manager ist der linke Bereich, der der Explorer-Leiste von Windows Internet Explorer ähnelt. Die Größe kann geändert oder entfernt werden, und es können neben der vertrauten Dateisystem Struktur auch mehrere Bereiche angezeigt werden, z. b. ein Suchbereich.

> [!Note]  
> Die Informationen in diesem Dokument gelten nicht für Windows XP, die behandelten Techniken gelten nur für frühere Versionen von Windows.

 

Die folgende Abbildung zeigt den Ordner Drucker im klassischen Stil.

![klassisches Format des Drucker Ordners.](images/webview1.png)

Der klassische Stil eignet sich gut für normale Dateisystem Ordner und-Dateien. Allerdings hat sich das Dateisystem mit der Einführung von Windows 95 in den-Namespace weiterentwickelt. Der-Namespace ermöglicht die Erstellung *virtueller Ordner*, z. b. Drucker oder Netzwerkumgebung, die sehr unterschiedliche Informationstypen darstellen können als ein normaler Dateisystem Ordner.

Der Webstil, auch bekannt als Webansicht, bietet eine flexiblere und leistungsfähigere Möglichkeit zur Darstellung von Informationen als klassischer Stil. In einer Webansicht zeigt der Benutzer den Namespace im Grunde mithilfe von Internet Explorer an und navigiert ihn. Das grundlegende Layout einer Webansicht ähnelt dem klassischen Stil. Die Explorer-Leiste ist unverändert. Die Region, die in der Datei Liste enthalten war, wird jedoch zu einem allgemeinen Anzeigebereich, bei dem es sich eigentlich um eine Webseite handelt. Eine Webansicht wird weiterhin zum Anzeigen von Informationen über den Inhalt eines Ordners verwendet. es gibt jedoch einige Einschränkungen, welche Informationen angezeigt werden, oder wie. Jeder Ordner kann über eine eigene Webansicht verfügen, die an die jeweiligen Features angepasst ist.

Die folgende Abbildung zeigt eine Webansicht des Ordners "Printers" (im klassischen Stil dargestellt).

![Standardweb Ansicht des Ordners "Drucker".](images/webview2.png)

Ähnlich wie herkömmliche Webseiten werden Webansichten von einer HTML-basierten Vorlage gesteuert. Das Erstellen einer webansichts Vorlage ist nahezu identisch mit dem Erstellen einer Webseite und bietet das gleiche Maß an Flexibilität in den Inhalten und dem Layout von Informationen. Webansichts Vorlagen können dynamisches HTML (DHTML) und Skripts verwenden, um auf Ereignisse zu reagieren, z. b. ein Benutzer, der auf ein Element klickt. Sie können auch Objekte hosten, die es Ihnen ermöglichen, Informationen aus dem Ordner oder dessen Inhalt abzurufen und anzuzeigen.

Der Benutzer kann eine Webansicht auswählen, indem er Windows-Explorer startet, im Menü **Ansicht** auf **Ordneroptionen** klickt und diese Option **aktiviert: Webinhalt in Ordnern aktivieren**. Der Benutzer kann jedoch auch Internet Explorer starten und den Browser auf das Dateisystem verweisen, indem er auf das Menü **Ansicht** , auf **Explorer-Leiste** zeigt und auf **Ordner** klickt. In einer Webansicht gibt es praktisch keinen Unterschied zwischen Internet Explorer und Windows Explorer.

Auf der linken Seite des rechten Bereichs wird in der Drucker Webansicht ein Banner mit dem Namen und dem Symbol des Ordners angezeigt, gefolgt von einem Informationsblock zum Ordner. Die übliche Datei Liste befindet sich auf der rechten Seite der Seite.

Wenn ein Benutzer auf ein Element klickt, werden ausführliche Informationen über das Element im Informationsblock angezeigt. Die Drucker-Webansicht zeigt tatsächlich die gleichen Informationen an, die im klassischen Stil verfügbar sind, aber in einem besser verwendbaren Format. Allerdings ist eine Webansicht nicht einfach eine andere Möglichkeit, um klassische Stil Informationen anzuzeigen. Beispielsweise kann ein Link zu einer nützlichen Website unter dem Informationsblock angezeigt werden, einem Feature, das im klassischen Stil nicht verfügbar ist. Wenn der Benutzer auf den Link klickt, wird die Website angezeigt.

Die in der obigen Abbildung gezeigte Drucker-Webansicht ähnelt dem klassischen Stil, da die zugrunde liegende webansichts Vorlage (eine htt-Datei) auf diese Weise geschrieben wurde. Die Liste der Dateien wird beispielsweise nicht direkt von der webansichts Vorlage generiert. Es wird von einem [**webviewfoldercontents**](webviewfoldercontents.md) -Objekt erstellt und angezeigt, das von der webansichts Vorlage gehostet wird. Mit den Methoden und Eigenschaften des Objekts kann die Webansicht das Layout Steuern und Informationen zu bestimmten Elementen abrufen. Der Inhalt und das Layout des Banners und des Informations Blocks werden in der webansichts Vorlage angegeben.

Da eine Webansicht DHTML unterstützt, kann die Vorlage auch verwendet werden, um die Benutzerinteraktion zu verarbeiten. Wenn ein Benutzer beispielsweise auf eines der Drucker Symbole klickt, löst das **WebViewFolderIcon** -Objekt ein [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) -Ereignis aus. Die Vorlage verwendet einen im Skript geschriebenen DHTML-Ereignishandler, um die angeforderten Informationen abzurufen und im Informationsblock anzuzeigen.

Dieses einfache Beispiel für den Drucker Ordner ist nicht die einzige Möglichkeit, eine Webansicht zu verwenden. Wenn Sie Ihre eigene Vorlage schreiben und ggf. Objekte verwenden, können Sie eine Webansicht verwenden, um Informationen anzuzeigen und mit dem Benutzer auf die gewünschte Weise zu interagieren. Beachten Sie, dass webansichts Vorlagen derzeit nur System definierte virtuelle Ordner anzeigen. Obwohl Entwickler einen virtuellen Ordner erstellen können, indem Sie eine Namespace Erweiterung implementieren, müssen Sie die unter [Namespace Erweiterungen](/windows/desktop/shell/nse-works) beschriebenen Techniken verwenden, um Sie anzuzeigen.

## <a name="using-the-web-view-template"></a>Verwenden der webansichts Vorlage

Die Art und Weise, in der Daten in einer Webansicht angezeigt werden, kann durch Ändern der Desktop.ini Datei eines Ordners eingeschränkt angepasst werden. Weitere Informationen finden Sie [unter Anpassen von Ordnern mit Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) . Eine viel flexiblere und leistungsfähigere Möglichkeit zum Anpassen einer Webansicht besteht darin, eine benutzerdefinierte webansichtenvorlage zu erstellen.

Die Vorlage Webansicht steuert, was in einer Webansicht angezeigt wird und wie. Dabei werden standardmäßige HTML-, DHTML-und Skript Verfahren verwendet, um Informationen abzurufen und anzuzeigen und mit dem Benutzer zu interagieren. In diesem Abschnitt wird erläutert, wie Sie eine Webansicht erstellen, indem Sie eine einfache Vorlage – Generic. htt) untersuchen.


```
<html>
    <style>
    <!-- This section defines a variety of styles that can be used
     when displaying the document -->
        body        {font: 8pt/10pt verdana; margin: 0}
        #Banner     {position: absolute; width: 100%; height: 88px; background: URL(res://webvw.dll/folder.gif) no-repeat top left}
        #MiniBanner {position: absolute; width: 100%; height: 32px; background: window}
        #Icon       {position: absolute; left: 11px; top: 12px; width: 64px; height: 64px}
        #FileList   {position: absolute; left: 30%; top: 88px; width: 1px; height: 1px}
        #Info       {position: absolute; top: 88px; width: 30%; background: window; overflow: auto}
        p       {margin-left: 20px; margin-right: 8px}
        p.Title     {font: 16pt/16pt verdana; font-weight: bold; color: #0099FF}
        a:link      {color: #FF6633}
        a:visited   {color: #0099FF}
        a:active    {color: black}
    </style>

    <head>
        <!-- allow references to any resources you might add to the
         folder -->
        <base href="%THISDIRPATH%\">

        <script language="JavaScript">
        
        <!-- This section defines a number of JavaScript utilities -->
            var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br><br>To get information about any of them, click the items icon.<br><br>";
            var L_Multiple_Text = " objects selected.";

            function FixSize() {
            // this function handles layout issues not covered by the style sheet

                var hideTop = 200;
                var hideLeft    = 400;
                var miniHeight  = 32;

                if (200 > document.body.clientHeight) {
                //A short window. Use the minibanner
                    document.all.Banner.style.visibility = "hidden";
                    document.all.MiniBanner.style.visibility = "visible";
                    document.all.FileList.style.top = 32;
                    document.all.Info.style.top = 32;
                }

                else {
                //A normal window. Use the normal banner
                    document.all.Banner.style.visibility = "visible";
                    document.all.MiniBanner.style.visibility = "hidden";
                    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
                    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
                    document.all.Rule.style.width = (document.body.clientWidth > 84 ? document.body.clientWidth - 84 : 0) + "px";     
                }
                if (400 > document.body.clientWidth) {
                //A narrow window. Hide the Info region and expand the file list region
                    document.all.Info.style.visibility = "hidden";
                    document.all.FileList.style.pixelLeft = 0;
                    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
                }

                else {
                //Normal width
                    document.all.Info.style.visibility = "visible";
                    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
                }
                document.all.FileList.style.pixelWidth = document.body.clientWidth - document.all.FileList.style.pixelLeft;
                document.all.FileList.style.pixelHeight = document.body.clientHeight - document.all.FileList.style.pixelTop;
                document.all.Info.style.pixelHeight = document.body.clientHeight - document.all.Info.style.pixelTop;
            }

            function Init() {
                /* Set the initial layout and have FixSize() called whenever the window is resized*/
                window.onresize = FixSize;
                FixSize();
                TextBlock.innerHTML = L_Intro_Text;
            }
        </script>

        <script language="JavaScript" for="FileList" event="SelectionChanged">
            // Updates the TextBlock region when an item is selected
            var data;
            var text;

            // name
            text = "<b>" + FileList.FocusedItem.Name + "</b>";

            // comment
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
            if (data)
                text += "<br>" + data;

            // documents
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
            if (data)
                text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

            // status
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
            if (data)
                text += "<br><br><b><font color=red>" + data + "</font></b>";

            // tip?
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
            if (data != "" && data != FileList.FocusedItem.Name)
                text += "<br><br>" + data;

            TextBlock.innerHTML = text;
        </script>
    </head>
<!-- The body of the document controls the actual data display.
 It uses several scripting objects to communicate with the
 namespace folder, and calls on the JavaScript objects defined
 in the header to handle much of the processing -->
    <body scroll=no onload="Init()">

        <!-- The normal banner. This banner displays the folder
         name and icon at the top of the WebView pane. This banner
         is used if the WebView pane is sufficiently large to
         display the icon and still have room for some information -->
        <div id="Banner" style="visibility: hidden">
            <!-- Display the folder name using a table with nowrap
             to prevent word wrapping. Explorer will replace
              %THISDIRNAME% with the current folder name -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 104px; margin-top: 16px">
                %THISDIRNAME% 
            </td></tr></table>
            <!-- this is more efficient than a long graphic, but it has to be adjusted in FixSize() -->
            <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
            <!-- Load the WebViewFolderIcon object, which extracts the folder's icon -->
            <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
                <param name="scale" value=200>
            </object>
        </div>

        <!-- The mini banner. This banner is used when the
         WebView pane is too short to display the icon. Instead,
          it displays only the folder name -->
        <div id="MiniBanner" style="visibility: hidden">
            <!-- use a table with nowrap to prevent word wrapping -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 16px; margin-top: 4px">
                %THISDIRNAME%
            </td></tr></table>
        </div>

        <!-- The Info region. This displays the information
         associated with a folder or file. Javascript in the header
         is used to generate the regions contents by by assigning
         a text block to TextBlock.innerHTML -->
        <div id="Info">
            <p style="margin-top: 16px");
            <span id="TextBlock">
            </span>
        </div>
        <!-- end left info panel -->

        <!-- Load the WebViewFolderContents object. This object
         returns information on the contents of the folder that
          can be used in the information display.  -->
        <object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>

    </body>
</html>
            
```



Eine einfache Möglichkeit zum Erstellen einer eigenen webansichtenvorlage besteht darin, Generic. htt zu erstellen und zu ändern. Da es ziemlich eingeschränkt ist, sollten Sie auch andere, komplexere Beispiele für weitere Ideen betrachten. Sie können Sie finden, indem Sie in Ihrem System nach der von allen webansichts Vorlagen verwendeten htt-Erweiterung suchen. Wenn Sie eine benutzerdefinierte Vorlage für einen Ordner erstellen möchten, sollten Sie mit der standardmäßigen htt-Vorlage "Folder" beginnen, die normalerweise entweder in "C: \\ Winnt \\ Web" oder "c: \\ Windows \\ Web" gespeichert ist. Beachten Sie, dass diese Dateien als ausgeblendet definiert sind. Daher müssen Sie möglicherweise die Windows-Explorer-Einstellungen ändern, um Sie anzuzeigen. Nachdem eine htt-Datei erstellt wurde, sollte Sie als schreibgeschützt markiert und ausgeblendet werden.

Webansichts Vorlagen verwenden die Erweiterung ". htt", da Sie sich geringfügig von herkömmlichen htm-Dokumenten unterscheiden. Der Hauptunterschied besteht aus mehreren speziellen Variablen in htt-Dateien, die das System durch die aktuellen Namespace Werte ersetzt. Die Variablen "% thisdir%" und "% thisdirpath%" stellen den Namen und den Pfad des aktuell ausgewählten Ordners dar. Die% templatedir%-Variable stellt den Ordner dar, in dem die Stylesheets der Webansicht gespeichert werden.

Wie die meisten HTML-Vorlagen bestehen auch htt-Dateien aus zwei grundlegenden Teilen: einem Text und einem Head. Der Vorlagen Text steuert das grundlegende Layout der Webansicht und lädt die Objekte, die für die Kommunikation mit dem Namespace und den Anzeigeinformationen verwendet werden. Die Kopfzeile enthält Skripts und Funktionen, die Aufgaben wie das Bearbeiten der Größe und das Abrufen von Informationen aus dem Ordner ausführen. Die meisten Vorlagen, einschließlich Generic. htt, enthalten auch ein Stylesheet. Im Allgemeinen ist es besser, die Stylesheet-Informationen in Ihre Vorlage einzubeziehen. Separate Stylesheets funktionieren möglicherweise nicht ordnungsgemäß, wenn eine Webansicht mit remotenamespaces verwendet wird.

### <a name="the-template-body"></a>Der Vorlagen Text

Der Text der Vorlage gibt an, was von einer Webansicht angezeigt wird. Außerdem werden die Objekte, die zum Anzeigen von Informationen und zum kommunizieren mit Namespace Ordnern verwendet werden, geladen. Das von Generic. htt definierte Layout ähnelt dem in der Abbildung im vorherigen Abschnitt dargestellten Layout. Es gibt drei Anzeige Bereiche: das Banner und den Informationsblock auf der linken Seite der Ansicht und die Datei Liste auf der rechten Seite.

Die Regionen sind alle zugewiesenen IDs, die von dem Stylesheet und DHTML verwendet werden sollen. Wie im nächsten Abschnitt erläutert, gibt es zwei mögliche Banner mit den Bezeichnern "Banner" und "Minibanner". Der Bezeichner des Informationsblock Bereichs lautet "Info". Der Bezeichner des Dateilisten Objekts ist "FileList". Die Details des Regions [Layouts](#controlling-the-web-view-layout) werden durch das Stylesheet und die Microsoft JScript-Funktion [FixSize](#adjusting-the-layout-by-using-the-fixsize-function)behandelt, die später in diesem Kapitel erläutert wird.

### <a name="the-banner-region"></a>Der Banner Bereich

Das Banner befindet sich am oberen Rand der Anzeige in der oberen linken Ecke der Webansicht. Das normale Banner zeigt den Namen und das Symbol des Ordners an, dessen Inhalt in der Datei Liste auf der rechten Seite angezeigt wird. Wenn das Fenster jedoch zu kurz wird, wird unter Umständen kein Platz unterhalb des Symbols zum Anzeigen von Informationen angezeigt. Aus diesem Grund definiert "Generic. htt" auch ein Minibanner, das nur den Ordnernamen anzeigt. Beide Banner werden anfänglich als ausgeblendet definiert. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) wählt aus, welches angezeigt werden soll, und legt es auf "Visible" fest.

Das normale Banner für Generic. htt wird wie folgt definiert:


```
<div id="Banner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
    <p class=Title style="margin-left: 104px; margin-top: 16px">
        %THISDIRNAME% 
    </td></tr></table>
    <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
    <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
        <param name="scale" value=200>
    </object>
</div>
                    
```



Der erste Teil des Banner Abschnitts zeigt den Titel mit einer horizontalen, darunter liegenden Regel an. Table-Tags werden verwendet, um die Position zu steuern. Das nowrap-Attribut wird für das <TD> -Tag, um die Wort Umbruch zu verhindern. Das System ersetzt "% thisdirname%" durch den Namen des aktuellen Ordners. Ein **WebViewFolderIcon** -Objekt mit dem Bezeichner "Icon" aus Gründen der Einfachheit wird dann geladen, um das Symbol des Ordners zu extrahieren und anzuzeigen.

Der Minibanner-Abschnitt ähnelt dem normalen Banner. Das Format des Titels wird etwas höher angeordnet und besitzt keine Regel. Da kein Symbol vorhanden ist, wird das **WebViewFolderIcon** -Objekt nicht geladen.


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a>Info Bereich

Der Teil der Webansicht unterhalb des Banners dient zum darstellen detaillierter Informationen über das ausgewählte Element. Wenn kein Element ausgewählt ist, wird eine Standardmeldung angezeigt. Da Generic. htt nur einen einzelnen TextBlock anzeigt, ist dieser Abschnitt recht einfach.


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



Die meisten Informationen zur Erfassung der Informationen werden von einem [Ordner Informations Skript](#retrieving-and-displaying-folder-information) verarbeitet, das weiter unten in diesem Kapitel erläutert wird. Sie zeigt die Informationen an, indem Sie den Text [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)zuweist.

Sie können die Anzeige von Informationen problemlos anpassen, indem Sie diese Elemente ändern oder weitere hinzufügen. Alles, was Sie auf einer Webseite platzieren können, kann verwendet werden. Wenn Sie z. b. einen Link zu Ihrer Website anzeigen möchten, können Sie ein Anker Element nach dem TextBlock in Generic. htt hinzufügen.


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
        <span>
        <p> Click on <a href="https://your.address"></a>
        </span>
</div>
                    
```



### <a name="the-filelist-region"></a>Der FileList-Bereich

Zum Schluss lädt Generic. htt ein [**webviewfoldercontents**](webviewfoldercontents.md) -Objekt für den FileList-Bereich. Da der Bezeichner auf "FileList" festgelegt ist, wird er von nun an als FileList-Objekt bezeichnet.


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



Das FileList-Objekt wird in den meisten Webansichten gefunden und dient mehreren Zwecken. FileList zeigt die Liste der Elemente an, die im ausgewählten Ordner enthalten sind, mit den gleichen Optionen und dem gleichen aussehen wie die Datei Liste im klassischen Stil. Wenn ein Element ausgewählt wird, benachrichtigt FileList die Webansicht, indem ein [SelectionChanged](#retrieving-and-displaying-folder-information) -Ereignis ausgelöst wird. FileList macht auch Methoden und Eigenschaften verfügbar, die zum Abrufen von Informationen über einzelne Elemente und zum Steuern der Position und Größe des Anzeige Bereichs verwendet werden können.

Obwohl das FileList-Objekt sehr nützlich ist, gibt es nur standardmäßige Dateisystem Informationen zurück, z. b. Dateigröße oder Attribute. Zum Abrufen anderer Arten von Informationen aus einem Shellordner müssen Sie zusätzliche Objekte laden und verarbeiten. Jedes Objekt, das von einer Webseite gehostet werden kann, kann mit einer Webansicht verwendet werden.

### <a name="the-template-head"></a>Der Vorlagen Kopf

Der Anfang der webansichts Vorlage enthält die Skripts und Funktionen, die den größten Teil der eigentlichen Arbeit ausführen. Es gibt zwei wichtige Aufgaben, die behandelt werden müssen. Eine ist das Layout der Anzeige der Webansicht, die an verschiedene Anzeige Bereiche angepasst werden muss. Das andere Element Ruft Informationen aus dem Ordner ab und zeigt diese an, wenn ein Element ausgewählt wird. Wie bei Stylesheets ist es besser, alle Skripts und Funktionen in die Vorlage einzubeziehen, anstatt Sie als separate Dateien zu referenzieren.

### <a name="controlling-the-web-view-layout"></a>Steuern des Layouts der Webansicht

Der Bereich, der für eine Webansicht verfügbar ist, hängt von der Größe des Fensters der Webansicht und davon ab, wie viel von der Windows-Explorer-Leiste benötigt wird. Dieser Bereich ändert sich, wenn die Größe des Fensters oder der Windows Explorer-Leiste geändert wird. Daher muss das Layout mit dem verfügbaren Bereich abgeglichen werden, wenn eine Webansicht geladen und entsprechend geändert wird, wenn die Größe geändert wird. Ein Großteil des Layouts wird im Stylesheet angegeben. Der Informationsbereich wird z. b. so definiert, dass er die am weitesten links stehenden 30 Prozent der Webansicht einnimmt.


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



Wenn die Größe einer Webansicht geändert wird, wird die Breite des Informationsbereichs geändert, um diesen Prozentsatz beizubehalten. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) verwaltet die Layoutprobleme, die nicht von einem Stylesheet behandelt werden können.

### <a name="loading-and-initializing-the-web-view"></a>Laden und Initialisieren der Webansicht

Wenn eine Webansicht geladen wird, muss das Layout an den verfügbaren Anzeigebereich angepasst werden. Da noch kein Element ausgewählt wurde, zeigen Webansichten normalerweise einige Standardinformationen an, die für den gesamten Ordner gelten. Um die Initialisierung zu verarbeiten, wird der <BODY> Tag for Generic. htt erkennt das [OnLoad](/previous-versions//ms531409(v=vs.85)) -Ereignis und ruft die **Init** -Funktion auf.


```
<body scroll=no onload="Init">
                    
```



**Init** ist eine einfache JScript-Funktion.


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



**Init** bindet [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) an das [Window. OnResize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) -Ereignis, sodass es aufgerufen wird, wenn sich der Anzeigebereich der Webansicht ändert. Dann führt er FixSize aus, um das anfängliche Layout festzulegen, und weist dem Info Bereich einen L-Einfügungs \_ \_ Text zu. L- \_ Intro- \_ Text ist ein Block von einführenden Text, der im Stylesheet-Abschnitt definiert ist.


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a>Anpassen des Layouts mithilfe der FixSize-Funktion

Die [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) -Funktion wird verwendet, um verschiedene Aspekte des Layouts anzugeben, die nicht vom Stylesheet behandelt werden können.

Abhängig von der Höhe der Webansicht können zwei mögliche Banner verwendet werden.


```
if (200 > document.body.clientHeight) {
    //A short window. Use the minibanner.
    document.all.Banner.style.visibility = "hidden";
    document.all.MiniBanner.style.visibility = "visible";
    document.all.FileList.style.top = 32;
    document.all.Info.style.top = 32;
}
else {
    //A normal window. Use the normal banner.
    document.all.Banner.style.visibility = "visible";
    document.all.MiniBanner.style.visibility = "hidden";
    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
    document.all.Rule.style.width = (document.body.clientWidth > 84 ?                                    document.body.clientWidth - 84 : 0) + "px";      
}
                    
```



Generic. htt verwendet eine Höhe von 200 Pixel als Trennlinie zwischen normalem und Minibanner. Der Stil des ausgewählten Banners wird auf "sichtbar" und das andere auf "ausgeblendet" festgelegt. Außerdem werden mehrere Layouteigenschaften für die Info-und die FileList-Bereiche festgelegt, damit Sie ordnungsgemäß mit dem ausgewählten Banner angepasst werden.

Wenn eine Webansicht zu schmal wird, verwendet [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) die gesamte Breite des Anzeige Bereichs für die FileList-Anzeige.


```
if (400 > document.body.clientWidth) {
    //A narrow window. Hide the Info region, and expand the file list region.
    document.all.Info.style.visibility = "hidden";
    document.all.FileList.style.pixelLeft = 0;
    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
}

else {
    //Normal width.
    document.all.Info.style.visibility = "visible";
    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
}
                    
```



Generic. htt verwendet 400 Pixel als Trennlinie zwischen schmalen und breiten anzeigen. Wenn die Webansicht zu schmal ist, blendet [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) den Informationsbereich aus und ändert die FileList [Pixel Left](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) -Eigenschaft so, dass Sie den gesamten Bereich unterhalb des Banners füllt.

Die letzten Zeilen von [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) passen verschiedene Layouteigenschaften basierend auf den Ergebnissen des vorangehenden Codes an. Die Breite des FileList-Bereichs wird so angepasst, dass er genau den Teil der Webansicht füllt, der nicht vom Informationsbereich belegt wird. Die Höhe des Info Bereichs ist für das Banner und den unteren Rand der Webansicht angepasst.


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a>Abrufen und Anzeigen von Ordner Informationen

Wenn ein Benutzer ein Element auswählt, löst das FileList-Objekt ein [SelectionChanged](#retrieving-and-displaying-folder-information) -Ereignis aus. Dieses Ereignis wird von einem JScript-Skript behandelt. Der Einfachheit halber geht das in Generic. htt gefundene Skript davon aus, dass jeweils nur ein Element ausgewählt werden kann.


```
<script language="JavaScript" for="FileList" event="SelectionChanged">
    // Updates the TextBlock region when an item is selected.
    var data;
    var text;

    // Name
    text = "<b>" + FileList.FocusedItem.Name + "</b>";

    // Comment
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
    if (data)
        text += "<br>" + data;

    // Documents
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
    if (data)
        text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

    // Status
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
    if (data)
        text += "<br><br><b><font color=red>" + data + "</font></b>";

    // Tip 
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
    if (data != "" && data != FileList.FocusedItem.Name)
        text += "<br><br>" + data;

    TextBlock.innerHTML = text;
</script>
                    
```



Das Skript verwendet zwei FileList-Eigenschaften, [**FileList. FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)und [**FileList. Folder**](/windows/desktop/shell/shellfolderview-folder) zum Abrufen von Informationen über das Element. **FileList. FocusedItem** identifiziert das ausgewählte Element mit dem Namen des Elements, das von **FileList.FocusedItem.Name** angegeben wird. " **FileList. Folder** " ist tatsächlich ein Zeiger auf ein [**Ordner**](../shell/folder.md) Objekt. Die [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) -Methode des Ordner Objekts wird verwendet, um die restlichen Informationen über das Element abzurufen.

Alle Informationen werden in einer einzelnen Text Zeichenfolge verkettet, getrennt durch <BR> Tags zur besseren Lesbarkeit. Der Text wird dann angezeigt, indem er [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)zugewiesen wird.

## <a name="summary"></a>Zusammenfassung

In diesem Kapitel werden einige der Techniken beschrieben, die Sie verwenden können, um die Art und Weise anzupassen, wie Windows-Explorer Informationen zu shellordnern anzeigt. Wenn Sie eine Desktop.ini Datei erstellen, können Sie einige einfache Anpassungen vornehmen, z. b. ein benutzerdefiniertes Symbol anstelle des Standardordner Symbols anzeigen. Wenn ein Ordner in einer Webansicht angezeigt wird, werden das Layout und die Anzeige von einer HTML-basierten Vorlage gesteuert, die bestimmt, welche Informationen angezeigt werden und wie. Sie können ein hohes Maß an Kontrolle über die Webansicht eines Ordners mit standardmäßigen HTML-, DHTML-und Skript Techniken zum Erstellen einer benutzerdefinierten Vorlage ausüben.

 

 