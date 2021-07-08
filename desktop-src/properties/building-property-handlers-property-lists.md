---
description: Nachdem Sie Ihre Eigenschaftsstrategie bewertet haben, müssen Sie bestimmen, welche Eigenschaften in der Windows Explorer-Benutzeroberfläche und wo angezeigt werden sollen.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Verwenden von Eigenschaftenlisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ade6cba2807e87306aa9cacb3649499d9e5ffe1
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481915"
---
# <a name="using-property-lists"></a><span data-ttu-id="8b51f-103">Verwenden von Eigenschaftenlisten</span><span class="sxs-lookup"><span data-stu-id="8b51f-103">Using Property Lists</span></span>

<span data-ttu-id="8b51f-104">Nachdem Sie Ihre Eigenschaftsstrategie bewertet haben, müssen Sie bestimmen, welche Eigenschaften in der Windows Explorer-Benutzeroberfläche und wo angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b51f-104">After you assess your property strategy, you must determine what properties to show in the Windows Explorer UI, and where.</span></span> <span data-ttu-id="8b51f-105">Es gibt verschiedene Speicherorte, an denen Eigenschaften schreibgeschützt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8b51f-105">There are various locations where properties are displayed in a read-only manner.</span></span> <span data-ttu-id="8b51f-106">Die Eigenschaftenbearbeitung ist dagegen nur im Dialogfeld **Eigenschaften** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8b51f-106">Property editing, on the other hand, is enabled only in the **Properties** dialog box.</span></span> <span data-ttu-id="8b51f-107">Dieses Dialogfeld kann entweder über den Link **Eigenschaften bearbeiten** im **Vorschaubereich** oder über das Kontextmenü eines Elements aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8b51f-107">That dialog box can be invoked through either the **Edit Properties** link in the **Preview Pane** or the shortcut menu of an item.</span></span>

<span data-ttu-id="8b51f-108">Bei den Eigenschaftenlisten handelt es sich um durch Semikolons getrennte Zeichenfolgen mit der folgenden Form.</span><span class="sxs-lookup"><span data-stu-id="8b51f-108">The property lists are semi-colon delimited strings that have the following form.</span></span>


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



<span data-ttu-id="8b51f-109">Das einzige derzeit verfügbare Flag wird in der folgenden Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8b51f-109">The only flag currently available is shown in the following table.</span></span>



| <span data-ttu-id="8b51f-110">Flag</span><span class="sxs-lookup"><span data-stu-id="8b51f-110">Flag</span></span> | <span data-ttu-id="8b51f-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b51f-111">Description</span></span>                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | <span data-ttu-id="8b51f-112">Zeigen Sie die Eigenschaft nicht wie im Registrierungsschlüsselwert **PreviewDetailsbewiesen** im **Vorschaubereich** an.</span><span class="sxs-lookup"><span data-stu-id="8b51f-112">Do not show the property in the **Preview Pane** as instructed in the **PreviewDetails** registry key value.</span></span> <span data-ttu-id="8b51f-113">Sehen Sie sich das Beispiel an, das auf die nächste Tabelle folgt, wenn der Wert dieser Eigenschaft nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8b51f-113">See the example that follows the next table if that property's value is not set.</span></span> |



 

