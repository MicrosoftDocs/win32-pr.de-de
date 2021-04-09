---
description: Nachdem Sie Ihre Eigenschafts Strategie bewertet haben, müssen Sie bestimmen, welche Eigenschaften in der Windows-Explorer-Benutzeroberfläche angezeigt werden sollen und wo.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Verwenden von Eigenschaften Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8644e0d51141751ac55d50966cd6163a3359435d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959362"
---
# <a name="using-property-lists"></a><span data-ttu-id="5585a-103">Verwenden von Eigenschaften Listen</span><span class="sxs-lookup"><span data-stu-id="5585a-103">Using Property Lists</span></span>

<span data-ttu-id="5585a-104">Nachdem Sie Ihre Eigenschafts Strategie bewertet haben, müssen Sie bestimmen, welche Eigenschaften in der Windows-Explorer-Benutzeroberfläche angezeigt werden sollen und wo.</span><span class="sxs-lookup"><span data-stu-id="5585a-104">After you assess your property strategy, you must determine what properties to show in the Windows Explorer UI, and where.</span></span> <span data-ttu-id="5585a-105">Es gibt verschiedene Speicherorte, an denen Eigenschaften schreibgeschützt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5585a-105">There are various locations where properties are displayed in a read-only manner.</span></span> <span data-ttu-id="5585a-106">Die Eigenschaften Bearbeitung hingegen ist nur im Dialogfeld " **Eigenschaften** " aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5585a-106">Property editing, on the other hand, is enabled only in the **Properties** dialog box.</span></span> <span data-ttu-id="5585a-107">Dieses Dialogfeld kann entweder über den Link **Eigenschaften bearbeiten** im **Vorschaufenster** oder das Kontextmenü eines Elements aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5585a-107">That dialog box can be invoked through either the **Edit Properties** link in the **Preview Pane** or the shortcut menu of an item.</span></span>

<span data-ttu-id="5585a-108">Die Eigenschaften Listen sind durch Semikolons getrennte Zeichen folgen, die die folgende Form aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5585a-108">The property lists are semi-colon delimited strings that have the following form.</span></span>


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



<span data-ttu-id="5585a-109">Das einzige derzeit verfügbare Flag ist in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5585a-109">The only flag currently available is shown in the following table.</span></span>



| <span data-ttu-id="5585a-110">Flag</span><span class="sxs-lookup"><span data-stu-id="5585a-110">Flag</span></span> | <span data-ttu-id="5585a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5585a-111">Description</span></span>                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | <span data-ttu-id="5585a-112">Zeigen Sie die-Eigenschaft im **Vorschau** Bereich nicht an, wie im **previewdetails** -Registrierungsschlüssel Wert beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5585a-112">Do not show the property in the **Preview Pane** as instructed in the **PreviewDetails** registry key value.</span></span> <span data-ttu-id="5585a-113">Sehen Sie sich das Beispiel an, das der nächsten Tabelle folgt, wenn der Wert dieser Eigenschaft nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5585a-113">See the example that follows the next table if that property's value is not set.</span></span> |



 

