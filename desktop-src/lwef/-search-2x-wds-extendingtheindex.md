---
title: Erweitern des Index (Ältere Windows-Umgebungsfeatures)
description: Erfahren Sie, wie Sie den Index in der Windows-Desktopsuche 2.x erweitern. Verwenden Sie für Windows-Releases, die höher als Windows XP und Windows Server 2003 sind, Windows Search.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63408cfe1efeb8da4d6a4540cc57b99ea56ae935
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407353"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a><span data-ttu-id="67719-104">Erweitern des Index (Ältere Windows-Umgebungsfeatures)</span><span class="sxs-lookup"><span data-stu-id="67719-104">Extending the Index (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="67719-105">Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="67719-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="67719-106">Verwenden Sie in späteren [Versionen Windows Search.](../search/-search-3x-wds-overview.md)</span><span class="sxs-lookup"><span data-stu-id="67719-106">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="67719-107">Die Verwendung von und entwicklung für die 2.x-Versionen von Microsoft Windows Desktop Search (WDS) wird dringend zugunsten von [Windows Search.](../search/-search-3x-wds-overview.md)</span><span class="sxs-lookup"><span data-stu-id="67719-107">The use of and development for the 2.x versions of Microsoft Windows Desktop Search (WDS) is strongly discouraged in favor of [Windows Search](../search/-search-3x-wds-overview.md).</span></span>

<span data-ttu-id="67719-108">WDS kann erweitert werden, um den Inhalt neuer Dateitypen und Datenspeicher zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="67719-108">WDS can be extended to index the contents of new file types and data stores.</span></span> <span data-ttu-id="67719-109">Derzeit enthält WDS 2.x Filter für mehr als 200 Elementtypen (einschließlich Klartextelementen wie HTML-, XML- und Quellcodedateien) und verwendet die gleiche [**IFilter-**](/windows/desktop/api/filter/nn-filter-ifilter)und Protokollhandlertechnologie wie SharePoint Services.</span><span class="sxs-lookup"><span data-stu-id="67719-109">Currently, WDS 2.x contains filters for over 200 types of items (including plaintext items such as HTML, XML, and source code files) and uses the same [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)and protocol handler technology as SharePoint Services.</span></span> <span data-ttu-id="67719-110">Wenn Sie bereits Filterimplementierungen für Ihre neuen Dateitypen installiert haben, kann WDS die vorhandenen Filterschnittstellen verwenden, um diese Daten zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="67719-110">If you already have filter implementations installed for your new file types, WDS can use the existing filter interfaces to index this data.</span></span>

