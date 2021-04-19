---
description: Wandelt Grad in Bogenmaß um.
ms.assetid: 450806bd-db2f-47be-ae80-c261088b1bb8
title: D3DXToRadian (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXToRadian
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: e06184a0d3c654a2c0e82431ff25a339f5682837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350679"
---
# <a name="d3dxtoradian"></a><span data-ttu-id="a908d-103">D3DXToRadian</span><span class="sxs-lookup"><span data-stu-id="a908d-103">D3DXToRadian</span></span>

<span data-ttu-id="a908d-104">Wandelt Grad in Bogenmaß um.</span><span class="sxs-lookup"><span data-stu-id="a908d-104">Converts degrees into radians.</span></span>

``` syntax
#define D3DXToRadian(degree) ((degree) * (D3DX_PI / 180.0f))
```

## <a name="parameters"></a><span data-ttu-id="a908d-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a908d-105">Parameters</span></span>



| <span data-ttu-id="a908d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a908d-106">Parameter</span></span>                                                           | <span data-ttu-id="a908d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a908d-107">Description</span></span>                                              |
|---------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="a908d-108"><span id="degree"></span><span id="DEGREE"></span>theits</span><span class="sxs-lookup"><span data-stu-id="a908d-108"><span id="degree"></span><span id="DEGREE"></span>degree</span></span><br/> | <span data-ttu-id="a908d-109">Der Wert in Grad, der in das Bogenmaß konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a908d-109">The value, in degrees, to convert to radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a908d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a908d-110">Return Value</span></span>

<span data-ttu-id="a908d-111">Das-Makro gibt den Wert für den Grad im Bogenmaß zurück.</span><span class="sxs-lookup"><span data-stu-id="a908d-111">The macro returns the degree value in radians.</span></span>

## <a name="requirements"></a><span data-ttu-id="a908d-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a908d-112">Requirements</span></span>



| <span data-ttu-id="a908d-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a908d-113">Requirement</span></span> | <span data-ttu-id="a908d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a908d-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a908d-115">Header</span><span class="sxs-lookup"><span data-stu-id="a908d-115">Header</span></span><br/> | <dl> <span data-ttu-id="a908d-116"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a908d-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a908d-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a908d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a908d-118">Makros</span><span class="sxs-lookup"><span data-stu-id="a908d-118">Macros</span></span>](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[<span data-ttu-id="a908d-119">**D3DXToDegree**</span><span class="sxs-lookup"><span data-stu-id="a908d-119">**D3DXToDegree**</span></span>](d3dxtodegree.md)
</dt> <dt>

[<span data-ttu-id="a908d-120">D3DX \_ Pi</span><span class="sxs-lookup"><span data-stu-id="a908d-120">D3DX\_PI</span></span>](other-d3dx-constants.md)
</dt> </dl>

 

 




