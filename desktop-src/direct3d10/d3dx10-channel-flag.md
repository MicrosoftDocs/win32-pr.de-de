---
description: Diese Flags werden von Funktionen verwendet, die auf einem oder mehreren Kanälen in einer Textur arbeiten.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: D3DX10_CHANNEL_FLAG-Enumeration (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f21958ab964a70116a551c0cb8dadbce6db88f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355636"
---
# <a name="d3dx10_channel_flag-enumeration"></a><span data-ttu-id="8498e-103">D3dx10 \_ - \_ kanalflag-Enumeration</span><span class="sxs-lookup"><span data-stu-id="8498e-103">D3DX10\_CHANNEL\_FLAG enumeration</span></span>

<span data-ttu-id="8498e-104">Diese Flags werden von Funktionen verwendet, die auf einem oder mehreren Kanälen in einer Textur arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8498e-104">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="8498e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8498e-105">Syntax</span></span>


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="8498e-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="8498e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8498e-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3dx10 \_ Kanal \_ rot**</span><span class="sxs-lookup"><span data-stu-id="8498e-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="8498e-108">Gibt an, dass der rote Kanal verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8498e-108">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="8498e-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3dx10 \_ Kanal \_ blau**</span><span class="sxs-lookup"><span data-stu-id="8498e-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="8498e-110">Gibt an, dass der blaue Kanal verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8498e-110">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="8498e-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3dx10 \_ Kanal \_ grün**</span><span class="sxs-lookup"><span data-stu-id="8498e-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3DX10\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="8498e-112">Gibt an, dass der grüne Kanal verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8498e-112">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="8498e-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3dx10 \_ Channel \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="8498e-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="8498e-114">Gibt an, dass der Alphakanal verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8498e-114">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="8498e-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**D3dx10 \_ Kanal- \_ Leuchtkraft**</span><span class="sxs-lookup"><span data-stu-id="8498e-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**D3DX10\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="8498e-116">Gibt an, dass die leuchtenden der roten, grünen und blauen Kanäle verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8498e-116">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8498e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8498e-117">Requirements</span></span>



| <span data-ttu-id="8498e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8498e-118">Requirement</span></span> | <span data-ttu-id="8498e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8498e-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8498e-120">Header</span><span class="sxs-lookup"><span data-stu-id="8498e-120">Header</span></span><br/> | <dl> <span data-ttu-id="8498e-121"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8498e-121"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8498e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8498e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8498e-123">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="8498e-123">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




