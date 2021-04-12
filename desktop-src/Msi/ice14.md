---
description: ICE14 überprüft die Funktions Tabelle einer Windows Installer Datenbank.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2e64a6106ae359fe02c6ead271bbae267eeb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346328"
---
# <a name="ice14"></a><span data-ttu-id="8decf-103">ICE14</span><span class="sxs-lookup"><span data-stu-id="8decf-103">ICE14</span></span>

<span data-ttu-id="8decf-104">ICE14 überprüft Folgendes für die Features:</span><span class="sxs-lookup"><span data-stu-id="8decf-104">ICE14 validates the following for features:</span></span>

-   <span data-ttu-id="8decf-105">Für diese übergeordneten Stamm Funktionen ist das msidbfeatureattributesfollowparent-Bit nicht in der Attribute-Spalte der [Funktions Tabelle](feature-table.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8decf-105">That root parent features do not have the msidbFeatureAttributesFollowParent bit set in the Attributes column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="8decf-106">Eine Stamm Funktion verfügt über kein übergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="8decf-106">A root feature does not have a parent.</span></span>
-   <span data-ttu-id="8decf-107">Diese Funktion enthält nicht denselben Eintrag in den \_ übergeordneten Spalten des Features und Features der [Funktions Tabelle](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8decf-107">That no feature has the same entry in the Feature and Feature\_Parent columns of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="8decf-108">Keine Funktion kann ein eigenes übergeordnetes Element sein.</span><span class="sxs-lookup"><span data-stu-id="8decf-108">No feature can be its own parent.</span></span>

## <a name="result"></a><span data-ttu-id="8decf-109">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="8decf-109">Result</span></span>

<span data-ttu-id="8decf-110">ICE14 gibt eine Fehlermeldung aus, wenn eine Funktion mit dem msidbfeatureattributesfollowparent-Bit festgelegt wurde, oder eine Funktion mit identischen Einträgen in den übergeordneten Spalten der Funktion und der Funktion \_ der Featuretabelle.</span><span class="sxs-lookup"><span data-stu-id="8decf-110">ICE14 posts an error message if it finds a root feature with the msidbFeatureAttributesFollowParent bit set or a feature with identical entries in the Feature and Feature\_Parent columns of the Feature table.</span></span>

## <a name="example"></a><span data-ttu-id="8decf-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8decf-111">Example</span></span>

<span data-ttu-id="8decf-112">ICE14 gibt die folgenden Fehler für das folgende Beispiel zurück:</span><span class="sxs-lookup"><span data-stu-id="8decf-112">ICE14 would return the following errors for the following example:</span></span>

-   <span data-ttu-id="8decf-113">Die Funktion "Sport" hat denselben Wert in den übergeordneten Spalten der Funktion und des Features der \_ Dateitabelle.</span><span class="sxs-lookup"><span data-stu-id="8decf-113">The feature Sport has the same value in the Feature and Feature\_Parent columns of the File table.</span></span>
-   <span data-ttu-id="8decf-114">Das "msidbfeatureattributesfollowparent"-Bit ist für die Hauptfunktion "Sport" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8decf-114">The root feature Sport has the msidbFeatureAttributesFollowParent bit set.</span></span>

<span data-ttu-id="8decf-115">In der Funktionsstruktur dieses Beispiels ist Sport das Stamm Feature und ein übergeordnetes Element der Features "Swimming" und "Football".</span><span class="sxs-lookup"><span data-stu-id="8decf-115">In the feature tree of this example, Sport is the root feature and a parent of the Swimming and Football features.</span></span> <span data-ttu-id="8decf-116">Freestyle ist ein untergeordnetes Feature von Swimming.</span><span class="sxs-lookup"><span data-stu-id="8decf-116">Freestyle is a child feature of Swimming.</span></span> <span data-ttu-id="8decf-117">Touchfootball ist ein untergeordnetes Feature von Fußball.</span><span class="sxs-lookup"><span data-stu-id="8decf-117">TouchFootball is a child feature of Football.</span></span>

<span data-ttu-id="8decf-118">[Funktions Tabelle](feature-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="8decf-118">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="8decf-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="8decf-119">Feature</span></span>       | <span data-ttu-id="8decf-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="8decf-120">Attributes</span></span> | <span data-ttu-id="8decf-121">Über \_ geordnetes Element</span><span class="sxs-lookup"><span data-stu-id="8decf-121">Feature\_Parent</span></span> |
|---------------|------------|-----------------|
| <span data-ttu-id="8decf-122">Sport</span><span class="sxs-lookup"><span data-stu-id="8decf-122">Sport</span></span>         | <span data-ttu-id="8decf-123">4</span><span class="sxs-lookup"><span data-stu-id="8decf-123">4</span></span>          | <span data-ttu-id="8decf-124">Sport</span><span class="sxs-lookup"><span data-stu-id="8decf-124">Sport</span></span>           |
| <span data-ttu-id="8decf-125">Innenpool</span><span class="sxs-lookup"><span data-stu-id="8decf-125">Swimming</span></span>      | <span data-ttu-id="8decf-126">1</span><span class="sxs-lookup"><span data-stu-id="8decf-126">1</span></span>          | <span data-ttu-id="8decf-127">Sport</span><span class="sxs-lookup"><span data-stu-id="8decf-127">Sport</span></span>           |
| <span data-ttu-id="8decf-128">Verbandes</span><span class="sxs-lookup"><span data-stu-id="8decf-128">Football</span></span>      | <span data-ttu-id="8decf-129">4</span><span class="sxs-lookup"><span data-stu-id="8decf-129">4</span></span>          | <span data-ttu-id="8decf-130">Sport</span><span class="sxs-lookup"><span data-stu-id="8decf-130">Sport</span></span>           |
| <span data-ttu-id="8decf-131">Frei</span><span class="sxs-lookup"><span data-stu-id="8decf-131">Freestyle</span></span>     | <span data-ttu-id="8decf-132">1</span><span class="sxs-lookup"><span data-stu-id="8decf-132">1</span></span>          | <span data-ttu-id="8decf-133">Innenpool</span><span class="sxs-lookup"><span data-stu-id="8decf-133">Swimming</span></span>        |
| <span data-ttu-id="8decf-134">Touchfootball</span><span class="sxs-lookup"><span data-stu-id="8decf-134">TouchFootball</span></span> | <span data-ttu-id="8decf-135">4</span><span class="sxs-lookup"><span data-stu-id="8decf-135">4</span></span>          | <span data-ttu-id="8decf-136">Verbandes</span><span class="sxs-lookup"><span data-stu-id="8decf-136">Football</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8decf-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8decf-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8decf-138">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="8decf-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



