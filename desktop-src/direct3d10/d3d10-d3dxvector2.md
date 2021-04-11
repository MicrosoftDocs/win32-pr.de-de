---
description: Beschreibt einen Vektor mit zwei Komponenten, einschließlich Operator Überladungen und Typumwandlungen.
ms.assetid: 5b7b4847-b994-48c6-ae3c-e48ee1716ddd
title: D3DXVECTOR2-Struktur (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR2
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 860c7ddaba61adcd93a38469117b2a95779240a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219618"
---
# <a name="d3dxvector2-structure-d3dx10mathh"></a><span data-ttu-id="30ba0-103">D3DXVECTOR2-Struktur (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="30ba0-103">D3DXVECTOR2 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="30ba0-104">Beschreibt einen Vektor mit zwei Komponenten, einschließlich Operator Überladungen und Typumwandlungen.</span><span class="sxs-lookup"><span data-stu-id="30ba0-104">Describes a two-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ba0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="30ba0-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR2 {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
```



## <a name="members"></a><span data-ttu-id="30ba0-106">Member</span><span class="sxs-lookup"><span data-stu-id="30ba0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="30ba0-107">**x**</span><span class="sxs-lookup"><span data-stu-id="30ba0-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="30ba0-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30ba0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="30ba0-109">Die x-Komponente.</span><span class="sxs-lookup"><span data-stu-id="30ba0-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="30ba0-110">**y**</span><span class="sxs-lookup"><span data-stu-id="30ba0-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="30ba0-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30ba0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="30ba0-112">Die y-Komponente.</span><span class="sxs-lookup"><span data-stu-id="30ba0-112">The y-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30ba0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30ba0-113">Remarks</span></span>

<span data-ttu-id="30ba0-114">**D3DXVECTOR2** verfügt über die folgenden C++-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="30ba0-114">**D3DXVECTOR2** has the following C++ extensions.</span></span>

### <a name="d3dxvector2-extensions"></a><span data-ttu-id="30ba0-115">D3DXVECTOR2-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="30ba0-115">D3DXVECTOR2 Extensions</span></span>


```
typedef struct D3DXVECTOR2
{
#ifdef __cplusplus
public:
    D3DXVECTOR2() {};
    D3DXVECTOR2( CONST FLOAT * );
    D3DXVECTOR2( CONST D3DXFLOAT16 * );
    D3DXVECTOR2( FLOAT x, FLOAT y );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR2& operator += ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator -= ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator *= ( FLOAT );
    D3DXVECTOR2& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR2 operator + () const;
    D3DXVECTOR2 operator - () const;

    // binary operators
    D3DXVECTOR2 operator + ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator - ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator * ( FLOAT ) const;
    D3DXVECTOR2 operator / ( FLOAT ) const;

    friend D3DXVECTOR2 operator * ( FLOAT, CONST D3DXVECTOR2& );

    BOOL operator == ( CONST D3DXVECTOR2& ) const;
    BOOL operator != ( CONST D3DXVECTOR2& ) const;


public:
#endif //__cplusplus
    FLOAT x, y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
        
```



## <a name="requirements"></a><span data-ttu-id="30ba0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30ba0-116">Requirements</span></span>



| <span data-ttu-id="30ba0-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30ba0-117">Requirement</span></span> | <span data-ttu-id="30ba0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="30ba0-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30ba0-119">Header</span><span class="sxs-lookup"><span data-stu-id="30ba0-119">Header</span></span><br/> | <dl> <span data-ttu-id="30ba0-120"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="30ba0-120"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30ba0-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30ba0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ba0-122">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="30ba0-122">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
