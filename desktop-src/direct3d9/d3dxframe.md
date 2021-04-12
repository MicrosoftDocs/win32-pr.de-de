---
description: Kapselt einen Transformations Rahmen in einer Transformations Frame Hierarchie.
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: D3DXFRAME-Struktur (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 152e620f6bf845f1f2528a321e39d8d746e8b893
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219514"
---
# <a name="d3dxframe-structure"></a><span data-ttu-id="62885-103">D3DXFRAME-Struktur</span><span class="sxs-lookup"><span data-stu-id="62885-103">D3DXFRAME structure</span></span>

<span data-ttu-id="62885-104">Kapselt einen Transformations Rahmen in einer Transformations Frame Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="62885-104">Encapsulates a transform frame in a transformation frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="62885-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="62885-105">Syntax</span></span>


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a><span data-ttu-id="62885-106">Member</span><span class="sxs-lookup"><span data-stu-id="62885-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="62885-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="62885-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="62885-108">Typ: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="62885-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="62885-109">Der Name des Frames.</span><span class="sxs-lookup"><span data-stu-id="62885-109">Name of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="62885-110">**Transformationmatrix**</span><span class="sxs-lookup"><span data-stu-id="62885-110">**TransformationMatrix**</span></span>
</dt> <dd>

<span data-ttu-id="62885-111">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="62885-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="62885-112">Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="62885-112">Transformation matrix.</span></span>

</dd> <dt>

<span data-ttu-id="62885-113">**pmeshcontainer**</span><span class="sxs-lookup"><span data-stu-id="62885-113">**pMeshContainer**</span></span>
</dt> <dd>

<span data-ttu-id="62885-114">Typ: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="62885-114">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

</dd> <dd>

<span data-ttu-id="62885-115">Zeiger auf den Mesh-Container.</span><span class="sxs-lookup"><span data-stu-id="62885-115">Pointer to the mesh container.</span></span>

</dd> <dt>

<span data-ttu-id="62885-116">**pframesierend**</span><span class="sxs-lookup"><span data-stu-id="62885-116">**pFrameSibling**</span></span>
</dt> <dd>

<span data-ttu-id="62885-117">Typ: \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="62885-117">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="62885-118">Zeiger auf einen gleich geordneten Frame.</span><span class="sxs-lookup"><span data-stu-id="62885-118">Pointer to a sibling frame.</span></span>

</dd> <dt>

<span data-ttu-id="62885-119">**pframefirstchild**</span><span class="sxs-lookup"><span data-stu-id="62885-119">**pFrameFirstChild**</span></span>
</dt> <dd>

<span data-ttu-id="62885-120">Typ: \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="62885-120">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="62885-121">Zeiger auf einen untergeordneten Frame.</span><span class="sxs-lookup"><span data-stu-id="62885-121">Pointer to a child frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62885-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62885-122">Remarks</span></span>

<span data-ttu-id="62885-123">Eine Anwendung kann von dieser Struktur abgeleitet werden, um weitere Daten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="62885-123">An application can derive from this structure to add other data.</span></span>

## <a name="requirements"></a><span data-ttu-id="62885-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62885-124">Requirements</span></span>



| <span data-ttu-id="62885-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62885-125">Requirement</span></span> | <span data-ttu-id="62885-126">Wert</span><span class="sxs-lookup"><span data-stu-id="62885-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62885-127">Header</span><span class="sxs-lookup"><span data-stu-id="62885-127">Header</span></span><br/> | <dl> <span data-ttu-id="62885-128"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="62885-128"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62885-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62885-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62885-130">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="62885-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




