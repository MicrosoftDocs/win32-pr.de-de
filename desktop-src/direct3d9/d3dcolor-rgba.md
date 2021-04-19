---
description: Initialisiert eine Farbe mit den angegebenen Werten für Rot, grün, blau und alpha.
ms.assetid: 87d322f1-4a26-42fd-a1c3-7be220cecf0f
title: D3DCOLOR_RGBA-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_RGBA
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c5047f29a9afbe5bb18db213f90e559b5e11d273
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357225"
---
# <a name="d3dcolor_rgba-macro"></a><span data-ttu-id="2805d-103">D3DCOLOR \_ RGBA-Makro</span><span class="sxs-lookup"><span data-stu-id="2805d-103">D3DCOLOR\_RGBA macro</span></span>

<span data-ttu-id="2805d-104">Initialisiert eine Farbe mit den angegebenen Werten für Rot, grün, blau und alpha.</span><span class="sxs-lookup"><span data-stu-id="2805d-104">Initializes a color with the supplied red, green, blue, and alpha values.</span></span>

## <a name="syntax"></a><span data-ttu-id="2805d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2805d-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_RGBA(
   int r,
   int g,
   int b,
   int a
);
```



## <a name="parameters"></a><span data-ttu-id="2805d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2805d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2805d-107">*r*</span><span class="sxs-lookup"><span data-stu-id="2805d-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="2805d-108">Rote Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="2805d-108">Red component of the color.</span></span> <span data-ttu-id="2805d-109">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="2805d-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="2805d-110">*g*</span><span class="sxs-lookup"><span data-stu-id="2805d-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="2805d-111">Grüne Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="2805d-111">Green component of the color.</span></span> <span data-ttu-id="2805d-112">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="2805d-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="2805d-113">*b*</span><span class="sxs-lookup"><span data-stu-id="2805d-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="2805d-114">Blaue Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="2805d-114">Blue component of the color.</span></span> <span data-ttu-id="2805d-115">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="2805d-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="2805d-116">*ein*</span><span class="sxs-lookup"><span data-stu-id="2805d-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="2805d-117">Alpha Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="2805d-117">Alpha component of the color.</span></span> <span data-ttu-id="2805d-118">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="2805d-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2805d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2805d-119">Return value</span></span>

<span data-ttu-id="2805d-120">Gibt den [**D3DCOLOR**](d3dcolor.md) -Wert zurück, der den angegebenen RGBA-Werten entspricht.</span><span class="sxs-lookup"><span data-stu-id="2805d-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="2805d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2805d-121">Requirements</span></span>



| <span data-ttu-id="2805d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2805d-122">Requirement</span></span> | <span data-ttu-id="2805d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2805d-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2805d-124">Header</span><span class="sxs-lookup"><span data-stu-id="2805d-124">Header</span></span><br/> | <dl> <span data-ttu-id="2805d-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2805d-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2805d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2805d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2805d-127">Makros</span><span class="sxs-lookup"><span data-stu-id="2805d-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="2805d-128">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="2805d-128">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="2805d-129">**D3DCOLOR \_ xrgb**</span><span class="sxs-lookup"><span data-stu-id="2805d-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




