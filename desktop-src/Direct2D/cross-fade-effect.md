---
title: Cross-Fade-Effekt
description: Dieser Effekt kombiniert zwei Bilder, indem gewichtete Pixel aus Eingabe Bildern hinzugefügt werden. Sie verfügt über zwei Eingaben, die als Ziel und Quelle bezeichnet werden.
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517729"
---
# <a name="cross-fade-effect"></a><span data-ttu-id="382b7-104">Cross-Fade-Effekt</span><span class="sxs-lookup"><span data-stu-id="382b7-104">Cross-fade effect</span></span>

<span data-ttu-id="382b7-105">Dieser Effekt kombiniert zwei Bilder, indem gewichtete Pixel aus Eingabe Bildern hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="382b7-105">This effect combines two images by adding weighted pixels from input images.</span></span> <span data-ttu-id="382b7-106">Sie verfügt über zwei Eingaben, die als Ziel und Quelle bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="382b7-106">It has two inputs, named Destination and Source.</span></span>

<span data-ttu-id="382b7-107">Die Cross-Fade-Formel lautet **Output = Weight \* Destination + (1-Weight) \* Source**.</span><span class="sxs-lookup"><span data-stu-id="382b7-107">The cross fade formula is **output = weight \* Destination + (1 - weight) \* Source**.</span></span>

<span data-ttu-id="382b7-108">Die CLSID für diesen Effekt ist CLSID \_ D2D1CrossFade.</span><span class="sxs-lookup"><span data-stu-id="382b7-108">The CLSID for this effect is CLSID\_D2D1CrossFade.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="382b7-109">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="382b7-109">Effect properties</span></span>

| <span data-ttu-id="382b7-110">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="382b7-110">Display name and index enumeration</span></span>             | <span data-ttu-id="382b7-111">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="382b7-111">Type and default value</span></span> | <span data-ttu-id="382b7-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="382b7-112">Description</span></span>                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="382b7-113">WeightD2D1 \_ Crossfade- \_ Prop- \_ Gewichtung</span><span class="sxs-lookup"><span data-stu-id="382b7-113">WeightD2D1\_CROSSFADE\_PROP\_WEIGHT</span></span><br/> | <span data-ttu-id="382b7-114">Float 0,5 f</span><span class="sxs-lookup"><span data-stu-id="382b7-114">FLOAT0.5f</span></span><br/>   | <span data-ttu-id="382b7-115">Gibt an, wie viel die Farbwerte des Quell Bilds im Vergleich zum Zielbild abgewogen werden.</span><span class="sxs-lookup"><span data-stu-id="382b7-115">How much to weigh the source image color values versus the destination image.</span></span> <span data-ttu-id="382b7-116">Der Minimalwert ist 0,0 f (verwendet ausschließlich das Zielbild, um die Ausgabe zu bestimmen), und der Höchstwert ist 1.0 f (verwendet ausschließlich das Quell Image zum Ermitteln der Ausgabe).</span><span class="sxs-lookup"><span data-stu-id="382b7-116">The minimum value is 0.0f (exclusively use the destination image to determine the output) and the maximum value is 1.0f (exclusively use the source image to determine the output).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="382b7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="382b7-117">Requirements</span></span>



| <span data-ttu-id="382b7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="382b7-118">Requirement</span></span> | <span data-ttu-id="382b7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="382b7-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="382b7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="382b7-120">Minimum supported client</span></span> | <span data-ttu-id="382b7-121">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="382b7-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="382b7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="382b7-122">Minimum supported server</span></span> | <span data-ttu-id="382b7-123">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="382b7-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="382b7-124">Header</span><span class="sxs-lookup"><span data-stu-id="382b7-124">Header</span></span>                   | <span data-ttu-id="382b7-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="382b7-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="382b7-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="382b7-126">Library</span></span>                  | <span data-ttu-id="382b7-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="382b7-127">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="382b7-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="382b7-128">Related topics</span></span>

* [<span data-ttu-id="382b7-129">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="382b7-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
