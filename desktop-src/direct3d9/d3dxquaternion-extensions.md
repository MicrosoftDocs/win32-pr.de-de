---
description: Stellt die folgenden Operator Überladungen und Typumwandlungen für D3DXQUATERNION-Strukturen bereit.
ms.assetid: a49975a4-a9a7-4183-91b3-3d56f70747ef
title: D3DXQUATERNION Extensions (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: a937dcf23f894d094fb5f6cc75a765b1d563a1b7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353352"
---
# <a name="d3dxquaternion-extensions"></a><span data-ttu-id="45d44-103">D3DXQUATERNION-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="45d44-103">D3DXQUATERNION Extensions</span></span>

<span data-ttu-id="45d44-104">Stellt die folgenden Operator Überladungen und Typumwandlungen für [**D3DXQUATERNION**](d3dxquaternion.md) -Strukturen bereit.</span><span class="sxs-lookup"><span data-stu-id="45d44-104">Supplies the following operator overloads and type casts for [**D3DXQUATERNION**](d3dxquaternion.md) structures.</span></span>

``` syntax
typedef struct D3DXQUATERNION
{
#ifdef __cplusplus
public:
    D3DXQUATERNION() {}
    D3DXQUATERNION( CONST FLOAT * );
    D3DXQUATERNION( CONST D3DXFLOAT16 * );
    D3DXQUATERNION( FLOAT x, FLOAT y, FLOAT z, FLOAT w );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXQUATERNION& operator += ( CONST D3DXQUATERNION& );
    D3DXQUATERNION& operator -= ( CONST D3DXQUATERNION& );
    D3DXQUATERNION& operator *= ( CONST D3DXQUATERNION& );
    D3DXQUATERNION& operator *= ( FLOAT );
    D3DXQUATERNION& operator /= ( FLOAT );

    // unary operators
    D3DXQUATERNION  operator + () const;
    D3DXQUATERNION  operator - () const;

    // binary operators
    D3DXQUATERNION operator + ( CONST D3DXQUATERNION& ) const;
    D3DXQUATERNION operator - ( CONST D3DXQUATERNION& ) const;
    D3DXQUATERNION operator * ( CONST D3DXQUATERNION& ) const;
    D3DXQUATERNION operator * ( FLOAT ) const;
    D3DXQUATERNION operator / ( FLOAT ) const;

    friend D3DXQUATERNION operator * (FLOAT, CONST D3DXQUATERNION& );

    BOOL operator == ( CONST D3DXQUATERNION& ) const;
    BOOL operator != ( CONST D3DXQUATERNION& ) const;

#endif //__cplusplus
    FLOAT x, y, z, w;
} D3DXQUATERNION, *LPD3DXQUATERNION;

```

<span data-ttu-id="45d44-105">Abgeleitete Typen: \* LPD3DXQUATERNION</span><span class="sxs-lookup"><span data-stu-id="45d44-105">Derived types: \*LPD3DXQUATERNION</span></span>

## <a name="remarks"></a><span data-ttu-id="45d44-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45d44-106">Remarks</span></span>

<span data-ttu-id="45d44-107">Weitere Informationen zu Strukturmembern finden Sie unter [**D3DXQUATERNION**](d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="45d44-107">For more information about structure members, refer to [**D3DXQUATERNION**](d3dxquaternion.md).</span></span>

<span data-ttu-id="45d44-108">Operator Überladungen und Typumwandlungen für diese Struktur werden in d3dx9math. INL implementiert.</span><span class="sxs-lookup"><span data-stu-id="45d44-108">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

## <a name="requirements"></a><span data-ttu-id="45d44-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45d44-109">Requirements</span></span>



| <span data-ttu-id="45d44-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45d44-110">Requirement</span></span> | <span data-ttu-id="45d44-111">Wert</span><span class="sxs-lookup"><span data-stu-id="45d44-111">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45d44-112">Header</span><span class="sxs-lookup"><span data-stu-id="45d44-112">Header</span></span><br/> | <dl> <span data-ttu-id="45d44-113"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="45d44-113"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45d44-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45d44-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d44-115">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="45d44-115">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




