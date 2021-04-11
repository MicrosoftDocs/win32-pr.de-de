---
description: Microsoft stellt mehrere Standardfilter mit Windows Search bereit. Clients bezeichnen diese Filter Handler (die Implementierungen der IFilter-Schnittstelle sind), um Text und Eigenschaften aus einem Dokument zu extrahieren.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Filtern von Handlern, die mit Windows ausgeliefert werden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd5603ab913117e2c968a7508b2fa061dfb4034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128568"
---
# <a name="filter-handlers-that-ship-with-windows"></a><span data-ttu-id="dd15c-104">Filtern von Handlern, die mit Windows ausgeliefert werden</span><span class="sxs-lookup"><span data-stu-id="dd15c-104">Filter Handlers that Ship with Windows</span></span>

<span data-ttu-id="dd15c-105">Microsoft stellt mehrere Standardfilter mit Windows Search bereit.</span><span class="sxs-lookup"><span data-stu-id="dd15c-105">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="dd15c-106">Clients bezeichnen diese Filter Handler (die Implementierungen der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle sind), um Text und Eigenschaften aus einem Dokument zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="dd15c-106">Clients call these filter handlers (which are implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) to extract text and properties from a document.</span></span>

<span data-ttu-id="dd15c-107">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="dd15c-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="dd15c-108">Implementierungs Hinweise zur Windows-Suche</span><span class="sxs-lookup"><span data-stu-id="dd15c-108">Windows Search Implementation Notes</span></span>](#windows-search-implementation-notes)
  - [<span data-ttu-id="dd15c-109">Windows 7-und 10-Implementierung</span><span class="sxs-lookup"><span data-stu-id="dd15c-109">Windows 7 and 10 Implementation</span></span>](#windows-7-and-10-implementation)
  - [<span data-ttu-id="dd15c-110">Windows Vista-Implementierung</span><span class="sxs-lookup"><span data-stu-id="dd15c-110">Windows Vista Implementation</span></span>](#windows-vista-implementation)
  - [<span data-ttu-id="dd15c-111">Legacy Implementierung</span><span class="sxs-lookup"><span data-stu-id="dd15c-111">Legacy Implementation</span></span>](#legacy-implementation)
- [<span data-ttu-id="dd15c-112">Windows-Suchfilter</span><span class="sxs-lookup"><span data-stu-id="dd15c-112">Windows Search Filters</span></span>](#filter-handlers-that-ship-with-windows)
  - [<span data-ttu-id="dd15c-113">MIME-Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-113">MIME Filter Handler</span></span>](#mime-filter-handler)
  - [<span data-ttu-id="dd15c-114">HTML-Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-114">HTML Filter Handler</span></span>](#html-filter-handler)
  - [<span data-ttu-id="dd15c-115">Dokument Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-115">Document Filter Handler</span></span>](#document-filter-handler)
  - [<span data-ttu-id="dd15c-116">Nur-Text-Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-116">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)
  - [<span data-ttu-id="dd15c-117">Binärer oder NULL-Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-117">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler)
- [<span data-ttu-id="dd15c-118">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dd15c-118">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="dd15c-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd15c-119">Related topics</span></span>](#related-topics)

## <a name="windows-search-implementation-notes"></a><span data-ttu-id="dd15c-120">Implementierungs Hinweise zur Windows-Suche</span><span class="sxs-lookup"><span data-stu-id="dd15c-120">Windows Search Implementation Notes</span></span>

<span data-ttu-id="dd15c-121">In Windows 7 und höher werden in verwaltetem Code geschriebene Filter explizit blockiert.</span><span class="sxs-lookup"><span data-stu-id="dd15c-121">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="dd15c-122">Filter müssen in nativem Code geschrieben werden, da mögliche Probleme bei der CLR-Versionsverwaltung mit dem Prozess auftreten, in dem mehrere Add-Ins ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dd15c-122">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="windows-7-and-10-implementation"></a><span data-ttu-id="dd15c-123">Windows 7-und 10-Implementierung</span><span class="sxs-lookup"><span data-stu-id="dd15c-123">Windows 7 and 10 Implementation</span></span>

<span data-ttu-id="dd15c-124">In Windows 7 und höher gibt es ein neues Verhalten, das beim Registrieren eines Filter Handlers, eines Eigenschaften Handlers oder einer neuen Erweiterung auftritt.</span><span class="sxs-lookup"><span data-stu-id="dd15c-124">In Windows 7 and later, there is new behavior that occurs when registering a filter handler, property handler, or new extension.</span></span> <span data-ttu-id="dd15c-125">Wenn ein neuer Eigenschaften Handler und/oder Filter Handler installiert wird, werden Dateien mit den entsprechenden Erweiterungen automatisch neu indiziert.</span><span class="sxs-lookup"><span data-stu-id="dd15c-125">When a new property handler and/or filter handler is installed, files with the corresponding extensions are automatically re-indexed.</span></span>

<span data-ttu-id="dd15c-126">In Windows 7 und höher wird empfohlen, dass Sie einen Filter Handler in Verbindung mit den entsprechenden Eigenschaften Handlern installieren und den Filter Handler vor dem Eigenschaften Handler registrieren.</span><span class="sxs-lookup"><span data-stu-id="dd15c-126">In Windows 7 and later, we recommend that you install a filter handler in conjunction with its corresponding property handlers, and that you register the filter handler before the property handler.</span></span> <span data-ttu-id="dd15c-127">Die Registrierung des Eigenschaften Handler initiiert die sofortige Neuindizierung von zuvor indizierten Dateien, ohne dass zuerst ein Neustart erforderlich ist, und nutzt alle zuvor registrierten Filter Handler für die Inhalts Indizierung.</span><span class="sxs-lookup"><span data-stu-id="dd15c-127">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a restart, and takes advantage of any previously registered filter handlers for the purpose of content indexing.</span></span>

<span data-ttu-id="dd15c-128">Wenn nur ein Filter Handler ohne einen entsprechenden Eigenschaften Handler installiert wird, erfolgt die automatische Neuindizierung entweder nach einem Neustart des Indizierungs dienstanzdienstanbieter oder einem Neustart des Systems.</span><span class="sxs-lookup"><span data-stu-id="dd15c-128">If only a filter handler is installed without a corresponding property handler, then automatic re-indexing occurs either after a restart of the indexing service, or a restart of the system.</span></span>

<span data-ttu-id="dd15c-129">Informationen zu eigenschaftenbeschreibungsflags, die speziell für Windows 7 gelten, finden Sie in den folgenden Referenz Themen: [getpropertystoreflags](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PropDesc \_ ColumnIndex \_ Type](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) und [PropDesc \_ SearchInfo \_ Flags](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).</span><span class="sxs-lookup"><span data-stu-id="dd15c-129">For property description flags specific to Windows 7, see the following reference topics: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC\_COLUMNINDEX\_TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) and [PROPDESC\_SEARCHINFO\_FLAGS](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).</span></span>

### <a name="windows-vista-implementation"></a><span data-ttu-id="dd15c-130">Windows Vista-Implementierung</span><span class="sxs-lookup"><span data-stu-id="dd15c-130">Windows Vista Implementation</span></span>

<span data-ttu-id="dd15c-131">In Windows Vista und früheren Versionen initiiert die Installation eines [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -oder Eigenschaften Handlers keine Neuindizierung vorhandener Elemente, es sei denn, ein unabhängiger Softwarehersteller (ISV) ruft explizit eine Neuerstellung oder Neuindizierung der übereinstimmenden URLs auf.</span><span class="sxs-lookup"><span data-stu-id="dd15c-131">In Windows Vista and earlier, installing an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or property handler does not initiate a re-indexing of existing items unless an independent software vendor (ISV) explicitly calls a rebuild or re-indexing of matching URLs.</span></span>

<span data-ttu-id="dd15c-132">Es gibt zwei wesentliche Unterschiede zwischen Legacy Anwendungen, wie z. b. dem Indizierungs Dienst und neueren Anwendungen wie Windows Search, die Sie beim Implementieren von Filtern beachten sollten:</span><span class="sxs-lookup"><span data-stu-id="dd15c-132">There are two major differences between legacy applications like Indexing Service and newer applications like Windows Search that you should be aware of when implementing filters:</span></span>

- <span data-ttu-id="dd15c-133">Verwendung der [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dd15c-133">Use of the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface.</span></span>
- <span data-ttu-id="dd15c-134">Verwendung von Eigenschaften Handlern.</span><span class="sxs-lookup"><span data-stu-id="dd15c-134">Use of property handlers.</span></span>

<span data-ttu-id="dd15c-135">Zuerst erfordern Windows Vista und Windows Search 3,0 und höher die Verwendung von [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) aus den folgenden Gründen:</span><span class="sxs-lookup"><span data-stu-id="dd15c-135">First, Windows Vista and Windows Search 3.0 and later require you use [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) for the following reasons:</span></span>

- <span data-ttu-id="dd15c-136">Um Leistung und zukünftige Kompatibilität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="dd15c-136">To ensure performance and future compatibility.</span></span>
- <span data-ttu-id="dd15c-137">, Um die Sicherheit zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="dd15c-137">To help increase security.</span></span> <span data-ttu-id="dd15c-138">Mit [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) implementierte Filter sind sicherer, da der Kontext, in dem der Filter ausgeführt wird, nicht die Berechtigung zum Öffnen von Dateien auf dem Datenträger oder über das Netzwerk benötigt.</span><span class="sxs-lookup"><span data-stu-id="dd15c-138">Filters implemented with [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) are more secure because the context in which the filter runs does not need the rights to open files on the disk or over the network.</span></span>

<span data-ttu-id="dd15c-139">Obwohl bei Windows Search nur [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)verwendet wird, können Sie die [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile) und/oder [IPersistStorage-Schnittstellen](/windows/win32/api/objidl/nn-objidl-ipersiststorage) Implementierungen in Ihren Filtern für die Abwärtskompatibilität einschließen.</span><span class="sxs-lookup"><span data-stu-id="dd15c-139">While Windows Search uses only [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), you can also include [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and/or [IPersistStorage Interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) implementations in your filters for backward compatibility.</span></span>

<span data-ttu-id="dd15c-140">Der zweite Hauptunterschied besteht darin, dass Windows Vista und Windows Search 3,0 und höher ein neues Eigenschaften [System](../properties/building-property-handlers.md) haben, das Eigenschafts Handler verwendet, um Eigenschaften von Elementen aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="dd15c-140">The second major difference is that Windows Vista and Windows Search 3.0 and later have a new [Property System](../properties/building-property-handlers.md) that uses property handlers to enumerate properties of items.</span></span>

<span data-ttu-id="dd15c-141">Es gibt jedoch Zeiten, in denen Sie einen Filter implementieren müssen, der sowohl den Inhalt als auch die Eigenschaften behandelt, um Folgendes zu tun:</span><span class="sxs-lookup"><span data-stu-id="dd15c-141">However, there are times when you need to implement a filter that handles both content and properties in order to:</span></span>

- <span data-ttu-id="dd15c-142">Unterstützung von Legacy-MSSearch-Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="dd15c-142">Support legacy MSSearch implementations.</span></span>
- <span data-ttu-id="dd15c-143">Durchsuchen von Links.</span><span class="sxs-lookup"><span data-stu-id="dd15c-143">Traverse links.</span></span>
- <span data-ttu-id="dd15c-144">Sprachinformationen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="dd15c-144">Preserve language information.</span></span>
- <span data-ttu-id="dd15c-145">Filtern Sie eingebettete Elemente rekursiv.</span><span class="sxs-lookup"><span data-stu-id="dd15c-145">Recursively filter embedded items.</span></span>

<span data-ttu-id="dd15c-146">In diesen Fällen benötigen Sie eine vollständige Filter Implementierung, einschließlich der [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) -Methode, um auf Eigenschaftswerte zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="dd15c-146">In these situations, you need a full filter implementation, including the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method to access property values.</span></span>

### <a name="legacy-implementation"></a><span data-ttu-id="dd15c-147">Legacy Implementierung</span><span class="sxs-lookup"><span data-stu-id="dd15c-147">Legacy Implementation</span></span>

<span data-ttu-id="dd15c-148">Wie bereits erwähnt, enthalten Windows Vista und Windows Search ein neues Eigenschaften System, das die Eigenschaften eines Elements kapselt, das vom Inhalt eines Elements getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="dd15c-148">As noted earlier, Windows Vista and Windows Search include a new property system that encapsulates an item's properties that is separate from an item's content.</span></span> <span data-ttu-id="dd15c-149">Dieses Eigenschaften System ist in früheren Versionen von Microsoft Windows Desktop Search (WDS) 2. x nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="dd15c-149">This property system does not exist in earlier versions of Microsoft Windows Desktop Search (WDS) 2.x.</span></span> <span data-ttu-id="dd15c-150">Wenn der Filter andere Anwendungen unterstützen muss, wie oben beschrieben, muss er möglicherweise sowohl den Inhalt als auch die Eigenschaften verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="dd15c-150">If your filter must support other applications as described above, it may need to handle both content and properties.</span></span>

<span data-ttu-id="dd15c-151">Weitere Informationen zum Entwickeln eines kompatiblen Filters finden Sie in den folgenden Themen: [IFilter (für ältere Anwendungen)](/windows/win32/api/filter/nn-filter-ifilter)und [entwickeln von Filter-Add-Ins (für ältere Anwendungen)](../lwef/-search-2x-wds-ifilteraddins.md).</span><span class="sxs-lookup"><span data-stu-id="dd15c-151">For more information on developing a compatible filter, see the following topics, [IFilter (for legacy applications)](/windows/win32/api/filter/nn-filter-ifilter), and [Developing Filter Add-ins (for legacy applications)](../lwef/-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="windows-search-filters"></a><span data-ttu-id="dd15c-152">Windows-Suchfilter</span><span class="sxs-lookup"><span data-stu-id="dd15c-152">Windows Search Filters</span></span>

<span data-ttu-id="dd15c-153">Microsoft stellt mehrere Standardfilter mit Windows Search bereit.</span><span class="sxs-lookup"><span data-stu-id="dd15c-153">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="dd15c-154">Der Inhalt der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  -dll wird in der folgenden Tabelle zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="dd15c-154">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  DLL contents are summarized in the following table.</span></span> <span data-ttu-id="dd15c-155">Wenn Sie auf den Namen eines Filter Handlers klicken, gelangen Sie zur Beschreibung der **IFilter** -Implementierung.</span><span class="sxs-lookup"><span data-stu-id="dd15c-155">Clicking the name of a filter handler takes you to the description for that **IFilter** implementation.</span></span>

| <span data-ttu-id="dd15c-156">Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-156">Filter handler</span></span>                                                  | <span data-ttu-id="dd15c-157">Gefilterte Dateien</span><span class="sxs-lookup"><span data-stu-id="dd15c-157">Files filtered</span></span>                              | <span data-ttu-id="dd15c-158">IFilter-DLL</span><span class="sxs-lookup"><span data-stu-id="dd15c-158">IFilter DLL</span></span>  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [<span data-ttu-id="dd15c-159">MIME-Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-159">MIME Filter Handler</span></span>](#mime-filter-handler)                     | <span data-ttu-id="dd15c-160">Mehrzweck-Internet Mail Erweiterung (MIME)</span><span class="sxs-lookup"><span data-stu-id="dd15c-160">Multipurpose Internet Mail Extension (MIME)</span></span> | <span data-ttu-id="dd15c-161">mimefilt.dll</span><span class="sxs-lookup"><span data-stu-id="dd15c-161">mimefilt.dll</span></span> |
| [<span data-ttu-id="dd15c-162">HTML-Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-162">HTML Filter Handler</span></span>](#html-filter-handler)                     | <span data-ttu-id="dd15c-163">HTML 3,0 oder früher</span><span class="sxs-lookup"><span data-stu-id="dd15c-163">HTML 3.0 or earlier</span></span>                         | <span data-ttu-id="dd15c-164">nlhtml.dll</span><span class="sxs-lookup"><span data-stu-id="dd15c-164">nlhtml.dll</span></span>   |
| [<span data-ttu-id="dd15c-165">Dokument Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-165">Document Filter Handler</span></span>](#document-filter-handler)             | <span data-ttu-id="dd15c-166">Microsoft Word, Excel, PowerPoint</span><span class="sxs-lookup"><span data-stu-id="dd15c-166">Microsoft Word, Excel, PowerPoint</span></span>           | <span data-ttu-id="dd15c-167">offfilt.dll</span><span class="sxs-lookup"><span data-stu-id="dd15c-167">offfilt.dll</span></span>  |
| [<span data-ttu-id="dd15c-168">Nur-Text-Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-168">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)         | <span data-ttu-id="dd15c-169">Nur-Text-Dateien-Standard-IFilter</span><span class="sxs-lookup"><span data-stu-id="dd15c-169">Plain text files - Default IFilter</span></span>          | <span data-ttu-id="dd15c-170">query.dll</span><span class="sxs-lookup"><span data-stu-id="dd15c-170">query.dll</span></span>    |
| [<span data-ttu-id="dd15c-171">Binärer oder NULL-Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-171">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler) | <span data-ttu-id="dd15c-172">Binäre Dateien-NULL-IFilter</span><span class="sxs-lookup"><span data-stu-id="dd15c-172">Binary files - Null IFilter</span></span>                 | <span data-ttu-id="dd15c-173">query.dll</span><span class="sxs-lookup"><span data-stu-id="dd15c-173">query.dll</span></span>    |

### <a name="mime-filter-handler"></a><span data-ttu-id="dd15c-174">MIME-Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-174">MIME Filter Handler</span></span>

<span data-ttu-id="dd15c-175">Der MIME-Filter Handler (in mimefilt.dll) extrahiert Text-und Eigenschafts Informationen aus Dateien mit den Erweiterungen ". eml", ". MHT" und ". MHTML".</span><span class="sxs-lookup"><span data-stu-id="dd15c-175">The MIME filter handler (in mimefilt.dll) extracts text and property information from files with the extensions .eml, .mht and .mhtml.</span></span>

### <a name="html-filter-handler"></a><span data-ttu-id="dd15c-176">HTML-Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-176">HTML Filter Handler</span></span>

<span data-ttu-id="dd15c-177">Der HTML-Filter Handler (in nlhtml.dll) extrahiert Text-und Eigenschafts Informationen aus der Klasse "HtmlFiles", sodass er von Windows Search indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="dd15c-177">The HTML filter handler (in nlhtml.dll) extracts text and property information from the class "htmlfiles" so that it can be indexed by Windows Search.</span></span> <span data-ttu-id="dd15c-178">Eine Beschreibung der Zuordnung zwischen [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) und Dateityp finden Sie unter "Suchen der IFilter-DLL für eine Datei" in [Registrieren von Filter Handlern](-search-ifilter-registering-filters.md).</span><span class="sxs-lookup"><span data-stu-id="dd15c-178">For a description of the association between [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and file type, see "Finding the IFilter DLL for a File" in [Registering Filter Handlers](-search-ifilter-registering-filters.md).</span></span>

<span data-ttu-id="dd15c-179">Sie können das `META` tagfeature von HTML-Dokumenten verwenden, um besondere Verarbeitungsanforderungen an den HTML- [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="dd15c-179">You can use the `META` tag feature of HTML documents to convey special handling requests to the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter).</span></span> <span data-ttu-id="dd15c-180">`META` Tags treten am Anfang einer HTML-Datei innerhalb der `HEAD ... /HEAD` Tags auf, wie im folgenden Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="dd15c-180">`META` tags occur near the beginning of an html file within the `HEAD ... /HEAD` tags, as illustrated in the following example.</span></span>

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

<span data-ttu-id="dd15c-181">Einige HTML- `META` Tags werden automatisch bekannten Eigenschaften Satz-und Eigenschafts-ID-Werten (eigenschaftenbezeichnerwerte (PID)) zugeordnet, damit Abfragen für diese Eigenschaften den zugeordneten Inhalt durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="dd15c-181">Some HTML `META` tags are automatically mapped to well known property set and property ID (property identifier (PID)) values so that queries on these properties will search the mapped contents.</span></span> <span data-ttu-id="dd15c-182">Einige Beispiele sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd15c-182">Some examples are listed in the following table.</span></span> <span data-ttu-id="dd15c-183">Eine Liste der Systemeigenschaften, die Sie für die Dateiformate verwenden können, finden Sie unter [System definierte Eigenschaften für benutzerdefinierte Dateiformate](-shell-systemdefinedpropertiesforfileformats.md).</span><span class="sxs-lookup"><span data-stu-id="dd15c-183">For a list of system properties that you can use for your file formats, see [System-Defined Properties for Custom File Formats](-shell-systemdefinedpropertiesforfileformats.md).</span></span>

| <span data-ttu-id="dd15c-184">Eigenschafts Beispiel</span><span class="sxs-lookup"><span data-stu-id="dd15c-184">Property example</span></span>                              | <span data-ttu-id="dd15c-185">Zugeordnet zu</span><span class="sxs-lookup"><span data-stu-id="dd15c-185">Mapped to</span></span>                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="dd15c-186">Meta Name = "Author" Content = "Ruth"</span><span class="sxs-lookup"><span data-stu-id="dd15c-186">meta name="author" content="ruth"</span></span>             | <span data-ttu-id="dd15c-187">Die Eigenschaft "Author" in der Eigenschaften Gruppe für Zusammenfassungs Informationen.</span><span class="sxs-lookup"><span data-stu-id="dd15c-187">The author property in the Summary Information property set.</span></span>            |
| <span data-ttu-id="dd15c-188">Meta Name = "Subject" Content = "Word Processing"</span><span class="sxs-lookup"><span data-stu-id="dd15c-188">meta name="subject" content="word processing"</span></span> | <span data-ttu-id="dd15c-189">Die Eigenschaft "Subject" in der Eigenschaften Gruppe für Zusammenfassungs Informationen.</span><span class="sxs-lookup"><span data-stu-id="dd15c-189">The subject property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="dd15c-190">Meta Name = "Keywords" Content = "Fonts, Serif"</span><span class="sxs-lookup"><span data-stu-id="dd15c-190">meta name="keywords" content="fonts, serif"</span></span>   | <span data-ttu-id="dd15c-191">Die Schlüsselwort Eigenschaft im Eigenschaften Satz für Zusammenfassungs Informationen.</span><span class="sxs-lookup"><span data-stu-id="dd15c-191">The keyword property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="dd15c-192">Meta Name = "MS. Category" Content = "Fiction"</span><span class="sxs-lookup"><span data-stu-id="dd15c-192">meta name="ms.category" content="fiction"</span></span>     | <span data-ttu-id="dd15c-193">Die Kategorieeigenschaft in der Eigenschaft für die Dokument Zusammenfassungs Informationen.</span><span class="sxs-lookup"><span data-stu-id="dd15c-193">The category property in the document Summary Information property set.</span></span> |

<span data-ttu-id="dd15c-194">Einige Features der HTML- [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd15c-194">Some features of the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) are listed in the following table.</span></span>

[comment]: # (Diese Tabelle muss HTML sein, damit die Beispiele ordnungsgemäß formatiert werden.)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd15c-196">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="dd15c-196">Task</span></span></th>
<th><span data-ttu-id="dd15c-197">Aktion</span><span class="sxs-lookup"><span data-stu-id="dd15c-197">Action</span></span></th>
<th><span data-ttu-id="dd15c-198">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dd15c-198">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd15c-199">Erstellen spezieller Abstracts aus Dateien</span><span class="sxs-lookup"><span data-stu-id="dd15c-199">Creating special abstracts from files</span></span></td>
<td><span data-ttu-id="dd15c-200">Verwenden Sie das- <code>META NAME=&quot;DESCRIPTION&quot;...</code> Tag, um den <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> anzuweisen, die Zeichenfolge nach dem <code>CONTENT</code> Schlüsselwort als Dokument abstrakt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dd15c-200">Use the <code>META NAME=&quot;DESCRIPTION&quot;...</code> tag to instruct the <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> to use the string following the <code>CONTENT</code> keyword as the document abstract.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="dd15c-201">Der Filterprozess kann für jede gefilterte Datei Abstraktionen generieren, bei denen es sich standardmäßig um einen Satz von Zeichen am Anfang der Datei handelt.</span><span class="sxs-lookup"><span data-stu-id="dd15c-201">The filtering process can generate abstracts for each filtered file, which default to being a set of characters at the beginning of the file.</span></span>
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd15c-202">Verhindern, dass einzelne Dateien gefiltert werden</span><span class="sxs-lookup"><span data-stu-id="dd15c-202">Preventing individual files from being filtered</span></span></td>
<td><span data-ttu-id="dd15c-203">Fügen Sie <code>meta name</code> der Datei ein-Tag hinzu.</span><span class="sxs-lookup"><span data-stu-id="dd15c-203">Add a <code>meta name</code> tag to the file.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd15c-204">Festlegen des Sprachcodes für eine Datei (um sicherzustellen, dass das System die richtigen Wörter Trennungen und Füll Wort Dateien der Sprache auswählt)</span><span class="sxs-lookup"><span data-stu-id="dd15c-204">Setting the language code for a file (to ensure the system chooses the correct language word breakers and noise word files)</span></span></td>
<td><span data-ttu-id="dd15c-205">Fügen Sie der Datei das folgende- <code>meta name</code> Tag hinzu, wobei das Inhaltsfeld den entsprechenden Sprachcode angibt (entweder in Zeichen oder mithilfe des Gebiets Schema Werts).</span><span class="sxs-lookup"><span data-stu-id="dd15c-205">Add the following <code>meta name</code> tag to the file, where the content field specifies the appropriate language code (either in characters or by using the locale value).</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a><span data-ttu-id="dd15c-206">Dokument Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-206">Document Filter Handler</span></span>

<span data-ttu-id="dd15c-207">Der Dokument Filter Handler (in offilt.dll) filtert Dateien für einige Erweiterungen von Dokumenten in Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="dd15c-207">The Document filter handler (in offilt.dll) filters files for some extensions of documents in Microsoft Office.</span></span> <span data-ttu-id="dd15c-208">Dazu zählen beispielsweise Dateien mit den Erweiterungen ". doc", ". mdb", "ppt" und ". xlt".</span><span class="sxs-lookup"><span data-stu-id="dd15c-208">These include files with the extensions .doc, .mdb, .ppt, and .xlt, for example.</span></span>

### <a name="plain-text-filter-handler"></a><span data-ttu-id="dd15c-209">Nur-Text-Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-209">Plain Text Filter Handler</span></span>

<span data-ttu-id="dd15c-210">Für nur-Text-Dateien verwendet Windows Search den Textfilter Handler, der sowohl die Systemeigenschaften (z. b. Dateinamen) als auch den Inhalt einer Datei filtert.</span><span class="sxs-lookup"><span data-stu-id="dd15c-210">For plain-text files, Windows Search uses the text filter handler, which filters both the system properties (such as file names) and the contents of a file.</span></span> <span data-ttu-id="dd15c-211">Wenn ein Dateityp nicht über eine [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Zuordnung in der Registrierung verfügt, indiziert Windows Search nur die Shelleigenschaften für die Datei.</span><span class="sxs-lookup"><span data-stu-id="dd15c-211">When a file type does not have an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) association in the registry, Windows Search indexes only the Shell properties for the file.</span></span> <span data-ttu-id="dd15c-212">Der Benutzer kann jedoch die **erweiterten Optionen** in der Systemsteuerung der **Indizierungs Optionen** verwenden, um Eigenschaften oder **Index Eigenschaften und Dateiinhalte** zu **indizieren** .</span><span class="sxs-lookup"><span data-stu-id="dd15c-212">However the user can use the **Advanced Options** in the **Indexing Options** control panel to **Index Properties** or **Index Properties and File Contents**.</span></span>

![Screenshot mit dem Dialogfeld "Erweiterte Optionen"](images/ifilteradvancedoptions.png)

<span data-ttu-id="dd15c-214">Wenn der Benutzer diese Option für einen Dateityp ohne zugeordneten [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)auswählt, wird der Inhalt der Datei mithilfe des Textfilter Handlers extrahiert.</span><span class="sxs-lookup"><span data-stu-id="dd15c-214">If the user chooses this option for a file type without an associated [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), the text filter handler is used to extract the content of the file.</span></span> <span data-ttu-id="dd15c-215">Der Textfilter Handler hat kein Verständnis für ein Dokumentformat. Wenn Sie den Inhalt einer Dateifiltern, wird die Datei als Sequenz von Zeichen behandelt.</span><span class="sxs-lookup"><span data-stu-id="dd15c-215">The text filter handler does not "understand" any document format; when filtering the contents of a file, it treats the file as a sequence of characters.</span></span> <span data-ttu-id="dd15c-216">Er überprüft die Unicode-Byte Reihenfolge Markierung am Anfang der Datei.</span><span class="sxs-lookup"><span data-stu-id="dd15c-216">It does check for the Unicode byte-order mark at the beginning of the file.</span></span>

### <a name="binary-or-null-filter-handler"></a><span data-ttu-id="dd15c-217">Binärer oder NULL-Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-217">Binary or Null Filter Handler</span></span>

<span data-ttu-id="dd15c-218">Wenn eine registrierte Binärdatei gefunden wird, wird der NULL-Filter Handler verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd15c-218">When a registered binary file is encountered, the null filter handler is used.</span></span> <span data-ttu-id="dd15c-219">Der NULL-Filter Handler ruft nur die Systemeigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="dd15c-219">The null filter handler retrieves only the system properties.</span></span> <span data-ttu-id="dd15c-220">Der Inhalt einer Binärdatei wird nicht gefiltert.</span><span class="sxs-lookup"><span data-stu-id="dd15c-220">The contents of a binary file are not filtered.</span></span> <span data-ttu-id="dd15c-221">Beispiele für Systemeigenschaften sind **Dateiname**, **lastschreitezeit**, **FileSize** und **Attribute**.</span><span class="sxs-lookup"><span data-stu-id="dd15c-221">Examples of system properties are **FileName**, **LastWriteTime**, **FileSize**, and **Attributes**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dd15c-222">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dd15c-222">Additional Resources</span></span>

- <span data-ttu-id="dd15c-223">Das in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)verfügbare [ifiltersample](-search-sample-ifiltersample.md) -Codebeispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="dd15c-223">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="dd15c-224">Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dd15c-224">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="dd15c-225">Eine Übersicht über die Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="dd15c-225">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="dd15c-226">Informationen zum Abfragen von Datei Zuordnungs Attributen für einen Dateityp finden Sie unter " [wahrtentypen", "systemfileassociation" und "Anwendungs Registrierung](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))".</span><span class="sxs-lookup"><span data-stu-id="dd15c-226">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd15c-227">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd15c-227">Related topics</span></span>

[<span data-ttu-id="dd15c-228">Entwickeln von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="dd15c-228">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="dd15c-229">Informationen zu Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="dd15c-229">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="dd15c-230">Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="dd15c-230">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="dd15c-231">Zurückgeben von Eigenschaften aus einem Filter Handler</span><span class="sxs-lookup"><span data-stu-id="dd15c-231">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="dd15c-232">Implementieren von Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="dd15c-232">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="dd15c-233">Registrieren von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="dd15c-233">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)

[<span data-ttu-id="dd15c-234">Testen von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="dd15c-234">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
