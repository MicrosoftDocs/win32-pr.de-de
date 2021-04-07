---
description: Alpha Setter-Effekt
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Alpha Setter-Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746369"
---
# <a name="alpha-setter-effect"></a><span data-ttu-id="47a2f-103">Alpha Setter-Effekt</span><span class="sxs-lookup"><span data-stu-id="47a2f-103">Alpha Setter Effect</span></span>

> [!Note]  
> <span data-ttu-id="47a2f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="47a2f-104">\[Deprecated.</span></span> <span data-ttu-id="47a2f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="47a2f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="47a2f-106">Der Alpha Setter-Effekt legt die Alpha Bits eines Video Bilds fest.</span><span class="sxs-lookup"><span data-stu-id="47a2f-106">The Alpha Setter effect sets the alpha bits on a video image.</span></span>

<span data-ttu-id="47a2f-107">Klassen-ID (CLSID): {506d89ae-909a-44f 7-9444-abd575896e35}</span><span class="sxs-lookup"><span data-stu-id="47a2f-107">Class ID (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}</span></span>

<span data-ttu-id="47a2f-108">CLSID-Variablen Name: CLSID \_ dxtalphasetter</span><span class="sxs-lookup"><span data-stu-id="47a2f-108">CLSID Variable Name: CLSID\_DxtAlphaSetter</span></span>

<span data-ttu-id="47a2f-109">Anzeige Name: "dxtalphasetter"</span><span class="sxs-lookup"><span data-stu-id="47a2f-109">Friendly Name: "DxtAlphaSetter"</span></span>

### <a name="properties"></a><span data-ttu-id="47a2f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47a2f-110">Properties</span></span>



| <span data-ttu-id="47a2f-111">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="47a2f-111">Property</span></span>  | <span data-ttu-id="47a2f-112">type</span><span class="sxs-lookup"><span data-stu-id="47a2f-112">Type</span></span>   | <span data-ttu-id="47a2f-113">Standard</span><span class="sxs-lookup"><span data-stu-id="47a2f-113">Default</span></span> | <span data-ttu-id="47a2f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47a2f-114">Description</span></span>                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| <span data-ttu-id="47a2f-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="47a2f-115">Alpha</span></span>     | <span data-ttu-id="47a2f-116">BYTE</span><span class="sxs-lookup"><span data-stu-id="47a2f-116">BYTE</span></span>   | <span data-ttu-id="47a2f-117">-1</span><span class="sxs-lookup"><span data-stu-id="47a2f-117">-1</span></span>      | <span data-ttu-id="47a2f-118">Legt das Alpha für das gesamte Bild fest.</span><span class="sxs-lookup"><span data-stu-id="47a2f-118">Sets the alpha for the entire image.</span></span>                        |
| <span data-ttu-id="47a2f-119">Alpharamp</span><span class="sxs-lookup"><span data-stu-id="47a2f-119">AlphaRamp</span></span> | <span data-ttu-id="47a2f-120">double</span><span class="sxs-lookup"><span data-stu-id="47a2f-120">double</span></span> | <span data-ttu-id="47a2f-121">-1.0</span><span class="sxs-lookup"><span data-stu-id="47a2f-121">-1.0</span></span>    | <span data-ttu-id="47a2f-122">Legt das Alpha als Prozentsatz des ursprünglichen Alpha Werts fest.</span><span class="sxs-lookup"><span data-stu-id="47a2f-122">Sets the alpha as a percentage of the original alpha value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="47a2f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47a2f-123">Remarks</span></span>

<span data-ttu-id="47a2f-124">Eine Eigenschaft mit einem negativen Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="47a2f-124">A property with a negative value is ignored.</span></span> <span data-ttu-id="47a2f-125">Nur eine Eigenschaft kann einen nicht negativen Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="47a2f-125">Only one property can have a non-negative value.</span></span> <span data-ttu-id="47a2f-126">Die Alpha-Eigenschaft gibt einen konstanten Alpha Wert für jedes Pixel im Bild an.</span><span class="sxs-lookup"><span data-stu-id="47a2f-126">The Alpha property specifies a constant alpha value for every pixel in the image.</span></span> <span data-ttu-id="47a2f-127">Diese Eigenschaft überschreibt die Alpha Werte aus dem ursprünglichen Bild.</span><span class="sxs-lookup"><span data-stu-id="47a2f-127">This property overwrites the alpha values from the original image.</span></span> <span data-ttu-id="47a2f-128">Die alpharamp-Eigenschaft gibt den Alpha Wert jedes Pixels als Prozentsatz des ursprünglichen Werts des Pixels an, von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="47a2f-128">The AlphaRamp property specifies each pixel's alpha value as a percentage of the pixel's original value, from 0.0 to 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47a2f-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47a2f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47a2f-130">Alpha Blending</span><span class="sxs-lookup"><span data-stu-id="47a2f-130">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



