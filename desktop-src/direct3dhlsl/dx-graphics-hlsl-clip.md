---
title: Clip
description: Verwirft das aktuelle Pixel, wenn der angegebene Wert kleiner als 0 (null) ist.
ms.assetid: c9f84a27-5572-45aa-a12f-4446614b7be5
keywords:
- HLSL-Clip
topic_type:
- apiref
api_name:
- clip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92a75f2839dbbb605d976e07fffa5c2f9b27fd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976720"
---
# <a name="clip"></a><span data-ttu-id="16f91-104">Clip</span><span class="sxs-lookup"><span data-stu-id="16f91-104">clip</span></span>

<span data-ttu-id="16f91-105">Verwirft das aktuelle Pixel, wenn der angegebene Wert kleiner als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="16f91-105">Discards the current pixel if the specified value is less than zero.</span></span>



| <span data-ttu-id="16f91-106">Clip (*x*)</span><span class="sxs-lookup"><span data-stu-id="16f91-106">clip(*x*)</span></span> |
|-----------|



 

## <a name="parameters"></a><span data-ttu-id="16f91-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="16f91-107">Parameters</span></span>



| <span data-ttu-id="16f91-108">Element</span><span class="sxs-lookup"><span data-stu-id="16f91-108">Item</span></span>                                                   | <span data-ttu-id="16f91-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16f91-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="16f91-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="16f91-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="16f91-111">\[im \] angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="16f91-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="16f91-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16f91-112">Return Value</span></span>

<span data-ttu-id="16f91-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="16f91-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="16f91-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="16f91-114">Remarks</span></span>

<span data-ttu-id="16f91-115">Verwenden Sie die intrinsische Funktion **Clip** HLSL, um Clippingebenen zu simulieren, wenn jede Komponente des *x* -Parameters den Abstand von einer Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="16f91-115">Use the **clip** HLSL intrinsic function to simulate clipping planes if each component of the *x* parameter represents the distance from a plane.</span></span>

<span data-ttu-id="16f91-116">Verwenden Sie außerdem die **Clip** -Funktion, um das Alpha-Verhalten zu testen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="16f91-116">Also, use the **clip** function to test for alpha behavior, as shown in the following example:</span></span>


```
clip( Input.Color.A < 0.1f ? -1:1 );
```



## <a name="type-description"></a><span data-ttu-id="16f91-117">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="16f91-117">Type Description</span></span>



| <span data-ttu-id="16f91-118">Name</span><span class="sxs-lookup"><span data-stu-id="16f91-118">Name</span></span> | [<span data-ttu-id="16f91-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="16f91-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="16f91-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="16f91-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="16f91-121">Size</span><span class="sxs-lookup"><span data-stu-id="16f91-121">Size</span></span> |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="16f91-122">*x*</span><span class="sxs-lookup"><span data-stu-id="16f91-122">*x*</span></span>  | <span data-ttu-id="16f91-123">[**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix**</span><span class="sxs-lookup"><span data-stu-id="16f91-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="16f91-124">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="16f91-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="16f91-125">any</span><span class="sxs-lookup"><span data-stu-id="16f91-125">any</span></span>  |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="16f91-126">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="16f91-126">Minimum Shader Model</span></span>

<span data-ttu-id="16f91-127">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16f91-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="16f91-128">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="16f91-128">Shader Model</span></span>                                              | <span data-ttu-id="16f91-129">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="16f91-129">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="16f91-130">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="16f91-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="16f91-131">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="16f91-131">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="16f91-132">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16f91-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="16f91-133">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="16f91-133">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="16f91-134">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16f91-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="16f91-135">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="16f91-135">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="16f91-136">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16f91-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="16f91-137">Ja (nur Pixel-Shader)</span><span class="sxs-lookup"><span data-stu-id="16f91-137">yes (pixel shader only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="16f91-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="16f91-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16f91-139">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="16f91-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

