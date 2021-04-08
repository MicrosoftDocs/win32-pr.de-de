---
description: Initialisiert eine Farbe mit den angegebenen Gleit Komma Werten für Rot, grün, blau und alpha.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: D3DCOLOR_COLORVALUE-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 3d5bb780a5999d8931335da1e9f49ad8af88dc12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761955"
---
# <a name="d3dcolor_colorvalue-macro"></a><span data-ttu-id="58406-103">D3DCOLOR \_ ColorValue-Makro</span><span class="sxs-lookup"><span data-stu-id="58406-103">D3DCOLOR\_COLORVALUE macro</span></span>

<span data-ttu-id="58406-104">Initialisiert eine Farbe mit den angegebenen Gleit Komma Werten für Rot, grün, blau und alpha.</span><span class="sxs-lookup"><span data-stu-id="58406-104">Initializes a color with the supplied red, green, blue, and alpha floating-point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="58406-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58406-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a><span data-ttu-id="58406-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58406-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58406-107">*r*</span><span class="sxs-lookup"><span data-stu-id="58406-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="58406-108">Rote Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="58406-108">Red component of the color.</span></span> <span data-ttu-id="58406-109">Dieser Wert muss ein Gleit Komma Wert im Bereich zwischen 0,0 und 1,0 sein.</span><span class="sxs-lookup"><span data-stu-id="58406-109">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="58406-110">*g*</span><span class="sxs-lookup"><span data-stu-id="58406-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="58406-111">Grüne Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="58406-111">Green component of the color.</span></span> <span data-ttu-id="58406-112">Dieser Wert muss ein Gleit Komma Wert im Bereich zwischen 0,0 und 1,0 sein.</span><span class="sxs-lookup"><span data-stu-id="58406-112">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="58406-113">*b*</span><span class="sxs-lookup"><span data-stu-id="58406-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="58406-114">Blaue Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="58406-114">Blue component of the color.</span></span> <span data-ttu-id="58406-115">Dieser Wert muss ein Gleit Komma Wert im Bereich zwischen 0,0 und 1,0 sein.</span><span class="sxs-lookup"><span data-stu-id="58406-115">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="58406-116">*ein*</span><span class="sxs-lookup"><span data-stu-id="58406-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="58406-117">Alpha Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="58406-117">Alpha component of the color.</span></span> <span data-ttu-id="58406-118">Dieser Wert muss ein Gleit Komma Wert im Bereich zwischen 0,0 und 1,0 sein.</span><span class="sxs-lookup"><span data-stu-id="58406-118">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58406-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58406-119">Return value</span></span>

<span data-ttu-id="58406-120">Gibt den [**D3DCOLOR**](d3dcolor.md) -Wert zurück, der den angegebenen RGBA-Werten entspricht.</span><span class="sxs-lookup"><span data-stu-id="58406-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="58406-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58406-121">Requirements</span></span>



| <span data-ttu-id="58406-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58406-122">Requirement</span></span> | <span data-ttu-id="58406-123">Wert</span><span class="sxs-lookup"><span data-stu-id="58406-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58406-124">Header</span><span class="sxs-lookup"><span data-stu-id="58406-124">Header</span></span><br/> | <dl> <span data-ttu-id="58406-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="58406-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58406-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58406-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58406-127">Makros</span><span class="sxs-lookup"><span data-stu-id="58406-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




