---
description: Das Eigenschaften System enthält eine Eigenschaft mit dem Namen System. Kind, die Elemente entsprechend der Dateinamenerweiterung in Typen unterteilt und die Endbenutzer leicht mit identifizieren können.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Verwenden von Kind-Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f358306deaeb04d4ea30b10b0665cdc8323b4d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344818"
---
# <a name="using-kind-names"></a><span data-ttu-id="68690-103">Verwenden von Kind-Namen</span><span class="sxs-lookup"><span data-stu-id="68690-103">Using Kind Names</span></span>

<span data-ttu-id="68690-104">Das-Eigenschaften System enthält eine Eigenschaft mit dem Namen `System.Kind` , die Elemente entsprechend der Dateinamenerweiterung in Typen unterteilt und die Endbenutzer leicht mit identifizieren können.</span><span class="sxs-lookup"><span data-stu-id="68690-104">The property system contains a property called `System.Kind`, which divides items into types according to the file name extension, and which end users can easily identify with.</span></span>

<span data-ttu-id="68690-105">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="68690-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="68690-106">Informationen zur System. Kind-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="68690-106">About the System.Kind Property</span></span>](#about-the-systemkind-property)
-   [<span data-ttu-id="68690-107">Kind-Wert Hierarchie und Registrierung</span><span class="sxs-lookup"><span data-stu-id="68690-107">Kind Value Hierarchy and Registration</span></span>](#kind-value-hierarchy-and-registration)
-   [<span data-ttu-id="68690-108">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="68690-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="68690-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="68690-109">Related topics</span></span>](#related-topics)

## <a name="about-the-systemkind-property"></a><span data-ttu-id="68690-110">Informationen zur System. Kind-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="68690-110">About the System.Kind Property</span></span>

<span data-ttu-id="68690-111">Art wurde in Windows Vista eingeführt, um einen benutzerfreundlicheren Begriff "Dateityp" auszudrücken.</span><span class="sxs-lookup"><span data-stu-id="68690-111">Kind was introduced in Windows Vista to express a more user-friendly notion of file type.</span></span> <span data-ttu-id="68690-112">Die `System.Kind` -Eigenschaft teilt Elemente in Typen auf und gibt einen Namen an, mit dem Endbenutzer identifizieren können (z. b. Dokumente, Musik, Bilder usw.).</span><span class="sxs-lookup"><span data-stu-id="68690-112">The `System.Kind` property divides items into types and provides a Kind name that end users can identify with, such as Documents, Music, Pictures, and so forth.</span></span> <span data-ttu-id="68690-113">Daher sind Kind-Namen als benutzerfreundlich bekannt.</span><span class="sxs-lookup"><span data-stu-id="68690-113">Hence, Kind names have come to be known as user-friendly.</span></span> <span data-ttu-id="68690-114">Da die `System.Kind` -Eigenschaft auf denselben Wert für Elemente desselben Dateityps festgelegt ist und Elemente, die ähnliche Merkmale aufweisen, mit einer gemeinsamen Eigenschaft verknüpft werden, können das System und der Benutzer für die Gruppe als Ganzes agieren.</span><span class="sxs-lookup"><span data-stu-id="68690-114">Because the `System.Kind` property is set to the same value for items of the same file type, and associates items that have similar characteristics with a common property, the system and the user can act on the group as a whole.</span></span> <span data-ttu-id="68690-115">Beispielsweise kann die- `System.Kind` Eigenschaft verwendet werden, um eine Suche auf Elemente einer bestimmten Art zu beschränken, die relevantesten Eigenschaften für ein Element in der Inhaltsansicht anzuzeigen oder ähnliche Elemente zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="68690-115">For example, the `System.Kind` property can be used to limit a search to items of a specific kind, display the most relevant properties for an item in the Content view, or group similar items together.</span></span>

<span data-ttu-id="68690-116">Da Kind eine mehrwertige Zeichen folgen Eigenschaft ist, können Sie einen- `audio;video` Wert oder einen- `link;document` Wert haben.</span><span class="sxs-lookup"><span data-stu-id="68690-116">Because Kind is a multi-value string property, you can have an `audio;video` or `link;document` Kind value.</span></span> <span data-ttu-id="68690-117">Ein- `System.Kind` Wert ist eine geordnete Liste von Zeichen folgen Werten.</span><span class="sxs-lookup"><span data-stu-id="68690-117">A `System.Kind` values is an ordered list of string values.</span></span> <span data-ttu-id="68690-118">In einigen Fällen gibt es möglicherweise nur ein Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="68690-118">In some cases, there might be only one element in that list.</span></span> <span data-ttu-id="68690-119">In anderen Fällen kann ein Element zu mehr als einer Art gehören.</span><span class="sxs-lookup"><span data-stu-id="68690-119">In other cases, an item can belong to more than one Kind.</span></span> <span data-ttu-id="68690-120">Ein Beispiel für ein Element, das zu mehr als einer Art gehört, finden Sie im Beispiel für den Registrierungsschlüssel in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="68690-120">For an example of an item that belongs to more than one Kind, see the registry key example in this topic.</span></span> <span data-ttu-id="68690-121">Die Zeichen folgen Werte stammen aus einem vordefinierten Satz bekannter Werte.</span><span class="sxs-lookup"><span data-stu-id="68690-121">The string values are from a predefined set of known values.</span></span> <span data-ttu-id="68690-122">Die Werte werden mithilfe der Groß-/Kleinschreibung und der Gebiets Schema spezifischen Zeichen folgen Vergleichsfunktionen verglichen.</span><span class="sxs-lookup"><span data-stu-id="68690-122">The values are compared by using case-insensitive and locale-insensitive string-compare functions.</span></span> <span data-ttu-id="68690-123">Diese Zeichen folgen sind nicht lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="68690-123">These strings are not localized.</span></span>

<span data-ttu-id="68690-124">Einige Arten von Namen sind bereits Eigenschaften und layoutmustern zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="68690-124">Some Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="68690-125">Beispielsweise werden Elementen, `Kind.Picture` die mit-und-Elementen verknüpft sind, die mit verknüpft sind `Kind.Document` , andere Eigenschaften angezeigt, auch wenn Sie sich in derselben Ansicht befinden, aufgrund der Eigenschaften und Layoutmuster, die diesen beiden Namen bereits zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="68690-125">For example, items associated with `Kind.Picture` and items associated with `Kind.Document` display different properties even when they are in the same view, because of the properties and layout patterns that are already associated with those two Kind names.</span></span> <span data-ttu-id="68690-126">Jede Elementart kann einem von vier eindeutigen layoutmustern zugeordnet werden, die die Anzahl der Eigenschaften definiert, die für jedes Element und dessen Layout angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="68690-126">Each item Kind can be associated with one of four unique layout patterns that defines the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="68690-127">Weitere Informationen finden Sie unter [Content View based on the file type or Kind Association](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="68690-127">For more information, see [Content View based on the File Type or Kind Association](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span></span>

## <a name="kind-value-hierarchy-and-registration"></a><span data-ttu-id="68690-128">Kind-Wert Hierarchie und Registrierung</span><span class="sxs-lookup"><span data-stu-id="68690-128">Kind Value Hierarchy and Registration</span></span>

<span data-ttu-id="68690-129">Ein `Kind` Wert muss einen der Werte in der folgenden Liste darstellen.</span><span class="sxs-lookup"><span data-stu-id="68690-129">A `Kind` value must represent one of the values in the following list.</span></span>

```
Item
   Folder
   Program
   Game
   WebHistory
   Feed
   Document
   Link
   Movie
   Music
   RecordedTV
   Video
   Picture
   Communications
      Calendar
      Contact
      E-Mail
      Task
      Journal
      Note
      InstantMessage
```

<span data-ttu-id="68690-130">Eigenschaften Handler können Ihre `System.Kind` Eigenschaft statisch über die Registrierung deklarieren, oder Sie können den Wert dynamisch über Ihren Code bereitstellen, wie dies bei einer Standard Eigenschaft der Fall wäre.</span><span class="sxs-lookup"><span data-stu-id="68690-130">Property handlers can declare their `System.Kind` property statically through the registry, or they can provide the value dynamically through their code as they would with a standard property.</span></span>

<span data-ttu-id="68690-131">Um die Eigenschaft statisch zu definieren `Kind` , wird unter dem **kindmap** -Registrierungsschlüssel ein **reg \_ SZ** -Wert Eintrag hinzugefügt, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="68690-131">To statically define the `Kind` property, a **REG\_SZ** value entry is added under the **KindMap** registry key as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     .recipe = Document
                     .ccc = Contact; Communications
```

<span data-ttu-id="68690-132">Beachten Sie, dass `Kind` ein einzelner Wert oder mehrere Werte in einer durch Semikolons getrennten Zeichenfolge sein kann.</span><span class="sxs-lookup"><span data-stu-id="68690-132">Note that the `Kind` can be a single value or multiple values in a semi-colon delimited string.</span></span> <span data-ttu-id="68690-133">Wenn Sie mehrere Werte angeben, wird der spezifischere `Kind` Wert zuerst mit dem am wenigsten spezifischen Wert aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="68690-133">When providing multiple values, the most specific `Kind` value is listed first with the least specific following.</span></span> <span data-ttu-id="68690-134">Im Beispiel wird "Contact" zuerst benannt, da es hierarchisch spezifischer als die Kommunikation ist.</span><span class="sxs-lookup"><span data-stu-id="68690-134">In the example, Contact is named first because it is hierarchically more specific than Communications.</span></span> <span data-ttu-id="68690-135">Das Wert **Element** wird angenommen und sollte nicht explizit explizit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="68690-135">The value **Item** is assumed and should not be explicity provided.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68690-136">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="68690-136">Additional Resources</span></span>

-   <span data-ttu-id="68690-137">Eine Referenz Dokumentation zu Eigenschaften finden Sie unter [System. Kind](./props-system-kind.md) und [System. kindtext](./props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="68690-137">For reference documentation about properties, see [System.Kind](./props-system-kind.md) and [System.KindText](./props-system-kindtext.md).</span></span>
-   <span data-ttu-id="68690-138">Weitere Informationen zum Erstellen neuer oder vorhandener Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="68690-138">For more information about creating new or using existing file types, see [File Types](../shell/fa-file-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="68690-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="68690-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68690-140">Grundlegendes zu Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="68690-140">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="68690-141">Verwenden von Eigenschaften Listen</span><span class="sxs-lookup"><span data-stu-id="68690-141">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="68690-142">Initialisieren von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="68690-142">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="68690-143">Registrieren und Verteilen von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="68690-143">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="68690-144">Bewährte Methoden und häufig gestellte Fragen zu Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="68690-144">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
