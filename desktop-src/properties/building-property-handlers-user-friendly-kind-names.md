---
description: Das Eigenschaftensystem enthält eine Eigenschaft namens System.Kind, die Elemente entsprechend der Dateinamenerweiterung in Typen aufteilt und mit der Endbenutzer leicht identifizieren können.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Verwenden von Kind-Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca36d7c1de587efd8d96f0c18aaca9457721714
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481875"
---
# <a name="using-kind-names"></a><span data-ttu-id="b7697-103">Verwenden von Kind-Namen</span><span class="sxs-lookup"><span data-stu-id="b7697-103">Using Kind Names</span></span>

<span data-ttu-id="b7697-104">Das Eigenschaftensystem enthält eine Eigenschaft namens `System.Kind` , die Elemente entsprechend der Dateinamenerweiterung in Typen aufteilt und mit der sich Endbenutzer leicht identifizieren können.</span><span class="sxs-lookup"><span data-stu-id="b7697-104">The property system contains a property called `System.Kind`, which divides items into types according to the file name extension, and which end users can easily identify with.</span></span>

<span data-ttu-id="b7697-105">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="b7697-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="b7697-106">Informationen zur System.Kind-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b7697-106">About the System.Kind Property</span></span>](#about-the-systemkind-property)
-   [<span data-ttu-id="b7697-107">Hierarchie und Registrierung von Kind-Werten</span><span class="sxs-lookup"><span data-stu-id="b7697-107">Kind Value Hierarchy and Registration</span></span>](#kind-value-hierarchy-and-registration)
-   [<span data-ttu-id="b7697-108">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b7697-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="b7697-109">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b7697-109">Related topics</span></span>](#related-topics)

## <a name="about-the-systemkind-property"></a><span data-ttu-id="b7697-110">Informationen zur System.Kind-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b7697-110">About the System.Kind Property</span></span>

<span data-ttu-id="b7697-111">Kind wurde in Windows Vista eingeführt, um ein benutzerfreundlicheres Konzept des Dateityps auszudrücken.</span><span class="sxs-lookup"><span data-stu-id="b7697-111">Kind was introduced in Windows Vista to express a more user-friendly notion of file type.</span></span> <span data-ttu-id="b7697-112">Die `System.Kind` -Eigenschaft unterteilt Elemente in Typen und stellt einen Kind-Namen bereit, mit dem Endbenutzer identifizieren können, z. B. Dokumente, Musik, Bilder usw.</span><span class="sxs-lookup"><span data-stu-id="b7697-112">The `System.Kind` property divides items into types and provides a Kind name that end users can identify with, such as Documents, Music, Pictures, and so forth.</span></span> <span data-ttu-id="b7697-113">Daher werden Kind-Namen als benutzerfreundliche Namen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b7697-113">Hence, Kind names have come to be known as user-friendly.</span></span> <span data-ttu-id="b7697-114">Da die `System.Kind` -Eigenschaft für Elemente desselben Dateityps auf den gleichen Wert festgelegt ist und Elemente mit ähnlichen Eigenschaften einer gemeinsamen Eigenschaft zuweist, können das System und der Benutzer für die gruppe als Ganzes agieren.</span><span class="sxs-lookup"><span data-stu-id="b7697-114">Because the `System.Kind` property is set to the same value for items of the same file type, and associates items that have similar characteristics with a common property, the system and the user can act on the group as a whole.</span></span> <span data-ttu-id="b7697-115">Beispielsweise kann die `System.Kind` -Eigenschaft verwendet werden, um eine Suche auf Elemente einer bestimmten Art zu beschränken, die relevantesten Eigenschaften für ein Element in der Inhaltsansicht anzuzeigen oder ähnliche Elemente zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="b7697-115">For example, the `System.Kind` property can be used to limit a search to items of a specific kind, display the most relevant properties for an item in the Content view, or group similar items together.</span></span>

<span data-ttu-id="b7697-116">Da Kind eine Zeichenfolgeneigenschaft mit mehreren Werten ist, können Sie über einen - oder einen `audio;video` `link;document` Kind-Wert verfügen.</span><span class="sxs-lookup"><span data-stu-id="b7697-116">Because Kind is a multi-value string property, you can have an `audio;video` or `link;document` Kind value.</span></span> <span data-ttu-id="b7697-117">Ein `System.Kind` Wert ist eine sortierte Liste von Zeichenfolgenwerten.</span><span class="sxs-lookup"><span data-stu-id="b7697-117">A `System.Kind` values is an ordered list of string values.</span></span> <span data-ttu-id="b7697-118">In einigen Fällen gibt es möglicherweise nur ein Element in dieser Liste.</span><span class="sxs-lookup"><span data-stu-id="b7697-118">In some cases, there might be only one element in that list.</span></span> <span data-ttu-id="b7697-119">In anderen Fällen kann ein Element zu mehreren Arten gehören.</span><span class="sxs-lookup"><span data-stu-id="b7697-119">In other cases, an item can belong to more than one Kind.</span></span> <span data-ttu-id="b7697-120">Ein Beispiel für ein Element, das zu mehreren Arten gehört, finden Sie im Registrierungsschlüsselbeispiel in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="b7697-120">For an example of an item that belongs to more than one Kind, see the registry key example in this topic.</span></span> <span data-ttu-id="b7697-121">Die Zeichenfolgenwerte stammen aus einem vordefinierten Satz bekannter Werte.</span><span class="sxs-lookup"><span data-stu-id="b7697-121">The string values are from a predefined set of known values.</span></span> <span data-ttu-id="b7697-122">Die Werte werden mithilfe von Zeichenfolgenvergleichsfunktionen ohne Unterscheidung nach Groß-/Kleinschreibung und gebietsschemaunabhängig verglichen.</span><span class="sxs-lookup"><span data-stu-id="b7697-122">The values are compared by using case-insensitive and locale-insensitive string-compare functions.</span></span> <span data-ttu-id="b7697-123">Diese Zeichenfolgen sind nicht lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="b7697-123">These strings are not localized.</span></span>

<span data-ttu-id="b7697-124">Einige Kind-Namen sind bereits Eigenschaften und Layoutmustern zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b7697-124">Some Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="b7697-125">Beispielsweise zeigen Elemente, die zugeordnet `Kind.Picture` sind, und Elemente, die zugeordnet `Kind.Document` sind, unterschiedliche Eigenschaften an, auch wenn sie sich in derselben Ansicht befinden. Dies liegt an den Eigenschaften und Layoutmustern, die diesen beiden Kind-Namen bereits zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b7697-125">For example, items associated with `Kind.Picture` and items associated with `Kind.Document` display different properties even when they are in the same view, because of the properties and layout patterns that are already associated with those two Kind names.</span></span> <span data-ttu-id="b7697-126">Jede Elementart kann einem von vier eindeutigen Layoutmustern zugeordnet werden, die die Anzahl der Eigenschaften definieren, die für jedes Element und dessen Layout angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b7697-126">Each item Kind can be associated with one of four unique layout patterns that defines the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="b7697-127">Weitere Informationen finden Sie unter [Inhaltsansicht basierend auf dem Dateityp oder der Art-Zuordnung.](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7697-127">For more information, see [Content View based on the File Type or Kind Association](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span></span>

## <a name="kind-value-hierarchy-and-registration"></a><span data-ttu-id="b7697-128">Hierarchie und Registrierung von Kind-Werten</span><span class="sxs-lookup"><span data-stu-id="b7697-128">Kind Value Hierarchy and Registration</span></span>

<span data-ttu-id="b7697-129">Ein `Kind` -Wert muss einen der Werte in der folgenden Liste darstellen.</span><span class="sxs-lookup"><span data-stu-id="b7697-129">A `Kind` value must represent one of the values in the following list.</span></span>

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

<span data-ttu-id="b7697-130">Eigenschaftenhandler können ihre `System.Kind` Eigenschaft statisch über die Registrierung deklarieren, oder sie können den Wert dynamisch über ihren Code bereitstellen, wie sie es mit einer Standardeigenschaft würden.</span><span class="sxs-lookup"><span data-stu-id="b7697-130">Property handlers can declare their `System.Kind` property statically through the registry, or they can provide the value dynamically through their code as they would with a standard property.</span></span>

<span data-ttu-id="b7697-131">Um die Eigenschaft statisch zu `Kind` definieren, wird ein **REG \_ SZ-Werteintrag** unter dem **KindMap-Registrierungsschlüssel** hinzugefügt, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7697-131">To statically define the `Kind` property, a **REG\_SZ** value entry is added under the **KindMap** registry key as shown in the following example.</span></span>

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

<span data-ttu-id="b7697-132">Beachten Sie, dass ein `Kind` einzelner Wert oder mehrere Werte in einer durch Semikolons getrennten Zeichenfolge sein können.</span><span class="sxs-lookup"><span data-stu-id="b7697-132">Note that the `Kind` can be a single value or multiple values in a semi-colon delimited string.</span></span> <span data-ttu-id="b7697-133">Wenn Sie mehrere Werte bereitstellen, wird der spezifischste `Kind` Wert zuerst mit dem am wenigsten spezifischen Wert aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7697-133">When providing multiple values, the most specific `Kind` value is listed first with the least specific following.</span></span> <span data-ttu-id="b7697-134">Im Beispiel wird Contact zuerst benannt, da er hierarchisch spezifischer als Communications ist.</span><span class="sxs-lookup"><span data-stu-id="b7697-134">In the example, Contact is named first because it is hierarchically more specific than Communications.</span></span> <span data-ttu-id="b7697-135">Der Wert **Item** wird angenommen und sollte nicht explizit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b7697-135">The value **Item** is assumed and should not be explicity provided.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7697-136">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b7697-136">Additional Resources</span></span>

-   <span data-ttu-id="b7697-137">Eine Referenzdokumentation zu Eigenschaften finden Sie unter [System.Kind](./props-system-kind.md) und [System.KindText.](./props-system-kindtext.md)</span><span class="sxs-lookup"><span data-stu-id="b7697-137">For reference documentation about properties, see [System.Kind](./props-system-kind.md) and [System.KindText](./props-system-kindtext.md).</span></span>
-   <span data-ttu-id="b7697-138">Weitere Informationen zum Erstellen neuer oder verwenden vorhandener Dateitypen finden Sie unter [Dateitypen.](../shell/fa-file-types.md)</span><span class="sxs-lookup"><span data-stu-id="b7697-138">For more information about creating new or using existing file types, see [File Types](../shell/fa-file-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7697-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b7697-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7697-140">Grundlegendes zu Eigenschaftenhandlern</span><span class="sxs-lookup"><span data-stu-id="b7697-140">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="b7697-141">Verwenden von Eigenschaftenlisten</span><span class="sxs-lookup"><span data-stu-id="b7697-141">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="b7697-142">Initialisieren von Eigenschaftenhandlern</span><span class="sxs-lookup"><span data-stu-id="b7697-142">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="b7697-143">Registrieren und Verteilen von Eigenschaftenhandlern</span><span class="sxs-lookup"><span data-stu-id="b7697-143">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="b7697-144">Bewährte Methoden und häufig gestellte Fragen zu Eigenschaftenhandlern</span><span class="sxs-lookup"><span data-stu-id="b7697-144">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
