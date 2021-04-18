---
description: Sie können die Windows-Suche so erweitern, dass der Inhalt und die Eigenschaften von neuen Dateiformaten und Daten speichern mithilfe von Daten-Add-in-Schnittstellen indiziert werden.
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: Erweitern des Indexes (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a74638dd5366732716335af938c00098cc3991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340166"
---
# <a name="extending-the-index-windows-search"></a><span data-ttu-id="4dbcf-103">Erweitern des Indexes (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="4dbcf-103">Extending the Index (Windows Search)</span></span>

<span data-ttu-id="4dbcf-104">Sie können die Windows-Suche so erweitern, dass der Inhalt und die Eigenschaften von neuen Dateiformaten und Daten speichern mithilfe von [Daten-Add-in-Schnittstellen](./-search-data-addins-interfaces-entry-page.md)indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="4dbcf-104">You can extend Windows Search to index the contents and properties of new file formats, and data stores using [data add-in interfaces](./-search-data-addins-interfaces-entry-page.md).</span></span> <span data-ttu-id="4dbcf-105">Zum Erstellen von Add-Ins für Windows-Suche müssen Entwickler von Drittanbietern zuerst einen shelldatenspeicher implementieren und dann einen Protokollhandler entwickeln, damit Windows Search auf die Daten für die Indizierung zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="4dbcf-105">To create Windows Search add-ins, third-party developers must first implement a Shell data store, and then develop a protocol handler so that Windows Search can access the data for indexing.</span></span> <span data-ttu-id="4dbcf-106">Wenn Sie ein benutzerdefiniertes Dateiformat haben, müssen Sie einen Filter Handler zum Indizieren von Dateiinhalten und einen Eigenschafts Handler für jeden Dateityp zum Indizieren von Eigenschaften entwickeln.</span><span class="sxs-lookup"><span data-stu-id="4dbcf-106">If you have a custom file format, you must develop a filter handler to index file contents, and a property handler for every file type to index properties.</span></span>

<span data-ttu-id="4dbcf-107">Windows Search unterstützt derzeit die Indizierung von über 200 Typen von Elementen (z. b. txt-, HTML-und XML-Dateiformate) und kann mit mehreren Typen von Daten speichern (z. b. dem NTFS-Dateisystem und Microsoft Outlook) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4dbcf-107">Windows Search currently supports the indexing of over 200 types of items (such as .txt, .html, and .xml file formats) and can work with multiple types of data stores (such as the NTFS file system and Microsoft Outlook).</span></span> <span data-ttu-id="4dbcf-108">Windows Search verwendet die Filter-und protokollhandlertechnologie, ähnlich wie SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="4dbcf-108">Windows Search uses filter and protocol handler technology similar to SharePoint Server.</span></span> <span data-ttu-id="4dbcf-109">Wenn Sie bereits über Implementierungen für das Dateiformat verfügen, können Sie daher die Implementierungen aktualisieren, die mit einem Stream initialisiert werden sollen, indem Sie [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) verwenden, damit der Filter mit Windows Search funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4dbcf-109">Hence, if you already have implementations for your file format, you can update the implementations to be initialized with a stream by using [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) so that the filter will work with Windows Search.</span></span>

> [!Note]  
> <span data-ttu-id="4dbcf-110">Filter Handler, Eigenschaften Handler und Protokollhandler müssen in nativem Code geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4dbcf-110">Filter handlers, property handlers, and protocol handlers must be written in native code.</span></span> <span data-ttu-id="4dbcf-111">Ursache hierfür sind potenzielle Probleme bei der Common Language Runtime (CLR) mit dem Prozess, in dem mehrere Add-Ins ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4dbcf-111">This is due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

 

<span data-ttu-id="4dbcf-112">In diesem Abschnitt zur Erweiterung des Indexes mit Add-Ins finden Sie die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="4dbcf-112">This section on extending the index with add-ins contains the following topics:</span></span>

-   [<span data-ttu-id="4dbcf-113">Entwickeln von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="4dbcf-113">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
-   [<span data-ttu-id="4dbcf-114">Entwickeln von Eigenschaften Handlern für Windows Search</span><span class="sxs-lookup"><span data-stu-id="4dbcf-114">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="4dbcf-115">Entwickeln von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="4dbcf-115">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a><span data-ttu-id="4dbcf-116">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4dbcf-116">Additional Resources</span></span>

<span data-ttu-id="4dbcf-117">Verwandte Codebeispiele finden Sie unter [Codebeispiele für Windows-Suche](-search-samples-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="4dbcf-117">For related code samples, see [Windows Search Code Samples](-search-samples-ovw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dbcf-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4dbcf-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dbcf-119">Entwicklungs Leit Faden für Windows-Suche</span><span class="sxs-lookup"><span data-stu-id="4dbcf-119">Windows Search Development Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="4dbcf-120">Verwalten des Indexes</span><span class="sxs-lookup"><span data-stu-id="4dbcf-120">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="4dbcf-121">Programm gesteuertes Abfragen des Indexes</span><span class="sxs-lookup"><span data-stu-id="4dbcf-121">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="4dbcf-122">Erweitern von Sprachressourcen</span><span class="sxs-lookup"><span data-stu-id="4dbcf-122">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
