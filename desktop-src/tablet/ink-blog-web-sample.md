---
description: Die Beispielanwendung "Ink-Blog" veranschaulicht, wie Sie eine verwaltete UserControl-Klasse erstellen, die über Einekungsfunktionen verfügt und diese Steuerung in Microsoft Internet Explorer hostet.
ms.assetid: b6c3ad92-3ab1-4311-b318-13939e1a1a5a
title: Ink-Blog-Webbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8796a05861d278015205b5ba0d3775e2e47af6a57ce1fee426c5c0c5011dacd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032358"
---
# <a name="ink-blog-web-sample"></a>Ink-Blog-Webbeispiel

Die Beispielanwendung "Ink-Blog" veranschaulicht, wie Sie eine verwaltete [UserControl-Klasse](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) erstellen, die über Einekungsfunktionen verfügt und diese Steuerung in Microsoft Internet Explorer hostet. Das Beispiel veranschaulicht auch ein Verfahren zum Senden von Ink-Daten über ein Netzwerk mithilfe von HTTP und zum Beibehalten von Ink auf einem Server.

> [!Note]  
> Zum Ausführen dieses Beispiels muss Microsoft-Internetinformationsdienste (IIS) mit ASP.NET installiert sein. Stellen Sie sicher, dass Ihr Computer die Anforderungen erfüllt, die erforderlich sind, damit ASP.NET Anwendungen auf Ihrem Computer ausgeführt werden können.

 

> [!Note]  
> Wenn Sie dieses Beispiel auf einem Nicht-Tablet-PC-Computer ausführen, auf dem das Microsoft Windows XP Tablet PC Edition Development Kit 1.7 installiert ist, funktioniert das Texterkennungsfeature für den Ink-Titel nicht. Dies liegt daran, dass auf einem Nicht-Tablet PC-Computer, auf dem das Tablet PC SDK 1.7 installiert ist, keine Erkennungen verfügbar sind. Der Rest der Anwendung wird wie beschrieben ausgeführt.

 

## <a name="overview"></a>Übersicht

Im Ink-Blogbeispiel wird ein Ink-fähiges Weblog erstellt. InkBlogWeb ist eine ASP.NET Anwendung. Die Inkeingabe erfolgt über ein Benutzersteuerelement, auf das von einer ASP.NET Seite verwiesen wird.

Das Benutzersteuerelement erkennt, ob die Tablet PC-Plattformkomponenten auf dem Clientcomputer installiert sind. Wenn ja, zeigt das Benutzersteuerelement dem Benutzer zwei Freihandbereiche auf der Webseite an: einen für das Freihandeingaben eines Titels für den Blogeintrag und einen für den Text des Eintrags. Wenn die Tablet PC Platform-Komponenten nicht installiert sind, erhält der Benutzer ein Standardtextfeld-Steuerelement für Titel und Text des Eintrags.

Wenn der Benutzer die Erstellung des Eintrags abgeschlossen hat, klickt er auf die Schaltfläche Blog hinzufügen, und der Beitrag wird zur Speicherung an den Webserver gesendet. Auf dem Server speichert die Anwendung den Titeltext und das Veröffentlichungsdatum sowie einen Verweis auf eine GIF-Datei (Graphics Interchange Format). Die GIF-Datei, die ebenfalls auf dem Server gespeichert ist, enthält die Ink-Daten aus dem Text in einer verstärkten GIF-Datei. Weitere Informationen zum verstärkten GIF-Format finden Sie unter [Speichern von Ink in HTML.](storing-ink-in-html.md)

Es gibt zwei Projekte in der InkBlog-Projektmappe: das **Projekt InkBlogControls** und das **Projekt InkBlogWeb.**

## <a name="inkblogcontrols-project"></a>InkBlogControls Project

Das **InkBlogControls-Projekt** ist ein [UserControl-Projekt,](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) das den Code für das Benutzersteuerelement enthält, das das Öffnen auf der Webseite ermöglicht. Der Code für dieses Steuerelement, das InkArea-Steuerelement, befindet sich in der Datei InkArea.cs.

Die `InkArea` -Klasse erbt von der [UserControl-Klasse.](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) Der Konstruktor für das `InkArea` Steuerelement ruft die Hilfsmethode `CreateInkCollectionSurface` auf.


```C++
public InkArea()
{
    // Standard template code

    try
    {
        inputArea = CreateInkCollectionSurface();
    }
    catch (FileNotFoundException)
    { 
        inputArea = new TextBox();
        ((TextBox)inputArea).Multiline = true;
    }

    inputArea.Size = this.Size;

    // Add the control used for collecting blog input
    this.Controls.Add(inputArea);
}
```



