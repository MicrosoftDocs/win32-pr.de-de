---
description: 'D3DXMATRIX-Struktur (D3DX10Math.h): Eine 4x4-Matrix, die Methoden und Operatorüberladungen enthält.'
ms.assetid: c354d28b-bb08-41c5-bb59-90a912181f0f
title: D3DXMATRIX-Struktur (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIX
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ba1b9533fe5dfa2cfd163a1f92b34a43d7dbd741
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113228"
---
# <a name="d3dxmatrix-structure-d3dx10mathh"></a><span data-ttu-id="f8ac9-103">D3DXMATRIX-Struktur (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="f8ac9-103">D3DXMATRIX structure (D3DX10Math.h)</span></span>

<span data-ttu-id="f8ac9-104">Eine 4x4-Matrix, die Methoden und Operatorüberladungen enthält.</span><span class="sxs-lookup"><span data-stu-id="f8ac9-104">A 4x4 matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ac9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8ac9-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a><span data-ttu-id="f8ac9-106">Member</span><span class="sxs-lookup"><span data-stu-id="f8ac9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8ac9-107">**\_Ij**</span><span class="sxs-lookup"><span data-stu-id="f8ac9-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="f8ac9-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8ac9-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8ac9-109">Die Komponente (i, j) der Matrix, wobei i die Zeilennummer und j die Spaltennummer ist.</span><span class="sxs-lookup"><span data-stu-id="f8ac9-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="f8ac9-110">34 bedeutet z. \_ B. das gleiche wie \[ a₃₄ \] , die Komponente in der dritten Zeile und vierten Spalte.</span><span class="sxs-lookup"><span data-stu-id="f8ac9-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8ac9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8ac9-111">Remarks</span></span>

<span data-ttu-id="f8ac9-112">C-Programmierer können die D3DXMATRIX-Struktur nicht verwenden, sie müssen die D3DMATRIX-Struktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="f8ac9-112">C programmers cannot use the D3DXMATRIX structure, they must use the D3DMATRIX structure.</span></span> <span data-ttu-id="f8ac9-113">C++-Programmierer können überladene Konstruktoren und Zuweisungsoperatoren, unäre und binäre Operatoren (einschließlich Gleichheit) nutzen.</span><span class="sxs-lookup"><span data-stu-id="f8ac9-113">C++ programmers can take advantage of overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

<span data-ttu-id="f8ac9-114">In D3DX darf das \_ 34-Element einer Projektionsmatrix keine negative Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="f8ac9-114">In D3DX, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="f8ac9-115">Wenn Ihre Anwendung an dieser Position einen negativen Wert verwenden muss, sollte stattdessen die gesamte Projektionsmatrix um -1 skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="f8ac9-115">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

### <a name="d3dxmatrix-extensions"></a><span data-ttu-id="f8ac9-116">D3DXMATRIX-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="f8ac9-116">D3DXMATRIX Extensions</span></span>

<span data-ttu-id="f8ac9-117">**D3DXMATRIX** verfügt über die folgenden C++-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="f8ac9-117">**D3DXMATRIX** has the following C++ extensions.</span></span>


```
#ifdef __cplusplus
typedef struct D3DXMATRIX : public D3DMATRIX
{
public:
    D3DXMATRIX() {};
    D3DXMATRIX( CONST FLOAT * );
    D3DXMATRIX( CONST D3DMATRIX& );
    D3DXMATRIX( CONST D3DXFLOAT16 * );
    D3DXMATRIX( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );


    // access grants
    FLOAT& operator () ( UINT Row, UINT Col );
    FLOAT  operator () ( UINT Row, UINT Col ) const;

    // casting operators
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXMATRIX& operator *= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator += ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator -= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator *= ( FLOAT );
    D3DXMATRIX& operator /= ( FLOAT );

    // unary operators
    D3DXMATRIX operator + () const;
    D3DXMATRIX operator - () const;

    // binary operators
    D3DXMATRIX operator * ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator + ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator - ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator * ( FLOAT ) const;
    D3DXMATRIX operator / ( FLOAT ) const;

    friend D3DXMATRIX operator * ( FLOAT, CONST D3DXMATRIX& );

    BOOL operator == ( CONST D3DXMATRIX& ) const;
    BOOL operator != ( CONST D3DXMATRIX& ) const;

} D3DXMATRIX, *LPD3DXMATRIX;

#else //!__cplusplus
typedef struct _D3DMATRIX D3DXMATRIX, *LPD3DXMATRIX;
#endif //!__cplusplus
        
```



## <a name="requirements"></a><span data-ttu-id="f8ac9-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8ac9-118">Requirements</span></span>



| <span data-ttu-id="f8ac9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8ac9-119">Requirement</span></span> | <span data-ttu-id="f8ac9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f8ac9-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ac9-121">Header</span><span class="sxs-lookup"><span data-stu-id="f8ac9-121">Header</span></span><br/> | <dl> <span data-ttu-id="f8ac9-122"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f8ac9-122"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8ac9-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f8ac9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ac9-124">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f8ac9-124">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
