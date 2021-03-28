---
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
title: Shellglossar
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2F463941-A4BA-4b34-B391-7E599E87BEEA
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6ec49f808f6c6dea74d3c8c2ac4408bc5d1a26e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345398"
---
# <a name="shell-glossary"></a><span data-ttu-id="39398-103">Shellglossar</span><span class="sxs-lookup"><span data-stu-id="39398-103">Shell Glossary</span></span>

## <a name="a"></a><span data-ttu-id="39398-104">Ein</span><span class="sxs-lookup"><span data-stu-id="39398-104">A</span></span>

<dl> <dt>

<span data-ttu-id="39398-105">**Anwalt**</span><span class="sxs-lookup"><span data-stu-id="39398-105">**association**</span></span>
</dt> <dd>

<span data-ttu-id="39398-106">Eine Zuordnung einer Dateinamenerweiterung (z. b.. MP3) oder eines Protokolls (z. b. http) zu einem programmatischen Bezeichner (ProgID).</span><span class="sxs-lookup"><span data-stu-id="39398-106">A mapping of a file name extension (for example, .mp3) or protocol (for example, http) to a programmatic identifier (ProgID).</span></span> <span data-ttu-id="39398-107">Diese Zuordnung wird in der Registrierung als benutzerspezifische Einstellung mit einem Fallback pro Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="39398-107">This mapping is stored in the registry as a per-user setting with a per-computer fallback.</span></span> <span data-ttu-id="39398-108">Anwendungen, die am Standardprogramm System teilnehmen, legen die Zuordnungs Zuordnung für die Dateinamenerweiterung oder das Protokoll fest, um auf die ProgID-Schlüssel zu verweisen, die Sie besitzen.</span><span class="sxs-lookup"><span data-stu-id="39398-108">Applications that participate in the Default Programs system set the association mapping for the file name extension or protocol to point to the ProgID keys that they own.</span></span>

</dd> <dt>

<span data-ttu-id="39398-109">**Zuordnungs Array**</span><span class="sxs-lookup"><span data-stu-id="39398-109">**association array**</span></span>
</dt> <dd>

<span data-ttu-id="39398-110">Eine geordnete Liste der Registrierungs Speicherorte, die zum Speichern von Informationen über einen Elementtyp verwendet werden, einschließlich Handler, Verben und anderen Attributen, wie z. b. Symbol und Anzeige Name des Typs.</span><span class="sxs-lookup"><span data-stu-id="39398-110">An ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="39398-111">Beispielsweise verfügt eine JPG-Datei über das folgende Zuordnungs Array auf einem standardmäßigen Windows-System: "HKCR \\ jpgfile", "HKCR \\ systemfileassociations \\ . jpg", "HKCR \\ systemfileassociation \\ Image", "HKCR \\ \* ", "HKCR \\ AllFilesystemObjects".</span><span class="sxs-lookup"><span data-stu-id="39398-111">For example, a .jpg file has the following association array on a default Windows system: "HKCR\\jpgfile", "HKCR\\SystemFileAssociations\\.jpg", "HKCR\\SystemFileAssociations\\image", "HKCR\\\*", "HKCR\\AllFileSystemObjects".</span></span>

</dd> </dl>

## <a name="b"></a><span data-ttu-id="39398-112">B</span><span class="sxs-lookup"><span data-stu-id="39398-112">B</span></span>

<dl> <dt>

<span data-ttu-id="39398-113">**bind**</span><span class="sxs-lookup"><span data-stu-id="39398-113">**bind**</span></span>
</dt> <dd>

<span data-ttu-id="39398-114">Zum Laden oder Zuordnen von Code mit Daten.</span><span class="sxs-lookup"><span data-stu-id="39398-114">To load or associate code with data.</span></span> <span data-ttu-id="39398-115">Beispielsweise kann ein Handler einer shelldatenquelle zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="39398-115">For example, a handler may be associated with a Shell data source.</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="39398-116">C</span><span class="sxs-lookup"><span data-stu-id="39398-116">C</span></span>

<dl> <dt>

<span data-ttu-id="39398-117">**Kanonischer Name**</span><span class="sxs-lookup"><span data-stu-id="39398-117">**canonical name**</span></span>
</dt> <dd>

<span data-ttu-id="39398-118">Der eindeutige Name einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="39398-118">The unique name of a resource.</span></span> <span data-ttu-id="39398-119">Kanonisch bedeutet "gemäß den Regeln".</span><span class="sxs-lookup"><span data-stu-id="39398-119">Canonical means "according to the rules."</span></span> <span data-ttu-id="39398-120">Siehe auch: kanonischer Verb Name.</span><span class="sxs-lookup"><span data-stu-id="39398-120">See also: canonical verb name.</span></span>

</dd> <dt>

<span data-ttu-id="39398-121">**Kanonischer Verb Name**</span><span class="sxs-lookup"><span data-stu-id="39398-121">**canonical verb name**</span></span>
</dt> <dd>

<span data-ttu-id="39398-122">Ein sprach neutraler Name, der unabhängig von der lokalisierten Zeichenfolge in der Benutzeroberfläche Programm gesteuert verwendet werden kann, um auf ein Verb zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="39398-122">A language-neutral name that can be used programmatically to refer to a verb, regardless of the localized string in the user interface.</span></span> <span data-ttu-id="39398-123">Siehe auch: kanonischer Name, Verb.</span><span class="sxs-lookup"><span data-stu-id="39398-123">See also: canonical name, verb.</span></span>

</dd> <dt>

<span data-ttu-id="39398-124">**container**</span><span class="sxs-lookup"><span data-stu-id="39398-124">**container**</span></span>
</dt> <dd>

<span data-ttu-id="39398-125">Ein Typ von shellelement, das andere Elemente enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="39398-125">A type of Shell item that can contain other items.</span></span> <span data-ttu-id="39398-126">Elemente in einem Container werden mithilfe einer shelldatenquelle für den Shellnamespace verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="39398-126">Items in a container are exposed to the Shell namespace by using a Shell data source.</span></span> <span data-ttu-id="39398-127">Beispiele hierfür sind Ordner, Laufwerke, Netzwerkserver und komprimierte Dateien mit der Dateinamenerweiterung ". zip".</span><span class="sxs-lookup"><span data-stu-id="39398-127">Examples include folders, drives, network servers, and compressed files with a .zip file name extension.</span></span> <span data-ttu-id="39398-128">Siehe auch: Shell-Datenquelle, Ordner, shellelement.</span><span class="sxs-lookup"><span data-stu-id="39398-128">See also: Shell data source, folder, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="39398-129">**content**</span><span class="sxs-lookup"><span data-stu-id="39398-129">**content**</span></span>
</dt> <dd>

