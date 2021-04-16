---
description: Initialisiert eine Farbe mit den angegebenen Werten für Rot, grün und blau.
ms.assetid: 832a4a78-c166-4e45-a907-57730da1c2c8
title: D3DCOLOR_XRGB-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XRGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 4932e34979b0913f27874e57cfa881f18fb16364
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394081"
---
# <a name="d3dcolor_xrgb-macro"></a><span data-ttu-id="d46cb-103">D3DCOLOR \_ xrgb-Makro</span><span class="sxs-lookup"><span data-stu-id="d46cb-103">D3DCOLOR\_XRGB macro</span></span>

<span data-ttu-id="d46cb-104">Initialisiert eine Farbe mit den angegebenen Werten für Rot, grün und blau.</span><span class="sxs-lookup"><span data-stu-id="d46cb-104">Initializes a color with the supplied red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d46cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d46cb-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XRGB(
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="d46cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d46cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d46cb-107">*r*</span><span class="sxs-lookup"><span data-stu-id="d46cb-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="d46cb-108">Rote Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="d46cb-108">Red component of the color.</span></span> <span data-ttu-id="d46cb-109">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="d46cb-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="d46cb-110">*g*</span><span class="sxs-lookup"><span data-stu-id="d46cb-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="d46cb-111">Grüne Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="d46cb-111">Green component of the color.</span></span> <span data-ttu-id="d46cb-112">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="d46cb-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="d46cb-113">*b*</span><span class="sxs-lookup"><span data-stu-id="d46cb-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="d46cb-114">Blaue Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="d46cb-114">Blue component of the color.</span></span> <span data-ttu-id="d46cb-115">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="d46cb-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d46cb-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d46cb-116">Return value</span></span>

<span data-ttu-id="d46cb-117">Gibt den [**D3DCOLOR**](d3dcolor.md) -Wert zurück, der den angegebenen RGB-Werten entspricht.</span><span class="sxs-lookup"><span data-stu-id="d46cb-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="d46cb-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d46cb-118">Requirements</span></span>



| <span data-ttu-id="d46cb-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d46cb-119">Requirement</span></span> | <span data-ttu-id="d46cb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d46cb-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d46cb-121">Header</span><span class="sxs-lookup"><span data-stu-id="d46cb-121">Header</span></span><br/> | <dl> <span data-ttu-id="d46cb-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d46cb-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d46cb-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d46cb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d46cb-124">Makros</span><span class="sxs-lookup"><span data-stu-id="d46cb-124">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="d46cb-125">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="d46cb-125">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="d46cb-126">**D3DCOLOR \_ RGBA**</span><span class="sxs-lookup"><span data-stu-id="d46cb-126">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> </dl>

 

 