Die `CreateInkCollectionSurface` -Methode bestimmt, ob die Freihandkomponenten des Tablet-PCs auf dem Client verfügbar sind, indem versucht wird, eine Instanz der [InkCollector-Klasse](/previous-versions/ms583683(v=vs.100)) zu erstellen. Wenn der Aufruf der `CreateInkCollectionSurface` -Methode erfolgreich ist, gibt die Methode ein [Panel-Objekt](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) als Steuerelement zurück.


```C++
protected Control CreateInkCollectionSurface()
{
    try
    {
        Panel inkPanel = new Panel();
        inkPanel.BorderStyle = BorderStyle.Fixed3D;
        inkCollector = new InkCollector(inkPanel);
        ((InkCollector)inkCollector).Enabled = true;
        return inkPanel;
    }
    catch
    {
        throw;
    }
}
```



Wenn der Konstruktor fehlschlägt, weil die Plattformdateien für die Markierung nicht gefunden werden, wird das `InputArea` Steuerelement als [TextBox-Steuerelement](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) anstelle eines [InkCollector-Steuerelements](/previous-versions/ms583683(v=vs.100)) instanziiert. Der Konstruktor dimensioniert das Steuerelement dann auf die Größe des übergeordneten Benutzersteuerelements und fügt es der Controls-Auflistung des übergeordneten Elements hinzu.

Die InkArea-Steuerelementklasse implementiert drei interessante öffentliche Eigenschaften: InkData, TextData und WebEnabled.

Die InkData-Eigenschaft ist schreibgeschützt und bietet Zugriff auf die serialisierten Ink-Daten, wenn der Client Dienung unterstützt. Wenn der Client Freihandhand nicht unterstützt, ruft die InkData-Eigenschaft eine leere Zeichenfolge ab. Die InkData-Eigenschaft ruft die Hilfsmethode SerializeInkData auf, um zu ermitteln, ob der Client Freihandhand unterstützt.


```C++
protected String SerializeInkData()
{
    Debug.Assert(InkEnabled, null, "Client must be ink-enabled");

    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    // Serialize the ink
    if (ink.Strokes.Count > 0) 
    {
        byte[] inkDataBytes = ink.Save(PersistenceFormat.Gif);
        return Convert.ToBase64String(inkDataBytes);
    }

    // Default to returning the empty string.
    return String.Empty;
}
```



In der `SerializeInkData` -Methode ist die Umwandlung [in InkCollector](/previous-versions/ms583683(v=vs.100)) erforderlich, wenn das [Ink-Objekt](/previous-versions/ms583670(v=vs.100)) erhalten wird, da `inputArea` als [Steuerelement](/dotnet/api/system.windows.forms.control?view=netcore-3.1)deklariert wird. Wenn das Ink-Objekt Striche enthält, werden die Ink-Daten als GIF im `inkDataBytes` Bytearray gespeichert (angegeben mithilfe des [PersistenceFormat-Enumerationswerts).](/previous-versions/ms552503(v=vs.100)) Die -Methode konvertiert dann das Bytearray in eine Base64-codierte Zeichenfolge und gibt diese Zeichenfolge zurück.

Unter der Annahme, dass der Client die Erkennung durchführen kann, gibt die `TextData` Eigenschaft das [RecognitionResult-Objekt](/previous-versions/ms552537(v=vs.100)) aus der Übergabe der Freihanddaten an eine Handschrifterkennung zurück. Wenn der Client keine Ink-Fähigen ist, wird der Inhalt des Textfelds zurückgegeben, wie im folgenden Code gezeigt.


```C++
public string TextData
{
    get
    {
        if (this.WebEnabled) 
        {
            return RecognizeInkData();
        }
        else
        {
            return ((TextBox)inputArea).Text;
        }
    }
}
```



Die `TextData` -Eigenschaft ruft die Hilfsmethode auf, `RecognizeInkData` die im folgenden Code gezeigt wird, um die Erkennung auszuführen. Wenn Erkennungs-Engines auf dem System vorhanden sind, gibt die `RecognizeInkData` Methode eine Zeichenfolge zurück, die die [TopString-Eigenschaft](/previous-versions/ms572009(v=vs.100)) des [RecognitionResult-Objekts](/previous-versions/ms552537(v=vs.100)) enthält. Andernfalls wird eine leere Zeichenfolge zurückgegeben.