<span data-ttu-id="39398-130">Text und Eigenschaften, die einem shellelement oder einer Inhaltsquelle zugeordnet sind, das indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="39398-130">Text and properties associated with a Shell item or a content source that can be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="39398-131">**Inhaltsquelle**</span><span class="sxs-lookup"><span data-stu-id="39398-131">**content source**</span></span>
</dt> <dd>

<span data-ttu-id="39398-132">Ein Element, auf das der Indexer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="39398-132">An item that can be accessed by the indexer.</span></span> <span data-ttu-id="39398-133">Inhalts Quellen sind über eine URL adressierbar und werden von einem Protokollhandler für den Indexer bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="39398-133">Content sources are addressable by a URL and are provided to the indexer by a protocol handler.</span></span> <span data-ttu-id="39398-134">Beispiele hierfür sind: Dateisystem Dateien und-Ordner, Microsoft Outlook-Elemente und-Ordner, Datenbankeinträge und gespeicherte Microsoft SharePoint-Elemente.</span><span class="sxs-lookup"><span data-stu-id="39398-134">Examples include: file system files and folders, Microsoft Outlook items and folders, database records, and Microsoft SharePoint stored items.</span></span> <span data-ttu-id="39398-135">Eine Inhaltsquelle kann als shellelemente verfügbar gemacht werden, indem eine shelldatenquelle implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="39398-135">A content source can be exposed as Shell items by implementing a Shell data source.</span></span> <span data-ttu-id="39398-136">Siehe auch: Inhalt, shellelement.</span><span class="sxs-lookup"><span data-stu-id="39398-136">See also: content, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="39398-137">**content view (Inhaltsansicht)**</span><span class="sxs-lookup"><span data-stu-id="39398-137">**content view**</span></span>
</dt> <dd>

<span data-ttu-id="39398-138">Eine Ansicht in Windows-Explorer (in Windows 7 und höher angeboten), die den relevantesten Inhalt für jedes Element in der Liste basierend auf der Dateinamenerweiterung oder der Art der Zuordnung anzeigt.</span><span class="sxs-lookup"><span data-stu-id="39398-138">A view in Windows Explorer (offered in Windows 7 and later) that displays the most relevant content for each item in the list based on its file name extension or Kind association.</span></span> <span data-ttu-id="39398-139">In der Inhaltsansicht wird eine Logik zur Größenänderung verwendet, mit der Eigenschaften gelöscht werden, wenn die Fenstergröße abnimmt, um sicherzustellen, dass die kritischsten Eigenschaften weiterhin Platz aufweisen, um klar lesbar</span><span class="sxs-lookup"><span data-stu-id="39398-139">Content view uses a resizing logic that drops properties when the window size decreases to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="39398-140">Siehe auch: Layoutmuster, Kind, Kind Association.</span><span class="sxs-lookup"><span data-stu-id="39398-140">See also: layout pattern, Kind, Kind association.</span></span>

</dd> <dt>

<span data-ttu-id="39398-141">**Inhalts Ansichtsmodus**</span><span class="sxs-lookup"><span data-stu-id="39398-141">**content view mode**</span></span>
</dt> <dd>

<span data-ttu-id="39398-142">Siehe Definition für: Inhaltsansicht.</span><span class="sxs-lookup"><span data-stu-id="39398-142">See definition for: content view.</span></span>

</dd> <dt>

<span data-ttu-id="39398-143">**Kontextmenü**</span><span class="sxs-lookup"><span data-stu-id="39398-143">**context menu**</span></span>
</dt> <dd>

<span data-ttu-id="39398-144">Dieser Begriff wird manchmal verwendet, um das Kontextmenü zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39398-144">This term is sometimes used to mean shortcut menu.</span></span> <span data-ttu-id="39398-145">Siehe Definition für: Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="39398-145">See definition for: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="39398-146">**Kontextmenü Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-146">**context menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-147">Dieser Begriff wird manchmal verwendet, um den Kontextmenü Handler zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39398-147">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="39398-148">Siehe Definition für: Kontextmenü Handler.</span><span class="sxs-lookup"><span data-stu-id="39398-148">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="39398-149">D</span><span class="sxs-lookup"><span data-stu-id="39398-149">D</span></span>

<dl> <dt>

<span data-ttu-id="39398-150">**Datenobjekt Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-150">**data object handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-151">Ein Handler, der zusätzliche Zwischenablage Formate für das Datenobjekt (IDataObject) eines Elements bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="39398-151">A handler that provides additional clipboard formats for the data object (IDataObject) of an item.</span></span> <span data-ttu-id="39398-152">Datenobjekte werden in Drag & Drop-und Kopier-/Einfüge Szenarien verwendet.</span><span class="sxs-lookup"><span data-stu-id="39398-152">Data objects are used in drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="39398-153">**Datenquelle**</span><span class="sxs-lookup"><span data-stu-id="39398-153">**data source**</span></span>
</dt> <dd>

<span data-ttu-id="39398-154">Dieser Begriff wird manchmal verwendet, um Datenspeicher oder Shell-Datenquelle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39398-154">This term is sometimes used to mean data store or Shell data source.</span></span> <span data-ttu-id="39398-155">Siehe Definition für: Datenspeicher, shelldatenquelle.</span><span class="sxs-lookup"><span data-stu-id="39398-155">See definition for: data store, Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="39398-156">**Datenspeicher**</span><span class="sxs-lookup"><span data-stu-id="39398-156">**data store**</span></span>
</dt> <dd>

<span data-ttu-id="39398-157">Ein Repository mit Daten.</span><span class="sxs-lookup"><span data-stu-id="39398-157">A repository of data.</span></span> <span data-ttu-id="39398-158">Ein Datenspeicher kann für das shellprogrammierungs Modell als Container mithilfe einer shelldatenquelle verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="39398-158">A data store can be exposed to the Shell programming model as a container using a Shell data source.</span></span> <span data-ttu-id="39398-159">Die Elemente in einem Datenspeicher können vom Windows-Suchsystem mithilfe eines Protokoll Handlers indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="39398-159">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

</dd> <dt>

<span data-ttu-id="39398-160">**Desktop Komposition**</span><span class="sxs-lookup"><span data-stu-id="39398-160">**desktop composition**</span></span>
</dt> <dd>

<span data-ttu-id="39398-161">Ein Windows Vista-Feature, das es ermöglicht, dass einzelne Fenster auf Offscreen-Oberflächen im Videospeicher anstatt direkt auf dem primären Anzeigegerät gezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="39398-161">A Windows Vista feature that enables individual windows to be drawn to off-screen surfaces in video memory instead of the being drawn directly to the primary display device.</span></span>

