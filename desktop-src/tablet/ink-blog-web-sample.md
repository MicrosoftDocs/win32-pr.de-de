---
description: Die frei Hand Blog-Beispielanwendung veranschaulicht, wie eine verwaltete UserControl-Klasse erstellt wird, die über die Funktion zum Erstellen und Hosten dieses Steuer Elements in Microsoft Internet Explorer verfügt.
ms.assetid: b6c3ad92-3ab1-4311-b318-13939e1a1a5a
title: Frei Hand Blog-webbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24f132d355a95c9cb8debebe074df3f976e3b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128436"
---
# <a name="ink-blog-web-sample"></a>Frei Hand Blog-webbeispiel

Die frei Hand Blog-Beispielanwendung veranschaulicht, wie eine verwaltete [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) -Klasse erstellt wird, die über die Funktion zum Erstellen und Hosten dieses Steuer Elements in Microsoft Internet Explorer verfügt. Das Beispiel veranschaulicht außerdem eine Technik zum Senden von frei Hand Daten über ein Netzwerk mithilfe von http und zum Beibehalten von frei Hand Eingaben auf einem Server.

> [!Note]  
> Zum Ausführen dieses Beispiels muss Microsoft Internetinformationsdienste (IIS) mit ASP.NET installiert sein. Stellen Sie sicher, dass der Computer die Anforderungen erfüllt, die für das Ausführen von ASP.NET-Anwendungen auf Ihrem Computer erforderlich sind.

 

> [!Note]  
> Wenn Sie dieses Beispiel auf einem nicht-Tablet PC-Computer mit installiertem Microsoft Windows XP Tablet PC Edition Development Kit 1,7 ausführen, funktioniert die Text Erkennungsfunktion für den frei Hand Titel nicht. Dies liegt daran, dass ein nicht Tablet PC-Computer, auf dem das Tablet PC SDK 1,7 installiert ist, keine Erkennungs Tools hat. Der Rest der Anwendung führt wie beschrieben aus.

 

## <a name="overview"></a>Übersicht

Das frei Hand Blog Beispiel erstellt ein frei Hand fähiges Weblog. Inkblogweb ist eine ASP.NET-Anwendung. Der Ink-Eintrag wird mithilfe eines Benutzer Steuer Elements durchgeführt, auf das von einer ASP.NET-Seite verwiesen wird.

Das Benutzer Steuerelement erkennt, ob die Tablet PC-Platt Form Komponenten auf dem Client Computer installiert sind. Wenn dies der Fall ist, stellt das Benutzer Steuerelement dem Benutzer zwei frei Hand fähige Bereiche auf der Webseite zur Seite: eine zum Binden eines Titels für den Blogeintrag und eine für den Text des Eintrags. Wenn die Tablet PC-Platt Form Komponenten nicht installiert sind, erhält der Benutzer ein Standard Textfeld-Steuerelement für den Titel und den Textkörper des Eintrags.

Nachdem der Benutzer die Erstellung des Eintrags abgeschlossen hat, klickt er auf eine Schaltfläche, Hinzufügen eines Blogs, und der Beitrag wird zum Speichern an den Webserver gesendet. Auf dem-Server speichert die Anwendung den Titeltext und das Posting-Datum sowie einen Verweis auf eine Graphics Interchange Format-Datei (GIF). Die GIF-Datei, die ebenfalls auf dem Server gespeichert ist, enthält die frei Hand Daten aus dem Text in einer verstärkten GIF-Datei. Weitere Informationen zum verstärkten GIF-Format finden Sie unter Speichern von frei Hand Eingaben [in HTML](storing-ink-in-html.md).

Es gibt zwei Projekte in der Projekt Mappe inkblog: das **inkblogcontrols** -Projekt und das **inkblogweb** -Projekt.

## <a name="inkblogcontrols-project"></a>Inkblogcontrols-Projekt

