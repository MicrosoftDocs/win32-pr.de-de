---
description: Stellt Informationen zu einem bestimmten dar.
MS-HAID: vspixengine.PixelHistoryIntersection
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixelhistoryschnittschnittstruktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D67A116D-B1D0-4E88-A2FF-611CDF4003B2
api_name:
- PixelHistoryIntersection
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 735adc5396551a18b5e2e2dfba781b358289475e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346208"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span data-ttu-id="06ed0-103"><span id="vspixengine.pixelhistoryintersection"></span>Pixelhistoryschnittschnittstruktur</span><span class="sxs-lookup"><span data-stu-id="06ed0-103"><span id="vspixengine.pixelhistoryintersection"></span>PixelHistoryIntersection structure</span></span>

<span data-ttu-id="06ed0-104">Stellt Informationen zu einem bestimmten</span><span class="sxs-lookup"><span data-stu-id="06ed0-104">Represents information about a particular</span></span>

## <a name="syntax"></a><span data-ttu-id="06ed0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06ed0-105">Syntax</span></span>


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a><span data-ttu-id="06ed0-106">Member</span><span class="sxs-lookup"><span data-stu-id="06ed0-106">Members</span></span>

<span data-ttu-id="06ed0-107">**Framezahl**</span><span class="sxs-lookup"><span data-stu-id="06ed0-107">**frameNumber**</span></span>  
<span data-ttu-id="06ed0-108">Der Rahmen des Grafik Ereignisses mit diesem Vorgang.</span><span class="sxs-lookup"><span data-stu-id="06ed0-108">The frame of the graphics event assocaited with this operation.</span></span>

<span data-ttu-id="06ed0-109">**VEI**</span><span class="sxs-lookup"><span data-stu-id="06ed0-109">**eid**</span></span>  
<span data-ttu-id="06ed0-110">Die ID des Grafik Ereignisses, das diesem Vorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="06ed0-110">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="06ed0-111">**rendertargetptr**</span><span class="sxs-lookup"><span data-stu-id="06ed0-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="06ed0-112">Das Renderziel, das ursprünglich (innerhalb der erfassten Anwendung) mit diesem Vorgang zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="06ed0-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="06ed0-113">**eventType**</span><span class="sxs-lookup"><span data-stu-id="06ed0-113">**eventType**</span></span>  
<span data-ttu-id="06ed0-114">Die Art des Ereignisses, das diesem Vorgang zugeordnet ist (insbesondere, ob es sich bei diesem Ereignis um einen zeichnen-Befehl handelt).</span><span class="sxs-lookup"><span data-stu-id="06ed0-114">The kind of event associated with this operation (specifically, whether this event is a draw call).</span></span>

<span data-ttu-id="06ed0-115">**Punkt**</span><span class="sxs-lookup"><span data-stu-id="06ed0-115">**point**</span></span>  
<span data-ttu-id="06ed0-116">Die Koordinaten des Pixels im Framebuffer.</span><span class="sxs-lookup"><span data-stu-id="06ed0-116">The coordinates of the pixel in the framebuffer.</span></span>

