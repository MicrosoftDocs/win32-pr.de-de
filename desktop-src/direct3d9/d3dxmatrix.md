---
description: 'D3DXMATRIX-Struktur (D3dx9math.h): Eine 4x4-Matrix, die Methoden und Operatorüberladungen enthält.'
ms.assetid: 0911088b-50cf-4c4a-996e-351386fc359b
title: D3DXMATRIX-Struktur (D3dx9math.h)
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
- d3dx9math.h
ms.openlocfilehash: fad44c13f7b856270fe6475f9e099f6e1714e064
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094218"
---
# <a name="d3dxmatrix-structure-d3dx9mathh"></a><span data-ttu-id="2b4c4-103">D3DXMATRIX-Struktur (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="2b4c4-103">D3DXMATRIX structure (D3dx9math.h)</span></span>

<span data-ttu-id="2b4c4-104">Eine 4x4-Matrix, die Methoden und Operatorüberladungen enthält.</span><span class="sxs-lookup"><span data-stu-id="2b4c4-104">A 4x4 matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b4c4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b4c4-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a><span data-ttu-id="2b4c4-106">Member</span><span class="sxs-lookup"><span data-stu-id="2b4c4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2b4c4-107">**\_Ij**</span><span class="sxs-lookup"><span data-stu-id="2b4c4-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="2b4c4-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b4c4-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2b4c4-109">Die Komponente (i, j) der Matrix, wobei i die Zeilennummer und j die Spaltennummer ist.</span><span class="sxs-lookup"><span data-stu-id="2b4c4-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="2b4c4-110">34 bedeutet z. B. dasselbe wie a₃₄ , die Komponente in der \_ dritten Zeile und vierten \[ \] Spalte.</span><span class="sxs-lookup"><span data-stu-id="2b4c4-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b4c4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b4c4-111">Remarks</span></span>

<span data-ttu-id="2b4c4-112">C-Programmierer können die D3DXMATRIX-Struktur nicht verwenden. Sie müssen die [**D3DMATRIX-Struktur**](d3dmatrix.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b4c4-112">C programmers cannot use the D3DXMATRIX structure, they must use the [**D3DMATRIX**](d3dmatrix.md) structure.</span></span> <span data-ttu-id="2b4c4-113">C++-Programmierer können überladene Konstruktoren und Zuweisungsoperatoren, unäre operatoren und binäre Operatoren (einschließlich Gleichheit) nutzen.</span><span class="sxs-lookup"><span data-stu-id="2b4c4-113">C++ programmers can take advantage of overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

<span data-ttu-id="2b4c4-114">In D3DX darf \_ das 34-Element einer Projektionsmatrix keine negative Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="2b4c4-114">In D3DX, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="2b4c4-115">Wenn Ihre Anwendung an dieser Position einen negativen Wert verwenden muss, sollte sie stattdessen die gesamte Projektionsmatrix um -1 skalieren.</span><span class="sxs-lookup"><span data-stu-id="2b4c4-115">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

### <a name="d3dxmatrix-extensions"></a><span data-ttu-id="2b4c4-116">D3DXMATRIX-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="2b4c4-116">D3DXMATRIX Extensions</span></span>

<span data-ttu-id="2b4c4-117">**D3DXMATRIX verfügt** über die folgenden C++-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="2b4c4-117">**D3DXMATRIX** has the following C++ extensions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2b4c4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b4c4-118">Requirements</span></span>



| <span data-ttu-id="2b4c4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b4c4-119">Requirement</span></span> | <span data-ttu-id="2b4c4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2b4c4-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b4c4-121">Header</span><span class="sxs-lookup"><span data-stu-id="2b4c4-121">Header</span></span><br/> | <dl> <span data-ttu-id="2b4c4-122"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2b4c4-122"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b4c4-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2b4c4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b4c4-124">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2b4c4-124">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="2b4c4-125">**D3DMATRIX**</span><span class="sxs-lookup"><span data-stu-id="2b4c4-125">**D3DMATRIX**</span></span>](d3dmatrix.md)
</dt> </dl>

 

 
