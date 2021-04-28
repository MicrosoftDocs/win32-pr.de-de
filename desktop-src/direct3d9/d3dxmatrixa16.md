---
description: 'D3DXMATRIXA16-Struktur (D3dx9math.h): Eine 4x4-, 16-Byte-ausgerichtete Matrix, die Methoden und Operatorüberladungen enthält.'
ms.assetid: c7082fe5-f98b-4ab7-b8c2-7cdbab4848ad
title: D3DXMATRIXA16-Struktur (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIXA16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 7bb14f23d041ec2634b9710d5620382d8b93da2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094208"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a><span data-ttu-id="79f1a-103">D3DXMATRIXA16-Struktur (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="79f1a-103">D3DXMATRIXA16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="79f1a-104">Eine 4x4-, 16-Byte-ausgerichtete Matrix, die Methoden und Operatorüberladungen enthält.</span><span class="sxs-lookup"><span data-stu-id="79f1a-104">A 4x4, 16-byte-aligned matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="79f1a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79f1a-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a><span data-ttu-id="79f1a-106">Member</span><span class="sxs-lookup"><span data-stu-id="79f1a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="79f1a-107">**\_Ij**</span><span class="sxs-lookup"><span data-stu-id="79f1a-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="79f1a-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79f1a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="79f1a-109">Die Komponente (i, j) der Matrix, wobei i die Zeilennummer und j die Spaltennummer ist.</span><span class="sxs-lookup"><span data-stu-id="79f1a-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="79f1a-110">34 bedeutet z. \_ B. das gleiche wie \[ a₃₄ \] , die Komponente in der dritten Zeile und vierten Spalte.</span><span class="sxs-lookup"><span data-stu-id="79f1a-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79f1a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79f1a-111">Remarks</span></span>

<span data-ttu-id="79f1a-112">Eine 16-Byte-ausgerichtete Matrix, die von mathematischen D3DX-Funktionen verwendet wird, wurde für eine verbesserte Leistung auf Intel Pentium 4-Prozessoren optimiert.</span><span class="sxs-lookup"><span data-stu-id="79f1a-112">A 16-byte aligned matrix, when used by D3DX math functions, has been optimized for improved performance on Intel Pentium 4 processors.</span></span> <span data-ttu-id="79f1a-113">Matrizen werden unabhängig davon ausgerichtet, wo sie erstellt werden: auf dem Programmstapel, im Heap oder im globalen Bereich.</span><span class="sxs-lookup"><span data-stu-id="79f1a-113">Matrices are aligned independent of where they are created: on the program stack, in the heap, or in global scope.</span></span> <span data-ttu-id="79f1a-114">Die Ausrichtung erfolgt mit \_ \_ declspec(align(16)), die nur mit Visual C++ .NET und mit Visual C++ 6.0 funktioniert, wenn das Prozessorpaket installiert ist.</span><span class="sxs-lookup"><span data-stu-id="79f1a-114">Alignment is accomplished using \_\_declspec(align(16)), which works with Visual C++ .NET and with Visual C++ 6.0 only when the processor pack is installed.</span></span> <span data-ttu-id="79f1a-115">Leider gibt es keine Möglichkeit, das Prozessorpaket zu erkennen, sodass die Byteausrichtung standardmäßig nur mit Visual C++ .NET aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="79f1a-115">Unfortunately, there is no way to detect the processor pack, so byte alignment is turned on by default only with Visual C++ .NET.</span></span>

<span data-ttu-id="79f1a-116">Vektoren und Quaternionen werden in D3DX nicht bytebündig ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="79f1a-116">Vectors and quaternions are not byte aligned in D3DX.</span></span> <span data-ttu-id="79f1a-117">Wenn Sie Vektoren und Quaternionen mit mathematischen D3DX-Funktionen verwenden, verwenden Sie \_ declspec(align(16)), um bytebündige Vektoren und Quaternionen zu generieren, da sie erheblich besser funktionieren.</span><span class="sxs-lookup"><span data-stu-id="79f1a-117">When using vectors and quaternions with D3DX math functions, use \_declspec(align(16)) to generate byte aligned vectors and quaternions, because they will perform significantly better.</span></span> <span data-ttu-id="79f1a-118">Die Definition von \_ declspec ist hier dargestellt.</span><span class="sxs-lookup"><span data-stu-id="79f1a-118">The definition of \_declspec is shown here.</span></span>


```
#define D3DX_ALIGN16 __declspec(align(16))
```



<span data-ttu-id="79f1a-119">Andere Compiler interpretieren D3DXMATRIXA16 als D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="79f1a-119">Other compilers interpret D3DXMATRIXA16 as D3DXMATRIX.</span></span> <span data-ttu-id="79f1a-120">Die Verwendung dieser Struktur auf einem Compiler, der die Matrix nicht tatsächlich ausrichtet, kann problematisch sein, da sie keine Fehler verfügbar macht, die die Ausrichtung ignorieren.</span><span class="sxs-lookup"><span data-stu-id="79f1a-120">Using this structure on a compiler that does not actually align the matrix can be problematic because it will not expose bugs that ignore alignment.</span></span> <span data-ttu-id="79f1a-121">Wenn sich z. B. ein D3DXMATRIXA16-Objekt innerhalb einer Struktur oder Klasse befindet, kann ein [**Memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) mit engem Packen (ohne 16-Byte-Grenzen) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="79f1a-121">For example, if a D3DXMATRIXA16 object is inside a structure or class, a [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) might be done with tight packing (ignoring 16-byte boundaries).</span></span> <span data-ttu-id="79f1a-122">Dies würde zu Buildunterbrechungen führen, wenn der Compiler irgendwann eine Matrixausrichtung hinzufügen würde.</span><span class="sxs-lookup"><span data-stu-id="79f1a-122">This would cause build breaks if the compiler were to sometime add matrix aligning.</span></span>

### <a name="d3dxmatrixa16"></a><span data-ttu-id="79f1a-123">D3DXMATRIXA16</span><span class="sxs-lookup"><span data-stu-id="79f1a-123">D3DXMATRIXA16</span></span>

<span data-ttu-id="79f1a-124">**D3DXMATRIXA16 verfügt** über die folgenden C++-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="79f1a-124">**D3DXMATRIXA16** has the following C++ extensions.</span></span>


```
typedef struct _D3DXMATRIXA16 : public D3DXMATRIX
{
    _D3DXMATRIXA16();
    _D3DXMATRIXA16( CONST FLOAT * f);
    _D3DXMATRIXA16( CONST D3DMATRIX& m);
    _D3DXMATRIXA16( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                    FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                    FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                    FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );
    void* operator new(size_t s);
    void* operator new[](size_t s);

    // The two operators below are not virtual operators. If you cast
    //   to D3DXMATRIX, do not delete using them
    void operator delete(void* p);
    void operator delete[](void* p);

    struct _D3DXMATRIXA16& operator=(CONST D3DXMATRIX& rhs);
} _D3DXMATRIXA16;

typedef D3DX_ALIGN16 _D3DXMATRIXA16 D3DXMATRIXA16, *LPD3DXMATRIXA16;
        
```



## <a name="requirements"></a><span data-ttu-id="79f1a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79f1a-125">Requirements</span></span>



| <span data-ttu-id="79f1a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79f1a-126">Requirement</span></span> | <span data-ttu-id="79f1a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="79f1a-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79f1a-128">Header</span><span class="sxs-lookup"><span data-stu-id="79f1a-128">Header</span></span><br/> | <dl> <span data-ttu-id="79f1a-129"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="79f1a-129"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79f1a-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="79f1a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f1a-131">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="79f1a-131">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="79f1a-132">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="79f1a-132">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> </dl>

 

 
