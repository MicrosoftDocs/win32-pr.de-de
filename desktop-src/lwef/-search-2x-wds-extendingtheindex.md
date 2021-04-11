---
title: Erweitern des Indexes (Features der Legacy-Windows-Umgebung)
description: Die Verwendung der-und-Entwicklung für die 2. x-Versionen von Microsoft Windows Desktop Search (WDS) wird zugunsten von Windows Search dringend empfohlen.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad766d6fa1c00649f7cbdc3118039ed50f13491
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102767"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a><span data-ttu-id="78178-103">Erweitern des Indexes (Features der Legacy-Windows-Umgebung)</span><span class="sxs-lookup"><span data-stu-id="78178-103">Extending the Index (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="78178-104">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="78178-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="78178-105">Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="78178-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="78178-106">Die Verwendung der-und-Entwicklung für die 2. x-Versionen von Microsoft Windows Desktop Search (WDS) wird zugunsten von [Windows Search](../search/-search-3x-wds-overview.md)dringend empfohlen.</span><span class="sxs-lookup"><span data-stu-id="78178-106">The use of and development for the 2.x versions of Microsoft Windows Desktop Search (WDS) is strongly discouraged in favor of [Windows Search](../search/-search-3x-wds-overview.md).</span></span>

<span data-ttu-id="78178-107">WDS kann erweitert werden, um den Inhalt neuer Dateitypen und Datenspeicher zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="78178-107">WDS can be extended to index the contents of new file types and data stores.</span></span> <span data-ttu-id="78178-108">Derzeit enthält WDS 2. x Filter für mehr als 200 Typen von Elementen (einschließlich Klartext-Elemente wie HTML-, XML-und Quell Code Dateien) und verwendet dieselbe [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-und protokollhandlertechnologie wie SharePoint Services.</span><span class="sxs-lookup"><span data-stu-id="78178-108">Currently, WDS 2.x contains filters for over 200 types of items (including plaintext items such as HTML, XML, and source code files) and uses the same [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)and protocol handler technology as SharePoint Services.</span></span> <span data-ttu-id="78178-109">Wenn Sie bereits Filter Implementierungen für Ihre neuen Dateitypen installiert haben, kann WDS die vorhandenen Filter Schnittstellen verwenden, um diese Daten zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="78178-109">If you already have filter implementations installed for your new file types, WDS can use the existing filter interfaces to index this data.</span></span>

<span data-ttu-id="78178-110">WDS 2. x-Add-Ins ermöglichen es dem Index, neue Daten und Datenstrukturen zu durchlaufen und zu analysieren, um Informationen zu dem durchsuchbaren Katalog hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="78178-110">WDS 2.x add-ins enable the index to traverse and parse new data and data structures for information to add to the searchable catalog.</span></span> <span data-ttu-id="78178-111">Diese Add-Ins können auch die Windows-Shell erweitern, um den neuen Dateitypen und Daten speichern Symbole und Kontextmenü Handler zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="78178-111">These add-ins can also extend the Windows Shell to associate icons and context-menu handlers with the new file types and data stores.</span></span> <span data-ttu-id="78178-112">Wenn Sie neue Dateitypen in den WDS-Katalog einschließen möchten, muss ein Add-in die [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="78178-112">To include new file types in the WDS catalog, an add-in must implement the [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface.</span></span> <span data-ttu-id="78178-113">Wenn Sie neue Datenspeicher einschließen möchten, muss es sich bei einem Add-in um einen Protokollhandler handeln.</span><span class="sxs-lookup"><span data-stu-id="78178-113">To include new data stores, an add-in must be a protocol handler.</span></span> <span data-ttu-id="78178-114">Wenn der neue Datenspeicher eingebettete Dateien oder neue Dateitypen selbst enthält, müssen Sie auch einen entsprechenden Filter schreiben.</span><span class="sxs-lookup"><span data-stu-id="78178-114">If the new data store includes embedded files or new file types itself, you will also need to write an appropriate filter as well.</span></span>

> [!Note]
>
> <span data-ttu-id="78178-115">Filter und Protokollhandler müssen in nativem Code geschrieben werden, da mögliche Probleme mit der CLR-Versionsverwaltung bei der Verarbeitung aller Add-Ins auftreten.</span><span class="sxs-lookup"><span data-stu-id="78178-115">Filters and protocol handlers must be written in native code due to potential CLR versioning issues with the process all add-ins run in.</span></span>

 

## <a name="adding-file-types-to-the-index"></a><span data-ttu-id="78178-116">Hinzufügen von Dateitypen zum Index</span><span class="sxs-lookup"><span data-stu-id="78178-116">Adding File Types to the Index</span></span>

<span data-ttu-id="78178-117">Mit Add-Ins können WDS erweitert werden, um neue oder proprietäre Dateitypen zu indizieren und jeden neuen Dateityp einem Datei spezifischen Symbol oder einem Kontextmenü zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="78178-117">Add-ins can extend WDS to index new or proprietary file types and to associate each new file type with a file-specific icon or context menu.</span></span> <span data-ttu-id="78178-118">Zu diesem Zweck können Sie ein Add-in erstellen und registrieren, das Folgendes:</span><span class="sxs-lookup"><span data-stu-id="78178-118">To do this, you can build and register an add-in that:</span></span>

1.  <span data-ttu-id="78178-119">Implementiert eine [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Schnittstelle für jeden Dateityp, sodass WDS auf den Text und die Metadaten des Dateityps zugreifen und diese indizieren kann.</span><span class="sxs-lookup"><span data-stu-id="78178-119">Implements an [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface for each file type so WDS can access and index the file type's text and metadata.</span></span>
2.  <span data-ttu-id="78178-120">Implementiert die Schnittstellen **iextracticon** und **IContextMenu** zum Hinzufügen von Symbolen und Kontextmenüs für eine bessere Integration und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="78178-120">Implements the **IExtractIcon** and **IContextMenu** interfaces to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="78178-121">Eine Erläuterung zum Implementieren von Filtern finden [Sie unter Entwickeln von IFilter-Add-ins](-search-2x-wds-ifilteraddins.md).</span><span class="sxs-lookup"><span data-stu-id="78178-121">For a discussion on implementing filters, see [Developing IFilter Add-ins](-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="adding-data-stores-to-the-index"></a><span data-ttu-id="78178-122">Hinzufügen von Daten speichern zum Index</span><span class="sxs-lookup"><span data-stu-id="78178-122">Adding Data Stores to the Index</span></span>

<span data-ttu-id="78178-123">Mit Add-Ins können WDS erweitert werden, um neue Datenspeicher zu indizieren und um Dateien einem Datei spezifischen Symbol oder einem Kontextmenü zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="78178-123">Add-ins can extend WDS to index new data stores and to associate files with a file-specific icon or context menu.</span></span> <span data-ttu-id="78178-124">Zu diesem Zweck können Sie einen Protokollhandler erstellen und registrieren, der Folgendes:</span><span class="sxs-lookup"><span data-stu-id="78178-124">To do this, you can build and register a protocol handler that:</span></span>

1.  <span data-ttu-id="78178-125">Implementiert die **isearchprotocol** -und **iurlaccessor** -Schnittstellen, um einzelne Elemente in der Inhaltsquelle zu verarbeiten und zu binden.</span><span class="sxs-lookup"><span data-stu-id="78178-125">Implements the **ISearchProtocol** and **IUrlAccessor** interfaces to process and bind individual items in the content source.</span></span> <span data-ttu-id="78178-126">WDS verwendet URLs, um Elemente eindeutig zu identifizieren, unabhängig davon, ob sich diese Elemente im Dateisystem, in einem Daten bankähnlichen Speicher oder im Web befinden.</span><span class="sxs-lookup"><span data-stu-id="78178-126">WDS uses URLs to uniquely identify items, whether those items are in the file system, inside a database-like store, or on the Web.</span></span>
2.  <span data-ttu-id="78178-127">Implementiert die **ipersistfolder** -Schnittstelle und Teile der **IShellFolder** -Schnittstelle zum Hinzufügen von Symbolen und Kontextmenüs für eine bessere Integration und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="78178-127">Implements the **IPersistFolder** interface and portions of the **IShellFolder** interface to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="78178-128">Eine Erörterung der Implementierung von Protokoll Handlern finden Sie unter [entwickeln von Protokoll Handlern](-search-2x-wds-phaddins.md).</span><span class="sxs-lookup"><span data-stu-id="78178-128">For a discussion on implementing protocol handlers, see [Developing Protocol Handlers](-search-2x-wds-phaddins.md).</span></span>

## <a name="add-in-installer-guidelines"></a><span data-ttu-id="78178-129">Richtlinien für Add-in-Installer</span><span class="sxs-lookup"><span data-stu-id="78178-129">Add-in Installer Guidelines</span></span>

<span data-ttu-id="78178-130">Die Installation eines Add-ins sollte die folgenden Richtlinien befolgen:</span><span class="sxs-lookup"><span data-stu-id="78178-130">Installation of an add-in should follow the following guidelines:</span></span>

-   <span data-ttu-id="78178-131">Das Installationsprogramm muss entweder exe oder das MSI-Installationsprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="78178-131">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="78178-132">Anmerkungen zu dieser Version müssen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="78178-132">Release notes must be provided.</span></span>
-   <span data-ttu-id="78178-133">Ein Eintrag zum **Hinzufügen/Entfernen von Programmen** muss für jedes installierte Add-in erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="78178-133">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="78178-134">Das Installationsprogramm muss alle Registrierungs Einstellungen für einen bestimmten Dateityp oder-Speicher übernehmen, den das aktuelle Add-in versteht.</span><span class="sxs-lookup"><span data-stu-id="78178-134">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="78178-135">Wenn ein vorheriges Add-in überschrieben wird, sollte das Installationsprogramm den Benutzer benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="78178-135">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="78178-136">Wenn das vorherige Add-in von einem neueren Add-in überschrieben wurde, sollte es möglich sein, die vorherige Add-in-Funktion wiederherzustellen und Sie als Standard-Add-in für diesen Dateityp oder-Speicher zu speichern.</span><span class="sxs-lookup"><span data-stu-id="78178-136">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type or store again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78178-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78178-137">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="78178-138">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="78178-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="78178-139">Entwickeln von IFilter-Add-ins</span><span class="sxs-lookup"><span data-stu-id="78178-139">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="78178-140">Entwickeln von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="78178-140">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

<span data-ttu-id="78178-141">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="78178-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="78178-142">**IFilter**</span><span class="sxs-lookup"><span data-stu-id="78178-142">**IFilter**</span></span>](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