<span data-ttu-id="06ed0-117">**bassemblerstagegeneratesinstanceid**</span><span class="sxs-lookup"><span data-stu-id="06ed0-117">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="06ed0-118">true, wenn der Eingabe Assembler Instanz-IDs generiert. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="06ed0-118">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="06ed0-119">**flags**</span><span class="sxs-lookup"><span data-stu-id="06ed0-119">**flags**</span></span>  
<span data-ttu-id="06ed0-120">Eine Kombination von pixelhistoryflags-Werten.</span><span class="sxs-lookup"><span data-stu-id="06ed0-120">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="06ed0-121">Weitere Informationen finden Sie unter der pixelhistoryflags-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="06ed0-121">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="06ed0-122">**"binitialred"**</span><span class="sxs-lookup"><span data-stu-id="06ed0-122">**fbInitialRed**</span></span>  
<span data-ttu-id="06ed0-123">Frame Puffer: Wert der roten Farbkomponente von Frame Puffer, bevor eine Pixel-Shader-Ausgabe zusammengeführt wird. Das heißt, am Anfang dieses Frames.</span><span class="sxs-lookup"><span data-stu-id="06ed0-123">Framebuffer: value of red color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="06ed0-124">**binitialgrün**</span><span class="sxs-lookup"><span data-stu-id="06ed0-124">**fbInitialGreen**</span></span>  
<span data-ttu-id="06ed0-125">Frame Puffer: Wert der grünen Farbkomponente von Frame Puffer, bevor eine Pixel-Shader-Ausgabe zusammengeführt wird. Das heißt, am Anfang dieses Frames.</span><span class="sxs-lookup"><span data-stu-id="06ed0-125">Framebuffer: value of green color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="06ed0-126">**"binitialblue"**</span><span class="sxs-lookup"><span data-stu-id="06ed0-126">**fbInitialBlue**</span></span>  
<span data-ttu-id="06ed0-127">Frame Puffer: Wert der blauen Farbkomponente von Frame Puffer, bevor eine Pixel-Shader-Ausgabe zusammengeführt wird. Das heißt, am Anfang dieses Frames.</span><span class="sxs-lookup"><span data-stu-id="06ed0-127">Framebuffer: value of blue color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="06ed0-128">**"binitialalpha"**</span><span class="sxs-lookup"><span data-stu-id="06ed0-128">**fbInitialAlpha**</span></span>  
<span data-ttu-id="06ed0-129">Frame Puffer: Wert der Alpha Farbkomponente von Frame Puffer, bevor eine Pixel-Shader-Ausgabe zusammengeführt wird. Das heißt, am Anfang dieses Frames.</span><span class="sxs-lookup"><span data-stu-id="06ed0-129">Framebuffer: value of alpha color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="06ed0-130">**Labelfbinitialred**</span><span class="sxs-lookup"><span data-stu-id="06ed0-130">**LabelFBInitialRed**</span></span>  
<span data-ttu-id="06ed0-131">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der roten Farbkomponente des Frame Puffer vor jeder Pixel Schattierung zugeordnet ist. Das heißt, am Anfang dieses Frames.</span><span class="sxs-lookup"><span data-stu-id="06ed0-131">A COM string containing the name of the label associated with the red color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="06ed0-132">**Labelfbinitialgreen**</span><span class="sxs-lookup"><span data-stu-id="06ed0-132">**LabelFBInitialGreen**</span></span>  
<span data-ttu-id="06ed0-133">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der grünen Farbkomponente des Frame Puffer vor jeder Pixel Schattierung zugeordnet ist. Das heißt, am Anfang dieses Frames.</span><span class="sxs-lookup"><span data-stu-id="06ed0-133">A COM string containing the name of the label associated with the green color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="06ed0-134">**Labelfbinitialblue**</span><span class="sxs-lookup"><span data-stu-id="06ed0-134">**LabelFBInitialBlue**</span></span>  
<span data-ttu-id="06ed0-135">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der blauen Farbkomponente des Frame Puffer vor jeder Pixel Schattierung zugeordnet ist. Das heißt, am Anfang dieses Frames.</span><span class="sxs-lookup"><span data-stu-id="06ed0-135">A COM string containing the name of the label associated with the blue color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="06ed0-136">**Labelfbinitialalpha**</span><span class="sxs-lookup"><span data-stu-id="06ed0-136">**LabelFBInitialAlpha**</span></span>  
<span data-ttu-id="06ed0-137">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der Alpha-Farbkomponente des Frame Puffer vor jeder Pixel Schattierung zugeordnet ist. Das heißt, am Anfang dieses Frames.</span><span class="sxs-lookup"><span data-stu-id="06ed0-137">A COM string containing the name of the label associated with the alpha color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="06ed0-138">**mit dem Namen**</span><span class="sxs-lookup"><span data-stu-id="06ed0-138">**fbRed**</span></span>  
<span data-ttu-id="06ed0-139">Frame Puffer: Wert der roten Farbkomponente von Frame Puffer, nachdem alle Pixel-Shader-Ausgaben zusammengeführt wurden. Das heißt, die endgültige framepufferfarbe.</span><span class="sxs-lookup"><span data-stu-id="06ed0-139">Framebuffer: value of red color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="06ed0-140">**bgrün**</span><span class="sxs-lookup"><span data-stu-id="06ed0-140">**fbGreen**</span></span>  
<span data-ttu-id="06ed0-141">Frame Puffer: Wert der grünen Farbkomponente von Frame Puffer, nachdem alle Pixel-Shader-Ausgaben zusammengeführt wurden. Das heißt, die endgültige framepufferfarbe.</span><span class="sxs-lookup"><span data-stu-id="06ed0-141">Framebuffer: value of green color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="06ed0-142">**"f"**</span><span class="sxs-lookup"><span data-stu-id="06ed0-142">**fbBlue**</span></span>  
<span data-ttu-id="06ed0-143">Frame Puffer: Wert der blauen Farbkomponente von Frame Puffer, nachdem alle Pixel-Shader-Ausgaben zusammengeführt wurden. Das heißt, die endgültige framepufferfarbe.</span><span class="sxs-lookup"><span data-stu-id="06ed0-143">Framebuffer: value of blue color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="06ed0-144">**"f"**</span><span class="sxs-lookup"><span data-stu-id="06ed0-144">**fbAlpha**</span></span>  
<span data-ttu-id="06ed0-145">Frame Puffer: Wert der Alpha Farbkomponente von Frame Puffer, nachdem alle Pixel-Shader-Ausgaben zusammengeführt wurden. Das heißt, die endgültige framepufferfarbe.</span><span class="sxs-lookup"><span data-stu-id="06ed0-145">Framebuffer: value of alpha color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="06ed0-146">**Labelfgezüchtet**</span><span class="sxs-lookup"><span data-stu-id="06ed0-146">**LabelFBRed**</span></span>  
<span data-ttu-id="06ed0-147">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der roten Farbkomponente des Frame Puffer nach der gesamten Pixel Schattierung zugeordnet ist. Das heißt, die endgültige framepufferfarbe.</span><span class="sxs-lookup"><span data-stu-id="06ed0-147">A COM string containing the name of the label associated with the red color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="06ed0-148">**Labelfbgrün**</span><span class="sxs-lookup"><span data-stu-id="06ed0-148">**LabelFBGreen**</span></span>  
<span data-ttu-id="06ed0-149">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der grünen Farbkomponente des Frame Puffer nach der gesamten Pixel Schattierung zugeordnet ist. Das heißt, die endgültige framepufferfarbe.</span><span class="sxs-lookup"><span data-stu-id="06ed0-149">A COM string containing the name of the label associated with the green color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="06ed0-150">**Labelfbblue**</span><span class="sxs-lookup"><span data-stu-id="06ed0-150">**LabelFBBlue**</span></span>  
<span data-ttu-id="06ed0-151">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der blauen Farbkomponente des Frame Puffer nach der gesamten Pixel Schattierung zugeordnet ist. Das heißt, die endgültige framepufferfarbe.</span><span class="sxs-lookup"><span data-stu-id="06ed0-151">A COM string containing the name of the label associated with the blue color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="06ed0-152">**Labelfbalpha**</span><span class="sxs-lookup"><span data-stu-id="06ed0-152">**LabelFBAlpha**</span></span>  
<span data-ttu-id="06ed0-153">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der Alpha Farbkomponente des Frame Puffer nach der gesamten Pixel Schattierung zugeordnet ist. Das heißt, die endgültige framepufferfarbe.</span><span class="sxs-lookup"><span data-stu-id="06ed0-153">A COM string containing the name of the label associated with the alpha color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="06ed0-154">**pixelkillreason**</span><span class="sxs-lookup"><span data-stu-id="06ed0-154">**pixelKillReason**</span></span>  
<span data-ttu-id="06ed0-155">Gibt den Grund an, warum der Farb Beitrag des Pixels abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="06ed0-155">Specifies the reason that the pixel's color contribution was killed.</span></span>

<span data-ttu-id="06ed0-156">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="06ed0-156">**HResult**</span></span>  
<span data-ttu-id="06ed0-157">Wenn ein Fehler aufgetreten ist, enthält das DirectX HRESULT, das den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="06ed0-157">If an error occurred, contains the DirectX HRESULT that specifies the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="06ed0-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06ed0-158">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="06ed0-159">Header</span><span class="sxs-lookup"><span data-stu-id="06ed0-159">Header</span></span></p></td><td><span data-ttu-id="06ed0-160">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="06ed0-160">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