<span data-ttu-id="8b51f-114">Nachdem Sie eine Eigenschaftenliste definiert haben, können Sie diese Zeichenfolge über das [Standardmäßige Shell-Dateizuordnungssystem](../shell/fa-file-types.md) unter HKEY CLASSES ROOT in der Registrierung **\_ \_ speichern.**</span><span class="sxs-lookup"><span data-stu-id="8b51f-114">After you define a property list, you can store that string in the registry through the standard [Shell file association](../shell/fa-file-types.md) system under **HKEY\_CLASSES\_ROOT.**</span></span> <span data-ttu-id="8b51f-115">In der folgenden Tabelle sind die Werte für die Eigenschaftenlisten zusammengefasst, die unter dem Registrierungsschlüssel für eine bestimmte Dateinamenerweiterung zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="8b51f-115">The following table summarizes the values for the property lists that can be assigned under the registry key for a particular file name extension.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b51f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8b51f-116">Value</span></span></th>
<th><span data-ttu-id="8b51f-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b51f-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8b51f-118">FullDetails</span><span class="sxs-lookup"><span data-stu-id="8b51f-118">FullDetails</span></span></td>
<td><span data-ttu-id="8b51f-119">Eigenschaften werden auf der Registerkarte <strong>Details</strong> des Dialogfelds <strong>Eigenschaften</strong> angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8b51f-119">Properties are displayed on the <strong>Details</strong> tab of the <strong>Properties</strong> dialog box.</span></span> <span data-ttu-id="8b51f-120">Dies ist die vollständige Liste der Eigenschaften, die vom Dateityp unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8b51f-120">This is the complete list of properties that the file type supports.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b51f-121">PreviewDetails</span><span class="sxs-lookup"><span data-stu-id="8b51f-121">PreviewDetails</span></span></td>
<td><span data-ttu-id="8b51f-122">Eigenschaften werden im <strong>Vorschaubereich</strong>angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8b51f-122">Properties are displayed in the <strong>Preview Pane</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b51f-123">PreviewTitle</span><span class="sxs-lookup"><span data-stu-id="8b51f-123">PreviewTitle</span></span></td>
<td><span data-ttu-id="8b51f-124">Eigenschaften werden im Titelbereich des <strong>Vorschaubereichs</strong> neben der Miniaturansicht für das Element angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8b51f-124">Properties are displayed in the title area of the <strong>Preview Pane</strong> next to the thumbnail for the item.</span></span> <span data-ttu-id="8b51f-125">Die maximale Anzahl von Einträgen beträgt 3.</span><span class="sxs-lookup"><span data-stu-id="8b51f-125">The maximum number of entries is 3.</span></span> <span data-ttu-id="8b51f-126">Wenn die Eigenschaftenliste mehr als die maximal zulässige Anzahl enthält, werden die restlichen Einträge ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8b51f-126">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b51f-127">TileInfo</span><span class="sxs-lookup"><span data-stu-id="8b51f-127">TileInfo</span></span></td>
<td><span data-ttu-id="8b51f-128">Eigenschaften werden angezeigt, wenn sich die Listenansicht im <strong>Ansichtsmodus Kacheln</strong> befindet.</span><span class="sxs-lookup"><span data-stu-id="8b51f-128">Properties are displayed when the list view is in <strong>Tiles</strong> view mode.</span></span> <span data-ttu-id="8b51f-129">Die maximale Anzahl von Einträgen beträgt 3.</span><span class="sxs-lookup"><span data-stu-id="8b51f-129">The maximum number of entries is 3.</span></span> <span data-ttu-id="8b51f-130">Wenn die Eigenschaftenliste mehr als die maximal zulässige Anzahl enthält, werden die restlichen Einträge ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8b51f-130">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8b51f-131">Dieser Wert war in Windows XP vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8b51f-131">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b51f-132">ExtendedTileInfo</span><span class="sxs-lookup"><span data-stu-id="8b51f-132">ExtendedTileInfo</span></span></td>
<td><span data-ttu-id="8b51f-133">Eigenschaften werden für ein Element angezeigt, <strong></strong> wenn sich die Listenansicht im Erweiterten Kachelansichtsmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="8b51f-133">Properties are displayed for an item when the list view is in <strong>Extended Tile</strong> view mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b51f-134">InfoTip</span><span class="sxs-lookup"><span data-stu-id="8b51f-134">InfoTip</span></span></td>
<td><span data-ttu-id="8b51f-135">Eigenschaften werden in einer Infotip angezeigt, wenn ein Benutzer auf ein Element zeigt.</span><span class="sxs-lookup"><span data-stu-id="8b51f-135">Properties are displayed in an infotip when a user hovers over an item.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8b51f-136">Dieser Wert war in Windows XP vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8b51f-136">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b51f-137">Quicktip</span><span class="sxs-lookup"><span data-stu-id="8b51f-137">QuickTip</span></span></td>
<td><span data-ttu-id="8b51f-138">Eigenschaften werden angezeigt, wenn es schwierig ist, Eigenschaften direkt aus einem Element abzurufen, z. B. wenn über eine langsame Netzwerkverbindung auf das Element zugegriffen werden muss.</span><span class="sxs-lookup"><span data-stu-id="8b51f-138">Properties are displayed when it is difficult to retrieve properties directly from an item, such as when the item must be accessed over a slow network connection.</span></span> <span data-ttu-id="8b51f-139">Es wird empfohlen, dass die hier benannten Eigenschaften wie Typ oder Größe nicht den Dateistream öffnen müssen, um ihren Wert zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8b51f-139">It is recommended that the properties named here, such as Type or Size, do not require opening the file stream to determine their value.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8b51f-140">Dieser Wert war in Windows XP vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8b51f-140">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8b51f-141">Im folgenden Beispiel wird der PreviewDetails-Wert für einen Rezeptdateityp mithilfe einer ProgID von **RecipeKey** definiert.</span><span class="sxs-lookup"><span data-stu-id="8b51f-141">The example below defines the PreviewDetails value for a .recipe file type, using a ProgID of **RecipeKey**.</span></span>

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