<span data-ttu-id="5585a-114">Nachdem Sie eine Eigenschaften Liste definiert haben, können Sie diese Zeichenfolge in der Registrierung über das standardmäßige [shelldateizuordnungssystem](../shell/fa-file-types.md) unter **HKEY \_ Classes \_ root speichern.**</span><span class="sxs-lookup"><span data-stu-id="5585a-114">After you define a property list, you can store that string in the registry through the standard [Shell file association](../shell/fa-file-types.md) system under **HKEY\_CLASSES\_ROOT.**</span></span> <span data-ttu-id="5585a-115">In der folgenden Tabelle werden die Werte für die Eigenschaften Listen zusammengefasst, die unter dem Registrierungsschlüssel für eine bestimmte Dateinamenerweiterung zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="5585a-115">The following table summarizes the values for the property lists that can be assigned under the registry key for a particular file name extension.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5585a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5585a-116">Value</span></span></th>
<th><span data-ttu-id="5585a-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5585a-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5585a-118">Voll Details</span><span class="sxs-lookup"><span data-stu-id="5585a-118">FullDetails</span></span></td>
<td><span data-ttu-id="5585a-119">Eigenschaften werden im Dialogfeld <strong>Eigenschaften</strong> auf der Registerkarte <strong>Details</strong> angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5585a-119">Properties are displayed on the <strong>Details</strong> tab of the <strong>Properties</strong> dialog box.</span></span> <span data-ttu-id="5585a-120">Dies ist die gesamte Liste der Eigenschaften, die vom Dateityp unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5585a-120">This is the complete list of properties that the file type supports.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5585a-121">Previewdetails</span><span class="sxs-lookup"><span data-stu-id="5585a-121">PreviewDetails</span></span></td>
<td><span data-ttu-id="5585a-122">Eigenschaften werden im <strong>Vorschaufenster</strong>angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5585a-122">Properties are displayed in the <strong>Preview Pane</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5585a-123">PreviewTitle</span><span class="sxs-lookup"><span data-stu-id="5585a-123">PreviewTitle</span></span></td>
<td><span data-ttu-id="5585a-124">Eigenschaften werden im Titelbereich des <strong>Vorschau</strong> Bereichs neben der Miniaturansicht des Elements angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5585a-124">Properties are displayed in the title area of the <strong>Preview Pane</strong> next to the thumbnail for the item.</span></span> <span data-ttu-id="5585a-125">Die maximale Anzahl von Einträgen beträgt 3.</span><span class="sxs-lookup"><span data-stu-id="5585a-125">The maximum number of entries is 3.</span></span> <span data-ttu-id="5585a-126">Wenn die Eigenschaften Liste mehr als die maximal zulässige Zahl enthält, werden die restlichen Einträge ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5585a-126">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5585a-127">TileInfo</span><span class="sxs-lookup"><span data-stu-id="5585a-127">TileInfo</span></span></td>
<td><span data-ttu-id="5585a-128">Eigenschaften werden angezeigt, wenn sich die Listenansicht im <strong>Kachel</strong> Ansichtsmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="5585a-128">Properties are displayed when the list view is in <strong>Tiles</strong> view mode.</span></span> <span data-ttu-id="5585a-129">Die maximale Anzahl von Einträgen beträgt 3.</span><span class="sxs-lookup"><span data-stu-id="5585a-129">The maximum number of entries is 3.</span></span> <span data-ttu-id="5585a-130">Wenn die Eigenschaften Liste mehr als die maximal zulässige Zahl enthält, werden die restlichen Einträge ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5585a-130">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5585a-131">Dieser Wert war in Windows XP vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5585a-131">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5585a-132">Extendedtileinfo</span><span class="sxs-lookup"><span data-stu-id="5585a-132">ExtendedTileInfo</span></span></td>
<td><span data-ttu-id="5585a-133">Eigenschaften werden für ein Element angezeigt, wenn sich die Listenansicht im <strong>erweiterten Kachel</strong> Ansichtsmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="5585a-133">Properties are displayed for an item when the list view is in <strong>Extended Tile</strong> view mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5585a-134">InfoTip</span><span class="sxs-lookup"><span data-stu-id="5585a-134">InfoTip</span></span></td>
<td><span data-ttu-id="5585a-135">Eigenschaften werden in einem InfoTipp angezeigt, wenn ein Benutzer auf ein Element zeigt.</span><span class="sxs-lookup"><span data-stu-id="5585a-135">Properties are displayed in an infotip when a user hovers over an item.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5585a-136">Dieser Wert war in Windows XP vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5585a-136">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5585a-137">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="5585a-137">QuickTip</span></span></td>
<td><span data-ttu-id="5585a-138">Eigenschaften werden angezeigt, wenn es schwierig ist, Eigenschaften direkt von einem Element abzurufen, z. b. wenn auf das Element über eine langsame Netzwerkverbindung zugegriffen werden muss.</span><span class="sxs-lookup"><span data-stu-id="5585a-138">Properties are displayed when it is difficult to retrieve properties directly from an item, such as when the item must be accessed over a slow network connection.</span></span> <span data-ttu-id="5585a-139">Es wird empfohlen, dass die hier genannten Eigenschaften, z. b. Typ oder Größe, nicht das Öffnen des Datei Datenstroms zum Ermitteln ihres Werts erfordern.</span><span class="sxs-lookup"><span data-stu-id="5585a-139">It is recommended that the properties named here, such as Type or Size, do not require opening the file stream to determine their value.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5585a-140">Dieser Wert war in Windows XP vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5585a-140">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5585a-141">Im folgenden Beispiel wird der previewdetails-Wert für einen. Rezept-Dateityp mithilfe einer ProgID von "Receive- **Key**" definiert.</span><span class="sxs-lookup"><span data-stu-id="5585a-141">The example below defines the PreviewDetails value for a .recipe file type, using a ProgID of **RecipeKey**.</span></span>

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

<span data-ttu-id="5585a-142">Wie im Thema [Shell-Datei](../shell/fa-file-types.md) Zuordnung erläutert, können Dateizuordnungen für die spezifischsten der allgemeinsten Form beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="5585a-142">As explained in the [Shell file association](../shell/fa-file-types.md) topic, file associations can be described for the most specific to the most general form.</span></span> <span data-ttu-id="5585a-143">Die spezifischere Form ist die einzelne Dateinamenerweiterung, und die allgemeinste Form ist ein Schlüssel, der für alle Dateien und Datei Ordner gilt.</span><span class="sxs-lookup"><span data-stu-id="5585a-143">The most specific form is the single file name extension and the most generic form is a key that applies to all files and file folders.</span></span> <span data-ttu-id="5585a-144">Zwischen diesen beiden extremen können Sie auch eine [ProgID](../shell/fa-progids.md) definieren, die eine Reihe von Dateinamen Erweiterungen gruppiert (z. t. jpg-und JPEG-Typen, die als **jpeer-Datei** gruppiert sind).</span><span class="sxs-lookup"><span data-stu-id="5585a-144">Between those two extremes, you can also define a [PROGID](../shell/fa-progids.md) that groups a set of file name extensions together (for instance, .jpg and .jpeg types grouped as **jpegfile**).</span></span> <span data-ttu-id="5585a-145">Wenn Sie Eigenschaften Listen definieren, sollten Sie diese für ProgIDs oder in einigen Fällen für bestimmte Dateinamen Erweiterungen definieren.</span><span class="sxs-lookup"><span data-stu-id="5585a-145">When you define property lists, you should define them for ProgIDs or, in some cases, specific file name extensions.</span></span> <span data-ttu-id="5585a-146">Vermeiden Sie die Verwendung von allgemeinen Einträgen, wie z. b. dem **AllFilesystemObjects** -Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="5585a-146">Avoid relying on broad entries such as the **AllFileSystemObjects** key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5585a-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5585a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5585a-148">Grundlegendes zu Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="5585a-148">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="5585a-149">Verwenden von Kind-Namen</span><span class="sxs-lookup"><span data-stu-id="5585a-149">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="5585a-150">Initialisieren von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="5585a-150">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="5585a-151">Registrieren und Verteilen von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="5585a-151">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="5585a-152">Bewährte Methoden und häufig gestellte Fragen zu Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="5585a-152">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