```C++
protected String RecognizeInkData()
{
    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    if (ink.Strokes.Count > 0) 
    {

        // Attempt to create a recognition context and use it to
        // retrieve the top alternate.
        try 
        {
            RecognizerContext recognizerContext = new RecognizerContext();
            RecognitionStatus recognitionStatus;
            recognizerContext.Strokes = ink.Strokes;
            RecognitionResult recognitionResult = recognizerContext.Recognize(out recognitionStatus);
            if (recognitionStatus == RecognitionStatus.NoError) && ( null != recognitionResult) )
            {
                return recognitionResult.TopString;
            }
        }
        catch (Exception)
        {
            // An exception will occur if the client does not have
            // any handwriting recognizers installed on their system.
            // In this case, we default to returning an empty string. 
        }
    }

    return String.Empty;
}
```



Die `InkEnabled` -Eigenschaft ist ein schreibgeschützter boolescher Wert, der angibt, ob die Inkundung auf dem Clientcomputer unterstützt wird.

Ein weiterer wichtiger öffentlicher Member der `InkArea` Steuerelementklasse ist die `DisposeResources` -Methode. Diese Methode ruft intern die `Dispose` -Methode auf, um sicherzustellen, dass alle vom Benutzersteuerelement genutzten Ressourcen bereinigt werden. Jede Anwendung, die das -Steuerelement verwendet, `InkArea` muss die `DisposeResources` -Methode aufrufen, wenn die Verwendung des Steuerelements abgeschlossen ist.

## <a name="inkblogweb-project"></a>InkBlogWeb Project

Das InkBlogWeb-Projekt ist ein Websetup-Bereitstellungsprojekt, das auf das `InkArea` Steuerelement verweist, um die Blogfunktion bereitzustellen. Weitere Informationen zu WebSetup-Bereitstellungsprojekten finden Sie unter [Bereitstellung eines Websetups Project](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).

Es gibt zwei ASPX-Dateien, die das Blogbeispiel implementieren: Default.aspx und AddBlog.aspx. Default.aspx ist die Standardseite für die Anwendung InkBlogWeb. Die Code-Behind-Datei für diese Seite ist Default.aspx.cs. Diese Seite enthält einen Link zu der Seite, die das neue Blogeintragsformular enthält, und zeigt alle vorhandenen Blogeinträge an. Dieser Vorgang wird später nach der folgenden Untersuchung der neuen Blogeintragsformularseite AddBlog.aspx beschrieben.

AddBlog.aspx und die zugehörige CodeBehind-Datei AddBlog.aspx.cs enthalten die Logik und den Benutzeroberflächencode zum Erstellen neuer Blogeinträge. AddBlox.aspx verweist auf zwei Instanzen der InkArea-Steuerelementklasse, die im InkBlogControls-Projekt mithilfe des HTML OBJECT-Elements erstellt wurde, wie im folgenden Beispiel gezeigt. Eine Instanz verfügt über das `id` Attribut inkBlogTitle und die andere über das ID-Attribut inkBlogBody.

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

Die InkBlogControls.dll Assembly muss sich im gleichen Verzeichnis wie die ASPX-Seite befinden, die auf sie verweist. Das Websetup-Bereitstellungsprojekt stellt sicher, dass dies der Fall ist. Dies wird durch das Vorhandensein des Elements "Primäre Ausgabe von InkBlogControls" im Project Bereitstellung belegt.

Das Titelsteuerelement ist nur 48 Pixel hoch, um die Eingabe einer einzelnen Ink-Zeile für den Titel zu erleichtern. Das Textsteuerelement ist 296 Pixel hoch, um Platz für größere Blogeinträge mit mehreren Zeilen oder vielleicht Zeichnungen zu schaffen.

Die InkArea-Steuerelemente sind mit der clientseitigen Skriptfunktion AddBlog über den onclick-Ereignishandler eines STANDARDMÄßIG-HTML BUTTON-Elements verbunden.

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

Es gibt auch ein HTML-Formular auf der Seite, das drei ausgeblendete INPUT-Elemente enthält: BlogTitleText, BlogBodyText und BlogBodyInkData. Dieses Formular wird verwendet, um die Blogeintragsdaten zurück an den Server zu posten. AddBlog.aspx ist der für das Formular definierte Postbackhandler.

Die in Microsoft JScript geschriebene AddBlog-Funktion <entity type="reg"/> extrahiert die Blogdaten aus den InkArea-Steuerelementen und sendet die Ergebnisse an den Server.


```C++
function AddBlog() 
{
    // Extract the blog's title data as ink and text
    form.BlogTitleText.value  = inkBlogTitle.TextData;
    
    // Extract the blog's body data as ink and text
    form.BlogBodyText.value = inkBlogBody.TextData;
    form.BlogBodyInkData.value = inkBlogBody.InkData;   

    form.submit();
}
```