Das **inkblogcontrols** -Projekt ist ein [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) -Projekt, das den Code für das Benutzer Steuerelement enthält, das das Binden auf der Webseite ermöglicht. Der Code für dieses Steuerelement, das inkarea-Steuerelement, befindet sich in der Datei "inkarea. cs".

Die `InkArea` Klasse erbt von der [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) -Klasse. Der Konstruktor für das- `InkArea` Steuerelement ruft eine Hilfsmethode auf `CreateInkCollectionSurface` .


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



Die- `CreateInkCollectionSurface` Methode bestimmt, ob die Tablet PC-Komponenten auf dem Client verfügbar sind, indem versucht wird, eine Instanz der [InkCollector](/previous-versions/ms583683(v=vs.100)) -Klasse zu erstellen. Wenn die Methode erfolgreich aufgerufen `CreateInkCollectionSurface` wird, gibt die Methode ein [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) -Objekt als Steuerelement zurück.


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



Wenn der Konstruktor ausfällt, da die Freihand-Platt Formdateien nicht gefunden werden, `InputArea` wird das Steuerelement als [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) -Steuerelement und nicht als [InkCollector](/previous-versions/ms583683(v=vs.100)) -Steuerelement instanziiert. Der Konstruktor passt dann die Größe des Steuer Elements auf die Größe des übergeordneten Benutzer Steuer Elements an und fügt es der Auflistung der Steuerelemente des übergeordneten Elements hinzu.

Die inkarea-Steuerelement Klasse implementiert drei interessante öffentliche Eigenschaften: inkdata, TextData und webEnabled.

Die inkdata-Eigenschaft ist schreibgeschützt und ermöglicht den Zugriff auf die serialisierten frei Hand Daten, wenn der Client das Binden unterstützt. Wenn der Client keine Verknüpfung unterstützt, ruft die inkdata-Eigenschaft eine leere Zeichenfolge ab. Die inkdata-Eigenschaft ruft die Hilfsmethode serializeinkdata auf, um zu bestimmen, ob der Client das Binden unterstützt.


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



In der- `SerializeInkData` Methode ist die Umwandlung in [InkCollector](/previous-versions/ms583683(v=vs.100)) erforderlich, wenn das [Ink](/previous-versions/ms583670(v=vs.100)) -Objekt angefordert wird, da `inputArea` als- [Steuer](/dotnet/api/system.windows.forms.control?view=netcore-3.1)Element deklariert wird. Wenn das Ink-Objekt beliebige Striche enthält, werden die frei Hand Daten `inkDataBytes` als GIF (angegeben mit dem [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) -Enumerationswert) im Bytearray gespeichert. Die-Methode konvertiert dann das Bytearray in eine Base64-codierte Zeichenfolge und gibt diese Zeichenfolge zurück.

Vorausgesetzt, dass der Client eine Erkennung ausführen kann, gibt die- `TextData` Eigenschaft das [erkentionresult](/previous-versions/ms552537(v=vs.100)) -Objekt zurück, das die frei Hand Daten an eine Handschrifterkennung übergibt. Wenn der Client nicht frei Hand fähig ist, wird der Text Feld Inhalt zurückgegeben, wie im folgenden Code dargestellt.


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



Die- `TextData` Eigenschaft ruft eine Hilfsmethode `RecognizeInkData` auf, die im folgenden Code gezeigt wird, um die Erkennung auszuführen. Wenn auf dem System Erkennungs-Engines vorhanden sind, `RecognizeInkData` gibt die Methode eine Zeichenfolge zurück, die die [TopString](/previous-versions/ms572009(v=vs.100)) -Eigenschaft des [erkentionresult](/previous-versions/ms552537(v=vs.100)) -Objekts enthält. Andernfalls wird eine leere Zeichenfolge zurückgegeben.


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



Die- `InkEnabled` Eigenschaft ist ein Schreib geschützter boolescher Wert, der angibt, ob das Freihand auf dem Client Computer unterstützt wird.

