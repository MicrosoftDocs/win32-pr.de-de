---
title: Atlas-Effekt
description: Sie können diesen Effekt verwenden, um einen Teil eines Bilds auszugeben, aber den Bereich außerhalb des Teils für die Verwendung in nachfolgenden Vorgängen beibehalten.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f9e1d4c6df0698d47a35eb2cbdaf670b98ed125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478234"
---
# <a name="atlas-effect"></a><span data-ttu-id="85242-103">Atlas-Effekt</span><span class="sxs-lookup"><span data-stu-id="85242-103">Atlas effect</span></span>

<span data-ttu-id="85242-104">Sie können diesen Effekt verwenden, um einen Teil eines Bilds auszugeben, aber den Bereich außerhalb des Teils für die Verwendung in nachfolgenden Vorgängen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="85242-104">You can use this effect to output a portion of an image but retain the region outside of the portion for use in subsequent operations.</span></span>

<span data-ttu-id="85242-105">Die CLSID für diesen Effekt ist CLSID \_ D2D1Atlas.</span><span class="sxs-lookup"><span data-stu-id="85242-105">The CLSID for this effect is CLSID\_D2D1Atlas.</span></span>

<span data-ttu-id="85242-106">Der Atlas-Effekt ist hilfreich, wenn Sie ein umfangreiches Bild laden möchten, das aus vielen kleineren Bildern besteht, z. b. aus verschiedenen Rahmen eines Sprite.</span><span class="sxs-lookup"><span data-stu-id="85242-106">The atlas effect is useful if you want to load a large image made up of many smaller images, such as various frames of a sprite.</span></span>

<span data-ttu-id="85242-107">So erstellen Sie die Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="85242-107">To create the output the effect:</span></span>

1.  <span data-ttu-id="85242-108">Fügt die Eingabe in die angegebene *inputrect* -Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="85242-108">Crops the input to the given *InputRect* property.</span></span>
2.  <span data-ttu-id="85242-109">Übersetzt den Ursprung des Ergebnisses in (0,0).</span><span class="sxs-lookup"><span data-stu-id="85242-109">Translates the origin of the result to (0,0).</span></span>

> [!Note]  
> <span data-ttu-id="85242-110">Die *inputpaddingrect* -Eigenschaft sollte nur dann größer sein, wenn die Pixel zwischen den zwei Rechtecke in der Eingabe transparent sind.</span><span class="sxs-lookup"><span data-stu-id="85242-110">The *InputPaddingRect* property should only be larger if and only if the pixels between the two rectangles are transparent black on the input.</span></span> <span data-ttu-id="85242-111">Dies kann dazu führen, dass Direct2D das Diagramm optimaler ausführt.</span><span class="sxs-lookup"><span data-stu-id="85242-111">This may result in Direct2D executing the graph more optimally.</span></span>

 

<span data-ttu-id="85242-112">Im folgenden finden Sie ein Beispiel für den Effekt.</span><span class="sxs-lookup"><span data-stu-id="85242-112">Here is an example of the effect.</span></span> <span data-ttu-id="85242-113">Dieses Bild ist für Illustrationszwecke klein und einfach.</span><span class="sxs-lookup"><span data-stu-id="85242-113">This image is small and simple for illustration purposes.</span></span>

![Eingabebild.](images/atlas.png)

<span data-ttu-id="85242-115">Die vorherige Abbildung ist die Eingabe für den Effekt.</span><span class="sxs-lookup"><span data-stu-id="85242-115">The preceding image is the input to the effect.</span></span> <span data-ttu-id="85242-116">Der Code hier erstellt einen Atlas-Effekt, legt die Eingabe fest, legt das Eingabe Rechteck fest und zeichnet dann die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="85242-116">The code here creates an atlas effect, sets the input, sets the input rectangle, and then draws the output.</span></span>


```C++
ComPtr<ID2D1Effect> atlasEffect;

// Create the Atlas Effect.
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Atlas, &atlasEffect));

// Set the input.
atlasEffect->SetInputEffect(0, inputImage.Get());

// The images here are 150 x 150 pixels.
float size = 150.0f;

// Compensate for the padding between images.
float padding = 10.0f;

// The input rectangle.  150 x 150 pixels with 10 pixel padding
D2D1_Vector_4F inputRect = D2D1::Vector4F(size + (padding * 2), padding, size, size);

DX::ThrowIfFailed(atlasEffect->SetValue(D2D1_ATLAS_PROP_INPUT_RECT, inputRect));

// Draw the image
m_d2dContext->DrawImage(atlasEffect.Get());
```