</dd> <dt>

<span data-ttu-id="39398-162">**document**</span><span class="sxs-lookup"><span data-stu-id="39398-162">**document**</span></span>
</dt> <dd>

<span data-ttu-id="39398-163">Ein shellelement, das Text enthält und für das die IFilter-Schnittstelle implementiert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="39398-163">A Shell item that contains text, and for which the IFilter interface could be implemented.</span></span>

</dd> <dt>

<span data-ttu-id="39398-164">**Drop-Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-164">**drop handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-165">Ein Handler, der einem bestimmten Elementtyp ermöglicht, Drag & Drop-und Kopier-/Einfüge Szenarien zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="39398-165">A handler that enables a particular item type to support drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="39398-166">**Ablage Ziel**</span><span class="sxs-lookup"><span data-stu-id="39398-166">**drop target**</span></span>
</dt> <dd>

<span data-ttu-id="39398-167">Ein Datenobjekt, das in eine Datei gezogen und dort abgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="39398-167">A data object that is dragged and dropped onto a file.</span></span> <span data-ttu-id="39398-168">Siehe auch: Daten Handler, Drop Handler.</span><span class="sxs-lookup"><span data-stu-id="39398-168">See also: data handler, drop handler.</span></span>

</dd> <dt>

<span data-ttu-id="39398-169">**Dynamisches Verb**</span><span class="sxs-lookup"><span data-stu-id="39398-169">**dynamic verb**</span></span>
</dt> <dd>

<span data-ttu-id="39398-170">Ein Verb, das vom Zustand eines shellelements oder des Systems abhängig ist. das Element ist Zustands basiert und erfordert, dass der ausführende Code bestimmt, ob das Element angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39398-170">A verb that depends on the state of a Shell item or of the system; the appearance of the item is state based and requires that the executing code determine whether the item should appear.</span></span> <span data-ttu-id="39398-171">Siehe auch: Kontextmenü Handler, statisches Verb, Verb.</span><span class="sxs-lookup"><span data-stu-id="39398-171">See also: shortcut menu handler, static verb, verb.</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="39398-172">E</span><span class="sxs-lookup"><span data-stu-id="39398-172">E</span></span>

<dl> <dt>

<span data-ttu-id="39398-173">**Explorer-Befehl**</span><span class="sxs-lookup"><span data-stu-id="39398-173">**Explorer command**</span></span>
</dt> <dd>

<span data-ttu-id="39398-174">Ein Objekt, das als Schaltfläche in der Nähe des oberen Fensters des Windows-Explorer-Fensters angezeigt werden kann, das Funktionen für Elemente und Container in diesem Fenster bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="39398-174">An object that can be presented as a button near the top of the Windows Explorer window that provides functionality for items and containers in that window.</span></span> <span data-ttu-id="39398-175">Eine shelldatenquelle stellt die Windows-Explorer-Befehls Objekte für ein bestimmtes Containerelement bereit.</span><span class="sxs-lookup"><span data-stu-id="39398-175">A Shell data source provides the Windows Explorer command objects for a particular container item.</span></span> <span data-ttu-id="39398-176">Befehle werden manchmal als Verben verwendet.</span><span class="sxs-lookup"><span data-stu-id="39398-176">Commands are sometimes used as verbs.</span></span>

</dd> </dl>

## <a name="f"></a><span data-ttu-id="39398-177">F</span><span class="sxs-lookup"><span data-stu-id="39398-177">F</span></span>

<dl> <dt>

<span data-ttu-id="39398-178">**Datei Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="39398-178">**file association**</span></span>
</dt> <dd>

<span data-ttu-id="39398-179">Siehe Definition für: Dateityp Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="39398-179">See definition for: file type association.</span></span>

</dd> <dt>

<span data-ttu-id="39398-180">**Dateiformat**</span><span class="sxs-lookup"><span data-stu-id="39398-180">**file format**</span></span>
</dt> <dd>

<span data-ttu-id="39398-181">Ein Format für Daten, die in einer Datei gespeichert sind, die über eine dokumentierte Format Spezifikation verfügt.</span><span class="sxs-lookup"><span data-stu-id="39398-181">A format for data stored in a file that has a documented format specification.</span></span> <span data-ttu-id="39398-182">Beispiele hierfür sind OLE DOCFILE, OPC, XML, zip und andere bekannte Datei Formatspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="39398-182">Examples include OLE DocFile, OPC, XML, ZIP and other well known file format specifications.</span></span> <span data-ttu-id="39398-183">Dateityp-Ersteller verwenden im Allgemeinen ein vorhandenes Dateiformat als Grundlage für einen neuen Dateityp.</span><span class="sxs-lookup"><span data-stu-id="39398-183">File type creators generally use an existing file format as the basis of a new file type.</span></span> <span data-ttu-id="39398-184">Ein Dateiformat kann einfach eine Definition sein, die nicht als Dateityp instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="39398-184">A file format can be simply a definition that is not instantiated as a file type.</span></span>

</dd> <dt>

<span data-ttu-id="39398-185">**Dateiformat Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-185">**file format handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-186">Dieser Begriff ist ein Synonym für den Dateityp Handler.</span><span class="sxs-lookup"><span data-stu-id="39398-186">This term is a synonym for file type handler.</span></span> <span data-ttu-id="39398-187">Siehe Definition für: Dateityp Handler.</span><span class="sxs-lookup"><span data-stu-id="39398-187">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="39398-188">**Dateinamenerweiterung**</span><span class="sxs-lookup"><span data-stu-id="39398-188">**file name extension**</span></span>
</dt> <dd>

<span data-ttu-id="39398-189">Der primäre Indikator eines Dateityps für Dateisystem Elemente, ist der Teil des Datei namens, der auf den letzten Punkt folgt.</span><span class="sxs-lookup"><span data-stu-id="39398-189">The primary indicator of a file type for file system items, it is the portion of the file name that follows the final dot.</span></span> <span data-ttu-id="39398-190">Die Dateinamenerweiterung darf keine Leerzeichen oder nicht-ASCII-Zeichen enthalten und gilt nur für Dateien (nicht für Ordner).</span><span class="sxs-lookup"><span data-stu-id="39398-190">The file name extension cannot contain spaces or non-ASCII characters and applies only to files (not folders).</span></span> <span data-ttu-id="39398-191">Dateinamen Erweiterungen werden mithilfe einer Vergleichsfunktion verglichen, bei der es sich nicht um groß-oder Kleinschreibung handelt.</span><span class="sxs-lookup"><span data-stu-id="39398-191">File name extensions are compared using a comparison function that is not sensitive to case or locale.</span></span> <span data-ttu-id="39398-192">Siehe auch: Dateiformat, Dateityp.</span><span class="sxs-lookup"><span data-stu-id="39398-192">See also: file format, file type.</span></span>

