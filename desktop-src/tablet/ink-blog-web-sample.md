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
# <a name="ink-blog-web-sample"></a><span data-ttu-id="5da6c-103">Frei Hand Blog-webbeispiel</span><span class="sxs-lookup"><span data-stu-id="5da6c-103">Ink Blog Web Sample</span></span>

<span data-ttu-id="5da6c-104">Die frei Hand Blog-Beispielanwendung veranschaulicht, wie eine verwaltete [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) -Klasse erstellt wird, die über die Funktion zum Erstellen und Hosten dieses Steuer Elements in Microsoft Internet Explorer verfügt.</span><span class="sxs-lookup"><span data-stu-id="5da6c-104">The Ink Blog sample application demonstrates how to create a managed [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class that has inking capability and host that control in Microsoft Internet Explorer.</span></span> <span data-ttu-id="5da6c-105">Das Beispiel veranschaulicht außerdem eine Technik zum Senden von frei Hand Daten über ein Netzwerk mithilfe von http und zum Beibehalten von frei Hand Eingaben auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="5da6c-105">The sample also demonstrates one technique for sending ink data across a network by using HTTP and for persisting ink on a server.</span></span>

> [!Note]  
> <span data-ttu-id="5da6c-106">Zum Ausführen dieses Beispiels muss Microsoft Internetinformationsdienste (IIS) mit ASP.NET installiert sein.</span><span class="sxs-lookup"><span data-stu-id="5da6c-106">You must have Microsoft Internet Information Services (IIS) with ASP.NET installed to run this sample.</span></span> <span data-ttu-id="5da6c-107">Stellen Sie sicher, dass der Computer die Anforderungen erfüllt, die für das Ausführen von ASP.NET-Anwendungen auf Ihrem Computer erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5da6c-107">Make sure that your computer meets the requirements necessary for ASP.NET applications to run on your computer.</span></span>

 

> [!Note]  
> <span data-ttu-id="5da6c-108">Wenn Sie dieses Beispiel auf einem nicht-Tablet PC-Computer mit installiertem Microsoft Windows XP Tablet PC Edition Development Kit 1,7 ausführen, funktioniert die Text Erkennungsfunktion für den frei Hand Titel nicht.</span><span class="sxs-lookup"><span data-stu-id="5da6c-108">If you run this sample on a non-Tablet PC computer with the Microsoft Windows XP Tablet PC Edition Development Kit 1.7 installed the text recognition feature for the ink title will not function.</span></span> <span data-ttu-id="5da6c-109">Dies liegt daran, dass ein nicht Tablet PC-Computer, auf dem das Tablet PC SDK 1,7 installiert ist, keine Erkennungs Tools hat.</span><span class="sxs-lookup"><span data-stu-id="5da6c-109">This occurs because a non-Tablet PC computer with the Tablet PC SDK 1.7 installed lacks recognizers.</span></span> <span data-ttu-id="5da6c-110">Der Rest der Anwendung führt wie beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="5da6c-110">The rest of the application performs as described.</span></span>

 

## <a name="overview"></a><span data-ttu-id="5da6c-111">Übersicht</span><span class="sxs-lookup"><span data-stu-id="5da6c-111">Overview</span></span>

<span data-ttu-id="5da6c-112">Das frei Hand Blog Beispiel erstellt ein frei Hand fähiges Weblog.</span><span class="sxs-lookup"><span data-stu-id="5da6c-112">The Ink Blog sample creates an ink-enabled Weblog.</span></span> <span data-ttu-id="5da6c-113">Inkblogweb ist eine ASP.NET-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5da6c-113">InkBlogWeb is an ASP.NET application.</span></span> <span data-ttu-id="5da6c-114">Der Ink-Eintrag wird mithilfe eines Benutzer Steuer Elements durchgeführt, auf das von einer ASP.NET-Seite verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5da6c-114">Ink entry is accomplished by means of a user control that is referenced from an ASP.NET page.</span></span>

<span data-ttu-id="5da6c-115">Das Benutzer Steuerelement erkennt, ob die Tablet PC-Platt Form Komponenten auf dem Client Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="5da6c-115">The user control detects whether the Tablet PC platform components are installed on the client computer.</span></span> <span data-ttu-id="5da6c-116">Wenn dies der Fall ist, stellt das Benutzer Steuerelement dem Benutzer zwei frei Hand fähige Bereiche auf der Webseite zur Seite: eine zum Binden eines Titels für den Blogeintrag und eine für den Text des Eintrags.</span><span class="sxs-lookup"><span data-stu-id="5da6c-116">If so, the user control presents the user with two ink-enabled areas on the Web page: one for inking a title for the blog entry and one for the body of the entry.</span></span> <span data-ttu-id="5da6c-117">Wenn die Tablet PC-Platt Form Komponenten nicht installiert sind, erhält der Benutzer ein Standard Textfeld-Steuerelement für den Titel und den Textkörper des Eintrags.</span><span class="sxs-lookup"><span data-stu-id="5da6c-117">If the Tablet PC Platform components are not installed, then the user is given a standard text box control for the title and body of the entry.</span></span>

<span data-ttu-id="5da6c-118">Nachdem der Benutzer die Erstellung des Eintrags abgeschlossen hat, klickt er auf eine Schaltfläche, Hinzufügen eines Blogs, und der Beitrag wird zum Speichern an den Webserver gesendet.</span><span class="sxs-lookup"><span data-stu-id="5da6c-118">When the user finishes creating the entry, she clicks a button, Add Blog, and the post is sent to the Web server for storage.</span></span> <span data-ttu-id="5da6c-119">Auf dem-Server speichert die Anwendung den Titeltext und das Posting-Datum sowie einen Verweis auf eine Graphics Interchange Format-Datei (GIF).</span><span class="sxs-lookup"><span data-stu-id="5da6c-119">On the server, the application saves the title text and posting date, as well as a reference to a Graphics Interchange Format (GIF) file.</span></span> <span data-ttu-id="5da6c-120">Die GIF-Datei, die ebenfalls auf dem Server gespeichert ist, enthält die frei Hand Daten aus dem Text in einer verstärkten GIF-Datei.</span><span class="sxs-lookup"><span data-stu-id="5da6c-120">The GIF file, also saved to the server, contains the ink data from the body in a fortified GIF file.</span></span> <span data-ttu-id="5da6c-121">Weitere Informationen zum verstärkten GIF-Format finden Sie unter Speichern von frei Hand Eingaben [in HTML](storing-ink-in-html.md).</span><span class="sxs-lookup"><span data-stu-id="5da6c-121">For more information about the fortified GIF format, see [Storing Ink in HTML](storing-ink-in-html.md).</span></span>

<span data-ttu-id="5da6c-122">Es gibt zwei Projekte in der Projekt Mappe inkblog: das **inkblogcontrols** -Projekt und das **inkblogweb** -Projekt.</span><span class="sxs-lookup"><span data-stu-id="5da6c-122">There are two projects in the InkBlog solution: the **InkBlogControls** project and the **InkBlogWeb** project.</span></span>

## <a name="inkblogcontrols-project"></a><span data-ttu-id="5da6c-123">Inkblogcontrols-Projekt</span><span class="sxs-lookup"><span data-stu-id="5da6c-123">InkBlogControls Project</span></span>

<span data-ttu-id="5da6c-124">Das **inkblogcontrols** -Projekt ist ein [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) -Projekt, das den Code für das Benutzer Steuerelement enthält, das das Binden auf der Webseite ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5da6c-124">The **InkBlogControls** project is a [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) project that contains the code for the user control that enables inking on the Web page.</span></span> <span data-ttu-id="5da6c-125">Der Code für dieses Steuerelement, das inkarea-Steuerelement, befindet sich in der Datei "inkarea. cs".</span><span class="sxs-lookup"><span data-stu-id="5da6c-125">The code for this control, the InkArea control, is in the InkArea.cs file.</span></span>

<span data-ttu-id="5da6c-126">Die `InkArea` Klasse erbt von der [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="5da6c-126">The `InkArea` Class inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class.</span></span> <span data-ttu-id="5da6c-127">Der Konstruktor für das- `InkArea` Steuerelement ruft eine Hilfsmethode auf `CreateInkCollectionSurface` .</span><span class="sxs-lookup"><span data-stu-id="5da6c-127">The constructor for the `InkArea` control calls a helper method, `CreateInkCollectionSurface`.</span></span>


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



<span data-ttu-id="5da6c-128">Die- `CreateInkCollectionSurface` Methode bestimmt, ob die Tablet PC-Komponenten auf dem Client verfügbar sind, indem versucht wird, eine Instanz der [InkCollector](/previous-versions/ms583683(v=vs.100)) -Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5da6c-128">The `CreateInkCollectionSurface` method determines whether the Tablet PC inking components are available on the client by attempting to create an instance of the [InkCollector](/previous-versions/ms583683(v=vs.100)) class.</span></span> <span data-ttu-id="5da6c-129">Wenn die Methode erfolgreich aufgerufen `CreateInkCollectionSurface` wird, gibt die Methode ein [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) -Objekt als Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="5da6c-129">If the call to the `CreateInkCollectionSurface` method succeeds, the method returns a [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) object as the control.</span></span>


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



<span data-ttu-id="5da6c-130">Wenn der Konstruktor ausfällt, da die Freihand-Platt Formdateien nicht gefunden werden, `InputArea` wird das Steuerelement als [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) -Steuerelement und nicht als [InkCollector](/previous-versions/ms583683(v=vs.100)) -Steuerelement instanziiert.</span><span class="sxs-lookup"><span data-stu-id="5da6c-130">If the constructor fails because the inking platform files are not found, then the `InputArea` control is instantiated as a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control rather than a [InkCollector](/previous-versions/ms583683(v=vs.100)) control.</span></span> <span data-ttu-id="5da6c-131">Der Konstruktor passt dann die Größe des Steuer Elements auf die Größe des übergeordneten Benutzer Steuer Elements an und fügt es der Auflistung der Steuerelemente des übergeordneten Elements hinzu.</span><span class="sxs-lookup"><span data-stu-id="5da6c-131">The constructor then sizes the control to the size of the parent user control and adds it to the parent's Controls collection.</span></span>

<span data-ttu-id="5da6c-132">Die inkarea-Steuerelement Klasse implementiert drei interessante öffentliche Eigenschaften: inkdata, TextData und webEnabled.</span><span class="sxs-lookup"><span data-stu-id="5da6c-132">The InkArea control class implements three interesting public properties: InkData, TextData, and WebEnabled.</span></span>

<span data-ttu-id="5da6c-133">Die inkdata-Eigenschaft ist schreibgeschützt und ermöglicht den Zugriff auf die serialisierten frei Hand Daten, wenn der Client das Binden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5da6c-133">The InkData property is read-only and provides access to the serialized ink data, if the client supports inking.</span></span> <span data-ttu-id="5da6c-134">Wenn der Client keine Verknüpfung unterstützt, ruft die inkdata-Eigenschaft eine leere Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="5da6c-134">If the client does not support inking, the InkData property gets an empty string.</span></span> <span data-ttu-id="5da6c-135">Die inkdata-Eigenschaft ruft die Hilfsmethode serializeinkdata auf, um zu bestimmen, ob der Client das Binden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5da6c-135">The InkData property calls a helper method, SerializeInkData, to determine if the client supports inking.</span></span>


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



<span data-ttu-id="5da6c-136">In der- `SerializeInkData` Methode ist die Umwandlung in [InkCollector](/previous-versions/ms583683(v=vs.100)) erforderlich, wenn das [Ink](/previous-versions/ms583670(v=vs.100)) -Objekt angefordert wird, da `inputArea` als- [Steuer](/dotnet/api/system.windows.forms.control?view=netcore-3.1)Element deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="5da6c-136">In the `SerializeInkData` method, the cast to [InkCollector](/previous-versions/ms583683(v=vs.100)) is necessary when obtaining the [Ink](/previous-versions/ms583670(v=vs.100)) object, because `inputArea` is declared as a [Control](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span></span> <span data-ttu-id="5da6c-137">Wenn das Ink-Objekt beliebige Striche enthält, werden die frei Hand Daten `inkDataBytes` als GIF (angegeben mit dem [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) -Enumerationswert) im Bytearray gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5da6c-137">If the Ink object contains any strokes, the ink data is saved into the `inkDataBytes` byte array as a GIF (specified by using the [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) enumeration value).</span></span> <span data-ttu-id="5da6c-138">Die-Methode konvertiert dann das Bytearray in eine Base64-codierte Zeichenfolge und gibt diese Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="5da6c-138">The method then converts the byte array to a Base64-encoded string and returns this string.</span></span>

<span data-ttu-id="5da6c-139">Vorausgesetzt, dass der Client eine Erkennung ausführen kann, gibt die- `TextData` Eigenschaft das [erkentionresult](/previous-versions/ms552537(v=vs.100)) -Objekt zurück, das die frei Hand Daten an eine Handschrifterkennung übergibt.</span><span class="sxs-lookup"><span data-stu-id="5da6c-139">Assuming that the client can perform recognition, the `TextData` property returns the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object from passing the ink data to a handwriting recognizer.</span></span> <span data-ttu-id="5da6c-140">Wenn der Client nicht frei Hand fähig ist, wird der Text Feld Inhalt zurückgegeben, wie im folgenden Code dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5da6c-140">If the client is not ink-aware, the text box contents are returned, as shown in the following code.</span></span>


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



<span data-ttu-id="5da6c-141">Die- `TextData` Eigenschaft ruft eine Hilfsmethode `RecognizeInkData` auf, die im folgenden Code gezeigt wird, um die Erkennung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5da6c-141">The `TextData` property calls a helper method, `RecognizeInkData`, shown in the following code, to carry out the recognition.</span></span> <span data-ttu-id="5da6c-142">Wenn auf dem System Erkennungs-Engines vorhanden sind, `RecognizeInkData` gibt die Methode eine Zeichenfolge zurück, die die [TopString](/previous-versions/ms572009(v=vs.100)) -Eigenschaft des [erkentionresult](/previous-versions/ms552537(v=vs.100)) -Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="5da6c-142">When recognition engines are present on the system, the `RecognizeInkData` method returns a string containing the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object's [TopString](/previous-versions/ms572009(v=vs.100)) property.</span></span> <span data-ttu-id="5da6c-143">Andernfalls wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5da6c-143">Otherwise, it returns an empty string.</span></span>


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



<span data-ttu-id="5da6c-144">Die- `InkEnabled` Eigenschaft ist ein Schreib geschützter boolescher Wert, der angibt, ob das Freihand auf dem Client Computer unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5da6c-144">The `InkEnabled` property is a read-only Boolean value that indicates whether inking is supported on the client machine.</span></span>

<span data-ttu-id="5da6c-145">Ein weiterer wichtiger öffentlicher Member der `InkArea` Steuerelement Klasse ist die- `DisposeResources` Methode.</span><span class="sxs-lookup"><span data-stu-id="5da6c-145">Another important public member of the `InkArea` control class is the `DisposeResources` method.</span></span> <span data-ttu-id="5da6c-146">Diese Methode ruft intern die- `Dispose` Methode auf, um sicherzustellen, dass alle Ressourcen, die vom Benutzer Steuerelement genutzt werden, bereinigt werden.</span><span class="sxs-lookup"><span data-stu-id="5da6c-146">This method internally calls the `Dispose` method to ensure that all resources leveraged by the user control are cleaned up.</span></span> <span data-ttu-id="5da6c-147">Jede Anwendung, die das-Steuerelement verwendet, `InkArea` muss die- `DisposeResources` Methode nach Abschluss der Verwendung des-Steuer Elements aufruft.</span><span class="sxs-lookup"><span data-stu-id="5da6c-147">Any application that uses the `InkArea` control must call the `DisposeResources` method when it is finished using the control.</span></span>

## <a name="inkblogweb-project"></a><span data-ttu-id="5da6c-148">Inkblogweb-Projekt</span><span class="sxs-lookup"><span data-stu-id="5da6c-148">InkBlogWeb Project</span></span>

<span data-ttu-id="5da6c-149">Das inkblogweb-Projekt ist ein Websetup-Bereitstellungs Projekt, das auf das-Steuerelement verweist, `InkArea` um die blogfunktionalität bereitzustellen</span><span class="sxs-lookup"><span data-stu-id="5da6c-149">The InkBlogWeb project is a Web Setup deployment project that references the `InkArea` control to provide the blogging functionality.</span></span> <span data-ttu-id="5da6c-150">Weitere Informationen zu Websetup-Bereitstellungs Projekten finden Sie unter [Bereitstellung eines Websetup-Projekts](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="5da6c-150">For more information about Web Setup deployment projects, see [Deployment of a Web Setup Project](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).</span></span>

<span data-ttu-id="5da6c-151">Es gibt zwei ASPX-Dateien, die das Blog Beispiel implementieren: default. aspx und addblog. aspx.</span><span class="sxs-lookup"><span data-stu-id="5da6c-151">There are two .aspx files that implement the blogging sample: Default.aspx and AddBlog.aspx.</span></span> <span data-ttu-id="5da6c-152">Default. aspx ist die Standardseite für die inkblogweb-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5da6c-152">Default.aspx is the default page for the InkBlogWeb application.</span></span> <span data-ttu-id="5da6c-153">Die Code Behind-Datei für diese Seite ist "default. aspx. cs".</span><span class="sxs-lookup"><span data-stu-id="5da6c-153">The code behind file for this page is Default.aspx.cs.</span></span> <span data-ttu-id="5da6c-154">Diese Seite enthält einen Link zu der Seite, die das neue Blogeintrag-Formular enthält, und zeigt alle vorhandenen Blogeinträge an.</span><span class="sxs-lookup"><span data-stu-id="5da6c-154">This page provides a link to the page containing the new blog entry form and displays any existing blog entries.</span></span> <span data-ttu-id="5da6c-155">Dieser Prozess wird später nach der folgenden Untersuchung der neuen Blogeintrag-Formularseite addblog. aspx beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5da6c-155">This process is described later, after the following examination of the new blog entry form page, AddBlog.aspx.</span></span>

<span data-ttu-id="5da6c-156">Addblog. aspx und die zugehörige Code Behind-Datei, addblog. aspx. cs, enthalten die Logik und den Benutzeroberflächen Code zum Erstellen neuer Blogeinträge.</span><span class="sxs-lookup"><span data-stu-id="5da6c-156">AddBlog.aspx and its code-behind file, AddBlog.aspx.cs, contain the logic and user interface code for creating new blog entries.</span></span> <span data-ttu-id="5da6c-157">Addblox. aspx verweist auf zwei Instanzen der inkarea-Steuerelement Klasse, die im Projekt inkblogcontrols erstellt wurde, indem das HTML-Objekt Element verwendet wird, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5da6c-157">AddBlox.aspx references two instances of the InkArea control class created in the InkBlogControls project by using the HTML OBJECT element as shown in the following example.</span></span> <span data-ttu-id="5da6c-158">Eine Instanz verfügt über ein `id` Attribut von inkblogtitle, das andere hat ein ID-Attribut von inkblogbody.</span><span class="sxs-lookup"><span data-stu-id="5da6c-158">One instance has an `id` attribute of inkBlogTitle and the other has an id attribute of inkBlogBody.</span></span>

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

<span data-ttu-id="5da6c-159">Die InkBlogControls.dll-Assembly muss sich im selben Verzeichnis befinden wie die ASPX-Seite, die darauf verweist.</span><span class="sxs-lookup"><span data-stu-id="5da6c-159">The InkBlogControls.dll assembly must be present in the same directory as the .aspx page that is referencing it.</span></span> <span data-ttu-id="5da6c-160">Das Websetup-Bereitstellungs Projekt stellt sicher, dass dies der Fall ist. Dies wird durch das vorhanden sein des Elements "primäre Ausgabe von inkblogcontrols" im Bereitstellungs Projekt deutlich.</span><span class="sxs-lookup"><span data-stu-id="5da6c-160">The Web Setup deployment project ensures that this is the case, as evidenced by the presence of the "Primary output from InkBlogControls" item in the Deployment Project.</span></span>

<span data-ttu-id="5da6c-161">Das Title-Steuerelement ist nur 48 Pixel hoch, um den Eintrag einer einzelnen Zeile frei Hand Eingaben für den Titel zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="5da6c-161">The title control is only 48 pixels high to facilitate the entry of a single line of ink for the title.</span></span> <span data-ttu-id="5da6c-162">Das Body-Steuerelement ist 296 Pixel hoch, um Platz für größere Blogeinträge mehrerer Zeilen oder möglicherweise Zeichnungen zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="5da6c-162">The body control is 296 pixels high to make room for larger blog entries of multiple lines or perhaps drawings.</span></span>

<span data-ttu-id="5da6c-163">Die inkarea-Steuerelemente sind mit einer Client seitigen Skriptfunktion, addblog, über den OnClick-Ereignishandler eines Standard-HTML-Schaltflächen Elements verbunden.</span><span class="sxs-lookup"><span data-stu-id="5da6c-163">The InkArea controls are connected to a client-side script function, AddBlog, by means of a standard HTML BUTTON element's onclick event handler.</span></span>

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

<span data-ttu-id="5da6c-164">Es gibt auch ein HTML-Formular auf der Seite, das drei verborgene Eingabeelemente enthält: blogtitletext, blogbodytext und blogbodyinkdata.</span><span class="sxs-lookup"><span data-stu-id="5da6c-164">There is also an HTML form on the page that contains three hidden INPUT elements: BlogTitleText, BlogBodyText, and BlogBodyInkData.</span></span> <span data-ttu-id="5da6c-165">Dieses Formular wird verwendet, um die Blogeintrags Daten an den Server zurückzusenden.</span><span class="sxs-lookup"><span data-stu-id="5da6c-165">This form is used to post the blog entry data back to the server.</span></span> <span data-ttu-id="5da6c-166">Addblog. aspx ist der Post Back Handler, der für das Formular definiert ist.</span><span class="sxs-lookup"><span data-stu-id="5da6c-166">AddBlog.aspx is the post-back handler defined for the form.</span></span>

<span data-ttu-id="5da6c-167">Die in Microsoft JScript geschriebene Funktion "addblog" <entity type="reg"/> extrahiert die Blog Daten aus den inkarea-Steuerelementen und sendet die Ergebnisse an den Server.</span><span class="sxs-lookup"><span data-stu-id="5da6c-167">The AddBlog function-written in Microsoft JScript<entity type="reg"/>-extracts the blog data from the InkArea controls and posts the results to the server.</span></span>


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



<span data-ttu-id="5da6c-168">Wenn die Daten auf dem Server eintreffen, prüft der Code in addblog. aspx. cs den \_ Ereignishandler für den Seiten Ladevorgang, um festzustellen, ob die Form-Eigenschaft des HttpRequest-Objekts Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="5da6c-168">When the data arrives at the server, the code in AddBlog.aspx.cs checks the Page\_Load event handler to see if the HttpRequest object's Form property contains any data.</span></span> <span data-ttu-id="5da6c-169">Wenn dies der Fall ist, wird ein Dateiname erstellt, der auf der aktuellen Systemzeit basiert, die Formulardaten in drei Zeichen folgen Variablen einfügt und die Daten in eine HTML-Datei und eine GIF-Datei, die die frei Hand Daten enthält (sofern vorhanden), wie im folgenden Code gezeigt, geschrieben.</span><span class="sxs-lookup"><span data-stu-id="5da6c-169">If so, it creates a file name based on the current system time, puts the form data into three string variables and writes the data out to an HTML file and a GIF file containing the ink data, if present, as shown in the following code.</span></span>


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



<span data-ttu-id="5da6c-170">Weitere Informationen zu den Hilfsmethoden finden Sie im Beispiel Quell Code.</span><span class="sxs-lookup"><span data-stu-id="5da6c-170">For more details about the helper methods, refer to the sample source code.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="5da6c-171">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="5da6c-171">Running the Sample</span></span>

<span data-ttu-id="5da6c-172">Das Tablet PC SDK 1,7 installiert standardmäßig das frei Hand Blog-webbeispiel.</span><span class="sxs-lookup"><span data-stu-id="5da6c-172">The Tablet PC SDK 1.7 installs the Ink Blog Web sample by default.</span></span> <span data-ttu-id="5da6c-173">Um das Beispiel auszuführen, navigieren Sie in Internet Explorer zu https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx .</span><span class="sxs-lookup"><span data-stu-id="5da6c-173">To run the sample, in Internet Explorer, navigate to https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx.</span></span> <span data-ttu-id="5da6c-174">Wenn Sie Windows Server 2003 ausführen, ersetzen Sie den Computernamen durch "localhost".</span><span class="sxs-lookup"><span data-stu-id="5da6c-174">If you are running Windows Server 2003, substitute your computer name for "localhost".</span></span>

> [!Note]  
> <span data-ttu-id="5da6c-175">Die kompilierten webbeispiele werden von der Standard Installationsoption für das SDK nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="5da6c-175">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="5da6c-176">Sie müssen eine benutzerdefinierte Installation durchführen und die unter Option "vorkompilierte webbeispiele" auswählen, um Sie zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5da6c-176">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

<span data-ttu-id="5da6c-177">Sie können das Beispiel auch ausführen, indem Sie das Projekt in Microsoft Visual Studio .NET öffnen und <entity type="reg"/> dann auf einem separaten Computer bereitstellen, auf dem IIS ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5da6c-177">You can also run the sample by opening and building the project in Microsoft Visual Studio<entity type="reg"/> .NET and then deploying it to a separate computer running IIS.</span></span>

## <a name="troubleshooting-the-sample"></a><span data-ttu-id="5da6c-178">Problembehandlung bei diesem Beispiel</span><span class="sxs-lookup"><span data-stu-id="5da6c-178">Troubleshooting the Sample</span></span>

<span data-ttu-id="5da6c-179">Drei Bereiche, die Schwierigkeiten verursachen können, wenn das Beispiel ausgeführt oder gehostet wird, sind Berechtigungen und Erkennung.</span><span class="sxs-lookup"><span data-stu-id="5da6c-179">Three areas that may cause difficulty when running or hosting the sample are permissions and recognition.</span></span>

### <a name="permissions"></a><span data-ttu-id="5da6c-180">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="5da6c-180">Permissions</span></span>

<span data-ttu-id="5da6c-181">Das Beispiel erfordert Schreibberechtigungen innerhalb des virtuellen Stamm Ordners für das Konto, das versucht, einen neuen Blogeintrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5da6c-181">The sample requires write permissions within the virtual root folder for the account that is attempting to create a new blog entry.</span></span> <span data-ttu-id="5da6c-182">Standardmäßig verfügt die kompilierte Version des Beispiels, das im Tablet PC SDK 1,7 bereitgestellt wurde, über die richtigen Berechtigungen, um diese Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="5da6c-182">By default, the compiled version of the sample provided in the Tablet PC SDK 1.7 has the correct permissions set to meet this requirement.</span></span>

<span data-ttu-id="5da6c-183">Wenn Sie das Beispiel mit dem bereitgestellten Websetup-Bereitstellungs Projekt erstellen und bereitstellen, müssen Sie der Gruppe "% MachineName% \\ Users" Schreibzugriff auf den Dateisystem Ordner zuweisen, auf den vom virtuellen Stammverzeichnis "inkblogweb" verwiesen wird (z. b. "C: \\ Inetpub \\ wwwroot \\ inkblogweb").</span><span class="sxs-lookup"><span data-stu-id="5da6c-183">If you build and deploy the sample by using the provided Web Setup deployment project, you must give the %MACHINENAME%\\Users group write-access to the file system folder pointed to by the InkBlogWeb virtual root (for example, C:\\InetPub\\WWWRoot\\InkBlogWeb).</span></span> <span data-ttu-id="5da6c-184">Die Gruppe Benutzer enthält das anonyme Konto, das von IIS verwendet wird. auf diese Weise kann die ASP.NET-Anwendung die neuen Blogeinträge in das Dateisystem schreiben.</span><span class="sxs-lookup"><span data-stu-id="5da6c-184">The Users group includes the Anonymous account used by IIS, thus allowing the ASP.NET application to write the new blog entries to the file system.</span></span> <span data-ttu-id="5da6c-185">Eine Alternative besteht darin, den anonymen Zugriff auf das virtuelle Stammverzeichnis zu entfernen und die Authentifizierung zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="5da6c-185">An alternative is to remove anonymous access to the virtual root and force authentication.</span></span>

### <a name="recognition"></a><span data-ttu-id="5da6c-186">Erkennung</span><span class="sxs-lookup"><span data-stu-id="5da6c-186">Recognition</span></span>

<span data-ttu-id="5da6c-187">Die Handschrifterkennung muss installiert sein, damit die frei Hand Eingaben im Titel des Blogs erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="5da6c-187">The handwriting recognizers must be installed in order to recognize the ink in the title of the blog.</span></span> <span data-ttu-id="5da6c-188">Wenn Sie von einem Computer mit einem anderen Betriebssystem als Windows XP Tablet PC Edition auf die Anwendung inkblog zugreifen, aber mit installiertem Tablet PC SDK 1,7, können Sie in den inkarea-Steuerelementen in Freihand schreiben, aber die Erkennungs-Engines sind nicht vorhanden, und für ihre Blogeinträge werden keine Titel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5da6c-188">If you access the InkBlog application from a computer with an operating system other than Windows XP Tablet PC Edition but with the Tablet PC SDK 1.7 installed, you can write in ink in the InkArea controls, but the recognition engines will not be present and no titles will appear for your blog entries.</span></span> <span data-ttu-id="5da6c-189">Der frei Hand Inhalt im Text wird jedoch immer noch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5da6c-189">The ink content in the body still appears, though.</span></span>

### <a name="machine-configuration"></a><span data-ttu-id="5da6c-190">Computerkonfiguration</span><span class="sxs-lookup"><span data-stu-id="5da6c-190">Machine Configuration</span></span>

<span data-ttu-id="5da6c-191">Wenn Sie ASP.net und den .NET Framework auf einem Computer installiert haben und anschließend IIS deinstallieren und neu installieren, werden die Skript Zuordnungen unterbrechen und ASP.NET funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="5da6c-191">If you have installed ASP.NET and the .NET Framework on a computer and you then uninstall and reinstall IIS, the script maps will break and ASP.NET will not work.</span></span> <span data-ttu-id="5da6c-192">Wenn dies der Fall ist, können Sie die ASP.NET-Skript Zuordnungen mit dem ASP.NET IIS-Registrierungs Tool (ASPNET \_regiis.exe-i) reparieren.</span><span class="sxs-lookup"><span data-stu-id="5da6c-192">If this happens, you can repair the ASP.NET script maps with the ASP.NET IIS Registration tool (Aspnet\_regiis.exe -i).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5da6c-193">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5da6c-193">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5da6c-194">[InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="5da6c-194">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="5da6c-195">Frei Hand Eingaben im Web</span><span class="sxs-lookup"><span data-stu-id="5da6c-195">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> <dt>

[<span data-ttu-id="5da6c-196">Frei Hand Datenformate</span><span class="sxs-lookup"><span data-stu-id="5da6c-196">Ink Data Formats</span></span>](ink-data-formats.md)
</dt> <dt>

[<span data-ttu-id="5da6c-197">System. Windows. Forms. UserControl-Klasse</span><span class="sxs-lookup"><span data-stu-id="5da6c-197">System.Windows.Forms.UserControl Class</span></span>](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
