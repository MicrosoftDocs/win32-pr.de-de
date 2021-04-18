---
description: Beschreibt eine Matrix.
ms.assetid: d6b98a32-e745-4724-b8ce-a81a3f5416f3
title: D3DMATRIX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6b4339d2e44e1add46103bae58ad3e02c8a6509b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354378"
---
# <a name="d3dmatrix"></a><span data-ttu-id="9b3f2-103">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="9b3f2-103">D3DMATRIX</span></span>

<span data-ttu-id="9b3f2-104">Beschreibt eine Matrix.</span><span class="sxs-lookup"><span data-stu-id="9b3f2-104">Describes a matrix.</span></span>

``` syntax
typedef struct _D3DMATRIX {
    union {
        struct {
            float        _11, _12, _13, _14;
            float        _21, _22, _23, _24;
            float        _31, _32, _33, _34;
            float        _41, _42, _43, _44;

        };
        float m[4][4];
    };
} D3DMATRIX;
```

<span data-ttu-id="9b3f2-105">Abgeleitete Typen: \* LPD3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="9b3f2-105">Derived types: \*LPD3DMATRIX</span></span>

## <a name="members"></a><span data-ttu-id="9b3f2-106">Member</span><span class="sxs-lookup"><span data-stu-id="9b3f2-106">Members</span></span>



| <span data-ttu-id="9b3f2-107">Element</span><span class="sxs-lookup"><span data-stu-id="9b3f2-107">Item</span></span>                                                        | <span data-ttu-id="9b3f2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b3f2-108">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b3f2-109"><span id="_ij"></span><span id="_IJ"></span>\_angesprochenen</span><span class="sxs-lookup"><span data-stu-id="9b3f2-109"><span id="_ij"></span><span id="_IJ"></span>\_ij</span></span><br/> | <span data-ttu-id="9b3f2-110">Ein Array von Gleit Komma Zahlen, die eine 4 x 4-Matrix darstellen, bei der es sich um die Zeilennummer und j um die Spaltennummer handelt.</span><span class="sxs-lookup"><span data-stu-id="9b3f2-110">An array of floats that represent a 4x4 matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="9b3f2-111">34 bedeutet beispielsweise, dass das \_ gleiche wie \[ ein ₃ ₄ \] , die Komponente in der dritten Zeile und vierten Spalte ist.</span><span class="sxs-lookup"><span data-stu-id="9b3f2-111">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9b3f2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b3f2-112">Remarks</span></span>

<span data-ttu-id="9b3f2-113">In Direct3D kann das \_ 34-Element einer Projektions Matrix keine negative Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="9b3f2-113">In Direct3D, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="9b3f2-114">Wenn die Anwendung an diesem Speicherort einen negativen Wert verwenden muss, sollte Sie stattdessen die gesamte Projektions Matrix um-1 skalieren.</span><span class="sxs-lookup"><span data-stu-id="9b3f2-114">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b3f2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b3f2-115">Requirements</span></span>



| <span data-ttu-id="9b3f2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b3f2-116">Requirement</span></span> | <span data-ttu-id="9b3f2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9b3f2-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b3f2-118">Header</span><span class="sxs-lookup"><span data-stu-id="9b3f2-118">Header</span></span><br/> | <dl> <span data-ttu-id="9b3f2-119"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b3f2-119"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b3f2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b3f2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b3f2-121">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9b3f2-121">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="9b3f2-122">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="9b3f2-122">**GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="9b3f2-123">**MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="9b3f2-123">**MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="9b3f2-124">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="9b3f2-124">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

<span data-ttu-id="9b3f2-125">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="9b3f2-125">**SetTransform**</span></span>
</dt> <dt>

[<span data-ttu-id="9b3f2-126">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="9b3f2-126">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> <dt>

[<span data-ttu-id="9b3f2-127">Transformationen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9b3f2-127">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