</dd> <dt>

<span data-ttu-id="39398-193">**Dateityp**</span><span class="sxs-lookup"><span data-stu-id="39398-193">**file type**</span></span>
</dt> <dd>

<span data-ttu-id="39398-194">Ein bestimmter Dateiname-Erweiterungs Wert, wie z. b. ". htm" oder ". jpg", der eine Klasse von Dateien definiert, die denselben Typ aufweisen und über einen gemeinsamen Satz von Zuordnungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="39398-194">A particular file name extension value, like ".htm" or ".jpg", that defines a class of files that are of the same type and have a common set of associations.</span></span> <span data-ttu-id="39398-195">Siehe auch: Kind, Dateityp Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="39398-195">See also: Kind, file type association.</span></span>

</dd> <dt>

<span data-ttu-id="39398-196">**Dateitypzuordnung**</span><span class="sxs-lookup"><span data-stu-id="39398-196">**file type association**</span></span>
</dt> <dd>

<span data-ttu-id="39398-197">Für eine bestimmte Dateinamenerweiterung werden die Zuordnungs Elemente, die angeben, wo Handler und andere Attribute registriert werden können, definiert.</span><span class="sxs-lookup"><span data-stu-id="39398-197">For a particular file name extension, the association array elements that define where handlers and other attributes can be registered.</span></span> <span data-ttu-id="39398-198">Siehe auch: Zuordnungs Array, Dateityp.</span><span class="sxs-lookup"><span data-stu-id="39398-198">See also: association array, file type.</span></span>

</dd> <dt>

<span data-ttu-id="39398-199">**Dateityp Anpassung**</span><span class="sxs-lookup"><span data-stu-id="39398-199">**file type customization**</span></span>
</dt> <dd>

<span data-ttu-id="39398-200">Eine Zuordnung, mit der Shell anpassen kann, wie Shell einen Dateityp behandelt.</span><span class="sxs-lookup"><span data-stu-id="39398-200">An association that enables Shell to customize how Shell treats a file type.</span></span> <span data-ttu-id="39398-201">Dateityp Anpassungen umfassen Folgendes: Angeben der Anwendung, die zum Öffnen der Datei beim Doppelklicken verwendet wurde, Hinzufügen von Befehlen zum Kontextmenü für einen Dateityp, Angeben eines benutzerdefinierten Symbols, Angeben eines MIME-Inhaltstyps, der einem Dateityp zugeordnet werden soll, Angeben eines erkannten Typs und Angeben einer oder mehrerer Anwendungen, die mit dem Dateityp verknüpft sind</span><span class="sxs-lookup"><span data-stu-id="39398-201">File type customizations include: specifying the application used to open the file when double-clicked, adding commands to the shortcut menu for a file type, specifying a custom icon, specifying a MIME content type to associate with a file type, specifying a perceived type, and specifying one or more applications associated by file type with the Open With dialog box.</span></span> <span data-ttu-id="39398-202">Siehe auch: wahrnehmvedtype.</span><span class="sxs-lookup"><span data-stu-id="39398-202">See also: PerceivedType.</span></span>

</dd> <dt>

<span data-ttu-id="39398-203">**Dateityp Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-203">**file type handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-204">Ein für einen Dateityp registrierter Handler.</span><span class="sxs-lookup"><span data-stu-id="39398-204">A handler registered for a file type.</span></span> <span data-ttu-id="39398-205">Siehe auch: Handler.</span><span class="sxs-lookup"><span data-stu-id="39398-205">See also: handler.</span></span>

</dd> <dt>

<span data-ttu-id="39398-206">**Pfalz**</span><span class="sxs-lookup"><span data-stu-id="39398-206">**folder**</span></span>
</dt> <dd>

<span data-ttu-id="39398-207">Siehe Definition für: Container.</span><span class="sxs-lookup"><span data-stu-id="39398-207">See definition for: container.</span></span>

</dd> <dt>

<span data-ttu-id="39398-208">**vollständige PIDL**</span><span class="sxs-lookup"><span data-stu-id="39398-208">**full PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="39398-209">Eine PIDL, die ein Objekt in Relation zum Desktop Ordner eindeutig beschreibt.</span><span class="sxs-lookup"><span data-stu-id="39398-209">A PIDL that uniquely describes an object relative to the desktop folder.</span></span>

</dd> </dl>

## <a name="h"></a><span data-ttu-id="39398-210">H</span><span class="sxs-lookup"><span data-stu-id="39398-210">H</span></span>

<dl> <dt>

<span data-ttu-id="39398-211">**lers**</span><span class="sxs-lookup"><span data-stu-id="39398-211">**handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-212">Ein COM-Objekt, das Funktionen für ein shellelement bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="39398-212">A COM object that provides functionality for a Shell item.</span></span> <span data-ttu-id="39398-213">Die meisten shelldatenquellen bieten ein erweiterbares System zum Binden von Handlern an Elemente.</span><span class="sxs-lookup"><span data-stu-id="39398-213">Most Shell data sources offer an extensible system for binding handlers to items.</span></span> <span data-ttu-id="39398-214">Beispielsweise verwendet der Dateisystem Ordner das Zuordnungs System, um die Handler für einen bestimmten Dateityp zu suchen.</span><span class="sxs-lookup"><span data-stu-id="39398-214">For example, the file system folder uses the association system to look up the handlers for a particular file type.</span></span> <span data-ttu-id="39398-215">Siehe auch: Datei Zuordnung, Dateityp, Dateityp Anpassung.</span><span class="sxs-lookup"><span data-stu-id="39398-215">See also: file association, file type, file type customization.</span></span>

</dd> </dl>

## <a name="i"></a><span data-ttu-id="39398-216">I</span><span class="sxs-lookup"><span data-stu-id="39398-216">I</span></span>

<dl> <dt>

<span data-ttu-id="39398-217">**Symbol Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-217">**icon handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-218">Ein Handler, der die zum Generieren und Zwischenspeichern eines Symbols für ein Element benötigten Informationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="39398-218">A handler that provides the information needed to generate and cache an icon for an item.</span></span> <span data-ttu-id="39398-219">Der Dateisystem-Datenspeicher unterstützt das Laden eines Symbol Handlers für ein Element auf der Grundlage des Dateityps, sodass dieser Handler ein Symbol bereitstellen kann, das für alle Instanzen dieses Dateityps verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39398-219">The file system data store supports loading an icon handler for an item based on the file type, enabling that handler to provide an icon that is used for all instances of that file type.</span></span>

