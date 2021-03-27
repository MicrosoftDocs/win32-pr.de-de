---
title: D3DX11_CHANNEL_FLAG-Enumeration (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Diese Flags werden von Funktionen verwendet, die auf einem oder mehreren Kanälen in einer Textur arbeiten.
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- D3DX11_CHANNEL_FLAG-Enumeration Direct3D 11
- LPD3DX11_CHANNEL_FLAG enumerationszeiger Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_CHANNEL_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e3097552637ce96663671dda443684ebda2b65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394254"
---
# <a name="d3dx11_channel_flag-enumeration"></a><span data-ttu-id="51523-106">Bibliothek d3dx11 \_ - \_ kanalflag-Enumeration</span><span class="sxs-lookup"><span data-stu-id="51523-106">D3DX11\_CHANNEL\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="51523-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51523-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="51523-108">Diese Flags werden von Funktionen verwendet, die auf einem oder mehreren Kanälen in einer Textur arbeiten.</span><span class="sxs-lookup"><span data-stu-id="51523-108">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="51523-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="51523-109">Syntax</span></span>


```C++
typedef enum D3DX11_CHANNEL_FLAG { 
  D3DX11_CHANNEL_RED        = (1 << 0),
  D3DX11_CHANNEL_BLUE       = (1 << 1),
  D3DX11_CHANNEL_GREEN      = (1 << 2),
  D3DX11_CHANNEL_ALPHA      = (1 << 3),
  D3DX11_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX11_CHANNEL_FLAG, *LPD3DX11_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="51523-110">Konstanten</span><span class="sxs-lookup"><span data-stu-id="51523-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="51523-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**Bibliothek d3dx11 \_ Kanal \_ rot**</span><span class="sxs-lookup"><span data-stu-id="51523-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="51523-112">Gibt an, dass der rote Kanal verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51523-112">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="51523-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**Bibliothek d3dx11 \_ Kanal \_ blau**</span><span class="sxs-lookup"><span data-stu-id="51523-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="51523-114">Gibt an, dass der blaue Kanal verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51523-114">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="51523-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**Bibliothek d3dx11 \_ Kanal \_ grün**</span><span class="sxs-lookup"><span data-stu-id="51523-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**D3DX11\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="51523-116">Gibt an, dass der grüne Kanal verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51523-116">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="51523-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**Bibliothek d3dx11 \_ Channel \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="51523-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**D3DX11\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="51523-118">Gibt an, dass der Alphakanal verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51523-118">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="51523-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**Bibliothek d3dx11 \_ Kanal- \_ Leuchtkraft**</span><span class="sxs-lookup"><span data-stu-id="51523-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**D3DX11\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="51523-120">Gibt an, dass die leuchtenden der roten, grünen und blauen Kanäle verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51523-120">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51523-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="51523-121">Requirements</span></span>



| <span data-ttu-id="51523-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51523-122">Requirement</span></span> | <span data-ttu-id="51523-123">Wert</span><span class="sxs-lookup"><span data-stu-id="51523-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51523-124">Header</span><span class="sxs-lookup"><span data-stu-id="51523-124">Header</span></span><br/> | <dl> <span data-ttu-id="51523-125"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="51523-125"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51523-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="51523-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51523-127">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="51523-127">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