Wenn die Daten beim Server eintreffen, überprüft der Code in AddBlog.aspx.cs den \_ Seitenladeereignishandler, um festzustellen, ob die Form-Eigenschaft des HttpRequest-Objekts Daten enthält. Wenn ja, wird ein Dateiname basierend auf der aktuellen Systemzeit erstellt, die Formulardaten werden in drei Zeichenfolgenvariablen geschrieben, und die Daten werden in eine HTML-Datei und eine GIF-Datei geschrieben, die die Ink-Daten enthält(sofern vorhanden), wie im folgenden Code gezeigt.


```C++
if ( (String.Empty != inkBody) )
{           
    // Use helper method to create a GIF image file from ink data 
    CreateGif(imagePath, fileName, inkBody);
    
    // Create an HTML fragment to reference the image file
    content = "<img src=\"Blogs/Images/" + fileName + ".gif\"></img>";
}                
else 
{
    // If no ink data is available create an HTML fragment that contains
    // the blog's text directly.
    content = "<P>" + textBody + "</P>";
}

// Use helper method to create the blog web page on the server
CreateHtm(blogPath, fileName, blogTitle, content);
```



Weitere Informationen zu den Hilfsmethoden finden Sie im Beispielquellcode.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Das Tablet PC SDK 1.7 installiert standardmäßig das Ink Blog Web-Beispiel. Navigieren Sie zum Ausführen des Beispiels in Internet Explorer zu https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx . Wenn Sie Windows Server 2003 ausführen, ersetzen Sie den Computernamen durch "localhost".

> [!Note]  
> Die kompilierten Webbeispiele werden nicht von der Standardinstallationsoption für das SDK installiert. Sie müssen eine benutzerdefinierte Installation abschließen und die Unteroption "Vorkompilierte Webbeispiele" auswählen, um sie zu installieren.

 

Sie können das Beispiel auch ausführen, indem Sie das Projekt in Microsoft Visual Studio .NET öffnen und erstellen <entity type="reg"/> und es dann auf einem separaten Computer mit IIS bereitstellen.

## <a name="troubleshooting-the-sample"></a>Problembehandlung bei diesem Beispiel

Drei Bereiche, die beim Ausführen oder Hosten des Beispiels Probleme verursachen können, sind Berechtigungen und Erkennung.

### <a name="permissions"></a>Berechtigungen

Das Beispiel erfordert Schreibberechtigungen innerhalb des virtuellen Stammordners für das Konto, das versucht, einen neuen Blogeintrag zu erstellen. Standardmäßig sind für die kompilierte Version des Im Tablet PC SDK 1.7 bereitgestellten Beispiels die richtigen Berechtigungen festgelegt, um diese Anforderung zu erfüllen.

Wenn Sie das Beispiel mithilfe des bereitgestellten Websetupbereitstellungsprojekts erstellen und bereitstellen, müssen Sie der Gruppe %MACHINENAME% \\ Benutzer Schreibzugriff auf den Dateisystemordner gewähren, auf den der virtuelle Stamm inkBlogWeb verweist (z. B. C: \\ InetPub \\ WWWRoot \\ InkBlogWeb). Die Gruppe Benutzer enthält das anonyme Konto, das von IIS verwendet wird, sodass die ASP.NET Anwendung die neuen Blogeinträge in das Dateisystem schreiben kann. Eine Alternative besteht darin, den anonymen Zugriff auf den virtuellen Stamm zu entfernen und die Authentifizierung zu erzwingen.

### <a name="recognition"></a>Erkennung

Die Handschrifterkennung muss installiert sein, um die Freihand im Titel des Blogs zu erkennen. Wenn Sie von einem Computer mit einem anderen Betriebssystem als Windows XP Tablet PC Edition auf die InkBlog-Anwendung zugreifen, aber das Tablet PC SDK 1.7 installiert ist, können Sie Ink-Ink in die InkArea-Steuerelemente schreiben, aber die Erkennungs-Engines sind nicht vorhanden, und es werden keine Titel für Ihre Blogeinträge angezeigt. Der Freihandinhalt im Text wird jedoch weiterhin angezeigt.

### <a name="machine-configuration"></a>Computerkonfiguration

Wenn Sie ASP.NET und die .NET Framework auf einem Computer installiert haben und IIS dann deinstallieren und neu installieren, werden die Skriptzuordnungen nicht mehr ausgeführt, und ASP.NET funktioniert nicht. In diesem Fall können Sie die ASP.NET Skriptzuordnungen mit dem ASP.NET IIS-Registrierungstool (Aspnet \_regiis.exe -i) reparieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Inkcollector](/previous-versions/ms583683(v=vs.100))
</dt> <dt>

[Ink im Web](ink-on-the-web.md)
</dt> <dt>

[Ink-Datenformate](ink-data-formats.md)
</dt> <dt>

[System. Windows. Forms.UserControl-Klasse](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
