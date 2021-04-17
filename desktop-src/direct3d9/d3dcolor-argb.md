---
description: Initialisiert eine Farbe mit den angegebenen Alpha-, rot-, grün-und blauen Werten.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: D3DCOLOR_ARGB-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_ARGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: bd0138c435c15c0c2ac026487471554e0edf0afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354426"
---
# <a name="d3dcolor_argb-macro"></a><span data-ttu-id="86558-103">D3DCOLOR \_ ARGB-Makro</span><span class="sxs-lookup"><span data-stu-id="86558-103">D3DCOLOR\_ARGB macro</span></span>

<span data-ttu-id="86558-104">Initialisiert eine Farbe mit den angegebenen Alpha-, rot-, grün-und blauen Werten.</span><span class="sxs-lookup"><span data-stu-id="86558-104">Initializes a color with the supplied alpha, red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="86558-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="86558-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_ARGB(
   int a,
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="86558-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="86558-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86558-107">*ein*</span><span class="sxs-lookup"><span data-stu-id="86558-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="86558-108">Alpha Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="86558-108">Alpha component of the color.</span></span> <span data-ttu-id="86558-109">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="86558-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="86558-110">*r*</span><span class="sxs-lookup"><span data-stu-id="86558-110">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="86558-111">Rote Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="86558-111">Red component of the color.</span></span> <span data-ttu-id="86558-112">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="86558-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="86558-113">*g*</span><span class="sxs-lookup"><span data-stu-id="86558-113">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="86558-114">Grüne Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="86558-114">Green component of the color.</span></span> <span data-ttu-id="86558-115">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="86558-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="86558-116">*b*</span><span class="sxs-lookup"><span data-stu-id="86558-116">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="86558-117">Blaue Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="86558-117">Blue component of the color.</span></span> <span data-ttu-id="86558-118">Dieser Wert muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="86558-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86558-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86558-119">Return value</span></span>

<span data-ttu-id="86558-120">Gibt den [D3DCOLOR](d3dcolor.md) -Wert zurück, der den angegebenen ARGB-Werten entspricht.</span><span class="sxs-lookup"><span data-stu-id="86558-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="86558-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86558-121">Requirements</span></span>



| <span data-ttu-id="86558-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86558-122">Requirement</span></span> | <span data-ttu-id="86558-123">Wert</span><span class="sxs-lookup"><span data-stu-id="86558-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86558-124">Header</span><span class="sxs-lookup"><span data-stu-id="86558-124">Header</span></span><br/> | <dl> <span data-ttu-id="86558-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="86558-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86558-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86558-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86558-127">Makros</span><span class="sxs-lookup"><span data-stu-id="86558-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="86558-128">**D3DCOLOR \_ RGBA**</span><span class="sxs-lookup"><span data-stu-id="86558-128">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> <dt>

[<span data-ttu-id="86558-129">**D3DCOLOR \_ xrgb**</span><span class="sxs-lookup"><span data-stu-id="86558-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