</dd> <dt>

<span data-ttu-id="39398-220">**Infotipp-Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-220">**infotip handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-221">Ein Handler, der Popup Text bereitstellt, wenn der Benutzer mit dem Mauszeiger auf ein Benutzeroberflächen Objekt zeigt.</span><span class="sxs-lookup"><span data-stu-id="39398-221">A handler that provides pop-up text when the user hovers the mouse pointer over a user interface object.</span></span>

</dd> <dt>

<span data-ttu-id="39398-222">**item**</span><span class="sxs-lookup"><span data-stu-id="39398-222">**item**</span></span>
</dt> <dd>

<span data-ttu-id="39398-223">Siehe Definition für: shellelement.</span><span class="sxs-lookup"><span data-stu-id="39398-223">See definition for: Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="39398-224">**Item-Klasse**</span><span class="sxs-lookup"><span data-stu-id="39398-224">**item class**</span></span>
</dt> <dd>

<span data-ttu-id="39398-225">Siehe Definition für: Dateityp.</span><span class="sxs-lookup"><span data-stu-id="39398-225">See definition for: file type.</span></span>

</dd> <dt>

<span data-ttu-id="39398-226">**Liste der Element Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="39398-226">**item identifier list**</span></span>
</dt> <dd>

<span data-ttu-id="39398-227">Sequenz von einer oder mehreren shitemid-Strukturen, die ein Objekt in Relation zu einem Stamm Objekt eindeutig definiert.</span><span class="sxs-lookup"><span data-stu-id="39398-227">Sequence of one or more SHITEMID structures that uniquely defines an object relative to some root object.</span></span>

</dd> </dl>

## <a name="k"></a><span data-ttu-id="39398-228">K</span><span class="sxs-lookup"><span data-stu-id="39398-228">K</span></span>

<dl> <dt>

<span data-ttu-id="39398-229">**Kind**</span><span class="sxs-lookup"><span data-stu-id="39398-229">**Kind**</span></span>
</dt> <dd>

<span data-ttu-id="39398-230">Eine Eigenschaft, die einen benutzerfreundlichen Namen bereitstellt und einer Liste von Eigenschaften und einem Layoutmuster zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="39398-230">A property that provides a user-friendly Kind name, and can be associated with a list of properties and a layout pattern.</span></span> <span data-ttu-id="39398-231">Art wurde in Windows Vista eingeführt, um einen benutzerfreundlicheren Begriff "Dateityp" zu lesen, und er wurde als mehrwertige Zeichen folgen Eigenschaft (kanonische Zeichen folgen Werte) definiert. Daher können Sie einen "Audiotext"-oder "Link; Dokument"-Wert haben.</span><span class="sxs-lookup"><span data-stu-id="39398-231">Kind was introduced in Windows Vista to express a more end-user friendly notion of file type and it was defined to be a multi-value string property (canonical string values), thus you can have an "audio;video" or "link;document" Kind value.</span></span> <span data-ttu-id="39398-232">Einige benutzerfreundliche Arten von Namen sind bereits Eigenschaften und layoutmustern zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="39398-232">Some user-friendly Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="39398-233">Beispielsweise werden Elementen, die mit "Kind. Picture" verknüpft sind, und Elementen, die mit Kind.Doc-Ereignis verknüpft sind, andere Eigenschaften angezeigt, auch wenn Sie sich in derselben Ansicht befinden</span><span class="sxs-lookup"><span data-stu-id="39398-233">For example, items associated with Kind.Picture and items associated with Kind.Document display different properties even when they are in the same view.</span></span> <span data-ttu-id="39398-234">Jede Elementart kann einem von vier eindeutigen layoutmustern zugeordnet werden, die die Anzahl der Eigenschaften definieren, die für die einzelnen Elemente und deren Layout angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="39398-234">Each item Kind can be associated with one of four unique layout patterns that define the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="39398-235">Siehe auch: Kind Association, Content View, Layout Pattern.</span><span class="sxs-lookup"><span data-stu-id="39398-235">See also: Kind association, content view, layout pattern.</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="39398-236">L</span><span class="sxs-lookup"><span data-stu-id="39398-236">L</span></span>

<dl> <dt>

<span data-ttu-id="39398-237">**Layoutmuster**</span><span class="sxs-lookup"><span data-stu-id="39398-237">**layout pattern**</span></span>
</dt> <dd>

<span data-ttu-id="39398-238">Eine von mehreren Anordnungen zum Anzeigen von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="39398-238">One of several arrangements for displaying properties.</span></span> <span data-ttu-id="39398-239">Wenn Sie in Windows 7 und höher einen neuen Dateityp registrieren, können Sie die Inhaltsansicht verwenden, um eine benutzerdefinierte Eigenschaften Liste und ein Layoutmuster für den Dateityp zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="39398-239">In Windows 7 and later, when you are registering a new file type, you can use the content view to register a custom property list and layout pattern for your file type.</span></span> <span data-ttu-id="39398-240">Sie können aus vier unterschiedlichen layoutmustern wählen: Alpha (für Dokument Suchergebnisse, die Code Ausschnitte enthalten), Beta (für e-Mail-Suchergebnisse mit Code Ausschnitten), Gamma (ähnlich wie Alpha, aber mit einem zweizeiligen Layout anstelle von vier) und Delta (für die Anzeige zahlreicher kürzerer Eigenschaften, z. b. mit Musik und Bildern).</span><span class="sxs-lookup"><span data-stu-id="39398-240">You can choose from four different layout patterns: Alpha (for document search results that contain code snippets), Beta (for email search results with code snippets), Gamma (similar to Alpha but with a two-line layout instead of four), and Delta (for showing many shorter properties, such as with music and pictures).</span></span> <span data-ttu-id="39398-241">Siehe auch: Inhaltsansicht, Kind, Kind Association.</span><span class="sxs-lookup"><span data-stu-id="39398-241">See also: content view, Kind, Kind association.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="39398-242">M</span><span class="sxs-lookup"><span data-stu-id="39398-242">M</span></span>

<dl> <dt>

<span data-ttu-id="39398-243">**Metadatenhandler**</span><span class="sxs-lookup"><span data-stu-id="39398-243">**metadata handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-244">Dieser Begriff wird manchmal verwendet, um den Eigenschafts Handler zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39398-244">This term is sometimes used to mean property handler.</span></span> <span data-ttu-id="39398-245">Siehe Definition für: Eigenschaften Handler.</span><span class="sxs-lookup"><span data-stu-id="39398-245">See definition for: property handler.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="39398-246">N</span><span class="sxs-lookup"><span data-stu-id="39398-246">N</span></span>

