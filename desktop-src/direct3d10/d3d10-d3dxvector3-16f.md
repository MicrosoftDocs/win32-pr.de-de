---
description: Identisch mit D3DXVECTOR3, verwendet jedoch 16-Bit-Gleit Komma Werte für x, y und z.
ms.assetid: b21676f1-5cff-4eef-bd60-5c09882283dc
title: D3DXVECTOR3_16F-Struktur (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR3_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: b7143e864eddf37842e19d7554150beaf50c0b53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961574"
---
# <a name="d3dxvector3_16f-structure"></a><span data-ttu-id="df6af-103">D3DXVECTOR3 \_ 16f-Struktur</span><span class="sxs-lookup"><span data-stu-id="df6af-103">D3DXVECTOR3\_16F structure</span></span>

<span data-ttu-id="df6af-104">Identisch mit [**D3DXVECTOR3**](d3d10-d3dxvector3.md), verwendet jedoch 16-Bit-Gleit Komma Werte für x, y und z.</span><span class="sxs-lookup"><span data-stu-id="df6af-104">Same as a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), but it uses 16-bit floating point values for x, y, and z.</span></span>

## <a name="syntax"></a><span data-ttu-id="df6af-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df6af-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR3_16F {
  FLOAT x;
  FLOAT y;
  FLOAT z;
} D3DXVECTOR3_16F, *LPD3DXVECTOR3_16F;
```



## <a name="members"></a><span data-ttu-id="df6af-106">Member</span><span class="sxs-lookup"><span data-stu-id="df6af-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="df6af-107">**x**</span><span class="sxs-lookup"><span data-stu-id="df6af-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="df6af-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df6af-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="df6af-109">Die x-Komponente.</span><span class="sxs-lookup"><span data-stu-id="df6af-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="df6af-110">**y**</span><span class="sxs-lookup"><span data-stu-id="df6af-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="df6af-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df6af-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="df6af-112">Die y-Komponente.</span><span class="sxs-lookup"><span data-stu-id="df6af-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="df6af-113">**z**</span><span class="sxs-lookup"><span data-stu-id="df6af-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="df6af-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df6af-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="df6af-115">Die z-Komponente.</span><span class="sxs-lookup"><span data-stu-id="df6af-115">The z-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df6af-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df6af-116">Remarks</span></span>

<span data-ttu-id="df6af-117">**D3DXVECTOR3 \_ 16f** verfügt über die folgenden C++-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="df6af-117">**D3DXVECTOR3\_16F** has the following C++ extensions.</span></span>

### <a name="d3dxvector3_16f-extensions"></a><span data-ttu-id="df6af-118">D3DXVECTOR3 \_ 16f-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="df6af-118">D3DXVECTOR3\_16F Extensions</span></span>


```

typedef struct D3DXVECTOR3_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR3_16F() {};
    D3DXVECTOR3_16F( CONST FLOAT * );
    D3DXVECTOR3_16F( CONST D3DVECTOR& );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 &x, CONST D3DXFLOAT16 &y, CONST D3DXFLOAT16 &z );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR3_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR3_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y, z;

} D3DXVECTOR3_16F, *LPD3DXVECTOR3_16F;
```



## <a name="requirements"></a><span data-ttu-id="df6af-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df6af-119">Requirements</span></span>



| <span data-ttu-id="df6af-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df6af-120">Requirement</span></span> | <span data-ttu-id="df6af-121">Wert</span><span class="sxs-lookup"><span data-stu-id="df6af-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df6af-122">Header</span><span class="sxs-lookup"><span data-stu-id="df6af-122">Header</span></span><br/> | <dl> <span data-ttu-id="df6af-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="df6af-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df6af-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df6af-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6af-125">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="df6af-125">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
