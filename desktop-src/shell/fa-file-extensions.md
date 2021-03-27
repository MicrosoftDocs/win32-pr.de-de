---
description: Das Registrieren eines Dateityps ist der erste Schritt beim Erstellen einer Datei Zuordnung, bei der der Dateityp \# 0034&&\# . Ohne Dateityp Handler kann die Shell dem Benutzer jedoch keine Informationen aus der Datei und der Datei verfügbar machen.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Dateityp Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba365b6eb704def7644002b8a87c3842b62aa77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862367"
---
# <a name="file-type-handlers"></a><span data-ttu-id="5e4dc-104">Dateityp Handler</span><span class="sxs-lookup"><span data-stu-id="5e4dc-104">File Type Handlers</span></span>

<span data-ttu-id="5e4dc-105">Das [Registrieren eines Dateityps](fa-how-work.md) ist der erste Schritt beim Erstellen einer Datei Zuordnung, die den Dateityp "bekannt" für die Shell macht.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-105">[Registering a file type](fa-how-work.md) is the first step in creating a file association, which makes that file type "known" to the Shell.</span></span> <span data-ttu-id="5e4dc-106">Ohne Dateityp Handler kann die Shell dem Benutzer jedoch keine Informationen aus der Datei und der Datei verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-106">However, without file type handlers, the Shell is unable to expose information to the user from and about the file.</span></span>