<dl> <dt>

<span data-ttu-id="39398-247">**Namespace Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="39398-247">**namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="39398-248">Siehe Definition für: shelldatenquelle.</span><span class="sxs-lookup"><span data-stu-id="39398-248">See definition for: Shell data source.</span></span>

</dd> </dl>

## <a name="o"></a><span data-ttu-id="39398-249">O</span><span class="sxs-lookup"><span data-stu-id="39398-249">O</span></span>

<dl> <dt>

<span data-ttu-id="39398-250">**Objekt Verknüpfungs-und Einbettungs Datenbank (OLE DB)**</span><span class="sxs-lookup"><span data-stu-id="39398-250">**Object Linking and Embedding Database (OLE DB)**</span></span>
</dt> <dd>

<span data-ttu-id="39398-251">Ein Standardsatz von Schnittstellen, der heterogenen Zugriff auf verschiedenartige Informationsquellen bietet, z. b. Dateisysteme, e-Mail-Ordner und Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="39398-251">A standard set of interfaces that provides heterogeneous access to disparate sources of information located anywhere, such as file systems, email folders, and databases.</span></span>

</dd> <dt>

<span data-ttu-id="39398-252">**OLE DB**</span><span class="sxs-lookup"><span data-stu-id="39398-252">**OLE DB**</span></span>
</dt> <dd>

<span data-ttu-id="39398-253">Siehe Definition für: Objekt Verknüpfungs-und Einbettungs Datenbank.</span><span class="sxs-lookup"><span data-stu-id="39398-253">See definition for: Object Linking and Embedding Database.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="39398-254">P</span><span class="sxs-lookup"><span data-stu-id="39398-254">P</span></span>

<dl> <dt>

<span data-ttu-id="39398-255">**Wahrnehmungstyp**</span><span class="sxs-lookup"><span data-stu-id="39398-255">**PerceivedType**</span></span>
</dt> <dd>

<span data-ttu-id="39398-256">Eine breite Kategorie von Dateiformat Typen.</span><span class="sxs-lookup"><span data-stu-id="39398-256">A broad category of file format types.</span></span> <span data-ttu-id="39398-257">"Wahrnehmvedtype" wurde in Windows XP eingeführt und unterstützt eine begrenzte Anzahl bekannter Dateitypen (Beispiele sind Bild-, Text-, Audio-und komprimierte Dateitypen).</span><span class="sxs-lookup"><span data-stu-id="39398-257">PerceivedType was introduced in Windows XP, and supports a limited set of known file types (examples include Image, Text, Audio, and Compressed file types).</span></span> <span data-ttu-id="39398-258">Dateitypen, in der Regel öffentliche Dateitypen, können auch über einen wahrgenommenen Typ verfügen.</span><span class="sxs-lookup"><span data-stu-id="39398-258">File types, generally public file types, can also have a perceived type.</span></span> <span data-ttu-id="39398-259">Beispielsweise sind die Image Dateitypen. BMP,. png,. jpg und. gif ebenfalls den wahrgenommenen Typ Image.</span><span class="sxs-lookup"><span data-stu-id="39398-259">For example, the image file types .bmp, .png, .jpg, and .gif are also of the perceived type, image.</span></span> <span data-ttu-id="39398-260">Auf der Programmier Ebene wird "wahrvedtype" als ganze Zahl ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="39398-260">At the programming layer, PerceivedType is expressed as an integer.</span></span> <span data-ttu-id="39398-261">Da es Code gibt, der "Kind" und "wahrnehmvedtype" verwendet, müssen Besitzer von Dateiformaten beide registrieren.</span><span class="sxs-lookup"><span data-stu-id="39398-261">Because there is code that uses Kind and PerceivedType, file format owners must register both.</span></span> <span data-ttu-id="39398-262">Beispielsweise ist "Play All" von "wahrnehmvedtype" abhängig.</span><span class="sxs-lookup"><span data-stu-id="39398-262">For example "play all" depends on PerceivedType.</span></span> <span data-ttu-id="39398-263">Siehe auch: Dateityp.</span><span class="sxs-lookup"><span data-stu-id="39398-263">See also: file type.</span></span>

</dd> <dt>

<span data-ttu-id="39398-264">**Vorschau Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-264">**preview handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-265">Ein Handler, der schnell eine schreibgeschützte, vereinfachte Ansicht des shellelements erstellt, das im Vorschaubereich von Windows-Explorer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39398-265">A handler that quickly produces a read-only, simplified view of the Shell item to be displayed in the Windows Explorer preview pane.</span></span>

</dd> <dt>

<span data-ttu-id="39398-266">**Eigenschaften Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-266">**property handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-267">Ein Handler, der in einer Datei gespeicherte Daten in ein strukturiertes Schema übersetzt, das von erkannt wird und auf das von Windows-Explorer, Windows Search und anderen Anwendungen zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="39398-267">A handler that translates data stored in a file into a structured schema that is recognized by and can be accessed by Windows Explorer, Windows Search, and other applications.</span></span> <span data-ttu-id="39398-268">Diese Systeme können dann mit dem Eigenschaften Handler interagieren, um Eigenschaften in die Datei zu schreiben und diese zu lesen.</span><span class="sxs-lookup"><span data-stu-id="39398-268">These systems can then interact with the property handler to write and read properties to and from the file.</span></span> <span data-ttu-id="39398-269">Zu den übersetzten Daten zählen Detailansicht, Infotipps, Detailbereich, Eigenschaften Seiten usw.</span><span class="sxs-lookup"><span data-stu-id="39398-269">The translated data includes details view, infotips, details pane, property pages, and so forth.</span></span> <span data-ttu-id="39398-270">Jeder Eigenschaften Handler ist einem bestimmten Dateityp zugeordnet, der durch die Dateinamenerweiterung gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="39398-270">Each property handler is associated with a particular file type, identified by the file name extension.</span></span> <span data-ttu-id="39398-271">Siehe auch: Eigenschaften System.</span><span class="sxs-lookup"><span data-stu-id="39398-271">See also: property system.</span></span>

</dd> <dt>

<span data-ttu-id="39398-272">**Eigenschaften Blatt Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-272">**property sheet handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-273">Ein Handler, der zum Erstellen benutzerdefinierter Eigenschaften Blätter mit UI-Bildern und Steuerelementen verwendet wird, die eine benutzerdefinierte Interaktion mit einem Dateityp ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="39398-273">A handler that is used to create custom property sheets with UI pictures and controls that permit custom interaction with a file type.</span></span>

