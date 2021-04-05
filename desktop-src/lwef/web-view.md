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
# <a name="customizing-a-folders-web-view"></a><span data-ttu-id="e7c41-108">Anpassen der Webansicht eines Ordners</span><span class="sxs-lookup"><span data-stu-id="e7c41-108">Customizing a Folder's Web View</span></span>

<span data-ttu-id="e7c41-109">\[Dieses Feature wird nur unter Windows XP oder früher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-109">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="e7c41-110">\]</span><span class="sxs-lookup"><span data-stu-id="e7c41-110">\]</span></span>

<span data-ttu-id="e7c41-111">Eine Webansicht ist eine leistungsstarke und flexible Möglichkeit, den Windows-Explorer zu verwenden, um Informationen zum Inhalt eines shellordners anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-111">A Web view is a powerful and flexible way to use the Windows Explorer to display information about the contents of a Shell folder.</span></span>

-   [<span data-ttu-id="e7c41-112">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="e7c41-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="e7c41-113">Verwenden der webansichts Vorlage</span><span class="sxs-lookup"><span data-stu-id="e7c41-113">Using the Web View Template</span></span>](#using-the-web-view-template)
    -   [<span data-ttu-id="e7c41-114">Der Vorlagen Text</span><span class="sxs-lookup"><span data-stu-id="e7c41-114">The Template Body</span></span>](#the-template-body)
    -   [<span data-ttu-id="e7c41-115">Der Vorlagen Kopf</span><span class="sxs-lookup"><span data-stu-id="e7c41-115">The Template Head</span></span>](#the-template-head)
-   [<span data-ttu-id="e7c41-116">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e7c41-116">Summary</span></span>](#summary)

## <a name="introduction"></a><span data-ttu-id="e7c41-117">Einführung</span><span class="sxs-lookup"><span data-stu-id="e7c41-117">Introduction</span></span>

<span data-ttu-id="e7c41-118">Windows bietet Benutzern zwei Hauptmöglichkeiten, den Shellnamespace anzuzeigen und zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="e7c41-118">Windows offers users two primary ways to view and navigate the Shell namespace.</span></span> <span data-ttu-id="e7c41-119">Die am häufigsten vertrauten, der klassischen Stil, ähneln dem vertrauten Windows-Datei-Manager.</span><span class="sxs-lookup"><span data-stu-id="e7c41-119">The most familiar of these, the Classic style, is similar to the familiar Windows File Manager.</span></span> <span data-ttu-id="e7c41-120">Im rechten Bereich wird der Inhalt des aktuell ausgewählten Ordners in einem von fünf Formaten aufgelistet: großes Symbol, kleines Symbol, Liste, Details und Miniaturansicht.</span><span class="sxs-lookup"><span data-stu-id="e7c41-120">The right pane lists the contents of the currently selected folder in one of five formats: Large Icon, Small Icon, List, Details, and Thumbnail.</span></span> <span data-ttu-id="e7c41-121">Der Hauptunterschied zwischen dem Windows-Datei-Manager ist der linke Bereich, der der Explorer-Leiste von Windows Internet Explorer ähnelt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-121">The major difference from Windows File Manager is the left pane, which looks very similar to the Explorer bar of Windows Internet Explorer.</span></span> <span data-ttu-id="e7c41-122">Die Größe kann geändert oder entfernt werden, und es können neben der vertrauten Dateisystem Struktur auch mehrere Bereiche angezeigt werden, z. b. ein Suchbereich.</span><span class="sxs-lookup"><span data-stu-id="e7c41-122">It can be resized or removed, and it can display several panes in addition to the familiar file system tree, such as a search pane.</span></span>

> [!Note]  
> <span data-ttu-id="e7c41-123">Die Informationen in diesem Dokument gelten nicht für Windows XP, die behandelten Techniken gelten nur für frühere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="e7c41-123">The information in this document does not apply to Windows XP, the techniques discussed apply only to earlier versions of Windows.</span></span>

 

<span data-ttu-id="e7c41-124">Die folgende Abbildung zeigt den Ordner Drucker im klassischen Stil.</span><span class="sxs-lookup"><span data-stu-id="e7c41-124">The following illustration shows the Printers folder in Classic style.</span></span>

![klassisches Format des Drucker Ordners.](images/webview1.png)

<span data-ttu-id="e7c41-126">Der klassische Stil eignet sich gut für normale Dateisystem Ordner und-Dateien.</span><span class="sxs-lookup"><span data-stu-id="e7c41-126">The Classic style works reasonably well for normal file system folders and files.</span></span> <span data-ttu-id="e7c41-127">Allerdings hat sich das Dateisystem mit der Einführung von Windows 95 in den-Namespace weiterentwickelt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-127">However, with the introduction of Windows 95, the file system has evolved into the namespace.</span></span> <span data-ttu-id="e7c41-128">Der-Namespace ermöglicht die Erstellung *virtueller Ordner*, z. b. Drucker oder Netzwerkumgebung, die sehr unterschiedliche Informationstypen darstellen können als ein normaler Dateisystem Ordner.</span><span class="sxs-lookup"><span data-stu-id="e7c41-128">The namespace allows the creation of *virtual folders*, such as Printers or Network Neighborhood, that can represent very different types of information than a normal file system folder.</span></span>

<span data-ttu-id="e7c41-129">Der Webstil, auch bekannt als Webansicht, bietet eine flexiblere und leistungsfähigere Möglichkeit zur Darstellung von Informationen als klassischer Stil.</span><span class="sxs-lookup"><span data-stu-id="e7c41-129">The Web style, also known as a Web view, offers a more flexible and powerful way of presenting information than Classic style.</span></span> <span data-ttu-id="e7c41-130">In einer Webansicht zeigt der Benutzer den Namespace im Grunde mithilfe von Internet Explorer an und navigiert ihn.</span><span class="sxs-lookup"><span data-stu-id="e7c41-130">In a Web view, the user basically views and navigates the namespace using Internet Explorer.</span></span> <span data-ttu-id="e7c41-131">Das grundlegende Layout einer Webansicht ähnelt dem klassischen Stil.</span><span class="sxs-lookup"><span data-stu-id="e7c41-131">The basic layout of a Web view is similar to Classic style.</span></span> <span data-ttu-id="e7c41-132">Die Explorer-Leiste ist unverändert.</span><span class="sxs-lookup"><span data-stu-id="e7c41-132">The Explorer bar is unchanged.</span></span> <span data-ttu-id="e7c41-133">Die Region, die in der Datei Liste enthalten war, wird jedoch zu einem allgemeinen Anzeigebereich, bei dem es sich eigentlich um eine Webseite handelt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-133">However, the region that was occupied by the file list becomes a general-purpose display area that is effectively a webpage.</span></span> <span data-ttu-id="e7c41-134">Eine Webansicht wird weiterhin zum Anzeigen von Informationen über den Inhalt eines Ordners verwendet. es gibt jedoch einige Einschränkungen, welche Informationen angezeigt werden, oder wie.</span><span class="sxs-lookup"><span data-stu-id="e7c41-134">A Web view is still used to display information about the contents of a folder, but there are few constraints on what information is displayed, or how.</span></span> <span data-ttu-id="e7c41-135">Jeder Ordner kann über eine eigene Webansicht verfügen, die an die jeweiligen Features angepasst ist.</span><span class="sxs-lookup"><span data-stu-id="e7c41-135">Each folder can have its own Web view, customized to suit its particular features.</span></span>

<span data-ttu-id="e7c41-136">Die folgende Abbildung zeigt eine Webansicht des Ordners "Printers" (im klassischen Stil dargestellt).</span><span class="sxs-lookup"><span data-stu-id="e7c41-136">The following illustration shows a Web view of the Printers folder (shown previously in Classic style).</span></span>

![Standardweb Ansicht des Ordners "Drucker".](images/webview2.png)

<span data-ttu-id="e7c41-138">Ähnlich wie herkömmliche Webseiten werden Webansichten von einer HTML-basierten Vorlage gesteuert.</span><span class="sxs-lookup"><span data-stu-id="e7c41-138">Much like conventional webpages, Web views are controlled by an HTML-based template.</span></span> <span data-ttu-id="e7c41-139">Das Erstellen einer webansichts Vorlage ist nahezu identisch mit dem Erstellen einer Webseite und bietet das gleiche Maß an Flexibilität in den Inhalten und dem Layout von Informationen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-139">Authoring a Web view template is nearly identical to authoring a webpage and provides the same degree of flexibility in content and layout of information.</span></span> <span data-ttu-id="e7c41-140">Webansichts Vorlagen können dynamisches HTML (DHTML) und Skripts verwenden, um auf Ereignisse zu reagieren, z. b. ein Benutzer, der auf ein Element klickt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-140">Web view templates can use Dynamic HTML (DHTML) and scripting to respond to events, such as a user clicking an item.</span></span> <span data-ttu-id="e7c41-141">Sie können auch Objekte hosten, die es Ihnen ermöglichen, Informationen aus dem Ordner oder dessen Inhalt abzurufen und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-141">They can also host objects that allow them to obtain and display information from the folder or its contents.</span></span>

<span data-ttu-id="e7c41-142">Der Benutzer kann eine Webansicht auswählen, indem er Windows-Explorer startet, im Menü **Ansicht** auf **Ordneroptionen** klickt und diese Option **aktiviert: Webinhalt in Ordnern aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="e7c41-142">The user can choose a Web view by starting Windows Explorer, clicking **Folder Options** on the **View** menu, and selecting this option: **Enable Web content in folders**.</span></span> <span data-ttu-id="e7c41-143">Der Benutzer kann jedoch auch Internet Explorer starten und den Browser auf das Dateisystem verweisen, indem er auf das Menü **Ansicht** , auf **Explorer-Leiste** zeigt und auf **Ordner** klickt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-143">However, the user can also start Internet Explorer and point the browser at the file system by clicking the **View** menu, pointing to **Explorer Bar**, and clicking **Folders**.</span></span> <span data-ttu-id="e7c41-144">In einer Webansicht gibt es praktisch keinen Unterschied zwischen Internet Explorer und Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="e7c41-144">In a Web view, there is virtually no difference between Internet Explorer and Windows Explorer.</span></span>

<span data-ttu-id="e7c41-145">Auf der linken Seite des rechten Bereichs wird in der Drucker Webansicht ein Banner mit dem Namen und dem Symbol des Ordners angezeigt, gefolgt von einem Informationsblock zum Ordner.</span><span class="sxs-lookup"><span data-stu-id="e7c41-145">On the left side of the right pane, the Printers Web view displays a banner with the folder's name and icon, followed by a block of information about the folder.</span></span> <span data-ttu-id="e7c41-146">Die übliche Datei Liste befindet sich auf der rechten Seite der Seite.</span><span class="sxs-lookup"><span data-stu-id="e7c41-146">The usual file list occupies the right side of the page.</span></span>

<span data-ttu-id="e7c41-147">Wenn ein Benutzer auf ein Element klickt, werden ausführliche Informationen über das Element im Informationsblock angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-147">When a user clicks an item, detailed information about the item appears in the information block.</span></span> <span data-ttu-id="e7c41-148">Die Drucker-Webansicht zeigt tatsächlich die gleichen Informationen an, die im klassischen Stil verfügbar sind, aber in einem besser verwendbaren Format.</span><span class="sxs-lookup"><span data-stu-id="e7c41-148">The Printers Web view actually displays much the same information that is available in Classic style, but it does so in a more usable format.</span></span> <span data-ttu-id="e7c41-149">Allerdings ist eine Webansicht nicht einfach eine andere Möglichkeit, um klassische Stil Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-149">However, a Web view is not simply a different way to display Classic style information.</span></span> <span data-ttu-id="e7c41-150">Beispielsweise kann ein Link zu einer nützlichen Website unter dem Informationsblock angezeigt werden, einem Feature, das im klassischen Stil nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e7c41-150">For example, a link to a useful website can be displayed below the information block, a feature that is not available in Classic style.</span></span> <span data-ttu-id="e7c41-151">Wenn der Benutzer auf den Link klickt, wird die Website angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-151">If the user clicks the link, the site will be displayed.</span></span>

<span data-ttu-id="e7c41-152">Die in der obigen Abbildung gezeigte Drucker-Webansicht ähnelt dem klassischen Stil, da die zugrunde liegende webansichts Vorlage (eine htt-Datei) auf diese Weise geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="e7c41-152">The Printers Web view shown in the preceding illustration is similar to the Classic style, because the underlying Web view template (an .htt file) was written that way.</span></span> <span data-ttu-id="e7c41-153">Die Liste der Dateien wird beispielsweise nicht direkt von der webansichts Vorlage generiert.</span><span class="sxs-lookup"><span data-stu-id="e7c41-153">The list of files, for instance, is not generated by the Web view template directly.</span></span> <span data-ttu-id="e7c41-154">Es wird von einem [**webviewfoldercontents**](webviewfoldercontents.md) -Objekt erstellt und angezeigt, das von der webansichts Vorlage gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-154">It is created and displayed by a [**WebViewFolderContents**](webviewfoldercontents.md) object hosted by the Web view template.</span></span> <span data-ttu-id="e7c41-155">Mit den Methoden und Eigenschaften des Objekts kann die Webansicht das Layout Steuern und Informationen zu bestimmten Elementen abrufen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-155">The object's methods and properties allow the Web view to control its layout and obtain information about particular items.</span></span> <span data-ttu-id="e7c41-156">Der Inhalt und das Layout des Banners und des Informations Blocks werden in der webansichts Vorlage angegeben.</span><span class="sxs-lookup"><span data-stu-id="e7c41-156">The content and layout of the banner and information block is specified in the Web view template.</span></span>

<span data-ttu-id="e7c41-157">Da eine Webansicht DHTML unterstützt, kann die Vorlage auch verwendet werden, um die Benutzerinteraktion zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e7c41-157">Because a Web view supports DHTML, the template can also be used to handle user interaction.</span></span> <span data-ttu-id="e7c41-158">Wenn ein Benutzer beispielsweise auf eines der Drucker Symbole klickt, löst das **WebViewFolderIcon** -Objekt ein [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="e7c41-158">For instance, when a user clicks one of the printer icons, the **WebViewFolderIcon** object fires a [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) event.</span></span> <span data-ttu-id="e7c41-159">Die Vorlage verwendet einen im Skript geschriebenen DHTML-Ereignishandler, um die angeforderten Informationen abzurufen und im Informationsblock anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-159">The template uses a DHTML event handler written in script to retrieve the requested information and display it in the information block.</span></span>

<span data-ttu-id="e7c41-160">Dieses einfache Beispiel für den Drucker Ordner ist nicht die einzige Möglichkeit, eine Webansicht zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7c41-160">This simple example for the Printers folder is by no means the only way to use a Web view.</span></span> <span data-ttu-id="e7c41-161">Wenn Sie Ihre eigene Vorlage schreiben und ggf. Objekte verwenden, können Sie eine Webansicht verwenden, um Informationen anzuzeigen und mit dem Benutzer auf die gewünschte Weise zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="e7c41-161">By writing your own template and, if necessary, objects, you can use a Web view to display information and interact with the user in whatever way you find most effective.</span></span> <span data-ttu-id="e7c41-162">Beachten Sie, dass webansichts Vorlagen derzeit nur System definierte virtuelle Ordner anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-162">Note that, at present, Web view templates only display system-defined virtual folders.</span></span> <span data-ttu-id="e7c41-163">Obwohl Entwickler einen virtuellen Ordner erstellen können, indem Sie eine Namespace Erweiterung implementieren, müssen Sie die unter [Namespace Erweiterungen](/windows/desktop/shell/nse-works) beschriebenen Techniken verwenden, um Sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-163">Although developers can create a virtual folder by implementing a namespace extension, they must use the techniques described in [Namespace Extensions](/windows/desktop/shell/nse-works) to display it.</span></span>

## <a name="using-the-web-view-template"></a><span data-ttu-id="e7c41-164">Verwenden der webansichts Vorlage</span><span class="sxs-lookup"><span data-stu-id="e7c41-164">Using the Web View Template</span></span>

<span data-ttu-id="e7c41-165">Die Art und Weise, in der Daten in einer Webansicht angezeigt werden, kann durch Ändern der Desktop.ini Datei eines Ordners eingeschränkt angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="e7c41-165">The way data is displayed in a Web view can be customized in a limited way by modifying a folder's Desktop.ini file.</span></span> <span data-ttu-id="e7c41-166">Weitere Informationen finden Sie [unter Anpassen von Ordnern mit Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) .</span><span class="sxs-lookup"><span data-stu-id="e7c41-166">See [Customizing Folders with Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) for details.</span></span> <span data-ttu-id="e7c41-167">Eine viel flexiblere und leistungsfähigere Möglichkeit zum Anpassen einer Webansicht besteht darin, eine benutzerdefinierte webansichtenvorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-167">A much more flexible and powerful way to customize a Web view is to create a custom Web view template.</span></span>

<span data-ttu-id="e7c41-168">Die Vorlage Webansicht steuert, was in einer Webansicht angezeigt wird und wie.</span><span class="sxs-lookup"><span data-stu-id="e7c41-168">The Web view template controls what is displayed in a Web view and how.</span></span> <span data-ttu-id="e7c41-169">Dabei werden standardmäßige HTML-, DHTML-und Skript Verfahren verwendet, um Informationen abzurufen und anzuzeigen und mit dem Benutzer zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="e7c41-169">It uses standard HTML, DHTML, and scripting techniques to obtain and display information and interact with the user.</span></span> <span data-ttu-id="e7c41-170">In diesem Abschnitt wird erläutert, wie Sie eine Webansicht erstellen, indem Sie eine einfache Vorlage – Generic. htt) untersuchen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-170">This section discusses how to create a Web view by examining a simple template—Generic.htt.</span></span>


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



<span data-ttu-id="e7c41-171">Eine einfache Möglichkeit zum Erstellen einer eigenen webansichtenvorlage besteht darin, Generic. htt zu erstellen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e7c41-171">A simple way to create your own Web view template is to take Generic.htt and modify it.</span></span> <span data-ttu-id="e7c41-172">Da es ziemlich eingeschränkt ist, sollten Sie auch andere, komplexere Beispiele für weitere Ideen betrachten.</span><span class="sxs-lookup"><span data-stu-id="e7c41-172">Because it is rather limited, you should also look at other, more complex examples for additional ideas.</span></span> <span data-ttu-id="e7c41-173">Sie können Sie finden, indem Sie in Ihrem System nach der von allen webansichts Vorlagen verwendeten htt-Erweiterung suchen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-173">You can find them by searching your system for the .htt extension used by all Web view templates.</span></span> <span data-ttu-id="e7c41-174">Wenn Sie eine benutzerdefinierte Vorlage für einen Ordner erstellen möchten, sollten Sie mit der standardmäßigen htt-Vorlage "Folder" beginnen, die normalerweise entweder in "C: \\ Winnt \\ Web" oder "c: \\ Windows \\ Web" gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="e7c41-174">If you want to create a custom template for a folder, you should start with the default Folder.htt template, which is usually stored in either C:\\Winnt\\Web or C:\\Windows\\Web.</span></span> <span data-ttu-id="e7c41-175">Beachten Sie, dass diese Dateien als ausgeblendet definiert sind. Daher müssen Sie möglicherweise die Windows-Explorer-Einstellungen ändern, um Sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-175">Note that these files are defined as hidden, so you may need to modify your Windows Explorer settings to view them.</span></span> <span data-ttu-id="e7c41-176">Nachdem eine htt-Datei erstellt wurde, sollte Sie als schreibgeschützt markiert und ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7c41-176">Once an .htt file is created, it should be marked as read-only and hidden.</span></span>

<span data-ttu-id="e7c41-177">Webansichts Vorlagen verwenden die Erweiterung ". htt", da Sie sich geringfügig von herkömmlichen htm-Dokumenten unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="e7c41-177">Web view templates use the .htt extension because they differ slightly from conventional .htm documents.</span></span> <span data-ttu-id="e7c41-178">Der Hauptunterschied besteht aus mehreren speziellen Variablen in htt-Dateien, die das System durch die aktuellen Namespace Werte ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-178">The main difference is several special variables in .htt files that the system replaces with the current namespace values.</span></span> <span data-ttu-id="e7c41-179">Die Variablen "% thisdir%" und "% thisdirpath%" stellen den Namen und den Pfad des aktuell ausgewählten Ordners dar.</span><span class="sxs-lookup"><span data-stu-id="e7c41-179">The %THISDIR% and %THISDIRPATH% variables represent the name and path of the currently selected folder.</span></span> <span data-ttu-id="e7c41-180">Die% templatedir%-Variable stellt den Ordner dar, in dem die Stylesheets der Webansicht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e7c41-180">The %TEMPLATEDIR% variable represents the folder where the Web view style sheets are stored.</span></span>

<span data-ttu-id="e7c41-181">Wie die meisten HTML-Vorlagen bestehen auch htt-Dateien aus zwei grundlegenden Teilen: einem Text und einem Head.</span><span class="sxs-lookup"><span data-stu-id="e7c41-181">Like most HTML templates, .htt files have two basic parts: a body and a head.</span></span> <span data-ttu-id="e7c41-182">Der Vorlagen Text steuert das grundlegende Layout der Webansicht und lädt die Objekte, die für die Kommunikation mit dem Namespace und den Anzeigeinformationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7c41-182">The template body controls the basic layout of the Web view and loads the objects used to communicate with the namespace and display information.</span></span> <span data-ttu-id="e7c41-183">Die Kopfzeile enthält Skripts und Funktionen, die Aufgaben wie das Bearbeiten der Größe und das Abrufen von Informationen aus dem Ordner ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-183">The head contains scripts and functions that do tasks such as handling resizing and obtaining information from the folder.</span></span> <span data-ttu-id="e7c41-184">Die meisten Vorlagen, einschließlich Generic. htt, enthalten auch ein Stylesheet.</span><span class="sxs-lookup"><span data-stu-id="e7c41-184">Most templates, including Generic.htt, also include a style sheet.</span></span> <span data-ttu-id="e7c41-185">Im Allgemeinen ist es besser, die Stylesheet-Informationen in Ihre Vorlage einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-185">In general, it is better to include the style sheet information in your template.</span></span> <span data-ttu-id="e7c41-186">Separate Stylesheets funktionieren möglicherweise nicht ordnungsgemäß, wenn eine Webansicht mit remotenamespaces verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-186">Separate style sheets may not work properly when a Web view is used with remote namespaces.</span></span>

### <a name="the-template-body"></a><span data-ttu-id="e7c41-187">Der Vorlagen Text</span><span class="sxs-lookup"><span data-stu-id="e7c41-187">The Template Body</span></span>

<span data-ttu-id="e7c41-188">Der Text der Vorlage gibt an, was von einer Webansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-188">The body of the template specifies what will be presented by a Web view.</span></span> <span data-ttu-id="e7c41-189">Außerdem werden die Objekte, die zum Anzeigen von Informationen und zum kommunizieren mit Namespace Ordnern verwendet werden, geladen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-189">It is also where the objects used to display information and communicate with namespace folders are loaded.</span></span> <span data-ttu-id="e7c41-190">Das von Generic. htt definierte Layout ähnelt dem in der Abbildung im vorherigen Abschnitt dargestellten Layout.</span><span class="sxs-lookup"><span data-stu-id="e7c41-190">The layout defined by Generic.htt is similar to that shown in the illustration in the previous section.</span></span> <span data-ttu-id="e7c41-191">Es gibt drei Anzeige Bereiche: das Banner und den Informationsblock auf der linken Seite der Ansicht und die Datei Liste auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="e7c41-191">There are three display regions: the banner and information block on the left side of the view, and the file list on the right.</span></span>

<span data-ttu-id="e7c41-192">Die Regionen sind alle zugewiesenen IDs, die von dem Stylesheet und DHTML verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-192">The regions are all assigned identifiers to be used by the style sheet and DHTML.</span></span> <span data-ttu-id="e7c41-193">Wie im nächsten Abschnitt erläutert, gibt es zwei mögliche Banner mit den Bezeichnern "Banner" und "Minibanner".</span><span class="sxs-lookup"><span data-stu-id="e7c41-193">As discussed in the next section, there are two possible banners, with identifiers of "Banner" and "MiniBanner".</span></span> <span data-ttu-id="e7c41-194">Der Bezeichner des Informationsblock Bereichs lautet "Info".</span><span class="sxs-lookup"><span data-stu-id="e7c41-194">The identifier of the information block's region is "Info".</span></span> <span data-ttu-id="e7c41-195">Der Bezeichner des Dateilisten Objekts ist "FileList".</span><span class="sxs-lookup"><span data-stu-id="e7c41-195">The file list object's identifier is "FileList".</span></span> <span data-ttu-id="e7c41-196">Die Details des Regions [Layouts](#controlling-the-web-view-layout) werden durch das Stylesheet und die Microsoft JScript-Funktion [FixSize](#adjusting-the-layout-by-using-the-fixsize-function)behandelt, die später in diesem Kapitel erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-196">The details of the region's [layout](#controlling-the-web-view-layout) are handled by the style sheet and a Microsoft JScript function, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), which is discussed later in the chapter.</span></span>

### <a name="the-banner-region"></a><span data-ttu-id="e7c41-197">Der Banner Bereich</span><span class="sxs-lookup"><span data-stu-id="e7c41-197">The Banner Region</span></span>

<span data-ttu-id="e7c41-198">Das Banner befindet sich am oberen Rand der Anzeige in der oberen linken Ecke der Webansicht.</span><span class="sxs-lookup"><span data-stu-id="e7c41-198">The banner is located at the top of the display, in the upper-left corner of the Web view.</span></span> <span data-ttu-id="e7c41-199">Das normale Banner zeigt den Namen und das Symbol des Ordners an, dessen Inhalt in der Datei Liste auf der rechten Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-199">The normal banner displays the name and icon of the folder whose contents are displayed in the file list on the right.</span></span> <span data-ttu-id="e7c41-200">Wenn das Fenster jedoch zu kurz wird, wird unter Umständen kein Platz unterhalb des Symbols zum Anzeigen von Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-200">However, if the window becomes too short, there may be no room below the icon to display information.</span></span> <span data-ttu-id="e7c41-201">Aus diesem Grund definiert "Generic. htt" auch ein Minibanner, das nur den Ordnernamen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-201">For this reason, Generic.htt also defines a minibanner that only displays the folder name.</span></span> <span data-ttu-id="e7c41-202">Beide Banner werden anfänglich als ausgeblendet definiert.</span><span class="sxs-lookup"><span data-stu-id="e7c41-202">Both banners are initially defined as hidden.</span></span> <span data-ttu-id="e7c41-203">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) wählt aus, welches angezeigt werden soll, und legt es auf "Visible" fest.</span><span class="sxs-lookup"><span data-stu-id="e7c41-203">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) chooses which one to display and sets it to "visible".</span></span>

<span data-ttu-id="e7c41-204">Das normale Banner für Generic. htt wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="e7c41-204">The normal banner for Generic.htt is defined by:</span></span>


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



<span data-ttu-id="e7c41-205">Der erste Teil des Banner Abschnitts zeigt den Titel mit einer horizontalen, darunter liegenden Regel an.</span><span class="sxs-lookup"><span data-stu-id="e7c41-205">The first part of the banner section displays the title with a horizontal rule underneath it.</span></span> <span data-ttu-id="e7c41-206">Table-Tags werden verwendet, um die Position zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e7c41-206">Table tags are used to control its position.</span></span> <span data-ttu-id="e7c41-207">Das nowrap-Attribut wird für das</span><span class="sxs-lookup"><span data-stu-id="e7c41-207">The nowrap attribute is set for the</span></span> <TD> <span data-ttu-id="e7c41-208">-Tag, um die Wort Umbruch zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="e7c41-208">tag to prevent word wrapping.</span></span> <span data-ttu-id="e7c41-209">Das System ersetzt "% thisdirname%" durch den Namen des aktuellen Ordners.</span><span class="sxs-lookup"><span data-stu-id="e7c41-209">The system will replace %THISDIRNAME% with the name of the current folder.</span></span> <span data-ttu-id="e7c41-210">Ein **WebViewFolderIcon** -Objekt mit dem Bezeichner "Icon" aus Gründen der Einfachheit wird dann geladen, um das Symbol des Ordners zu extrahieren und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-210">A **WebViewFolderIcon** object, with an identifier of "Icon" for simplicity, is then loaded to extract and display the folder's icon.</span></span>

<span data-ttu-id="e7c41-211">Der Minibanner-Abschnitt ähnelt dem normalen Banner.</span><span class="sxs-lookup"><span data-stu-id="e7c41-211">The minibanner section is similar to the normal banner.</span></span> <span data-ttu-id="e7c41-212">Das Format des Titels wird etwas höher angeordnet und besitzt keine Regel.</span><span class="sxs-lookup"><span data-stu-id="e7c41-212">The format of the title is placed slightly higher and does not have a rule.</span></span> <span data-ttu-id="e7c41-213">Da kein Symbol vorhanden ist, wird das **WebViewFolderIcon** -Objekt nicht geladen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-213">Because there is no icon, the **WebViewFolderIcon** object is not loaded.</span></span>


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a><span data-ttu-id="e7c41-214">Info Bereich</span><span class="sxs-lookup"><span data-stu-id="e7c41-214">The Info Region</span></span>

<span data-ttu-id="e7c41-215">Der Teil der Webansicht unterhalb des Banners dient zum darstellen detaillierter Informationen über das ausgewählte Element.</span><span class="sxs-lookup"><span data-stu-id="e7c41-215">The portion of the Web view below the banner is used to present detailed information about the selected item.</span></span> <span data-ttu-id="e7c41-216">Wenn kein Element ausgewählt ist, wird eine Standardmeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-216">If no item is selected, a default message is shown.</span></span> <span data-ttu-id="e7c41-217">Da Generic. htt nur einen einzelnen TextBlock anzeigt, ist dieser Abschnitt recht einfach.</span><span class="sxs-lookup"><span data-stu-id="e7c41-217">Because Generic.htt only displays a single block of text, this section is quite simple.</span></span>


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



<span data-ttu-id="e7c41-218">Die meisten Informationen zur Erfassung der Informationen werden von einem [Ordner Informations Skript](#retrieving-and-displaying-folder-information) verarbeitet, das weiter unten in diesem Kapitel erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-218">Most of the work of collecting the information is handled by a [folder information script](#retrieving-and-displaying-folder-information) that is discussed later in the chapter.</span></span> <span data-ttu-id="e7c41-219">Sie zeigt die Informationen an, indem Sie den Text [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)zuweist.</span><span class="sxs-lookup"><span data-stu-id="e7c41-219">It displays the information by assigning the text to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

<span data-ttu-id="e7c41-220">Sie können die Anzeige von Informationen problemlos anpassen, indem Sie diese Elemente ändern oder weitere hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-220">You can easily customize the information display by modifying these elements or including additional ones.</span></span> <span data-ttu-id="e7c41-221">Alles, was Sie auf einer Webseite platzieren können, kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7c41-221">Anything that you can put on a webpage can be used.</span></span> <span data-ttu-id="e7c41-222">Wenn Sie z. b. einen Link zu Ihrer Website anzeigen möchten, können Sie ein Anker Element nach dem TextBlock in Generic. htt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-222">For example, to display a link to your website, you can add an anchor element after the text block in Generic.htt.</span></span>


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



### <a name="the-filelist-region"></a><span data-ttu-id="e7c41-223">Der FileList-Bereich</span><span class="sxs-lookup"><span data-stu-id="e7c41-223">The FileList Region</span></span>

<span data-ttu-id="e7c41-224">Zum Schluss lädt Generic. htt ein [**webviewfoldercontents**](webviewfoldercontents.md) -Objekt für den FileList-Bereich.</span><span class="sxs-lookup"><span data-stu-id="e7c41-224">Finally, Generic.htt loads a [**WebViewFolderContents**](webviewfoldercontents.md) object for the FileList region.</span></span> <span data-ttu-id="e7c41-225">Da der Bezeichner auf "FileList" festgelegt ist, wird er von nun an als FileList-Objekt bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e7c41-225">Because its identifier is set to "FileList", it will be referred to as the FileList object from now on.</span></span>


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



<span data-ttu-id="e7c41-226">Das FileList-Objekt wird in den meisten Webansichten gefunden und dient mehreren Zwecken.</span><span class="sxs-lookup"><span data-stu-id="e7c41-226">The FileList object is found in most Web views and serves several purposes.</span></span> <span data-ttu-id="e7c41-227">FileList zeigt die Liste der Elemente an, die im ausgewählten Ordner enthalten sind, mit den gleichen Optionen und dem gleichen aussehen wie die Datei Liste im klassischen Stil.</span><span class="sxs-lookup"><span data-stu-id="e7c41-227">FileList displays the list of items contained by the selected folder with the same options and appearance as the file list in Classic style.</span></span> <span data-ttu-id="e7c41-228">Wenn ein Element ausgewählt wird, benachrichtigt FileList die Webansicht, indem ein [SelectionChanged](#retrieving-and-displaying-folder-information) -Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-228">When an item is selected, FileList notifies the Web view by firing a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="e7c41-229">FileList macht auch Methoden und Eigenschaften verfügbar, die zum Abrufen von Informationen über einzelne Elemente und zum Steuern der Position und Größe des Anzeige Bereichs verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e7c41-229">FileList also exposes methods and properties that can be used to retrieve information about individual items and control the position and size of its display area.</span></span>

<span data-ttu-id="e7c41-230">Obwohl das FileList-Objekt sehr nützlich ist, gibt es nur standardmäßige Dateisystem Informationen zurück, z. b. Dateigröße oder Attribute.</span><span class="sxs-lookup"><span data-stu-id="e7c41-230">Although the FileList object is very useful, it only returns standard file system information, such as file size or attributes.</span></span> <span data-ttu-id="e7c41-231">Zum Abrufen anderer Arten von Informationen aus einem Shellordner müssen Sie zusätzliche Objekte laden und verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e7c41-231">To retrieve other kinds of information from a Shell folder, you will have to load and handle additional objects.</span></span> <span data-ttu-id="e7c41-232">Jedes Objekt, das von einer Webseite gehostet werden kann, kann mit einer Webansicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7c41-232">Any object that can be hosted by a webpage can be used with a Web view.</span></span>

### <a name="the-template-head"></a><span data-ttu-id="e7c41-233">Der Vorlagen Kopf</span><span class="sxs-lookup"><span data-stu-id="e7c41-233">The Template Head</span></span>

<span data-ttu-id="e7c41-234">Der Anfang der webansichts Vorlage enthält die Skripts und Funktionen, die den größten Teil der eigentlichen Arbeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-234">The head of the Web view template contains the scripts and functions that do most of the actual work.</span></span> <span data-ttu-id="e7c41-235">Es gibt zwei wichtige Aufgaben, die behandelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-235">There are two essential tasks that need to be handled.</span></span> <span data-ttu-id="e7c41-236">Eine ist das Layout der Anzeige der Webansicht, die an verschiedene Anzeige Bereiche angepasst werden muss.</span><span class="sxs-lookup"><span data-stu-id="e7c41-236">One is the layout of the Web view display, which needs to be adjusted to accommodate different display regions.</span></span> <span data-ttu-id="e7c41-237">Das andere Element Ruft Informationen aus dem Ordner ab und zeigt diese an, wenn ein Element ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-237">The other is retrieving and displaying information from the folder when an item is selected.</span></span> <span data-ttu-id="e7c41-238">Wie bei Stylesheets ist es besser, alle Skripts und Funktionen in die Vorlage einzubeziehen, anstatt Sie als separate Dateien zu referenzieren.</span><span class="sxs-lookup"><span data-stu-id="e7c41-238">As with style sheets, it is better to include all scripts and functions in the template instead of referencing them as separate files.</span></span>

### <a name="controlling-the-web-view-layout"></a><span data-ttu-id="e7c41-239">Steuern des Layouts der Webansicht</span><span class="sxs-lookup"><span data-stu-id="e7c41-239">Controlling the Web View Layout</span></span>

<span data-ttu-id="e7c41-240">Der Bereich, der für eine Webansicht verfügbar ist, hängt von der Größe des Fensters der Webansicht und davon ab, wie viel von der Windows-Explorer-Leiste benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-240">The area available for a Web view depends on the size of the Web view window and how much of it is taken up by the Windows Explorer bar.</span></span> <span data-ttu-id="e7c41-241">Dieser Bereich ändert sich, wenn die Größe des Fensters oder der Windows Explorer-Leiste geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-241">This area will change anytime the window or Windows Explorer bar is resized.</span></span> <span data-ttu-id="e7c41-242">Daher muss das Layout mit dem verfügbaren Bereich abgeglichen werden, wenn eine Webansicht geladen und entsprechend geändert wird, wenn die Größe geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-242">So the layout needs to be matched to the available area when a Web view is loaded and change appropriately when it is resized.</span></span> <span data-ttu-id="e7c41-243">Ein Großteil des Layouts wird im Stylesheet angegeben.</span><span class="sxs-lookup"><span data-stu-id="e7c41-243">Much of the layout is specified in the style sheet.</span></span> <span data-ttu-id="e7c41-244">Der Informationsbereich wird z. b. so definiert, dass er die am weitesten links stehenden 30 Prozent der Webansicht einnimmt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-244">The Info region, for example, is defined to occupy the leftmost 30 percent of the Web view.</span></span>


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



<span data-ttu-id="e7c41-245">Wenn die Größe einer Webansicht geändert wird, wird die Breite des Informationsbereichs geändert, um diesen Prozentsatz beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="e7c41-245">As a Web view is resized, the width of the Info region will change to maintain that percentage.</span></span> <span data-ttu-id="e7c41-246">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) verwaltet die Layoutprobleme, die nicht von einem Stylesheet behandelt werden können.</span><span class="sxs-lookup"><span data-stu-id="e7c41-246">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) manages the layout issues that can't be handled by a style sheet.</span></span>

### <a name="loading-and-initializing-the-web-view"></a><span data-ttu-id="e7c41-247">Laden und Initialisieren der Webansicht</span><span class="sxs-lookup"><span data-stu-id="e7c41-247">Loading and Initializing the Web View</span></span>

<span data-ttu-id="e7c41-248">Wenn eine Webansicht geladen wird, muss das Layout an den verfügbaren Anzeigebereich angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="e7c41-248">When a Web view is loaded, the layout needs to be adjusted to fit the available display area.</span></span> <span data-ttu-id="e7c41-249">Da noch kein Element ausgewählt wurde, zeigen Webansichten normalerweise einige Standardinformationen an, die für den gesamten Ordner gelten.</span><span class="sxs-lookup"><span data-stu-id="e7c41-249">Because no item has been selected yet, Web views normally display some default information that applies to the whole folder.</span></span> <span data-ttu-id="e7c41-250">Um die Initialisierung zu verarbeiten, wird der</span><span class="sxs-lookup"><span data-stu-id="e7c41-250">To handle initialization, the</span></span> <BODY> <span data-ttu-id="e7c41-251">Tag for Generic. htt erkennt das [OnLoad](/previous-versions//ms531409(v=vs.85)) -Ereignis und ruft die **Init** -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="e7c41-251">tag for Generic.htt detects the [onload](/previous-versions//ms531409(v=vs.85)) event and calls the **Init** function.</span></span>


```
<body scroll=no onload="Init">
                    
```



<span data-ttu-id="e7c41-252">**Init** ist eine einfache JScript-Funktion.</span><span class="sxs-lookup"><span data-stu-id="e7c41-252">**Init** is a simple JScript function.</span></span>


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



<span data-ttu-id="e7c41-253">**Init** bindet [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) an das [Window. OnResize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) -Ereignis, sodass es aufgerufen wird, wenn sich der Anzeigebereich der Webansicht ändert.</span><span class="sxs-lookup"><span data-stu-id="e7c41-253">**Init** binds [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) to the [window.onresize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) event so that it will be called whenever the Web view display area changes.</span></span> <span data-ttu-id="e7c41-254">Dann führt er FixSize aus, um das anfängliche Layout festzulegen, und weist dem Info Bereich einen L-Einfügungs \_ \_ Text zu.</span><span class="sxs-lookup"><span data-stu-id="e7c41-254">It then runs FixSize to set the initial layout and assigns L\_Intro\_Text to the Info region.</span></span> <span data-ttu-id="e7c41-255">L- \_ Intro- \_ Text ist ein Block von einführenden Text, der im Stylesheet-Abschnitt definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e7c41-255">L\_Intro\_Text is a block of introductory text that is defined in the style sheet section.</span></span>


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a><span data-ttu-id="e7c41-256">Anpassen des Layouts mithilfe der FixSize-Funktion</span><span class="sxs-lookup"><span data-stu-id="e7c41-256">Adjusting the Layout by using the FixSize function</span></span>

<span data-ttu-id="e7c41-257">Die [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) -Funktion wird verwendet, um verschiedene Aspekte des Layouts anzugeben, die nicht vom Stylesheet behandelt werden können.</span><span class="sxs-lookup"><span data-stu-id="e7c41-257">The [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) function is used to specify several aspects of the layout that can't be handled by the style sheet.</span></span>

<span data-ttu-id="e7c41-258">Abhängig von der Höhe der Webansicht können zwei mögliche Banner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7c41-258">There are two possible banners that can be used, depending on the height of the Web view.</span></span>


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



<span data-ttu-id="e7c41-259">Generic. htt verwendet eine Höhe von 200 Pixel als Trennlinie zwischen normalem und Minibanner.</span><span class="sxs-lookup"><span data-stu-id="e7c41-259">Generic.htt uses a height of 200 pixels as the dividing line between normal and minibanners.</span></span> <span data-ttu-id="e7c41-260">Der Stil des ausgewählten Banners wird auf "sichtbar" und das andere auf "ausgeblendet" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-260">It sets the style of the selected banner to visible and the other to hidden.</span></span> <span data-ttu-id="e7c41-261">Außerdem werden mehrere Layouteigenschaften für die Info-und die FileList-Bereiche festgelegt, damit Sie ordnungsgemäß mit dem ausgewählten Banner angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="e7c41-261">It also sets several layout properties for the Info and FileList regions so that they fit properly with the selected banner.</span></span>

<span data-ttu-id="e7c41-262">Wenn eine Webansicht zu schmal wird, verwendet [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) die gesamte Breite des Anzeige Bereichs für die FileList-Anzeige.</span><span class="sxs-lookup"><span data-stu-id="e7c41-262">If a Web view becomes too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) uses the full width of the display area for the FileList display.</span></span>


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



<span data-ttu-id="e7c41-263">Generic. htt verwendet 400 Pixel als Trennlinie zwischen schmalen und breiten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-263">Generic.htt uses 400 pixels as the dividing line between narrow and wide displays.</span></span> <span data-ttu-id="e7c41-264">Wenn die Webansicht zu schmal ist, blendet [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) den Informationsbereich aus und ändert die FileList [Pixel Left](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) -Eigenschaft so, dass Sie den gesamten Bereich unterhalb des Banners füllt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-264">If the Web view is too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) hides the Info region and modifies the FileList [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) property so that it fills the entire region below the banner.</span></span>

<span data-ttu-id="e7c41-265">Die letzten Zeilen von [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) passen verschiedene Layouteigenschaften basierend auf den Ergebnissen des vorangehenden Codes an.</span><span class="sxs-lookup"><span data-stu-id="e7c41-265">The final few lines of [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) adjust several layout properties based on the results of the preceding code.</span></span> <span data-ttu-id="e7c41-266">Die Breite des FileList-Bereichs wird so angepasst, dass er genau den Teil der Webansicht füllt, der nicht vom Informationsbereich belegt wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-266">The width of the FileList region is adjusted so that it exactly fills the portion of the Web view not occupied by the Info region.</span></span> <span data-ttu-id="e7c41-267">Die Höhe des Info Bereichs ist für das Banner und den unteren Rand der Webansicht angepasst.</span><span class="sxs-lookup"><span data-stu-id="e7c41-267">The height of the Info region is sized to fit between the banner and the bottom of the Web view.</span></span>


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a><span data-ttu-id="e7c41-268">Abrufen und Anzeigen von Ordner Informationen</span><span class="sxs-lookup"><span data-stu-id="e7c41-268">Retrieving and Displaying Folder Information</span></span>

<span data-ttu-id="e7c41-269">Wenn ein Benutzer ein Element auswählt, löst das FileList-Objekt ein [SelectionChanged](#retrieving-and-displaying-folder-information) -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="e7c41-269">When a user selects an item, the FileList object fires a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="e7c41-270">Dieses Ereignis wird von einem JScript-Skript behandelt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-270">This event is handled by a JScript script.</span></span> <span data-ttu-id="e7c41-271">Der Einfachheit halber geht das in Generic. htt gefundene Skript davon aus, dass jeweils nur ein Element ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e7c41-271">For simplicity, the script found in Generic.htt assumes that only one item can be selected at a time.</span></span>


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



<span data-ttu-id="e7c41-272">Das Skript verwendet zwei FileList-Eigenschaften, [**FileList. FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)und [**FileList. Folder**](/windows/desktop/shell/shellfolderview-folder) zum Abrufen von Informationen über das Element.</span><span class="sxs-lookup"><span data-stu-id="e7c41-272">The script uses two FileList properties, [**FileList.FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)and [**FileList.Folder**](/windows/desktop/shell/shellfolderview-folder) to obtain information about the item.</span></span> <span data-ttu-id="e7c41-273">**FileList. FocusedItem** identifiziert das ausgewählte Element mit dem Namen des Elements, das von **FileList.FocusedItem.Name** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-273">**FileList.FocusedItem** identifies the selected item, with the item's name given by **FileList.FocusedItem.Name**.</span></span> <span data-ttu-id="e7c41-274">" **FileList. Folder** " ist tatsächlich ein Zeiger auf ein [**Ordner**](../shell/folder.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-274">**FileList.Folder** is actually a pointer to a [**Folder**](../shell/folder.md) object.</span></span> <span data-ttu-id="e7c41-275">Die [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) -Methode des Ordner Objekts wird verwendet, um die restlichen Informationen über das Element abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-275">The Folder object's [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) method is used to retrieve the remaining information about the item.</span></span>

<span data-ttu-id="e7c41-276">Alle Informationen werden in einer einzelnen Text Zeichenfolge verkettet, getrennt durch</span><span class="sxs-lookup"><span data-stu-id="e7c41-276">All the information is concatenated into a single text string, separated by</span></span> <BR> <span data-ttu-id="e7c41-277">Tags zur besseren Lesbarkeit.</span><span class="sxs-lookup"><span data-stu-id="e7c41-277">tags for readability.</span></span> <span data-ttu-id="e7c41-278">Der Text wird dann angezeigt, indem er [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e7c41-278">The text is then displayed by assigning it to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="e7c41-279">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e7c41-279">Summary</span></span>

<span data-ttu-id="e7c41-280">In diesem Kapitel werden einige der Techniken beschrieben, die Sie verwenden können, um die Art und Weise anzupassen, wie Windows-Explorer Informationen zu shellordnern anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e7c41-280">This chapter outlines some of the techniques you can use to customize the way the Windows Explorer displays information about Shell folders.</span></span> <span data-ttu-id="e7c41-281">Wenn Sie eine Desktop.ini Datei erstellen, können Sie einige einfache Anpassungen vornehmen, z. b. ein benutzerdefiniertes Symbol anstelle des Standardordner Symbols anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e7c41-281">Creating a Desktop.ini file allows you to do some simple customization, such as displaying a custom icon in place of the standard folder icon.</span></span> <span data-ttu-id="e7c41-282">Wenn ein Ordner in einer Webansicht angezeigt wird, werden das Layout und die Anzeige von einer HTML-basierten Vorlage gesteuert, die bestimmt, welche Informationen angezeigt werden und wie.</span><span class="sxs-lookup"><span data-stu-id="e7c41-282">When a folder appears in a Web view, its layout and display are controlled by an HTML-based template that determines what information is displayed and how.</span></span> <span data-ttu-id="e7c41-283">Sie können ein hohes Maß an Kontrolle über die Webansicht eines Ordners mit standardmäßigen HTML-, DHTML-und Skript Techniken zum Erstellen einer benutzerdefinierten Vorlage ausüben.</span><span class="sxs-lookup"><span data-stu-id="e7c41-283">You can exercise a high degree of control over a folder's Web view by using standard HTML, DHTML, and scripting techniques to create a custom template.</span></span>

 

 