---
title: Anpassen der Webansicht eines Ordners
description: Eine Webansicht ist eine leistungsstarke und flexible Möglichkeit, den Windows-Explorer zum Anzeigen von Informationen zum Inhalt eines Shellordners zu verwenden.
ms.assetid: a894df21-bcc6-4760-b7d7-9bf95a0dba7f
keywords:
- Webansichten
- Klassischer Stil
- Webstil
- Banner
- FileList-Region
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac85478bd42737f0a240b356bb6b3b73e838a8ee
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884528"
---
# <a name="customizing-a-folders-web-view"></a>Anpassen der Webansicht eines Ordners

\[Dieses Feature wird nur unter Windows XP oder früher unterstützt. \]

Eine Webansicht ist eine leistungsstarke und flexible Möglichkeit, den Windows-Explorer zum Anzeigen von Informationen zum Inhalt eines Shellordners zu verwenden.

-   [Introduction (Einführung)](#introduction)
-   [Verwenden der Webansichtsvorlage](#using-the-web-view-template)
    -   [Der Vorlagentext](#the-template-body)
    -   [Der Vorlagenkopf](#the-template-head)
-   [Zusammenfassung](#summary)

## <a name="introduction"></a>Einführung

Windows bietet Benutzern zwei primäre Möglichkeiten zum Anzeigen und Navigieren im Shellnamespace. Die vertrautesten davon, der klassische Stil, ähneln dem vertrauten Windows Datei-Manager. Im rechten Bereich werden die Inhalte des aktuell ausgewählten Ordners in einem von fünf Formaten aufgelistet: Großes Symbol, Kleines Symbol, Liste, Details und Miniaturansicht. Der hauptunterschied zu Windows Datei-Manager ist der linke Bereich, der der Explorer-Leiste von Windows Internet Explorer sehr ähnlich aussieht. Die Größe kann geändert oder entfernt werden, und es können neben der vertrauten Dateisystemstruktur mehrere Bereiche angezeigt werden, z. B. ein Suchbereich.

> [!Note]  
> Die Informationen in diesem Dokument gelten nicht für Windows XP. Die beschriebenen Techniken gelten nur für frühere Versionen von Windows.

 

Die folgende Abbildung zeigt den Ordner Drucker im klassischen Stil.

![klassischer Stil des Druckerordners.](images/webview1.png)

Der klassische Stil funktioniert relativ gut für normale Dateisystemordner und -dateien. Mit der Einführung von Windows 95 hat sich das Dateisystem jedoch in den Namespace weiterentwickelt. Der -Namespace ermöglicht die Erstellung *von virtuellen Ordnern* wie Druckern oder Netzwerkumgebungen, die sehr unterschiedliche Informationstypen als ein normaler Dateisystemordner darstellen können.

Der Webstil, auch als Webansicht bezeichnet, bietet eine flexiblere und leistungsfähigere Möglichkeit zur Darstellung von Informationen als der klassische Stil. In einer Webansicht zeigt der Benutzer mithilfe von Internet Explorer im Grunde den Namespace an und navigiert durch den Namespace. Das grundlegende Layout einer Webansicht ähnelt dem klassischen Stil. Die Explorer-Leiste ist unverändert. Die Von der Dateiliste belegte Region wird jedoch zu einem allgemeinen Anzeigebereich, bei dem es sich effektiv um eine Webseite handelt. Eine Webansicht wird weiterhin verwendet, um Informationen über den Inhalt eines Ordners anzuzeigen, aber es gibt einige Einschränkungen hinsichtlich der anzeige- oder wie-Informationen. Jeder Ordner kann über eine eigene Webansicht verfügen, die an die jeweiligen Features angepasst ist.

Die folgende Abbildung zeigt eine Webansicht des Ordners Drucker (zuvor im klassischen Stil dargestellt).

![Standardwebansicht des Druckerordners.](images/webview2.png)

Ähnlich wie herkömmliche Webseiten werden Webansichten durch eine HTML-basierte Vorlage gesteuert. Das Erstellen einer Webansichtsvorlage ist nahezu identisch mit der Erstellung einer Webseite und bietet das gleiche Maß an Flexibilität in Inhalt und Layout von Informationen. Webansichtsvorlagen können dynamic HTML (DHTML) und Skripts verwenden, um auf Ereignisse zu reagieren, z. B. ein Benutzer, der auf ein Element klickt. Sie können auch Objekte hosten, mit denen sie Informationen aus dem Ordner oder dessen Inhalt abrufen und anzeigen können.

Der Benutzer kann eine Webansicht auswählen, indem er Windows Explorer startet, im Menü **Ansicht** auf **Ordneroptionen** klickt und diese Option auswählt: **Webinhalt in Ordnern aktivieren.** Der Benutzer kann jedoch auch Internet Explorer starten und den Browser auf das Dateisystem verweisen, indem er auf das Menü **Ansicht** klickt, auf die **Explorer-Leiste** zeigt und auf **Ordner klickt.** In einer Webansicht gibt es praktisch keinen Unterschied zwischen Internet Explorer und Windows Explorer.

Auf der linken Seite des rechten Bereichs zeigt die Druckerwebansicht ein Banner mit dem Namen und Symbol des Ordners an, gefolgt von einem Informationsblock zum Ordner. Die übliche Dateiliste befindet sich auf der rechten Seite der Seite.

Wenn ein Benutzer auf ein Element klickt, werden ausführliche Informationen zum Element im Informationsblock angezeigt. Die Drucker-Webansicht zeigt tatsächlich die gleichen Informationen an, die im klassischen Stil verfügbar sind, jedoch in einem besser verwendbaren Format. Eine Webansicht ist jedoch nicht einfach eine andere Möglichkeit, Informationen im klassischen Stil anzuzeigen. Beispielsweise kann ein Link zu einer nützlichen Website unterhalb des Informationsblocks angezeigt werden, einem Feature, das im klassischen Stil nicht verfügbar ist. Wenn der Benutzer auf den Link klickt, wird die Website angezeigt.

Die in der obigen Abbildung gezeigte Druckerwebansicht ähnelt dem klassischen Stil, da die zugrunde liegende Webansichtsvorlage (eine HTT-Datei) auf diese Weise geschrieben wurde. Die Liste der Dateien wird beispielsweise nicht direkt von der Webansichtsvorlage generiert. Sie wird von einem [**WebViewFolderContents-Objekt**](webviewfoldercontents.md) erstellt und angezeigt, das von der Webansichtsvorlage gehostet wird. Die Methoden und Eigenschaften des Objekts ermöglichen es der Webansicht, ihr Layout zu steuern und Informationen zu bestimmten Elementen abzurufen. Inhalt und Layout des Banners und informationsblocks werden in der Webansichtsvorlage angegeben.

Da eine Webansicht DHTML unterstützt, kann die Vorlage auch zum Verarbeiten der Benutzerinteraktion verwendet werden. Wenn ein Benutzer beispielsweise auf eines der Druckersymbole klickt, löst das **WebViewFolderIcon-Objekt** ein [**SelectionChanged-Ereignis**](/windows/desktop/shell/application-support-bumper) aus. Die Vorlage verwendet einen im Skript geschriebenen DHTML-Ereignishandler, um die angeforderten Informationen abzurufen und im Informationsblock anzuzeigen.

Dieses einfache Beispiel für den Ordner Drucker ist keinesfalls die einzige Möglichkeit, eine Webansicht zu verwenden. Indem Sie Ihre eigene Vorlage und ggf. Objekte schreiben, können Sie eine Webansicht verwenden, um Informationen anzuzeigen und mit dem Benutzer auf die effektivste Weise zu interagieren. Beachten Sie, dass Webansichtsvorlagen derzeit nur systemdefinierte virtuelle Ordner anzeigen. Obwohl Entwickler einen virtuellen Ordner erstellen können, indem sie eine Namespaceerweiterung implementieren, müssen sie die unter [Namespaceerweiterungen beschriebenen](/windows/desktop/shell/nse-works) Verfahren verwenden, um ihn anzuzeigen.

## <a name="using-the-web-view-template"></a>Verwenden der Webansichtsvorlage

Die Art und Weise, wie Daten in einer Webansicht angezeigt werden, kann eingeschränkt angepasst werden, indem die Desktop.ini-Datei eines Ordners geändert wird. Weitere Informationen finden Sie unter [Anpassen von Ordnern mit Desktop.ini.](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) Eine viel flexiblere und leistungsfähigere Möglichkeit zum Anpassen einer Webansicht ist das Erstellen einer benutzerdefinierten Webansichtsvorlage.

Die Webansichtsvorlage steuert, was in einer Webansicht angezeigt wird und wie. Es werden standardmäßige HTML-, DHTML- und Skriptverfahren verwendet, um Informationen abzurufen und anzuzeigen und mit dem Benutzer zu interagieren. In diesem Abschnitt wird erläutert, wie Sie eine Webansicht erstellen, indem Sie eine einfache Vorlage – Generic.htt – untersuchen.


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



Eine einfache Möglichkeit zum Erstellen einer eigenen Webansichtsvorlage besteht darin, Generic.htt zu verwenden und zu ändern. Da sie eher begrenzt ist, sollten Sie sich auch andere, komplexere Beispiele für weitere Ideen ansehen. Sie finden sie, indem Sie in Ihrem System nach der .htt-Erweiterung suchen, die von allen Webansichtsvorlagen verwendet wird. Wenn Sie eine benutzerdefinierte Vorlage für einen Ordner erstellen möchten, sollten Sie mit der Standardvorlage Folder.htt beginnen, die normalerweise entweder in C: \\ Winnt Web oder C: Windows Web gespeichert \\ \\ \\ wird. Beachten Sie, dass diese Dateien als ausgeblendet definiert sind, sodass Sie möglicherweise Ihre Windows Explorer-Einstellungen ändern müssen, um sie anzuzeigen. Nachdem eine HTT-Datei erstellt wurde, sollte sie als schreibgeschützt und ausgeblendet markiert werden.

Webansichtsvorlagen verwenden die .htt-Erweiterung, da sie sich geringfügig von herkömmlichen .htm Dokumenten unterscheiden. Der Hauptunterschied besteht in mehreren speziellen Variablen in HTT-Dateien, die das System durch die aktuellen Namespacewerte ersetzt. Die Variablen %THISDIR% und %THISDIRPATH% stellen den Namen und Pfad des aktuell ausgewählten Ordners dar. Die %TEMPLATEDIR%-Variable stellt den Ordner dar, in dem die Webansichts-Stylesheets gespeichert werden.

Wie die meisten HTML-Vorlagen bestehen HTT-Dateien aus zwei grundlegenden Teilen: einem Text und einem Kopf. Der Vorlagentext steuert das grundlegende Layout der Webansicht und lädt die Objekte, die für die Kommunikation mit dem Namespace und Anzeigeinformationen verwendet werden. Der Hauptordner enthält Skripts und Funktionen, die Aufgaben wie das Ändern der Größe und das Abrufen von Informationen aus dem Ordner ausführen. Die meisten Vorlagen, einschließlich Generic.htt, enthalten auch ein Stylesheet. Im Allgemeinen ist es besser, die Stylesheetinformationen in Ihre Vorlage einzufügen. Separate Stylesheets funktionieren möglicherweise nicht ordnungsgemäß, wenn eine Webansicht mit Remotenamespaces verwendet wird.

### <a name="the-template-body"></a>Der Vorlagentext

Der Text der Vorlage gibt an, was von einer Webansicht dargestellt wird. Dort werden auch die Objekte geladen, die zum Anzeigen von Informationen und zum Kommunizieren mit Namespaceordnern verwendet werden. Das von Generic.htt definierte Layout ähnelt dem in der Abbildung im vorherigen Abschnitt gezeigten Layout. Es gibt drei Anzeigebereiche: das Banner und den Informationsblock auf der linken Seite der Ansicht und die Dateiliste auf der rechten Seite.

Alle Bereiche sind zugewiesene Bezeichner, die vom Stylesheet und DHTML verwendet werden sollen. Wie im nächsten Abschnitt erläutert, gibt es zwei mögliche Banner mit den Bezeichnern "Banner" und "MiniBanner". Der Bezeichner des Bereichs des Informationsblocks ist "Info". Der Bezeichner des Dateilistenobjekts ist "FileList". Die Details des [Layouts](#controlling-the-web-view-layout) der Region werden vom Stylesheet und der Microsoft JScript-Funktion [FixSize](#adjusting-the-layout-by-using-the-fixsize-function)behandelt, die weiter unten in diesem Kapitel erläutert wird.

### <a name="the-banner-region"></a>Der Bannerbereich

Das Banner befindet sich oben auf der Anzeige in der oberen linken Ecke der Webansicht. Das normale Banner zeigt den Namen und das Symbol des Ordners an, dessen Inhalt in der Dateiliste auf der rechten Seite angezeigt wird. Wenn das Fenster jedoch zu kurz wird, ist unter dem Symbol möglicherweise kein Platz zum Anzeigen von Informationen vorhanden. Aus diesem Grund definiert Generic.htt auch einen Minibanner, der nur den Ordnernamen anzeigt. Beide Banner werden anfänglich als ausgeblendet definiert. [FixSize wählt](#adjusting-the-layout-by-using-the-fixsize-function) aus, welches angezeigt werden soll, und legt es auf "sichtbar" fest.

Das normale Banner für Generic.htt wird definiert durch:


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



Im ersten Teil des Bannerabschnitts wird der Titel mit einer horizontalen Regel darunter angezeigt. Tabellentags werden verwendet, um die Position zu steuern. Das nowrap-Attribut wird für festgelegt. <TD> -Tag, um das Umschließen von Wörtern zu verhindern. Das System ersetzt %THISDIRNAME% durch den Namen des aktuellen Ordners. Ein **WebViewFolderIcon-Objekt** mit dem Bezeichner "Icon" wird dann geladen, um das Symbol des Ordners zu extrahieren und anzuzeigen.

Der Abschnitt minibanner ähnelt dem normalen Banner. Das Format des Titels wird etwas höher platziert und verfügt nicht über eine Regel. Da es kein Symbol gibt, wird **das WebViewFolderIcon-Objekt** nicht geladen.


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a>Der Infobereich

Der Teil der Webansicht unter dem Banner wird verwendet, um ausführliche Informationen zum ausgewählten Element zu präsentieren. Wenn kein Element ausgewählt ist, wird eine Standardmeldung angezeigt. Da Generic.htt nur einen einzelnen Textblock anzeigt, ist dieser Abschnitt recht einfach.


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



Der Großteil der Arbeit beim Sammeln der Informationen wird von einem Ordnerinformationsskript [verarbeitet,](#retrieving-and-displaying-folder-information) das später in diesem Kapitel erläutert wird. Sie zeigt die Informationen an, indem der Text [TextBlock.innerHTML zugewiesen wird.](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)

Sie können die Angezeigten Informationen einfach anpassen, indem Sie diese Elemente ändern oder zusätzliche Elemente hinzufügen. Alles, was Sie auf einer Webseite veröffentlichen können, kann verwendet werden. Um beispielsweise einen Link zu Ihrer Website anzuzeigen, können Sie nach dem Textblock in Generic.htt ein Ankerelement hinzufügen.


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

Schließlich lädt Generic.htt ein [**WebViewFolderContents-Objekt**](webviewfoldercontents.md) für den FileList-Bereich. Da der Bezeichner auf "FileList" festgelegt ist, wird er ab sofort als FileList-Objekt bezeichnet.


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



Das FileList-Objekt befindet sich in den meisten Webansichten und dient mehreren Zwecken. FileList zeigt die Liste der Elemente im ausgewählten Ordner mit den gleichen Optionen und der gleichen Darstellung wie die Dateiliste im klassischen Stil an. Wenn ein Element ausgewählt ist, benachrichtigt FileList die Webansicht, indem ein [SelectionChanged-Ereignis angezeigt](#retrieving-and-displaying-folder-information) wird. FileList macht auch Methoden und Eigenschaften verfügbar, die verwendet werden können, um Informationen zu einzelnen Elementen abzurufen und die Position und Größe des Anzeigebereichs zu steuern.

Obwohl das FileList-Objekt sehr nützlich ist, gibt es nur Standarddateisysteminformationen zurück, z. B. Dateigröße oder Attribute. Um andere Arten von Informationen aus einem Shellordner abzurufen, müssen Sie zusätzliche Objekte laden und verarbeiten. Jedes Objekt, das von einer Webseite gehostet werden kann, kann mit einer Webansicht verwendet werden.

### <a name="the-template-head"></a>Der Vorlagenkopf

Der Hauptkopf der Webansichtsvorlage enthält die Skripts und Funktionen, die den Großteil der eigentlichen Arbeit ausführen. Es gibt zwei wichtige Aufgaben, die behandelt werden müssen. Eine davon ist das Layout der Webansichtsanzeige, die angepasst werden muss, um unterschiedliche Anzeigeregionen zu unterstützen. Die andere ist das Abrufen und Anzeigen von Informationen aus dem Ordner, wenn ein Element ausgewählt wird. Wie bei Stylesheets ist es besser, alle Skripts und Funktionen in die Vorlage zu übernehmen, anstatt auf sie als separate Dateien zu verweisen.

### <a name="controlling-the-web-view-layout"></a>Steuern des Webansichtslayouts

Der für eine Webansicht verfügbare Bereich hängt von der Größe des Webansichtsfensters ab und davon, wie viel davon von der Leiste des Windows wird. Dieser Bereich ändert sich immer dann, wenn die Größe des Fensters oder Windows Explorer-Leiste geändert wird. Daher muss das Layout mit dem verfügbaren Bereich übereinstimmen, wenn eine Webansicht geladen wird, und sich entsprechend ändern, wenn die Größe geändert wird. Ein Teil des Layouts wird im Stylesheet angegeben. Der Infobereich wird z. B. so definiert, dass er die 30 Prozent der Webansicht ganz links ein belegt.


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



Wenn die Größe einer Webansicht geändert wird, ändert sich die Breite des Infobereichs, um diesen Prozentsatz zu erhalten. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) verwaltet die Layoutprobleme, die nicht von einem Stylesheet behandelt werden können.

### <a name="loading-and-initializing-the-web-view"></a>Laden und Initialisieren der Webansicht

Wenn eine Webansicht geladen wird, muss das Layout an den verfügbaren Anzeigebereich angepasst werden. Da noch kein Element ausgewählt wurde, zeigen Webansichten normalerweise einige Standardinformationen an, die für den gesamten Ordner gelten. Um die Initialisierung zu verarbeiten, erkennt &lt; das BODY-Tag &gt; für Generic.htt das [onload-Ereignis](/previous-versions//ms531409(v=vs.85)) und ruft die **Init-Funktion** auf.


```
<body scroll=no onload="Init">
                    
```



**Init** ist eine einfache JScript Funktion.


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



**Init** bindet [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) an das [Window.onresize-Ereignis,](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) sodass es immer dann aufgerufen wird, wenn sich der Anzeigebereich der Webansicht ändert. Anschließend wird FixSize ausgeführt, um das anfängliche Layout zu festlegen, und L \_ Intro \_ Text wird dem Infobereich zugewiesen. L \_ Intro \_ Text ist ein Block mit Einführungstext, der im Stylesheetabschnitt definiert ist.


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a>Anpassen des Layouts mithilfe der FixSize-Funktion

Die [FixSize-Funktion](#adjusting-the-layout-by-using-the-fixsize-function) wird verwendet, um verschiedene Aspekte des Layouts anzugeben, die nicht vom Stylesheet behandelt werden können.

Es gibt zwei mögliche Banner, die je nach Höhe der Webansicht verwendet werden können.


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



Generic.htt verwendet eine Höhe von 200 Pixeln als Trennlinie zwischen normalen und Minibannern. Er legt den Stil des ausgewählten Banners auf sichtbar und das andere auf ausgeblendet fest. Außerdem werden mehrere Layouteigenschaften für die Bereiche Info und FileList so konfiguriert, dass sie ordnungsgemäß in das ausgewählte Banner passen.

Wenn eine Webansicht zu schmal wird, verwendet [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) die vollständige Breite des Anzeigebereichs für die FileList-Anzeige.


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



Generic.htt verwendet 400 Pixel als Trennlinie zwischen schmalen und breiten Anzeigen. Wenn die Webansicht zu schmal ist, blendet [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) den Infobereich aus und ändert die FileList [pixelLeft-Eigenschaft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) so, dass sie den gesamten Bereich unter dem Banner ausfüllt.

In den letzten Zeilen von [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) werden mehrere Layouteigenschaften basierend auf den Ergebnissen des vorherigen Codes angepasst. Die Breite des FileList-Bereiches wird so angepasst, dass er genau den Teil der Webansicht ausfüllt, der nicht vom Infobereich belegt wird. Die Höhe des Infobereichs wird so dimensioniert, dass sie zwischen dem Banner und dem unteren Rand der Webansicht passt.


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a>Abrufen und Anzeigen von Ordnerinformationen

Wenn ein Benutzer ein Element auswählt, gibt das FileList-Objekt ein [SelectionChanged-Ereignis](#retrieving-and-displaying-folder-information) aus. Dieses Ereignis wird von einem JScript behandelt. Der Einfachheit halber geht das in Generic.htt gefundene Skript davon aus, dass immer nur ein Element gleichzeitig ausgewählt werden kann.


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



Das Skript verwendet die beiden FileList-Eigenschaften [**FileList.FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)und [**FileList.Folder,**](/windows/desktop/shell/shellfolderview-folder) um Informationen zum Element zu erhalten. **FileList.FocusedItem** identifiziert das ausgewählte Element mit dem Namen des Elements, der von **FileList.FocusedItem.Name.** **FileList.Folder** ist tatsächlich ein Zeiger auf ein [**Folder-Objekt.**](../shell/folder.md) Die [**GetDetailsOf-Methode**](/windows/desktop/shell/folder-getdetailsof) des Folder-Objekts wird verwendet, um die verbleibenden Informationen über das Element abzurufen.

Alle Informationen werden in einer einzelnen Textzeichenfolge verkettet, getrennt durch <BR> -Tags zur Lesbarkeit. Der Text wird dann angezeigt, indem er [TextBlock.innerHTML zugewiesen wird.](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)

## <a name="summary"></a>Zusammenfassung

In diesem Kapitel werden einige der Techniken beschrieben, mit denen Sie anpassen können, wie der Windows Explorer Informationen zu Shellordnern anzeigt. Wenn Sie Desktop.ini erstellen, können Sie einige einfache Anpassungen vornehmen, z. B. das Anzeigen eines benutzerdefinierten Symbols statt des Standardordnersymbols. Wenn ein Ordner in einer Webansicht angezeigt wird, werden layout und display durch eine HTML-basierte Vorlage gesteuert, die bestimmt, welche Informationen wie angezeigt werden. Sie können ein hohes Maß an Kontrolle über die Webansicht eines Ordners mithilfe von STANDARD-HTML-, DHTML- und Skripttechniken zum Erstellen einer benutzerdefinierten Vorlage verwenden.

 

 
