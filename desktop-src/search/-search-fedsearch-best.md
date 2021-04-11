---
description: In diesem Thema werden die bewährten Methoden aufgeführt, mit denen Sie einen webbasierten Datenspeicher erstellen können, der mithilfe der Windows-Verbund Suche durchsucht werden kann, und Ihre Remote Datenquellen mit Windows-Explorer integrieren, ohne dass Windows-Client seitiger Code geschrieben oder bereitgestellt werden muss.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Bewährte Methoden bei der Windows-Verbund Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed94f42b4470694209e37f5ede8a05d87a290d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128576"
---
# <a name="following-best-practices-in-windows-federated-search"></a><span data-ttu-id="c3a06-103">Bewährte Methoden bei der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="c3a06-103">Following Best Practices in Windows Federated Search</span></span>

<span data-ttu-id="c3a06-104">In diesem Thema werden die bewährten Methoden aufgeführt, mit denen Sie einen webbasierten Datenspeicher erstellen können, der mithilfe der Windows-Verbund Suche durchsucht werden kann, und Ihre Remote Datenquellen mit Windows-Explorer integrieren, ohne dass Windows-Client seitiger Code geschrieben oder bereitgestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c3a06-104">This topic lists the best practices through which you can build a web-based data store that can be searched using Windows federated search, and integrates your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="c3a06-105">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="c3a06-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="c3a06-106">Bewährte Methoden für die Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="c3a06-106">Best Practices for Windows Federated Search</span></span>](#best-practices-for-windows-federated-search)
-   [<span data-ttu-id="c3a06-107">Bewährte Methoden zum Erstellen von RSS-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3a06-107">Best Practices for Creating RSS Output</span></span>](#best-practices-for-creating-rss-output)
-   [<span data-ttu-id="c3a06-108">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c3a06-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="c3a06-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c3a06-109">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a><span data-ttu-id="c3a06-110">Bewährte Methoden für die Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="c3a06-110">Best Practices for Windows Federated Search</span></span>

<span data-ttu-id="c3a06-111">Die bewährten Methoden für die Arbeit mit [OpenSearch](https://github.com/dewitt/opensearch) in Windows 7 lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3a06-111">Best practices for working with [OpenSearch](https://github.com/dewitt/opensearch) in Windows 7 are as follows:</span></span>

-   <span data-ttu-id="c3a06-112">Unterstützen Sie die Parameter " *{startIndex}* " und " *{count}* ", und geben Sie die Anzahl der angeforderten Elemente immer zurück, es sei denn, Sie geben die letzten Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="c3a06-112">Support the *{startIndex}* and *{count}* parameters, and be sure to always return the number of items requested unless you are returning the last of the results.</span></span>
-   <span data-ttu-id="c3a06-113">Wenn Sie die Dateinamenerweiterung kennen, ordnen Sie Sie der Windows Shell-Eigenschaft [System. FileExtension](../properties/props-system-fileextension.md) zu.</span><span class="sxs-lookup"><span data-stu-id="c3a06-113">If you know the file name extension, map it to the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property.</span></span> <span data-ttu-id="c3a06-114">Die Verwendung von Dateinamen Erweiterungen ist eine bessere Möglichkeit, einen Dateityp als MIME-Typ zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c3a06-114">Using file name extensions is a better way to identify a file type than MIME type.</span></span>
-   <span data-ttu-id="c3a06-115">Stellen Sie sicher, dass der MIME-Typ oder die Dateinamenerweiterung, die Sie in der RSS angeben, mit dem Dateinamen und dem MIME-Typ übereinstimmt, der vom Webserver, der das Element hostet, wenn der Element Inhalt angefordert wird</span><span class="sxs-lookup"><span data-stu-id="c3a06-115">Ensure that the MIME type or file name extension that you specify in the RSS matches the file name and MIME type returned in the HTTP header by the web server that hosts the item when the item content is requested.</span></span>
-   <span data-ttu-id="c3a06-116">Wenn Sie Dateielemente zurückgeben, sollten Sie nach Möglichkeit eine Dateigröße zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c3a06-116">If you are returning file items, return a file size whenever possible.</span></span> <span data-ttu-id="c3a06-117">Dadurch wird sichergestellt, dass das Dialogfeld Download Fortschritt korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="c3a06-117">This ensures that the download progress dialog box is accurate.</span></span>
-   <span data-ttu-id="c3a06-118">Stellen Sie sicher, dass Anforderungen für Elemente hinter dem Ende des Resultsets keine Ergebnisse zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c3a06-118">Verify that requests for items beyond the end of the results set return no results.</span></span>
    > [!Note]  
    > <span data-ttu-id="c3a06-119">Die Ergebnisse werden nicht wiederholt.</span><span class="sxs-lookup"><span data-stu-id="c3a06-119">Do not repeat results.</span></span>

     

-   <span data-ttu-id="c3a06-120">Fügen Sie keine HTML-Tags an, die nicht zu gehören.</span><span class="sxs-lookup"><span data-stu-id="c3a06-120">Do not put HTML tags where they don't belong.</span></span> <span data-ttu-id="c3a06-121">Gemäß der RSS-Spezifikation sind Sie im Beschreibungsfeld gültig, aber nicht im Feld "Title".</span><span class="sxs-lookup"><span data-stu-id="c3a06-121">Per the RSS specification, they are valid in the description field, but not in the title field.</span></span>
-   <span data-ttu-id="c3a06-122">Erstellen Sie keine Gehäuse für Webseiten Elemente.</span><span class="sxs-lookup"><span data-stu-id="c3a06-122">Do not create enclosures for webpage items.</span></span> <span data-ttu-id="c3a06-123">Wenn Sie z. b. ein Gehäuse erstellen und die Dateinamenerweiterung ". aspx" zuordnen, wird die Datei vom Windows-Explorer in den Internet Cache heruntergeladen und von dort aus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3a06-123">For example, if you create an enclosure and map a file name extension of .aspx, the file is downloaded by Windows Explorer to the Internet cache and executed from there.</span></span> <span data-ttu-id="c3a06-124">Webbrowser verarbeiten den ASPX-Dateityp nicht.</span><span class="sxs-lookup"><span data-stu-id="c3a06-124">Web browsers do not handle the .aspx file type.</span></span> <span data-ttu-id="c3a06-125">Der Benutzer erhält ein Dialogfeld " **Öffnen mit** ", oder die Datei wird möglicherweise von einer Anwendung wie Microsoft Visual Studio geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c3a06-125">The user would get an **Open with** dialog box, or the file might be opened by an application like Microsoft Visual Studio.</span></span> <span data-ttu-id="c3a06-126">Vermeiden Sie dies, indem Sie ein Link Element nur für Webseiten zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c3a06-126">Avoid this by returning a link element only for webpages.</span></span>
-   <span data-ttu-id="c3a06-127">Geben Sie mithilfe einer URL-Vorlage mit eine webrollenurl in der OSDX-Datei an `format="text\html"` .</span><span class="sxs-lookup"><span data-stu-id="c3a06-127">Provide a web roll-over URL in the .osdx file using a URL template with `format="text\html"`.</span></span>
-   <span data-ttu-id="c3a06-128">Geben Sie eine URL für den übergeordneten Ordner, den Container oder die Webseite an, indem Sie der Eigenschaft [System. itemfolderpathdisplay](../properties/props-system-itempathdisplay.md) der Windows-Shell den Wert einer benutzerdefinierten Element-URL zuordnet.</span><span class="sxs-lookup"><span data-stu-id="c3a06-128">Provide a URL to the parent folder, container, or webpage by mapping a custom element URL value to the [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows Shell property.</span></span>

## <a name="best-practices-for-creating-rss-output"></a><span data-ttu-id="c3a06-129">Bewährte Methoden zum Erstellen von RSS-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3a06-129">Best Practices for Creating RSS Output</span></span>

<span data-ttu-id="c3a06-130">Es folgen die bewährten Methoden für das Erstellen von RSS-Ausgaben:</span><span class="sxs-lookup"><span data-stu-id="c3a06-130">Best practices for creating RSS output are as follows:</span></span>

-   <span data-ttu-id="c3a06-131">Jedes Element muss eine URL oder einen Wert zurückgeben `link` `enclosure` (oder äquivalent, z. b. `media:content` ).</span><span class="sxs-lookup"><span data-stu-id="c3a06-131">Each item MUST return a URL `link` or `enclosure` value (or equivalent, such as `media:content`)</span></span>
-   <span data-ttu-id="c3a06-132">Fügen Sie keine HTML-Formatierungs Tags in das **Title** -Attribut ein, oder diese Tags werden im Titel angezeigt und im Windows-Explorer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c3a06-132">Do not include any HTML formatting tags in the **title** attribute, or those tags will appear in the title and be displayed in Windows Explorer.</span></span>
-   <span data-ttu-id="c3a06-133">Für das **Description** -Element:</span><span class="sxs-lookup"><span data-stu-id="c3a06-133">For the **description** element:</span></span>
    -   <span data-ttu-id="c3a06-134">Zeigen Sie genügend Informationen an, damit der Benutzer weiß, warum dieses Ergebnis relevant sein könnte.</span><span class="sxs-lookup"><span data-stu-id="c3a06-134">Show enough information so that the user knows why this result might be relevant.</span></span>
    -   <span data-ttu-id="c3a06-135">HTML-Formatierung nicht einschließen.</span><span class="sxs-lookup"><span data-stu-id="c3a06-135">Do not include HTML formatting.</span></span> <span data-ttu-id="c3a06-136">Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter entfernt die Formatierung, was möglicherweise zu weniger als wünschenswerten für Ihre Beschreibung führt.</span><span class="sxs-lookup"><span data-stu-id="c3a06-136">The [OpenSearch](https://github.com/dewitt/opensearch) provider removes the formatting, which might result in less than desirable results for your description.</span></span>
    -   <span data-ttu-id="c3a06-137">Fügen Sie keine Metadaten ein, die bereits in anderen Elementen enthalten sind, wie z. b. den Dateinamen des Gehäuses, die Größe, das Änderungsdatum usw., da Windows Explorer die Metadaten bereits anzeigt.</span><span class="sxs-lookup"><span data-stu-id="c3a06-137">Do not include metadata that is already provided in other elements, such as enclosure file name, size, modified date, and so forth, because Windows Explorer already displays the metadata.</span></span> <span data-ttu-id="c3a06-138">Die Anzeige im **Description** -Element wäre redundant.</span><span class="sxs-lookup"><span data-stu-id="c3a06-138">Displaying it in the **description** element would be redundant.</span></span>
-   <span data-ttu-id="c3a06-139">Für Gehäuse-oder Inhalts-URLs:</span><span class="sxs-lookup"><span data-stu-id="c3a06-139">For enclosure or content URLs:</span></span>
    -   <span data-ttu-id="c3a06-140">Geben Sie das Type-Attribut als gültigen MIME-Typ an.</span><span class="sxs-lookup"><span data-stu-id="c3a06-140">Specify the type attribute as a valid MIME type.</span></span>
    -   <span data-ttu-id="c3a06-141">Geben Sie die Dateigröße in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="c3a06-141">Specify the file size in bytes.</span></span>
-   <span data-ttu-id="c3a06-142">Wenn Sie die RSS-Ausgabe in .NET mithilfe von implementieren `DateTime` , testen Sie Ihren Feed in Microsoft Internet Explorer, um zu überprüfen, ob er gültig ist, bevor Sie ihn in Windows Explorer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c3a06-142">If you are implementing RSS output in .NET using `DateTime`, test your feed in Microsoft Internet Explorer to see if it is valid before deploying it to Windows Explorer.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3a06-143">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c3a06-143">Additional Resources</span></span>

<span data-ttu-id="c3a06-144">Weitere Informationen zum Implementieren eines Such Verbunds in Remote Datenspeicher mithilfe von OpenSearch-Technologien in Windows 7 und höher finden Sie unter "zusätzliche Ressourcen" bei der [Verbund Suche in Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c3a06-144">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3a06-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c3a06-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3a06-146">Verbundsuche in Windows 10</span><span class="sxs-lookup"><span data-stu-id="c3a06-146">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="c3a06-147">Ersten Einstieg in die Verbund Suche in Windows</span><span class="sxs-lookup"><span data-stu-id="c3a06-147">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="c3a06-148">Verbinden des Webdiensts in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="c3a06-148">Connecting Your Web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="c3a06-149">Aktivieren des Datenspeicher in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="c3a06-149">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="c3a06-150">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="c3a06-150">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="c3a06-151">Bereitstellen von Suchconnectors in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="c3a06-151">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> <dt>

[<span data-ttu-id="c3a06-152">Erweitern des Indexes</span><span class="sxs-lookup"><span data-stu-id="c3a06-152">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