</dd> <dt>

<span data-ttu-id="39398-274">**Eigenschaften System**</span><span class="sxs-lookup"><span data-stu-id="39398-274">**property system**</span></span>
</dt> <dd>

<span data-ttu-id="39398-275">Ein erweiterbares Lese-/Schreibsystem von Daten Definitionen, das Eigenschaften verwendet, die als Name-Wert-Paare implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="39398-275">An extensible read/write system of data definitions that uses properties implemented as name-value pairs.</span></span> <span data-ttu-id="39398-276">Siehe auch: Eigenschaften Handler, shellelement.</span><span class="sxs-lookup"><span data-stu-id="39398-276">See also: property handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="39398-277">**Eigenschafts Wert**</span><span class="sxs-lookup"><span data-stu-id="39398-277">**property value**</span></span>
</dt> <dd>

<span data-ttu-id="39398-278">Ein Wert, der einem Eigenschaftsnamen für ein shellelement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="39398-278">A value associated with a property name for a Shell item.</span></span> <span data-ttu-id="39398-279">Beispielsweise sind "Author", "size" und "Date Taken" Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="39398-279">For example, "Author", "Size", and "Date Taken" are properties.</span></span> <span data-ttu-id="39398-280">Eigenschaftswerte werden als PROPVARIANT-Struktur ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="39398-280">Property values are expressed as a PROPVARIANT structure.</span></span>

</dd> <dt>

<span data-ttu-id="39398-281">**Protokollhandler**</span><span class="sxs-lookup"><span data-stu-id="39398-281">**protocol handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-282">Ein Handler, der auf Inhalts Quellen zugreift und ein iurlaccessor-Objekt für ein angegebenes Protokoll und eine URL bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="39398-282">A handler that accesses content sources and provides an IUrlAccessor object for a specified protocol and URL.</span></span> <span data-ttu-id="39398-283">Protokollhandler erweitern die Windows-Suchfunktionen und stellen möglicherweise Änderungs Benachrichtigungen für Indexer bereit.</span><span class="sxs-lookup"><span data-stu-id="39398-283">Protocol handlers extend Windows Search functionality, and may provide change notifications to indexers.</span></span> <span data-ttu-id="39398-284">Zum Indizieren bestimmter Typen von Daten speichern sind unterschiedliche Protokollhandler erforderlich.</span><span class="sxs-lookup"><span data-stu-id="39398-284">Different protocol handlers are required to index specific types of data stores.</span></span> <span data-ttu-id="39398-285">Zum Bereitstellen eines angemessenen Benutzer Erlebnisses müssen Sie zusätzlich zur Implementierung des Protokoll Handlers auch eine Shell-Datenquelle für den Datenspeicher bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="39398-285">To provide a reasonable user experience, you must also provide a Shell data source for the data store in addition to implementing your protocol handler.</span></span> <span data-ttu-id="39398-286">Der Protokollhandler macht die Elemente im Datenspeicher für den Indexer verfügbar, während die shelldatenquelle die Elemente im Datenspeicher für die Shell verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="39398-286">The protocol handler exposes the items in the data store to the indexer, while the Shell data source exposes the items in the data store to the Shell.</span></span>

</dd> </dl>

## <a name="r"></a><span data-ttu-id="39398-287">R</span><span class="sxs-lookup"><span data-stu-id="39398-287">R</span></span>

<dl> <dt>

<span data-ttu-id="39398-288">**relative PIDL**</span><span class="sxs-lookup"><span data-stu-id="39398-288">**relative PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="39398-289">Eine PIDL, die relativ zu einem Stamm Objekt im Shell-Namespace ist, das nicht der Desktop Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="39398-289">A PIDL that is relative to some root object in the shell namespace other than the desktop folder.</span></span> <span data-ttu-id="39398-290">Dies ist in der Regel der übergeordnete Ordner des Elements.</span><span class="sxs-lookup"><span data-stu-id="39398-290">This is commonly the parent folder of the item.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="39398-291">E</span><span class="sxs-lookup"><span data-stu-id="39398-291">S</span></span>

<dl> <dt>

<span data-ttu-id="39398-292">**Shelldatenquelle**</span><span class="sxs-lookup"><span data-stu-id="39398-292">**Shell data source**</span></span>
</dt> <dd>

<span data-ttu-id="39398-293">Eine Komponente, die verwendet wird, um den Shellnamespace zu erweitern und Elemente in einem Datenspeicher verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="39398-293">A component that is used to extend the Shell namespace and expose items in a data store.</span></span> <span data-ttu-id="39398-294">In der Vergangenheit wurde die shelldatenquelle als Shell-Namespace Erweiterung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="39398-294">In the past, the Shell data source was referred to as the Shell namespace extension.</span></span> <span data-ttu-id="39398-295">Siehe auch: Container, Handler, shellelement.</span><span class="sxs-lookup"><span data-stu-id="39398-295">See also: container, handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="39398-296">**Shellerweiterung**</span><span class="sxs-lookup"><span data-stu-id="39398-296">**Shell extension**</span></span>
</dt> <dd>

<span data-ttu-id="39398-297">Dieser Begriff wird manchmal verwendet, um den Dateityp Handler zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39398-297">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="39398-298">Siehe Definition für: Dateityp Handler.</span><span class="sxs-lookup"><span data-stu-id="39398-298">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="39398-299">**Shellerweiterungs Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-299">**Shell extension handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-300">Dieser Begriff wird manchmal verwendet, um den Dateityp Handler zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39398-300">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="39398-301">Siehe Definition für: Dateityp Handler.</span><span class="sxs-lookup"><span data-stu-id="39398-301">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="39398-302">**Shellhandler**</span><span class="sxs-lookup"><span data-stu-id="39398-302">**Shell handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-303">Dieser Begriff wird manchmal verwendet, um den Dateityp Handler zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39398-303">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="39398-304">Siehe Definition für: Dateityp Handler.</span><span class="sxs-lookup"><span data-stu-id="39398-304">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="39398-305">**Shellelement**</span><span class="sxs-lookup"><span data-stu-id="39398-305">**Shell item**</span></span>
</dt> <dd>

