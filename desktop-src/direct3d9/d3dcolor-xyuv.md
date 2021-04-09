---
description: Initialisiert eine Farbe mit den Werten (y, u, v).
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: D3DCOLOR_XYUV-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 12d539e44528c5e54a54209763e4cbe262cd16f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870087"
---
# <a name="d3dcolor_xyuv-macro"></a><span data-ttu-id="5bbad-103">D3DCOLOR \_ XYUV-Makro</span><span class="sxs-lookup"><span data-stu-id="5bbad-103">D3DCOLOR\_XYUV macro</span></span>

<span data-ttu-id="5bbad-104">Initialisiert eine Farbe mit den Werten (y, u, v).</span><span class="sxs-lookup"><span data-stu-id="5bbad-104">Initializes a color with the (y, u, v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bbad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bbad-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XYUV(
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="5bbad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bbad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bbad-107">*y*</span><span class="sxs-lookup"><span data-stu-id="5bbad-107">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbad-108">Die Leuchtkraft Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="5bbad-108">Luminance component of the color.</span></span> <span data-ttu-id="5bbad-109">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="5bbad-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="5bbad-110">*n*</span><span class="sxs-lookup"><span data-stu-id="5bbad-110">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbad-111">Blaue Helligkeit der Farbe.</span><span class="sxs-lookup"><span data-stu-id="5bbad-111">Blue brightness of the color.</span></span> <span data-ttu-id="5bbad-112">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="5bbad-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="5bbad-113">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="5bbad-113">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbad-114">Rote Helligkeit der Farbe.</span><span class="sxs-lookup"><span data-stu-id="5bbad-114">Red brightness of the color.</span></span> <span data-ttu-id="5bbad-115">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="5bbad-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bbad-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5bbad-116">Return value</span></span>

<span data-ttu-id="5bbad-117">Gibt den [**D3DCOLOR**](d3dcolor.md) -Wert zurück, der den angegebenen Werten (y, u, v) entspricht.</span><span class="sxs-lookup"><span data-stu-id="5bbad-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied (y, u, v) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bbad-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bbad-118">Remarks</span></span>

<span data-ttu-id="5bbad-119">Eine RGB-Farbe kann auf 16 Bits pro Pixel reduziert werden, indem Sie in Leuchtkraft-und Farbunterschiede mit den folgenden Gleichungen konvertiert wird:</span><span class="sxs-lookup"><span data-stu-id="5bbad-119">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="5bbad-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bbad-120">Requirements</span></span>



| <span data-ttu-id="5bbad-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bbad-121">Requirement</span></span> | <span data-ttu-id="5bbad-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5bbad-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bbad-123">Header</span><span class="sxs-lookup"><span data-stu-id="5bbad-123">Header</span></span><br/> | <dl> <span data-ttu-id="5bbad-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bbad-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bbad-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bbad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bbad-126">Makros</span><span class="sxs-lookup"><span data-stu-id="5bbad-126">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="5bbad-127">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="5bbad-127">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="5bbad-128">**D3DCOLOR \_ ayuv**</span><span class="sxs-lookup"><span data-stu-id="5bbad-128">**D3DCOLOR\_AYUV**</span></span>](d3dcolor-ayuv.md)
</dt> </dl>

 

 




