---
description: Liefert Operator Überladungen und Typumwandlungen für D3DXFLOAT16-Strukturen.
ms.assetid: d287efb5-d15e-46dc-924d-012e1a108efc
title: D3DXFLOAT16 Extensions (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f97e8917f453e7c2c2db99b8f894d557d7b7909f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050852"
---
# <a name="d3dxfloat16-extensions"></a><span data-ttu-id="a66bd-103">D3DXFLOAT16-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="a66bd-103">D3DXFLOAT16 Extensions</span></span>

<span data-ttu-id="a66bd-104">Liefert Operator Überladungen und Typumwandlungen für [**D3DXFLOAT16**](d3dxfloat16.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="a66bd-104">Supplies operator overloads and type casts for [**D3DXFLOAT16**](d3dxfloat16.md) structures.</span></span>

``` syntax
typedef struct D3DXFLOAT16
{
#ifdef __cplusplus
public:
    D3DXFLOAT16() {};
    D3DXFLOAT16( FLOAT );
    D3DXFLOAT16( CONST D3DXFLOAT16& );

    // casting
    operator FLOAT ();

    // binary operators
    BOOL operator == ( CONST D3DXFLOAT16& ) const;
    BOOL operator != ( CONST D3DXFLOAT16& ) const;

protected:
#endif //__cplusplus
    WORD value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```

<span data-ttu-id="a66bd-105">Abgeleitete Typen: \* LPD3DXFLOAT16</span><span class="sxs-lookup"><span data-stu-id="a66bd-105">Derived types: \*LPD3DXFLOAT16</span></span>

## <a name="members"></a><span data-ttu-id="a66bd-106">Member</span><span class="sxs-lookup"><span data-stu-id="a66bd-106">Members</span></span>

<span data-ttu-id="a66bd-107">Weitere Informationen zu Strukturmembern finden Sie unter D3DXFLOAT16.</span><span class="sxs-lookup"><span data-stu-id="a66bd-107">For more information about structure members, refer to D3DXFLOAT16.</span></span>

## <a name="remarks"></a><span data-ttu-id="a66bd-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a66bd-108">Remarks</span></span>

<span data-ttu-id="a66bd-109">Operator Überladungen und Typumwandlungen für diese Struktur werden in d3dx9math. INL implementiert.</span><span class="sxs-lookup"><span data-stu-id="a66bd-109">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

## <a name="requirements"></a><span data-ttu-id="a66bd-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a66bd-110">Requirements</span></span>



| <span data-ttu-id="a66bd-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a66bd-111">Requirement</span></span> | <span data-ttu-id="a66bd-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a66bd-112">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a66bd-113">Header</span><span class="sxs-lookup"><span data-stu-id="a66bd-113">Header</span></span><br/> | <dl> <span data-ttu-id="a66bd-114"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a66bd-114"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a66bd-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a66bd-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a66bd-116">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a66bd-116">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




