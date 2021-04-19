---
description: Initialisiert eine Farbe mit den Werten (a, y, u, v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: D3DCOLOR_AYUV-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355168"
---
# <a name="d3dcolor_ayuv-macro"></a><span data-ttu-id="30181-103">D3DCOLOR \_ ayuv-Makro</span><span class="sxs-lookup"><span data-stu-id="30181-103">D3DCOLOR\_AYUV macro</span></span>

<span data-ttu-id="30181-104">Initialisiert eine Farbe mit den Werten (a, y, u, v).</span><span class="sxs-lookup"><span data-stu-id="30181-104">Initializes a color using the (a,y,u,v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="30181-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="30181-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="30181-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30181-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30181-107">*ein*</span><span class="sxs-lookup"><span data-stu-id="30181-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="30181-108">Alpha Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="30181-108">Alpha component of the color.</span></span> <span data-ttu-id="30181-109">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="30181-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="30181-110">*y*</span><span class="sxs-lookup"><span data-stu-id="30181-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="30181-111">Die Leuchtkraft Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="30181-111">Luminance component of the color.</span></span> <span data-ttu-id="30181-112">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="30181-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="30181-113">*n*</span><span class="sxs-lookup"><span data-stu-id="30181-113">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="30181-114">Blaue Helligkeit der Farbe.</span><span class="sxs-lookup"><span data-stu-id="30181-114">Blue brightness of the color.</span></span> <span data-ttu-id="30181-115">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="30181-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="30181-116">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="30181-116">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="30181-117">Rote Helligkeit der Farbe.</span><span class="sxs-lookup"><span data-stu-id="30181-117">Red brightness of the color.</span></span> <span data-ttu-id="30181-118">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="30181-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30181-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30181-119">Return value</span></span>

<span data-ttu-id="30181-120">Gibt den [D3DCOLOR](d3dcolor.md) -Wert zurück, der den angegebenen ARGB-Werten entspricht.</span><span class="sxs-lookup"><span data-stu-id="30181-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="remarks"></a><span data-ttu-id="30181-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30181-121">Remarks</span></span>

<span data-ttu-id="30181-122">Eine RGB-Farbe kann auf 16 Bits pro Pixel reduziert werden, indem Sie in Leuchtkraft-und Farbunterschiede mit den folgenden Gleichungen konvertiert wird:</span><span class="sxs-lookup"><span data-stu-id="30181-122">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="30181-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30181-123">Requirements</span></span>



| <span data-ttu-id="30181-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30181-124">Requirement</span></span> | <span data-ttu-id="30181-125">Wert</span><span class="sxs-lookup"><span data-stu-id="30181-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30181-126">Header</span><span class="sxs-lookup"><span data-stu-id="30181-126">Header</span></span><br/> | <dl> <span data-ttu-id="30181-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="30181-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30181-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30181-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30181-129">Makros</span><span class="sxs-lookup"><span data-stu-id="30181-129">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="30181-130">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="30181-130">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="30181-131">**D3DCOLOR \_ XYUV**</span><span class="sxs-lookup"><span data-stu-id="30181-131">**D3DCOLOR\_XYUV**</span></span>](d3dcolor-xyuv.md)
</dt> </dl>

 

 




