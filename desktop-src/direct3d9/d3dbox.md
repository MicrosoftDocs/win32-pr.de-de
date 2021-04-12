---
description: Definiert ein Volume.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: D3DBOX-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 882f6aadf0d49284b30132d4f08a9c583e5c9d73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219463"
---
# <a name="d3dbox-structure"></a><span data-ttu-id="f164d-103">D3DBOX-Struktur</span><span class="sxs-lookup"><span data-stu-id="f164d-103">D3DBOX structure</span></span>

<span data-ttu-id="f164d-104">Definiert ein Volume.</span><span class="sxs-lookup"><span data-stu-id="f164d-104">Defines a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="f164d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f164d-105">Syntax</span></span>


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a><span data-ttu-id="f164d-106">Member</span><span class="sxs-lookup"><span data-stu-id="f164d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f164d-107">**Left**</span><span class="sxs-lookup"><span data-stu-id="f164d-107">**Left**</span></span>
</dt> <dd>

<span data-ttu-id="f164d-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f164d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f164d-109">Die Position der linken Seite des Felds auf der x-Achse.</span><span class="sxs-lookup"><span data-stu-id="f164d-109">Position of the left side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="f164d-110">**Top**</span><span class="sxs-lookup"><span data-stu-id="f164d-110">**Top**</span></span>
</dt> <dd>

<span data-ttu-id="f164d-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f164d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f164d-112">Die Position des oberen Rands auf der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="f164d-112">Position of the top of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="f164d-113">**Right**</span><span class="sxs-lookup"><span data-stu-id="f164d-113">**Right**</span></span>
</dt> <dd>

<span data-ttu-id="f164d-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f164d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f164d-115">Die Position der rechten Seite des Felds auf der x-Achse.</span><span class="sxs-lookup"><span data-stu-id="f164d-115">Position of the right side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="f164d-116">**bottom**</span><span class="sxs-lookup"><span data-stu-id="f164d-116">**Bottom**</span></span>
</dt> <dd>

<span data-ttu-id="f164d-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f164d-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f164d-118">Die Position des unteren Feldes des Felds auf der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="f164d-118">Position of the bottom of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="f164d-119">**Front**</span><span class="sxs-lookup"><span data-stu-id="f164d-119">**Front**</span></span>
</dt> <dd>

<span data-ttu-id="f164d-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f164d-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f164d-121">Position der Vorderseite des Felds auf der z-Achse.</span><span class="sxs-lookup"><span data-stu-id="f164d-121">Position of the front of the box on the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="f164d-122">**Zurück**</span><span class="sxs-lookup"><span data-stu-id="f164d-122">**Back**</span></span>
</dt> <dd>

<span data-ttu-id="f164d-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f164d-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f164d-124">Position der Rückseite des Felds auf der z-Achse.</span><span class="sxs-lookup"><span data-stu-id="f164d-124">Position of the back of the box on the z-axis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f164d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f164d-125">Remarks</span></span>

<span data-ttu-id="f164d-126">**D3DBOX** schließt die linken, oberen und vorderen Ränder ein. der Rechte, der untere und der hintere Rand sind jedoch nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="f164d-126">**D3DBOX** includes the left, top, and front edges; however, the right, bottom, and back edges are not included.</span></span> <span data-ttu-id="f164d-127">Beispielsweise wird ein Feld, das 100 Einheiten breit ist und bei 0 beginnt (d.h. die Punkte bis einschließlich und einschließlich 99), mit dem Wert 0 für das linke Element und dem Wert 100 für das Rechte Element ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="f164d-127">For example, a box that is 100 units wide and begins at 0 (thus, including the points up to and including 99) would be expressed with a value of 0 for the Left member and a value of 100 for the Right member.</span></span> <span data-ttu-id="f164d-128">Beachten Sie, dass der Wert 99 nicht für das Rechte Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f164d-128">Note that a value of 99 is not used for the Right member.</span></span>

<span data-ttu-id="f164d-129">Die Einschränkungen bei der für **D3DBOX** beobachteten Seiten Anordnung sind von links nach rechts, von oben nach unten und von vorne nach hinten.</span><span class="sxs-lookup"><span data-stu-id="f164d-129">The restrictions on side ordering observed for **D3DBOX** are left to right, top to bottom, and front to back.</span></span>

## <a name="requirements"></a><span data-ttu-id="f164d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f164d-130">Requirements</span></span>



| <span data-ttu-id="f164d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f164d-131">Requirement</span></span> | <span data-ttu-id="f164d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f164d-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f164d-133">Header</span><span class="sxs-lookup"><span data-stu-id="f164d-133">Header</span></span><br/> | <dl> <span data-ttu-id="f164d-134"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f164d-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f164d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f164d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f164d-136">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f164d-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