Ein weiterer wichtiger öffentlicher Member der `InkArea` Steuerelement Klasse ist die- `DisposeResources` Methode. Diese Methode ruft intern die- `Dispose` Methode auf, um sicherzustellen, dass alle Ressourcen, die vom Benutzer Steuerelement genutzt werden, bereinigt werden. Jede Anwendung, die das-Steuerelement verwendet, `InkArea` muss die- `DisposeResources` Methode nach Abschluss der Verwendung des-Steuer Elements aufruft.

## <a name="inkblogweb-project"></a>Inkblogweb-Projekt

Das inkblogweb-Projekt ist ein Websetup-Bereitstellungs Projekt, das auf das-Steuerelement verweist, `InkArea` um die blogfunktionalität bereitzustellen Weitere Informationen zu Websetup-Bereitstellungs Projekten finden Sie unter [Bereitstellung eines Websetup-Projekts](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).

Es gibt zwei ASPX-Dateien, die das Blog Beispiel implementieren: default. aspx und addblog. aspx. Default. aspx ist die Standardseite für die inkblogweb-Anwendung. Die Code Behind-Datei für diese Seite ist "default. aspx. cs". Diese Seite enthält einen Link zu der Seite, die das neue Blogeintrag-Formular enthält, und zeigt alle vorhandenen Blogeinträge an. Dieser Prozess wird später nach der folgenden Untersuchung der neuen Blogeintrag-Formularseite addblog. aspx beschrieben.

Addblog. aspx und die zugehörige Code Behind-Datei, addblog. aspx. cs, enthalten die Logik und den Benutzeroberflächen Code zum Erstellen neuer Blogeinträge. Addblox. aspx verweist auf zwei Instanzen der inkarea-Steuerelement Klasse, die im Projekt inkblogcontrols erstellt wurde, indem das HTML-Objekt Element verwendet wird, wie im folgenden Beispiel gezeigt. Eine Instanz verfügt über ein `id` Attribut von inkblogtitle, das andere hat ein ID-Attribut von inkblogbody.

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

Die InkBlogControls.dll-Assembly muss sich im selben Verzeichnis befinden wie die ASPX-Seite, die darauf verweist. Das Websetup-Bereitstellungs Projekt stellt sicher, dass dies der Fall ist. Dies wird durch das vorhanden sein des Elements "primäre Ausgabe von inkblogcontrols" im Bereitstellungs Projekt deutlich.

Das Title-Steuerelement ist nur 48 Pixel hoch, um den Eintrag einer einzelnen Zeile frei Hand Eingaben für den Titel zu vereinfachen. Das Body-Steuerelement ist 296 Pixel hoch, um Platz für größere Blogeinträge mehrerer Zeilen oder möglicherweise Zeichnungen zu schaffen.

Die inkarea-Steuerelemente sind mit einer Client seitigen Skriptfunktion, addblog, über den OnClick-Ereignishandler eines Standard-HTML-Schaltflächen Elements verbunden.

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

Es gibt auch ein HTML-Formular auf der Seite, das drei verborgene Eingabeelemente enthält: blogtitletext, blogbodytext und blogbodyinkdata. Dieses Formular wird verwendet, um die Blogeintrags Daten an den Server zurückzusenden. Addblog. aspx ist der Post Back Handler, der für das Formular definiert ist.

Die in Microsoft JScript geschriebene Funktion "addblog" <entity type="reg"/> extrahiert die Blog Daten aus den inkarea-Steuerelementen und sendet die Ergebnisse an den Server.


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



Wenn die Daten auf dem Server eintreffen, prüft der Code in addblog. aspx. cs den \_ Ereignishandler für den Seiten Ladevorgang, um festzustellen, ob die Form-Eigenschaft des HttpRequest-Objekts Daten enthält. Wenn dies der Fall ist, wird ein Dateiname erstellt, der auf der aktuellen Systemzeit basiert, die Formulardaten in drei Zeichen folgen Variablen einfügt und die Daten in eine HTML-Datei und eine GIF-Datei, die die frei Hand Daten enthält (sofern vorhanden), wie im folgenden Code gezeigt, geschrieben.


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