<span data-ttu-id="8b51f-142">Wie im Thema [Shell-Dateizuordnung](../shell/fa-file-types.md) erläutert, können Dateizuordnungen für die spezifischste für die allgemeinste Form beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8b51f-142">As explained in the [Shell file association](../shell/fa-file-types.md) topic, file associations can be described for the most specific to the most general form.</span></span> <span data-ttu-id="8b51f-143">Das spezifischste Formular ist die Erweiterung mit einem einzelnen Dateinamen, und das allgemeinste Formular ist ein Schlüssel, der für alle Dateien und Dateiordner gilt.</span><span class="sxs-lookup"><span data-stu-id="8b51f-143">The most specific form is the single file name extension and the most generic form is a key that applies to all files and file folders.</span></span> <span data-ttu-id="8b51f-144">Zwischen diesen beiden Extremen können Sie auch eine [PROGID](../shell/fa-progids.md) definieren, die einen Satz von Dateinamenerweiterungen gruppiert (z. B. .jpg- und JPEG-Typen, die als **jpegfile** gruppiert sind).</span><span class="sxs-lookup"><span data-stu-id="8b51f-144">Between those two extremes, you can also define a [PROGID](../shell/fa-progids.md) that groups a set of file name extensions together (for instance, .jpg and .jpeg types grouped as **jpegfile**).</span></span> <span data-ttu-id="8b51f-145">Wenn Sie Eigenschaftenlisten definieren, sollten Sie diese für ProgIDs oder in einigen Fällen bestimmte Dateinamenerweiterungen definieren.</span><span class="sxs-lookup"><span data-stu-id="8b51f-145">When you define property lists, you should define them for ProgIDs or, in some cases, specific file name extensions.</span></span> <span data-ttu-id="8b51f-146">Vermeiden Sie es, sich auf allgemeine Einträge wie den **AllFileSystemObjects-Schlüssel** zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="8b51f-146">Avoid relying on broad entries such as the **AllFileSystemObjects** key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b51f-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8b51f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b51f-148">Grundlegendes zu Eigenschaftenhandlern</span><span class="sxs-lookup"><span data-stu-id="8b51f-148">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="8b51f-149">Verwenden von Kind-Namen</span><span class="sxs-lookup"><span data-stu-id="8b51f-149">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="8b51f-150">Initialisieren von Eigenschaftenhandlern</span><span class="sxs-lookup"><span data-stu-id="8b51f-150">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="8b51f-151">Registrieren und Verteilen von Eigenschaftenhandlern</span><span class="sxs-lookup"><span data-stu-id="8b51f-151">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="8b51f-152">Bewährte Methoden und häufig gestellte Fragen zu Eigenschaftenhandlern</span><span class="sxs-lookup"><span data-stu-id="8b51f-152">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
