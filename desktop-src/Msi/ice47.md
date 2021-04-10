---
description: ICE47 überprüft die Funktions-und FeatureComponents-Tabellen auf Features mit 1600 oder mehr Komponenten.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa04c2df52571f56612242d2dc7da8b5a91647c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215912"
---
# <a name="ice47"></a><span data-ttu-id="1ea53-103">ICE47</span><span class="sxs-lookup"><span data-stu-id="1ea53-103">ICE47</span></span>

<span data-ttu-id="1ea53-104">ICE47 überprüft die [Funktions](feature-table.md) -und [FeatureComponents](featurecomponents-table.md) -Tabellen auf Features mit 1600 oder mehr Komponenten.</span><span class="sxs-lookup"><span data-stu-id="1ea53-104">ICE47 checks the [Feature](feature-table.md) and [FeatureComponents](featurecomponents-table.md) tables for features with 1600 or more components.</span></span>

## <a name="result"></a><span data-ttu-id="1ea53-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="1ea53-105">Result</span></span>

<span data-ttu-id="1ea53-106">ICE47 gibt eine Fehlermeldung aus, wenn eine Funktion den maximalen Grenzwert von 1600 Komponenten pro Feature überschreitet.</span><span class="sxs-lookup"><span data-stu-id="1ea53-106">ICE47 posts an error message if a feature exceeds the maximum limit of 1600 components per feature.</span></span>

## <a name="example"></a><span data-ttu-id="1ea53-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1ea53-107">Example</span></span>

<span data-ttu-id="1ea53-108">ICE47 würde die folgende Warnung melden:</span><span class="sxs-lookup"><span data-stu-id="1ea53-108">ICE47 would report the following warning:</span></span>

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

<span data-ttu-id="1ea53-109">[Funktions Tabelle](feature-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="1ea53-109">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="1ea53-110">Funktion</span><span class="sxs-lookup"><span data-stu-id="1ea53-110">Feature</span></span>  |
|----------|
| <span data-ttu-id="1ea53-111">Feature1</span><span class="sxs-lookup"><span data-stu-id="1ea53-111">Feature1</span></span> |



 

<span data-ttu-id="1ea53-112">[FeatureComponents-Tabelle](featurecomponents-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="1ea53-112">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="1ea53-113">Aktion</span><span class="sxs-lookup"><span data-stu-id="1ea53-113">Action</span></span>   | <span data-ttu-id="1ea53-114">Bedingung</span><span class="sxs-lookup"><span data-stu-id="1ea53-114">Condition</span></span>     |
|----------|---------------|
| <span data-ttu-id="1ea53-115">Feature1</span><span class="sxs-lookup"><span data-stu-id="1ea53-115">Feature1</span></span> | <span data-ttu-id="1ea53-116">Component1</span><span class="sxs-lookup"><span data-stu-id="1ea53-116">Component1</span></span>    |
| <span data-ttu-id="1ea53-117">Feature1</span><span class="sxs-lookup"><span data-stu-id="1ea53-117">Feature1</span></span> | <span data-ttu-id="1ea53-118">Component1600</span><span class="sxs-lookup"><span data-stu-id="1ea53-118">Component1600</span></span> |



 

<span data-ttu-id="1ea53-119">Um diese Warnung zu beheben, teilen Sie die Funktion in mehrere Funktionen auf.</span><span class="sxs-lookup"><span data-stu-id="1ea53-119">To fix this warning, try splitting the feature into several features</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ea53-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ea53-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ea53-121">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="1ea53-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