Weitere Informationen zu den Hilfsmethoden finden Sie im Beispiel Quell Code.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Das Tablet PC SDK 1,7 installiert standardmäßig das frei Hand Blog-webbeispiel. Um das Beispiel auszuführen, navigieren Sie in Internet Explorer zu https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx . Wenn Sie Windows Server 2003 ausführen, ersetzen Sie den Computernamen durch "localhost".

> [!Note]  
> Die kompilierten webbeispiele werden von der Standard Installationsoption für das SDK nicht installiert. Sie müssen eine benutzerdefinierte Installation durchführen und die unter Option "vorkompilierte webbeispiele" auswählen, um Sie zu installieren.

 

Sie können das Beispiel auch ausführen, indem Sie das Projekt in Microsoft Visual Studio .NET öffnen und <entity type="reg"/> dann auf einem separaten Computer bereitstellen, auf dem IIS ausgeführt wird.

## <a name="troubleshooting-the-sample"></a>Problembehandlung bei diesem Beispiel

Drei Bereiche, die Schwierigkeiten verursachen können, wenn das Beispiel ausgeführt oder gehostet wird, sind Berechtigungen und Erkennung.

### <a name="permissions"></a>Berechtigungen

Das Beispiel erfordert Schreibberechtigungen innerhalb des virtuellen Stamm Ordners für das Konto, das versucht, einen neuen Blogeintrag zu erstellen. Standardmäßig verfügt die kompilierte Version des Beispiels, das im Tablet PC SDK 1,7 bereitgestellt wurde, über die richtigen Berechtigungen, um diese Anforderung zu erfüllen.

Wenn Sie das Beispiel mit dem bereitgestellten Websetup-Bereitstellungs Projekt erstellen und bereitstellen, müssen Sie der Gruppe "% MachineName% \\ Users" Schreibzugriff auf den Dateisystem Ordner zuweisen, auf den vom virtuellen Stammverzeichnis "inkblogweb" verwiesen wird (z. b. "C: \\ Inetpub \\ wwwroot \\ inkblogweb"). Die Gruppe Benutzer enthält das anonyme Konto, das von IIS verwendet wird. auf diese Weise kann die ASP.NET-Anwendung die neuen Blogeinträge in das Dateisystem schreiben. Eine Alternative besteht darin, den anonymen Zugriff auf das virtuelle Stammverzeichnis zu entfernen und die Authentifizierung zu erzwingen.

### <a name="recognition"></a>Erkennung

Die Handschrifterkennung muss installiert sein, damit die frei Hand Eingaben im Titel des Blogs erkannt werden. Wenn Sie von einem Computer mit einem anderen Betriebssystem als Windows XP Tablet PC Edition auf die Anwendung inkblog zugreifen, aber mit installiertem Tablet PC SDK 1,7, können Sie in den inkarea-Steuerelementen in Freihand schreiben, aber die Erkennungs-Engines sind nicht vorhanden, und für ihre Blogeinträge werden keine Titel angezeigt. Der frei Hand Inhalt im Text wird jedoch immer noch angezeigt.

### <a name="machine-configuration"></a>Computerkonfiguration

Wenn Sie ASP.net und den .NET Framework auf einem Computer installiert haben und anschließend IIS deinstallieren und neu installieren, werden die Skript Zuordnungen unterbrechen und ASP.NET funktioniert nicht. Wenn dies der Fall ist, können Sie die ASP.NET-Skript Zuordnungen mit dem ASP.NET IIS-Registrierungs Tool (ASPNET \_regiis.exe-i) reparieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[InkCollector](/previous-versions/ms583683(v=vs.100))
</dt> <dt>

[Frei Hand Eingaben im Web](ink-on-the-web.md)
</dt> <dt>

[Frei Hand Datenformate](ink-data-formats.md)
</dt> <dt>

[System. Windows. Forms. UserControl-Klasse](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
