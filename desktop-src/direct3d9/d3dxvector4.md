---
description: Beschreibt einen Vektor mit vier Komponenten, einschließlich Operator Überladungen und Typumwandlungen.
ms.assetid: fbfe7851-7bec-4fa0-b4dc-52f5cb83d0a4
title: D3DXVECTOR4-Struktur (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR4
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 1647705877d5cacabbaeb79c4055de298e23b68f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394266"
---
# <a name="d3dxvector4-structure-d3dx9mathh"></a><span data-ttu-id="6edb5-103">D3DXVECTOR4-Struktur (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="6edb5-103">D3DXVECTOR4 structure (D3dx9math.h)</span></span>

<span data-ttu-id="6edb5-104">Beschreibt einen Vektor mit vier Komponenten, einschließlich Operator Überladungen und Typumwandlungen.</span><span class="sxs-lookup"><span data-stu-id="6edb5-104">Describes a four-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="6edb5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6edb5-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR4 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXVECTOR4, *LPD3DXVECTOR4;
```



## <a name="members"></a><span data-ttu-id="6edb5-106">Member</span><span class="sxs-lookup"><span data-stu-id="6edb5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6edb5-107">**x**</span><span class="sxs-lookup"><span data-stu-id="6edb5-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="6edb5-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6edb5-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6edb5-109">Die x-Komponente.</span><span class="sxs-lookup"><span data-stu-id="6edb5-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="6edb5-110">**y**</span><span class="sxs-lookup"><span data-stu-id="6edb5-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="6edb5-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6edb5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6edb5-112">Die y-Komponente.</span><span class="sxs-lookup"><span data-stu-id="6edb5-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="6edb5-113">**z**</span><span class="sxs-lookup"><span data-stu-id="6edb5-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="6edb5-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6edb5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6edb5-115">Die z-Komponente.</span><span class="sxs-lookup"><span data-stu-id="6edb5-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="6edb5-116">**w**</span><span class="sxs-lookup"><span data-stu-id="6edb5-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="6edb5-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6edb5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6edb5-118">Die w-Komponente.</span><span class="sxs-lookup"><span data-stu-id="6edb5-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6edb5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6edb5-119">Remarks</span></span>

### <a name="d3dxvector4-extensions"></a><span data-ttu-id="6edb5-120">D3DXVECTOR4-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="6edb5-120">D3DXVECTOR4 Extensions</span></span>

<span data-ttu-id="6edb5-121">D3DXVECTOR4 verfügt über die folgenden C++-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="6edb5-121">D3DXVECTOR4 has the following C++ extensions.</span></span>


```
typedef struct D3DXVECTOR4
{
#ifdef __cplusplus
public:
    D3DXVECTOR4() {};
    D3DXVECTOR4( CONST FLOAT* );
    D3DXVECTOR4( CONST D3DXFLOAT16 * );
    D3DXVECTOR4( CONST D3DVECTOR& xyz, FLOAT w );
    D3DXVECTOR4( FLOAT x, FLOAT y, FLOAT z, FLOAT w );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR4& operator += ( CONST D3DXVECTOR4& );
    D3DXVECTOR4& operator -= ( CONST D3DXVECTOR4& );
    D3DXVECTOR4& operator *= ( FLOAT );
    D3DXVECTOR4& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR4 operator + () const;
    D3DXVECTOR4 operator - () const;

    // binary operators
    D3DXVECTOR4 operator + ( CONST D3DXVECTOR4& ) const;
    D3DXVECTOR4 operator - ( CONST D3DXVECTOR4& ) const;
    D3DXVECTOR4 operator * ( FLOAT ) const;
    D3DXVECTOR4 operator / ( FLOAT ) const;

    friend D3DXVECTOR4 operator * ( FLOAT, CONST D3DXVECTOR4& );

    BOOL operator == ( CONST D3DXVECTOR4& ) const;
    BOOL operator != ( CONST D3DXVECTOR4& ) const;

public:
#endif //__cplusplus
    FLOAT x, y, z, w;
} D3DXVECTOR4, *LPD3DXVECTOR4;



typedef struct D3DXVECTOR4_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR4_16F() {};
    D3DXVECTOR4_16F( CONST FLOAT * );
    D3DXVECTOR4_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR4_16F( CONST D3DXVECTOR3_16F& xyz, CONST D3DXFLOAT16& w );
    D3DXVECTOR4_16F( CONST D3DXFLOAT16& x, CONST D3DXFLOAT16& y, CONST D3DXFLOAT16& z, CONST D3DXFLOAT16& w );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR4_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR4_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y, z, w;

} D3DXVECTOR4_16F, *LPD3DXVECTOR4_16F;
        
```



## <a name="requirements"></a><span data-ttu-id="6edb5-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6edb5-122">Requirements</span></span>



| <span data-ttu-id="6edb5-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6edb5-123">Requirement</span></span> | <span data-ttu-id="6edb5-124">Wert</span><span class="sxs-lookup"><span data-stu-id="6edb5-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6edb5-125">Header</span><span class="sxs-lookup"><span data-stu-id="6edb5-125">Header</span></span><br/> | <dl> <span data-ttu-id="6edb5-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6edb5-126"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6edb5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6edb5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6edb5-128">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="6edb5-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
