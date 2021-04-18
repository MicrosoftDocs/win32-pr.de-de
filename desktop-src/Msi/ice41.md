---
description: ICE41 überprüft, ob die Einträge in den Klassen-und Erweiterungs Tabellen auf Einträge in der Komponenten Tabelle verweisen, die das Klassenobjekt oder die Erweiterung der Komponente implementieren.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc6c0a8bb634706750810484963e56b6d6e0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359001"
---
# <a name="ice41"></a><span data-ttu-id="284b7-103">ICE41</span><span class="sxs-lookup"><span data-stu-id="284b7-103">ICE41</span></span>

<span data-ttu-id="284b7-104">ICE41 überprüft, ob die Einträge in den [Klassen](class-table.md) -und [Erweiterungs](extension-table.md) Tabellen auf Einträge in der [Komponenten Tabelle](component-table.md) verweisen, die das Klassenobjekt oder die Erweiterung der Komponente implementieren.</span><span class="sxs-lookup"><span data-stu-id="284b7-104">ICE41 validates that the entries in the [Class](class-table.md) and [Extension](extension-table.md) tables refer to entries in the [Component table](component-table.md) that implement the class object or extension of the component.</span></span>

## <a name="result"></a><span data-ttu-id="284b7-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="284b7-105">Result</span></span>

<span data-ttu-id="284b7-106">ICE41 gibt einen Fehler aus, wenn eine Funktion vorhanden ist, die nicht die Komponente enthält, die das Klassenobjekt oder die Erweiterung implementiert.</span><span class="sxs-lookup"><span data-stu-id="284b7-106">ICE41 posts an error if there is a feature that does not contain the component implementing the class object or extension.</span></span>

## <a name="example"></a><span data-ttu-id="284b7-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="284b7-107">Example</span></span>

<span data-ttu-id="284b7-108">ICE41 meldet die folgenden Fehler für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="284b7-108">ICE41 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="284b7-109">ICE41-Fehler</span><span class="sxs-lookup"><span data-stu-id="284b7-109">ICE41 error</span></span>                                                                                                                                                                                    | <span data-ttu-id="284b7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="284b7-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="284b7-111">Class {00000000-0000-0000-0000-0000000000000} References Feature Feature2 und Component Component1, aber die Komponente ist nicht mit dieser Funktion in der FeatureComponents-Tabelle verknüpft.</span><span class="sxs-lookup"><span data-stu-id="284b7-111">Class {00000000-0000-0000-0000-0000000000000} references feature Feature2 and component Component1, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span> | <span data-ttu-id="284b7-112">Es gibt eine Funktion, die nicht die Komponente enthält, die das Klassenobjekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="284b7-112">There is a feature that does not contain the component implementing the class object.</span></span> <span data-ttu-id="284b7-113">Dies bedeutet, dass das Installationsprogramm die Komponente nicht mit der Funktion installiert, und dass die Werbung möglicherweise nicht wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="284b7-113">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="284b7-114">Um diesen Fehler zu beheben, ändern Sie den Eintrag in der \_ featurespalte des [Klassen Tabellen](class-table.md) Eintrags, um auf eine Funktion zu verweisen, mit der die in der Spalte Komponente aufgeführte Komponente installiert wird, \_ oder ändern Sie die Funktion und die Komponente, die in der [FeatureComponents](featurecomponents-table.md)</span><span class="sxs-lookup"><span data-stu-id="284b7-114">To fix this error, change the entry in the Feature\_ column of the [Class table](class-table.md) entry to reference a feature that installs component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/>          |
| <span data-ttu-id="284b7-115">Die Erweiterung. Yip verweist auf die Features Feature1 und Component Component2, aber diese Komponente ist nicht mit dieser Funktion in der FeatureComponents-Tabelle verknüpft.</span><span class="sxs-lookup"><span data-stu-id="284b7-115">Extension .yip references feature Feature1 and component Component2, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span>                                | <span data-ttu-id="284b7-116">Es gibt eine Funktion, die nicht die Komponente enthält, die die Erweiterung implementiert.</span><span class="sxs-lookup"><span data-stu-id="284b7-116">There is a feature that does not contain the component implementing the extension.</span></span> <span data-ttu-id="284b7-117">Dies bedeutet, dass das Installationsprogramm die Komponente nicht mit der Funktion installiert, und dass die Werbung möglicherweise nicht wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="284b7-117">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="284b7-118">Um diesen Fehler zu beheben, ändern Sie den Eintrag in der \_ featurespalte des [Erweiterungs Tabellen](extension-table.md) Eintrags, um auf eine Funktion zu verweisen, mit der die in der Spalte Komponente aufgeführte Komponente installiert wird, \_ oder ändern Sie die Funktion und die Komponente, die in der [Tabelle FeatureComponents](featurecomponents-table.md)</span><span class="sxs-lookup"><span data-stu-id="284b7-118">To fix this error, change the entry in the Feature\_ column of the [Extension table](extension-table.md) entry to reference a feature that installs the component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/> |



 

<span data-ttu-id="284b7-119">[FeatureComponents-Tabelle](featurecomponents-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="284b7-119">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="284b7-120">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="284b7-120">Feature\_</span></span> |
|-----------|
| <span data-ttu-id="284b7-121">Feature1</span><span class="sxs-lookup"><span data-stu-id="284b7-121">Feature1</span></span>  |
| <span data-ttu-id="284b7-122">Feature2</span><span class="sxs-lookup"><span data-stu-id="284b7-122">Feature2</span></span>  |



 

<span data-ttu-id="284b7-123">[Klassen Tabelle](class-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="284b7-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="284b7-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="284b7-124">CLSID</span></span>                                  | <span data-ttu-id="284b7-125">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="284b7-125">Component\_</span></span> | <span data-ttu-id="284b7-126">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="284b7-126">Feature\_</span></span> |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | <span data-ttu-id="284b7-127">Component1</span><span class="sxs-lookup"><span data-stu-id="284b7-127">Component1</span></span>  | <span data-ttu-id="284b7-128">Feature2</span><span class="sxs-lookup"><span data-stu-id="284b7-128">Feature2</span></span>  |



 

<span data-ttu-id="284b7-129">[Klassen Tabelle](class-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="284b7-129">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="284b7-130">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="284b7-130">Extension</span></span> | <span data-ttu-id="284b7-131">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="284b7-131">Component\_</span></span> | <span data-ttu-id="284b7-132">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="284b7-132">Feature\_</span></span> |
|-----------|-------------|-----------|
| <span data-ttu-id="284b7-133">. Yip</span><span class="sxs-lookup"><span data-stu-id="284b7-133">.yip</span></span>      | <span data-ttu-id="284b7-134">Component2</span><span class="sxs-lookup"><span data-stu-id="284b7-134">Component2</span></span>  | <span data-ttu-id="284b7-135">Feature1</span><span class="sxs-lookup"><span data-stu-id="284b7-135">Feature1</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="284b7-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="284b7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="284b7-137">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="284b7-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