<span data-ttu-id="85242-117">Der vorangehende Code wählt ein Rechteck aus, das sich um das zweite Dreieck dreht.</span><span class="sxs-lookup"><span data-stu-id="85242-117">The preceding code selects a rectangle that is around the second triangle.</span></span> <span data-ttu-id="85242-118">Der Abstand um diese wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="85242-118">The padding around it is ignored.</span></span> <span data-ttu-id="85242-119">Hier sehen Sie das resultierende Image.</span><span class="sxs-lookup"><span data-stu-id="85242-119">Here is the resulting image.</span></span>

![Ausgabe Bild.](images/atlas2.png)

> [!Note]  
> <span data-ttu-id="85242-121">Dies ist eine Situation, in der Sie ggf. eine *inputpaddingrect* -Angabe festlegen können, da der Abstand transparent schwarz ist.</span><span class="sxs-lookup"><span data-stu-id="85242-121">This is a situation where you may choose to specify a *InputPaddingRect* because the padding is transparent black.</span></span> <span data-ttu-id="85242-122">Das Rechteck wäre `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .</span><span class="sxs-lookup"><span data-stu-id="85242-122">The rectangle would be `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);`.</span></span>

 

## <a name="effect-properties"></a><span data-ttu-id="85242-123">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85242-123">Effect properties</span></span>



| <span data-ttu-id="85242-124">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="85242-124">Display name and index enumeration</span></span>                                             | <span data-ttu-id="85242-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85242-125">Description</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85242-126">Input Rect</span><span class="sxs-lookup"><span data-stu-id="85242-126">InputRect</span></span><br/> <span data-ttu-id="85242-127">D2D1 \_ Atlas \_ - \_ Eingabe \_ Rect</span><span class="sxs-lookup"><span data-stu-id="85242-127">D2D1\_ATLAS\_PROP\_INPUT\_RECT</span></span><br/>                 | <span data-ttu-id="85242-128">Der Teil des Bilds, der an den nächsten Effekt weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="85242-128">The portion of the image passed to the next effect.</span></span><br/> <span data-ttu-id="85242-129">Typ: D2D1 \_ Vector \_ 4f</span><span class="sxs-lookup"><span data-stu-id="85242-129">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="85242-130">Der Standardwert ist (-f \_ Max,-f Max \_ , SLT \_ Max, SLT \_ max).</span><span class="sxs-lookup"><span data-stu-id="85242-130">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span> <br/> |
| <span data-ttu-id="85242-131">Input paddingrect</span><span class="sxs-lookup"><span data-stu-id="85242-131">InputPaddingRect</span></span><br/> <span data-ttu-id="85242-132">D2D1 \_ Atlas \_ \_ Eingabe \_ \_ Auffüll Auffüll Text Rect</span><span class="sxs-lookup"><span data-stu-id="85242-132">D2D1\_ATLAS\_PROP\_INPUT\_PADDING\_RECT</span></span><br/> | <span data-ttu-id="85242-133">Die maximale Größe, die für das Ausgabe Rechteck Stichprobe ist.</span><span class="sxs-lookup"><span data-stu-id="85242-133">The maximum size sampled for the output rectangle.</span></span><br/> <span data-ttu-id="85242-134">Typ: D2D1 \_ Vector \_ 4f</span><span class="sxs-lookup"><span data-stu-id="85242-134">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="85242-135">Der Standardwert ist (-f \_ Max,-f Max \_ , SLT \_ Max, SLT \_ max).</span><span class="sxs-lookup"><span data-stu-id="85242-135">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="85242-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85242-136">Requirements</span></span>



| <span data-ttu-id="85242-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85242-137">Requirement</span></span> | <span data-ttu-id="85242-138">Wert</span><span class="sxs-lookup"><span data-stu-id="85242-138">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85242-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85242-139">Minimum supported client</span></span> | <span data-ttu-id="85242-140">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85242-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="85242-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85242-141">Minimum supported server</span></span> | <span data-ttu-id="85242-142">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85242-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="85242-143">Header</span><span class="sxs-lookup"><span data-stu-id="85242-143">Header</span></span>                   | <span data-ttu-id="85242-144">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="85242-144">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="85242-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="85242-145">Library</span></span>                  | <span data-ttu-id="85242-146">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="85242-146">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="85242-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="85242-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85242-148">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="85242-148">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