<span data-ttu-id="5e4dc-107">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="5e4dc-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="5e4dc-108">Erstellen eines Dateityps, der Shell bekannt ist</span><span class="sxs-lookup"><span data-stu-id="5e4dc-108">Make a File Type Known to Shell</span></span>](#make-a-file-type-known-to-shell)
-   [<span data-ttu-id="5e4dc-109">Dateityp Handler-Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5e4dc-109">File Type Handler Descriptions</span></span>](#file-type-handler-descriptions)
-   [<span data-ttu-id="5e4dc-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e4dc-110">Related topics</span></span>](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a><span data-ttu-id="5e4dc-111">Erstellen eines Dateityps, der Shell bekannt ist</span><span class="sxs-lookup"><span data-stu-id="5e4dc-111">Make a File Type Known to Shell</span></span>

<span data-ttu-id="5e4dc-112">Im folgenden Screenshot von Windows-Explorer wird die Bilddatei "Desert. Known" in der **shellbilder** -Bibliothek angezeigt und nur mit der Paint-Anwendung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-112">In the following screen shot of Windows Explorer, the image file Desert.known appears in the Shell **Pictures** library, and is associated only with the Paint application.</span></span>

![Screenshot, der zeigt, wie der Explorer ein Bild ohne Dateityp öffnet](images/file-assoc/fileassoc-filetypehandler.png)

<span data-ttu-id="5e4dc-114">In der Datei "Desert. Known" im vorherigen Screenshot fehlen die folgenden Funktionen, die von einem Dateityp Handler aktiviert werden:</span><span class="sxs-lookup"><span data-stu-id="5e4dc-114">The Desert.known file in the preceding screen shot lacks the following functionality that is enabled by a file type handler:</span></span>

-   <span data-ttu-id="5e4dc-115">Miniaturansicht oder Vorschau</span><span class="sxs-lookup"><span data-stu-id="5e4dc-115">Thumbnail or preview</span></span>
-   <span data-ttu-id="5e4dc-116">Bild spezifische Verben im Kontextmenü, z. b.:</span><span class="sxs-lookup"><span data-stu-id="5e4dc-116">Image-specific verbs in the shortcut menu, such as:</span></span>
    -   <span data-ttu-id="5e4dc-117">Vorschau drehen</span><span class="sxs-lookup"><span data-stu-id="5e4dc-117">Rotate Preview</span></span>
    -   <span data-ttu-id="5e4dc-118">Als Desktop Hintergrund festlegen</span><span class="sxs-lookup"><span data-stu-id="5e4dc-118">Set as Desktop Background</span></span>
    -   <span data-ttu-id="5e4dc-119">Drucken</span><span class="sxs-lookup"><span data-stu-id="5e4dc-119">Print</span></span>
-   <span data-ttu-id="5e4dc-120">Bild spezifische Eigenschaften im **Detail** Bereich, z. b.:</span><span class="sxs-lookup"><span data-stu-id="5e4dc-120">Image-specific properties in the **Details** pane, such as:</span></span>
    -   <span data-ttu-id="5e4dc-121">Datum der Erstellung</span><span class="sxs-lookup"><span data-stu-id="5e4dc-121">Date Taken</span></span>
    -   <span data-ttu-id="5e4dc-122">`Tags`</span><span class="sxs-lookup"><span data-stu-id="5e4dc-122">Tags</span></span>
    -   <span data-ttu-id="5e4dc-123">Rating</span><span class="sxs-lookup"><span data-stu-id="5e4dc-123">Rating</span></span>
-   <span data-ttu-id="5e4dc-124">Indizierung von Datei Text</span><span class="sxs-lookup"><span data-stu-id="5e4dc-124">Indexing of file text</span></span>

<span data-ttu-id="5e4dc-125">Im folgenden Screenshot weist die gleiche Datei (Wüsten. Known) die Erweiterung. jpg auf, bei der es sich um einen registrierten Dateityp mit zugeordneten Dateityp Handlern handelt, sodass ein Miniaturbild und weitere Eigenschaften angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-125">In the following screen shot, the same file (Desert.known) has the .jpg extension, which is a registered file type that has associated file type handlers, so a thumbnail image and more properties are shown.</span></span>

![Bild mit einem registrierten Dateityp und zugeordneten Dateityp Handlern](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a><span data-ttu-id="5e4dc-127">Dateityp Handler-Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5e4dc-127">File Type Handler Descriptions</span></span>

<span data-ttu-id="5e4dc-128">Die Funktionen, die von jedem Dateityp Handler bereitgestellt werden, sind in der folgenden Tabelle aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="5e4dc-128">The functionality provided by each file type handler is listed in the following table:</span></span>



| <span data-ttu-id="5e4dc-129">Handler</span><span class="sxs-lookup"><span data-stu-id="5e4dc-129">Handler</span></span>                                                      | <span data-ttu-id="5e4dc-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e4dc-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e4dc-131">Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="5e4dc-131">Shortcut menu</span></span>](context-menu-handlers.md)                   | <span data-ttu-id="5e4dc-132">Ein Kontextmenü Handler, der manchmal auch als Kontextmenü Handler bezeichnet wird, ist ein Dateityp Handler, der einem vorhandenen Kontextmenü Befehle hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-132">A shortcut menu handler, sometimes referred to as a context menu handler, is a file type handler that adds commands to an existing context menu.</span></span> <span data-ttu-id="5e4dc-133">Diese Handler sind einem bestimmten Dateityp zugeordnet und werden jedes Mal aufgerufen, wenn ein Kontextmenü für einen Member des Dateityps angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-133">These handlers are associated with a particular file type and are called any time a context menu is displayed for a member of the file type.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="5e4dc-134">Miniaturansicht</span><span class="sxs-lookup"><span data-stu-id="5e4dc-134">Thumbnail</span></span>](thumbnail-providers.md)                         | <span data-ttu-id="5e4dc-135">Ein Handler, der ein Bild bereitstellt, das ein shellelement darstellen soll.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-135">A handler that provides an image to represent a Shell item.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="5e4dc-136">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5e4dc-136">Property</span></span>](../properties/building-property-handlers-properties.md) | <span data-ttu-id="5e4dc-137">Ein Eigenschaften Handler, der den Zugriff auf Element Eigenschaften für Windows Search, den Windows-Explorer und andere Anwendungen ermöglicht, die auf Eigenschaften zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-137">A property handler that provides access to item properties for Windows Search, the Windows Explorer and other applications that need to access properties.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="5e4dc-138">Vorschau</span><span class="sxs-lookup"><span data-stu-id="5e4dc-138">Preview</span></span>](preview-handlers.md)                              | <span data-ttu-id="5e4dc-139">Ein Handler, der schnell eine schreibgeschützte, vereinfachte Ansicht des Elements erstellt, das im Vorschaubereich von Windows-Explorer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-139">A handler that quickly produces a read-only, simplified view of the item to be displayed in the Windows Explorer preview pane.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="5e4dc-140">Filter</span><span class="sxs-lookup"><span data-stu-id="5e4dc-140">Filters</span></span>](../search/-search-3x-wds-extidx-filters.md)              | <span data-ttu-id="5e4dc-141">Ein Filter, eine Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle, die Dokumente für Text und Eigenschaften (auch als Attribute bezeichnet) scannt.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-141">A filter, an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface, that scans documents for text and properties (also called attributes).</span></span> <span data-ttu-id="5e4dc-142">Es extrahiert Textabschnitte aus diesen Dokumenten, filtert eingebettete Formatierungen heraus und behält Informationen über die Position des Texts bei.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-142">It extracts chunks of text from these documents, filtering out embedded formatting and retaining information about the position of the text.</span></span> <span data-ttu-id="5e4dc-143">Außerdem werden Werte Blöcke extrahiert, bei denen es sich um Eigenschaften eines gesamten Dokuments oder um klar definierte Teile eines Dokuments handelt.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-143">It also extracts chunks of values, which are properties of an entire document or of well defined parts of a document.</span></span> <span data-ttu-id="5e4dc-144">**IFilter** ist die Grundlage für das Entwickeln von Anwendungen höherer Ebene, z. b. dokumentindexer und Anwendungs unabhängige Viewer.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-144">**IFilter** provides the foundation for building higher-level applications such as document indexers and application-independent viewers.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5e4dc-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e4dc-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e4dc-146">Anwendungs Registrierung</span><span class="sxs-lookup"><span data-stu-id="5e4dc-146">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="5e4dc-147">Dateitypen</span><span class="sxs-lookup"><span data-stu-id="5e4dc-147">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="5e4dc-148">Funktionsweise von Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="5e4dc-148">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="5e4dc-149">Inhaltsansicht nach Dateityp oder-Art</span><span class="sxs-lookup"><span data-stu-id="5e4dc-149">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="5e4dc-150">Dateityp Überprüfung</span><span class="sxs-lookup"><span data-stu-id="5e4dc-150">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="5e4dc-151">Programmgesteuerte Bezeichner</span><span class="sxs-lookup"><span data-stu-id="5e4dc-151">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="5e4dc-152">Wahrgenommene Typen</span><span class="sxs-lookup"><span data-stu-id="5e4dc-152">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="5e4dc-153">Zuordnungs Arrays</span><span class="sxs-lookup"><span data-stu-id="5e4dc-153">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
