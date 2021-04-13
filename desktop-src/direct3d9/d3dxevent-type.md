---
description: Beschreibt den Typ der Ereignisse, die vom Animations Controller verschlüsselt werden können.
ms.assetid: d98b398e-29e1-41b5-84eb-37983bac8d0a
title: D3DXEVENT_TYPE-Enumeration (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 97219478b898dc47e385e8e00a5cc9b5484730ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354877"
---
# <a name="d3dxevent_type-enumeration"></a><span data-ttu-id="4b019-103">D3DXEVENT- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="4b019-103">D3DXEVENT\_TYPE enumeration</span></span>

<span data-ttu-id="4b019-104">Beschreibt den Typ der Ereignisse, die vom Animations Controller verschlüsselt werden können.</span><span class="sxs-lookup"><span data-stu-id="4b019-104">Describes the type of events that can be keyed by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b019-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b019-105">Syntax</span></span>


```C++
typedef enum D3DXEVENT_TYPE { 
  D3DXEVENT_TRACKSPEED     = 0,
  D3DXEVENT_TRACKWEIGHT    = 1,
  D3DXEVENT_TRACKPOSITION  = 2,
  D3DXEVENT_TRACKENABLE    = 3,
  D3DXEVENT_PRIORITYBLEND  = 4,
  D3DXEVENT_FORCE_DWORD    = 0x7fffffff
} D3DXEVENT_TYPE, *LPD3DXEVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="4b019-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="4b019-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4b019-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT \_ trackspeed**</span><span class="sxs-lookup"><span data-stu-id="4b019-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT\_TRACKSPEED**</span></span>
</dt> <dd>

<span data-ttu-id="4b019-108">Nachverfolgen der Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="4b019-108">Track speed.</span></span>

</dd> <dt>

<span data-ttu-id="4b019-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT \_ trackweight**</span><span class="sxs-lookup"><span data-stu-id="4b019-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT\_TRACKWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="4b019-110">Last nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="4b019-110">Track weight.</span></span>

</dd> <dt>

<span data-ttu-id="4b019-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT \_ trackposition**</span><span class="sxs-lookup"><span data-stu-id="4b019-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT\_TRACKPOSITION**</span></span>
</dt> <dd>

<span data-ttu-id="4b019-112">Position nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="4b019-112">Track position.</span></span>

</dd> <dt>

<span data-ttu-id="4b019-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT \_ trackenable**</span><span class="sxs-lookup"><span data-stu-id="4b019-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT\_TRACKENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="4b019-114">Flag aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4b019-114">Enable flag.</span></span>

</dd> <dt>

<span data-ttu-id="4b019-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT \_ priorityblend**</span><span class="sxs-lookup"><span data-stu-id="4b019-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT\_PRIORITYBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="4b019-116">Wert für die Prioritäts Mischung.</span><span class="sxs-lookup"><span data-stu-id="4b019-116">Priority blend value.</span></span>

</dd> <dt>

<span data-ttu-id="4b019-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b019-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="4b019-118">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="4b019-118">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="4b019-119">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="4b019-119">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="4b019-120">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b019-120">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b019-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b019-121">Requirements</span></span>



| <span data-ttu-id="4b019-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b019-122">Requirement</span></span> | <span data-ttu-id="4b019-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4b019-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b019-124">Header</span><span class="sxs-lookup"><span data-stu-id="4b019-124">Header</span></span><br/> | <dl> <span data-ttu-id="4b019-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b019-125"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b019-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b019-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b019-127">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="4b019-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