<span data-ttu-id="39398-306">Ein einzelnes Inhalts Element.</span><span class="sxs-lookup"><span data-stu-id="39398-306">A single piece of content.</span></span> <span data-ttu-id="39398-307">Einige shellelemente sind Inhalts Quellen, andere hingegen nicht.</span><span class="sxs-lookup"><span data-stu-id="39398-307">Some Shell items are content sources, and some are not.</span></span> <span data-ttu-id="39398-308">Ein Ordner ist eine Inhaltsquelle, z. b. eine JPG-Datei.</span><span class="sxs-lookup"><span data-stu-id="39398-308">A folder is a content source, for example, but a .jpg file is not.</span></span> <span data-ttu-id="39398-309">Dateityp Handler machen shellelemente verfügbar.</span><span class="sxs-lookup"><span data-stu-id="39398-309">File type handlers expose Shell items.</span></span> <span data-ttu-id="39398-310">In manchen Kontexten wird "Item" verwendet, um Container von nicht Containern zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="39398-310">In some contexts "item" is used to distinguish containers from noncontainers.</span></span> <span data-ttu-id="39398-311">Siehe auch: Container, Inhaltsquelle, Dateityp Handler.</span><span class="sxs-lookup"><span data-stu-id="39398-311">See also: container, content source, file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="39398-312">**Shell-Namespace Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="39398-312">**Shell namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="39398-313">Dieser Begriff wird manchmal zum Mean der shelldatenquelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="39398-313">This term is sometimes used to mean Shell data source.</span></span> <span data-ttu-id="39398-314">Siehe Definition für: shelldatenquelle.</span><span class="sxs-lookup"><span data-stu-id="39398-314">See definition for: Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="39398-315">**Kontextmenü**</span><span class="sxs-lookup"><span data-stu-id="39398-315">**shortcut menu**</span></span>
</dt> <dd>

<span data-ttu-id="39398-316">Eine Benutzeroberfläche, die verwendet wird, um eine Auflistung von Verben darzustellen, die einem Benutzeroberflächen Element zugeordnet sind, z. b. eine Datei oder ein Ordner.</span><span class="sxs-lookup"><span data-stu-id="39398-316">A user interface that is used to present a collection of verbs associated with a user interface element, such as a file or folder.</span></span>

</dd> <dt>

<span data-ttu-id="39398-317">**Kontextmenü Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-317">**Shortcut menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-318">Ein Handler, der Verben für ein Element oder Elemente hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="39398-318">A handler that adds verbs for an item or items.</span></span> <span data-ttu-id="39398-319">Diese Verben werden in der Regel in einem Kontextmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39398-319">These verbs are commonly displayed in a shortcut menu.</span></span> <span data-ttu-id="39398-320">Siehe auch: Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="39398-320">See also: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="39398-321">**einfache PIDL**</span><span class="sxs-lookup"><span data-stu-id="39398-321">**simple PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="39398-322">Eine PIDL, die ohne Datenträger Überprüfung analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="39398-322">A PIDL that is parsed without disk verification.</span></span>

</dd> <dt>

<span data-ttu-id="39398-323">**statisches Verb**</span><span class="sxs-lookup"><span data-stu-id="39398-323">**static verb**</span></span>
</dt> <dd>

<span data-ttu-id="39398-324">Ein Verb, das für ein shellelement gilt, ohne den aktuellen Zustand eines Elements oder Systems überprüfen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="39398-324">A verb that applies to a Shell item without needing to inspect the current state of an item or system.</span></span> <span data-ttu-id="39398-325">Ein statisches Verb basiert auf einer statischen Registrierung der zugeordneten Elemente eines Elements und ändert sich nicht.</span><span class="sxs-lookup"><span data-stu-id="39398-325">A static verb is based on a static registration of the associated elements of an item, and does not change.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="39398-326">T</span><span class="sxs-lookup"><span data-stu-id="39398-326">T</span></span>

<dl> <dt>

<span data-ttu-id="39398-327">**Miniatur Ansichts Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-327">**thumbnail handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-328">Ein Handler, der ein statisches Bild bereitstellt, das ein shellelement darstellen soll.</span><span class="sxs-lookup"><span data-stu-id="39398-328">A handler that provides a static image to represent a Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="39398-329">**Miniatur Ansichts Anbieter**</span><span class="sxs-lookup"><span data-stu-id="39398-329">**thumbnail provider**</span></span>
</dt> <dd>

<span data-ttu-id="39398-330">Dieser Begriff wird manchmal verwendet, um den Miniatur Ansichts Handler zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39398-330">This term is sometimes used to mean thumbnail handler.</span></span> <span data-ttu-id="39398-331">Siehe Definition für: Miniatur Ansichts Handler.</span><span class="sxs-lookup"><span data-stu-id="39398-331">See definition for: thumbnail handler.</span></span>

</dd> </dl>

## <a name="u"></a><span data-ttu-id="39398-332">U</span><span class="sxs-lookup"><span data-stu-id="39398-332">U</span></span>

<dl> <dt>

<span data-ttu-id="39398-333">**benutzerfreundlicher Name der Art**</span><span class="sxs-lookup"><span data-stu-id="39398-333">**user friendly kind name**</span></span>
</dt> <dd>

<span data-ttu-id="39398-334">Siehe Definition für: Kind.</span><span class="sxs-lookup"><span data-stu-id="39398-334">See definition for: Kind.</span></span>

</dd> </dl>

## <a name="v"></a><span data-ttu-id="39398-335">V</span><span class="sxs-lookup"><span data-stu-id="39398-335">V</span></span>

<dl> <dt>

<span data-ttu-id="39398-336">**Verb**</span><span class="sxs-lookup"><span data-stu-id="39398-336">**verb**</span></span>
</dt> <dd>

<span data-ttu-id="39398-337">Eine einzelne Aktion, die von einem shellelement aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="39398-337">An individual action that can be called by a Shell item.</span></span> <span data-ttu-id="39398-338">Beispiele hierfür sind Open und Print.</span><span class="sxs-lookup"><span data-stu-id="39398-338">Examples include open and print.</span></span> <span data-ttu-id="39398-339">Verben werden manchmal als Befehle oder Aufgaben bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="39398-339">Verbs are sometimes referred to as commands or tasks.</span></span> <span data-ttu-id="39398-340">Siehe auch: Dynamisches Verb, Kontextmenü Handler, statisches Verb.</span><span class="sxs-lookup"><span data-stu-id="39398-340">See also: dynamic verb, shortcut menu handler, static verb.</span></span>

</dd> <dt>

<span data-ttu-id="39398-341">**Verb Handler**</span><span class="sxs-lookup"><span data-stu-id="39398-341">**verb handler**</span></span>
</dt> <dd>

<span data-ttu-id="39398-342">Dieser Begriff wird manchmal verwendet, um den Kontextmenü Handler zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39398-342">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="39398-343">Siehe Definition für: Kontextmenü Handler.</span><span class="sxs-lookup"><span data-stu-id="39398-343">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

 

 



