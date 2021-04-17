---
title: Leuchtkraft zum Alpha Effekt
description: Legen Sie den Alpha-Kanal mit der Leuchtkraft des Bilds fest, und legen Sie die Farbkanäle auf 0 fest.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- Leuchtkraft zum Alpha Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb4c6fb78a1d49498b2adab6716d41e93d30deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104553037"
---
# <a name="luminance-to-alpha-effect"></a><span data-ttu-id="c9b86-104">Leuchtkraft zum Alpha Effekt</span><span class="sxs-lookup"><span data-stu-id="c9b86-104">Luminance to alpha effect</span></span>

<span data-ttu-id="c9b86-105">Legen Sie den Alpha-Kanal mit der Leuchtkraft des Bilds fest, und legen Sie die Farbkanäle auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="c9b86-105">Use the luminance to alpha effect to set the alpha channel to the luminance of the image and sets the color channels to 0.</span></span> <span data-ttu-id="c9b86-106">Sie können die Ausgabe dieses Effekts verwenden, um einen semitransparenten Overlay basierend auf der Helligkeit des Eingabe Bilds zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9b86-106">You can use the output of this effect to make a semitransparent overlay based on the brightness of the input image.</span></span> <span data-ttu-id="c9b86-107">Oder Sie können Sie verwenden, um eine Bildmaske zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9b86-107">Or you can use it to make an image mask.</span></span>

> [!Note]  
> <span data-ttu-id="c9b86-108">Dieser Effekt hat keine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c9b86-108">This effect has no properties.</span></span>

 

<span data-ttu-id="c9b86-109">Die CLSID für diesen Effekt ist CLSID \_ D2D1LuminanceToAlpha.</span><span class="sxs-lookup"><span data-stu-id="c9b86-109">The CLSID for this effect is CLSID\_D2D1LuminanceToAlpha.</span></span>

## <a name="example-image"></a><span data-ttu-id="c9b86-110">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="c9b86-110">Example image</span></span>

<span data-ttu-id="c9b86-111">Dieses Beispiel zeigt die Ausgabe des Leuchtkraft-und Alpha Effekts, der über einer weißen Oberfläche zusammengesetzt wird, um Deckkraft anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c9b86-111">This example shows the output of the luminance to alpha effect composited over a white surface to show opacity.</span></span>



| <span data-ttu-id="c9b86-112">Vorher</span><span class="sxs-lookup"><span data-stu-id="c9b86-112">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)        |
| <span data-ttu-id="c9b86-114">Nach</span><span class="sxs-lookup"><span data-stu-id="c9b86-114">After</span></span>                                                             |
| ![das Bild nach der Transformation.](images/18-luminancetoalpha.png) |



 


```C++
ComPtr<ID2D1Effect> luminanceToAlphaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LuminanceToAlpha, &luminanceToAlphaEffect);

luminanceToAlphaEffect->SetInput(0, bitmap);

// LuminanceToAlpha result is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);
floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, luminanceToAlphaEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="c9b86-116">Durch diesen Effekt wird der Alphakanal der Ausgabe mit dieser Farbmatrix auf die Leuchtkraft des Eingabe Bilds festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c9b86-116">This effect sets the alpha channel of the output to the luminance of the input image using this color matrix.</span></span>

![die Farbmatrix, die der Effekt zum Festlegen des Alphakanals verwendet.](images/luminance-to-alpha-math1.png)

<span data-ttu-id="c9b86-118">Diese Auswirkung verarbeitet und gibt vorab multiplizierte Alpha Bilder aus.</span><span class="sxs-lookup"><span data-stu-id="c9b86-118">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="c9b86-119">Der Effekt funktioniert nicht bei geraden Alpha Bildern, es sei denn, Sie sind vollständig undurchsichtig.</span><span class="sxs-lookup"><span data-stu-id="c9b86-119">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

> [!Note]
>
> <span data-ttu-id="c9b86-120">Da Bilder in einem Gamma kompensierten Format gespeichert werden, sollten Sie vor dem Berechnen der Leuchtkraft für ein Bild zuerst eine umgekehrte Gammakorrektur durchführen, um die tatsächlichen Farbwerte für das Bild zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c9b86-120">Because images are stored in a gamma-compensated format, before you calculate the luminance for an image you should first perform inverse gamma correction to get the true color values for the image.</span></span> <span data-ttu-id="c9b86-121">Da Images normalerweise in 2,2 Gamma gespeichert werden, können Sie den Gamma-Übertragungs Effekt mit einem Exponenten von (1/2.2) verwenden und dann die Ausgabe dieses Effekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9b86-121">Since images are normally stored at 2.2 gamma, you can use the Gamma transfer effect with an exponent of (1/2.2) and then use the output of that effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c9b86-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9b86-122">Requirements</span></span>



| <span data-ttu-id="c9b86-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9b86-123">Requirement</span></span> | <span data-ttu-id="c9b86-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c9b86-124">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b86-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9b86-125">Minimum supported client</span></span> | <span data-ttu-id="c9b86-126">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9b86-126">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c9b86-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9b86-127">Minimum supported server</span></span> | <span data-ttu-id="c9b86-128">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9b86-128">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c9b86-129">Header</span><span class="sxs-lookup"><span data-stu-id="c9b86-129">Header</span></span>                   | <span data-ttu-id="c9b86-130">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="c9b86-130">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="c9b86-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c9b86-131">Library</span></span>                  | <span data-ttu-id="c9b86-132">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="c9b86-132">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="output-bitmap"></a><span data-ttu-id="c9b86-133">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="c9b86-133">Output bitmap</span></span>

<span data-ttu-id="c9b86-134">Die Ausgabe entspricht der Größe des Eingabe Bilds.</span><span class="sxs-lookup"><span data-stu-id="c9b86-134">The output is the same size as the input image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9b86-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9b86-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9b86-136">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="c9b86-136">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
