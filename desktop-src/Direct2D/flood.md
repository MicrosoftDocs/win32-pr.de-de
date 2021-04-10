---
title: Überflutungseffekt
description: Verwenden Sie den überflutungseffekt, um eine Bitmap basierend auf der angegebenen Farbe und dem angegebenen Alpha Wert zu generieren. Sie können diesen Effekt verwenden, wenn Sie eine bestimmte Farbe als Eingabe für einen Effekt verwenden möchten, z. b. eine Hintergrundfarbe.
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- überflutungseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956851"
---
# <a name="flood-effect"></a><span data-ttu-id="b70d5-105">Überflutungseffekt</span><span class="sxs-lookup"><span data-stu-id="b70d5-105">Flood effect</span></span>

<span data-ttu-id="b70d5-106">Verwenden Sie den überflutungseffekt, um eine Bitmap basierend auf der angegebenen Farbe und dem angegebenen Alpha Wert zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b70d5-106">Use the flood effect to generate a bitmap based on the specified color and alpha value.</span></span> <span data-ttu-id="b70d5-107">Sie können diesen Effekt verwenden, wenn Sie eine bestimmte Farbe als Eingabe für einen Effekt verwenden möchten, z. b. eine Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="b70d5-107">You can use this effect when you want a specific color as an input for an effect, like a background color.</span></span>

> [!Note]  
> <span data-ttu-id="b70d5-108">Der Effekt wird an den angegebenen Farbwert weitergeleitet, wie angegeben.</span><span class="sxs-lookup"><span data-stu-id="b70d5-108">The effect passes along the specified color value as specified.</span></span> <span data-ttu-id="b70d5-109">Sie müssen die Werte manuell vorab multiplizieren, wenn Sie beabsichtigen, die Ausgabe an Effekte zu übergeben, die eine vorab multiplizierte Eingabe erwarten.</span><span class="sxs-lookup"><span data-stu-id="b70d5-109">You must manually pre-multiply the values if you plan to pass the output to effects that expect a pre-multiplied input.</span></span>

 

<span data-ttu-id="b70d5-110">Die CLSID für diesen Effekt ist CLSID \_ D2D1Flood.</span><span class="sxs-lookup"><span data-stu-id="b70d5-110">The CLSID for this effect is CLSID\_D2D1Flood.</span></span>

<span data-ttu-id="b70d5-111">Der überflutungseffekt hat kein Eingabebild.</span><span class="sxs-lookup"><span data-stu-id="b70d5-111">The flood effect has no input image.</span></span>

-   [<span data-ttu-id="b70d5-112">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="b70d5-112">Example image</span></span>](#example-image)
-   [<span data-ttu-id="b70d5-113">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b70d5-113">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="b70d5-114">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="b70d5-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="b70d5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b70d5-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b70d5-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b70d5-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="b70d5-117">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="b70d5-117">Example image</span></span>

![Beispiel Bild des Überflutungs Effekts aus grün.](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="b70d5-119">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b70d5-119">Effect properties</span></span>



| <span data-ttu-id="b70d5-120">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="b70d5-120">Display name and index enumeration</span></span>                   | <span data-ttu-id="b70d5-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b70d5-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b70d5-122">Color</span><span class="sxs-lookup"><span data-stu-id="b70d5-122">Color</span></span><br/> <span data-ttu-id="b70d5-123">D2D1- \_ Überflutungs \_ \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="b70d5-123">D2D1\_FLOOD\_PROP\_COLOR</span></span><br/> | <span data-ttu-id="b70d5-124">Die Farbe und die Deckkraft der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="b70d5-124">The color and opacity of the bitmap.</span></span> <span data-ttu-id="b70d5-125">Diese Eigenschaft ist ein D2D1 \_ Vector \_ 4f.</span><span class="sxs-lookup"><span data-stu-id="b70d5-125">This property is a D2D1\_VECTOR\_4F.</span></span> <span data-ttu-id="b70d5-126">Die einzelnen Werte für die einzelnen Kanäle sind vom Typ float, ungebunden und unitless.</span><span class="sxs-lookup"><span data-stu-id="b70d5-126">The individual values for each channel are of type FLOAT, unbounded and unitless.</span></span> <span data-ttu-id="b70d5-127">Der Effekt ändert nicht die Werte für die Kanäle.</span><span class="sxs-lookup"><span data-stu-id="b70d5-127">The effect doesn't modify the values for the channels.</span></span><br/> <span data-ttu-id="b70d5-128">Die RGBA-Werte für jeden Kanal reichen von 0 bis 1.</span><span class="sxs-lookup"><span data-stu-id="b70d5-128">The RGBA values for each channel range from 0 to 1.</span></span><br/> <span data-ttu-id="b70d5-129">Der Typ ist "D2D1 \_ Vector \_ 4f".</span><span class="sxs-lookup"><span data-stu-id="b70d5-129">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="b70d5-130">Der Standardwert ist {0,0 f, 0,0 f, 0,0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="b70d5-130">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="b70d5-131">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="b70d5-131">Output bitmap</span></span>

<span data-ttu-id="b70d5-132">Dieser Effekt generiert eine Bitmap mit logischer unbegrenzter groß.</span><span class="sxs-lookup"><span data-stu-id="b70d5-132">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="b70d5-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b70d5-133">Requirements</span></span>



| <span data-ttu-id="b70d5-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b70d5-134">Requirement</span></span> | <span data-ttu-id="b70d5-135">Wert</span><span class="sxs-lookup"><span data-stu-id="b70d5-135">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b70d5-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b70d5-136">Minimum supported client</span></span> | <span data-ttu-id="b70d5-137">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b70d5-137">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b70d5-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b70d5-138">Minimum supported server</span></span> | <span data-ttu-id="b70d5-139">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b70d5-139">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b70d5-140">Header</span><span class="sxs-lookup"><span data-stu-id="b70d5-140">Header</span></span>                   | <span data-ttu-id="b70d5-141">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="b70d5-141">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="b70d5-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b70d5-142">Library</span></span>                  | <span data-ttu-id="b70d5-143">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b70d5-143">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="b70d5-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b70d5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b70d5-145">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="b70d5-145">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

