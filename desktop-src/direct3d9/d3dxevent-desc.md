---
description: Beschreibt ein Animations Ereignis.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: D3DXEVENT_DESC-Struktur (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 32e02e75d3d73569b60c466f45dace2c074a6b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363972"
---
# <a name="d3dxevent_desc-structure"></a><span data-ttu-id="67c04-103">D3DXEVENT- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="67c04-103">D3DXEVENT\_DESC structure</span></span>

<span data-ttu-id="67c04-104">Beschreibt ein Animations Ereignis.</span><span class="sxs-lookup"><span data-stu-id="67c04-104">Describes an animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="67c04-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="67c04-105">Syntax</span></span>


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a><span data-ttu-id="67c04-106">Member</span><span class="sxs-lookup"><span data-stu-id="67c04-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="67c04-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="67c04-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="67c04-108">Type: **[ **D3DXEVENT- \_ Typ**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="67c04-108">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67c04-109">Der Ereignistyp, wie in [**D3DXEVENT \_ Type**](./d3dxevent-type.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="67c04-109">Event type, as defined in [**D3DXEVENT\_TYPE**](./d3dxevent-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="67c04-110">**Nachverfolgen**</span><span class="sxs-lookup"><span data-stu-id="67c04-110">**Track**</span></span>
</dt> <dd>

<span data-ttu-id="67c04-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67c04-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67c04-112">Bezeichner des Ereignis Titels.</span><span class="sxs-lookup"><span data-stu-id="67c04-112">Event track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="67c04-113">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="67c04-113">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="67c04-114">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67c04-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67c04-115">Die Startzeit des Ereignisses in der globalen Zeit.</span><span class="sxs-lookup"><span data-stu-id="67c04-115">Start time of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="67c04-116">**Dauer**</span><span class="sxs-lookup"><span data-stu-id="67c04-116">**Duration**</span></span>
</dt> <dd>

<span data-ttu-id="67c04-117">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67c04-117">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67c04-118">Die Dauer des Ereignisses in der globalen Zeit.</span><span class="sxs-lookup"><span data-stu-id="67c04-118">Duration of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="67c04-119">**Umstellung**</span><span class="sxs-lookup"><span data-stu-id="67c04-119">**Transition**</span></span>
</dt> <dd>

<span data-ttu-id="67c04-120">Type: **[ **D3DXTRANSITION- \_ Typ**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="67c04-120">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67c04-121">Die Übergangs Art des Ereignisses, wie in [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="67c04-121">Transition style of the event, as defined in [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="67c04-122">**Weight**</span><span class="sxs-lookup"><span data-stu-id="67c04-122">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="67c04-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67c04-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67c04-124">Die Gewichtung für das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="67c04-124">Track weight for the event.</span></span>

</dd> <dt>

<span data-ttu-id="67c04-125">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="67c04-125">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="67c04-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67c04-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67c04-127">Nachverfolgen der Geschwindigkeit für das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="67c04-127">Track speed for the event.</span></span>

</dd> <dt>

<span data-ttu-id="67c04-128">**Position**</span><span class="sxs-lookup"><span data-stu-id="67c04-128">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="67c04-129">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67c04-129">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67c04-130">Position für das Ereignis nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="67c04-130">Track position for the event.</span></span>

</dd> <dt>

<span data-ttu-id="67c04-131">**Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="67c04-131">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="67c04-132">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67c04-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67c04-133">Flag aktivieren.</span><span class="sxs-lookup"><span data-stu-id="67c04-133">Enable flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67c04-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67c04-134">Requirements</span></span>



| <span data-ttu-id="67c04-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67c04-135">Requirement</span></span> | <span data-ttu-id="67c04-136">Wert</span><span class="sxs-lookup"><span data-stu-id="67c04-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67c04-137">Header</span><span class="sxs-lookup"><span data-stu-id="67c04-137">Header</span></span><br/> | <dl> <span data-ttu-id="67c04-138"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="67c04-138"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67c04-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67c04-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c04-140">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="67c04-140">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