<span data-ttu-id="67719-111">WDS 2.x-Add-Ins ermöglichen es dem Index, neue Daten und Datenstrukturen zu durchlaufen und zu analysieren, um Informationen zum durchsuchbaren Katalog hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="67719-111">WDS 2.x add-ins enable the index to traverse and parse new data and data structures for information to add to the searchable catalog.</span></span> <span data-ttu-id="67719-112">Diese Add-Ins können auch die Windows-Shell erweitern, um den neuen Dateitypen und Datenspeichern Symbole und Kontextmenühandler zu zuordnen.</span><span class="sxs-lookup"><span data-stu-id="67719-112">These add-ins can also extend the Windows Shell to associate icons and context-menu handlers with the new file types and data stores.</span></span> <span data-ttu-id="67719-113">Um neue Dateitypen in den WDS-Katalog ein include zu setzen, muss ein Add-In die [**IFilter-Schnittstelle**](/windows/desktop/api/filter/nn-filter-ifilter)implementieren.</span><span class="sxs-lookup"><span data-stu-id="67719-113">To include new file types in the WDS catalog, an add-in must implement the [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface.</span></span> <span data-ttu-id="67719-114">Um neue Datenspeicher ein include, muss ein Add-In ein Protokollhandler sein.</span><span class="sxs-lookup"><span data-stu-id="67719-114">To include new data stores, an add-in must be a protocol handler.</span></span> <span data-ttu-id="67719-115">Wenn der neue Datenspeicher eingebettete Dateien oder neue Dateitypen selbst enthält, müssen Sie auch einen entsprechenden Filter schreiben.</span><span class="sxs-lookup"><span data-stu-id="67719-115">If the new data store includes embedded files or new file types itself, you will also need to write an appropriate filter as well.</span></span>

> [!Note]
>
> <span data-ttu-id="67719-116">Filter und Protokollhandler müssen aufgrund potenzieller CLR-Versionsprobleme mit dem Prozess, in dem alle Add-Ins ausgeführt werden, in nativem Code geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="67719-116">Filters and protocol handlers must be written in native code due to potential CLR versioning issues with the process all add-ins run in.</span></span>

 

## <a name="adding-file-types-to-the-index"></a><span data-ttu-id="67719-117">Hinzufügen von Dateitypen zum Index</span><span class="sxs-lookup"><span data-stu-id="67719-117">Adding File Types to the Index</span></span>

<span data-ttu-id="67719-118">Add-Ins können WDS erweitern, um neue oder proprietäre Dateitypen zu indizieren und jeden neuen Dateityp einem dateispezifischen Symbol oder Kontextmenü zu zuordnen.</span><span class="sxs-lookup"><span data-stu-id="67719-118">Add-ins can extend WDS to index new or proprietary file types and to associate each new file type with a file-specific icon or context menu.</span></span> <span data-ttu-id="67719-119">Hierzu können Sie ein Add-In erstellen und registrieren, das:</span><span class="sxs-lookup"><span data-stu-id="67719-119">To do this, you can build and register an add-in that:</span></span>

1.  <span data-ttu-id="67719-120">Implementiert eine [**IFilter-Schnittstelle**](/windows/desktop/api/filter/nn-filter-ifilter)für jeden Dateityp, damit WDS auf den Text und die Metadaten des Dateityps zugreifen und diese indizieren kann.</span><span class="sxs-lookup"><span data-stu-id="67719-120">Implements an [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface for each file type so WDS can access and index the file type's text and metadata.</span></span>
2.  <span data-ttu-id="67719-121">Implementiert die **Schnittstellen IExtractIcon** und **IContextMenu,** um Symbole und Kontextmenüs hinzuzufügen, um die Integration und Benutzerfreundlichkeit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="67719-121">Implements the **IExtractIcon** and **IContextMenu** interfaces to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="67719-122">Eine Erörterung zum Implementieren von Filtern finden Sie unter [Entwickeln von IFilter-Add-Ins.](-search-2x-wds-ifilteraddins.md)</span><span class="sxs-lookup"><span data-stu-id="67719-122">For a discussion on implementing filters, see [Developing IFilter Add-ins](-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="adding-data-stores-to-the-index"></a><span data-ttu-id="67719-123">Hinzufügen von Datenspeichern zum Index</span><span class="sxs-lookup"><span data-stu-id="67719-123">Adding Data Stores to the Index</span></span>

<span data-ttu-id="67719-124">Add-Ins können WDS erweitern, um neue Datenspeicher zu indizieren und Dateien einem dateispezifischen Symbol oder Kontextmenü zu zuordnen.</span><span class="sxs-lookup"><span data-stu-id="67719-124">Add-ins can extend WDS to index new data stores and to associate files with a file-specific icon or context menu.</span></span> <span data-ttu-id="67719-125">Hierzu können Sie einen Protokollhandler erstellen und registrieren, der:</span><span class="sxs-lookup"><span data-stu-id="67719-125">To do this, you can build and register a protocol handler that:</span></span>

1.  <span data-ttu-id="67719-126">Implementiert die **Schnittstellen ISearchProtocol** und **IUrlAccessor,** um einzelne Elemente in der Inhaltsquelle zu verarbeiten und zu binden.</span><span class="sxs-lookup"><span data-stu-id="67719-126">Implements the **ISearchProtocol** and **IUrlAccessor** interfaces to process and bind individual items in the content source.</span></span> <span data-ttu-id="67719-127">WDS verwendet URLs, um Elemente eindeutig zu identifizieren, unabhängig davon, ob sich diese Elemente im Dateisystem, in einem datenbankbasierten Speicher oder im Web befinden.</span><span class="sxs-lookup"><span data-stu-id="67719-127">WDS uses URLs to uniquely identify items, whether those items are in the file system, inside a database-like store, or on the Web.</span></span>
2.  <span data-ttu-id="67719-128">Implementiert die **IPersistFolder-Schnittstelle** und Teile der **IShellFolder-Schnittstelle,** um Symbole und Kontextmenüs hinzuzufügen, um die Integration und Benutzerfreundlichkeit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="67719-128">Implements the **IPersistFolder** interface and portions of the **IShellFolder** interface to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="67719-129">Eine Erörterung zur Implementierung von Protokollhandlern finden Sie unter Developing Protocol Handlers ( [Entwickeln von Protokollhandlern](-search-2x-wds-phaddins.md)).</span><span class="sxs-lookup"><span data-stu-id="67719-129">For a discussion on implementing protocol handlers, see [Developing Protocol Handlers](-search-2x-wds-phaddins.md).</span></span>

## <a name="add-in-installer-guidelines"></a><span data-ttu-id="67719-130">Richtlinien für Das Add-In-Installationsprogramm</span><span class="sxs-lookup"><span data-stu-id="67719-130">Add-in Installer Guidelines</span></span>

<span data-ttu-id="67719-131">Die Installation eines Add-Ins sollte den folgenden Richtlinien entsprechen:</span><span class="sxs-lookup"><span data-stu-id="67719-131">Installation of an add-in should follow the following guidelines:</span></span>

-   <span data-ttu-id="67719-132">Das Installationsprogramm muss entweder EXE- oder MSI-Installationsprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="67719-132">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="67719-133">Versionshinweise müssen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="67719-133">Release notes must be provided.</span></span>
-   <span data-ttu-id="67719-134">Für **jedes installierte Add-In** muss ein Eintrag Zum Hinzufügen/Entfernen von Programmen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="67719-134">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="67719-135">Das Installationsprogramm muss alle Registrierungseinstellungen für den jeweiligen Dateityp oder Speicher übernehmen, den das aktuelle Add-In versteht.</span><span class="sxs-lookup"><span data-stu-id="67719-135">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="67719-136">Wenn ein vorheriges Add-In überschrieben wird, sollte das Installationsprogramm den Benutzer benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="67719-136">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="67719-137">Wenn ein neueres Add-In das vorherige Add-In überschrieben hat, sollte es die Möglichkeit geben, die Funktionalität des vorherigen Add-Ins wiederherzustellen und es wieder zum Standard-Add-In für diesen Dateityp oder -speicher zu machen.</span><span class="sxs-lookup"><span data-stu-id="67719-137">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type or store again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67719-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67719-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="67719-139">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="67719-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="67719-140">Entwickeln von IFilter-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="67719-140">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="67719-141">Entwickeln von Protokollhandlern</span><span class="sxs-lookup"><span data-stu-id="67719-141">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

<span data-ttu-id="67719-142">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="67719-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="67719-143">**Ifilter**</span><span class="sxs-lookup"><span data-stu-id="67719-143">**IFilter**</span></span>](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
