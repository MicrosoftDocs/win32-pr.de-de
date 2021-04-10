---
description: Eine 4 x 4-Matrix mit 16 Bytes, die Methoden und Operator Überladungen enthält.
ms.assetid: d9e9c1cc-7555-4011-a4b4-8cce20404841
title: D3DXMATRIXA16-Struktur (D3DX10Math. h)
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
- D3DX10Math.h
ms.openlocfilehash: a33b5efa0e5e714c0b161fed8191702066a44b01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219666"
---
# <a name="d3dxmatrixa16-structure-d3dx10mathh"></a><span data-ttu-id="af802-103">D3DXMATRIXA16-Struktur (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="af802-103">D3DXMATRIXA16 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="af802-104">Eine 4 x 4-Matrix mit 16 Bytes, die Methoden und Operator Überladungen enthält.</span><span class="sxs-lookup"><span data-stu-id="af802-104">A 4x4, 16-byte-aligned matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="af802-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="af802-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a><span data-ttu-id="af802-106">Member</span><span class="sxs-lookup"><span data-stu-id="af802-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="af802-107">**\_angesprochenen**</span><span class="sxs-lookup"><span data-stu-id="af802-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="af802-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af802-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af802-109">Die Komponente (i, j) der Matrix, bei der es sich um die Zeilennummer und j um die Spaltennummer handelt.</span><span class="sxs-lookup"><span data-stu-id="af802-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="af802-110">34 bedeutet beispielsweise, dass das \_ gleiche wie \[ ein ₃ ₄ \] , die Komponente in der dritten Zeile und vierten Spalte ist.</span><span class="sxs-lookup"><span data-stu-id="af802-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af802-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af802-111">Remarks</span></span>

<span data-ttu-id="af802-112">Bei der Verwendung durch D3DX Math-Funktionen wurde eine aus 16 Bytes ausgerichtete Matrix optimiert, um die Leistung von Intel Pentium 4-Prozessoren zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="af802-112">A 16-byte aligned matrix, when used by D3DX math functions, has been optimized for improved performance on Intel Pentium 4 processors.</span></span> <span data-ttu-id="af802-113">Matrizen werden unabhängig von ihrem Speicherort ausgerichtet: auf dem Programm Stapel, im Heap oder im globalen Gültigkeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="af802-113">Matrices are aligned independent of where they are created: on the program stack, in the heap, or in global scope.</span></span> <span data-ttu-id="af802-114">Die Ausrichtung erfolgt mithilfe \_ \_ von "declspec (align (16))", die mit Visual C++ .net und nur mit Visual C++ 6,0 funktioniert, wenn das Prozessor Paket installiert ist.</span><span class="sxs-lookup"><span data-stu-id="af802-114">Alignment is accomplished using \_\_declspec(align(16)), which works with Visual C++ .NET and with Visual C++ 6.0 only when the processor pack is installed.</span></span> <span data-ttu-id="af802-115">Leider gibt es keine Möglichkeit, das Prozessor Paket zu erkennen, sodass die Byte Ausrichtung standardmäßig nur mit Visual C++ .NET aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="af802-115">Unfortunately, there is no way to detect the processor pack, so byte alignment is turned on by default only with Visual C++ .NET.</span></span>

<span data-ttu-id="af802-116">Vektoren und Quaternionen sind in D3DX nicht Byte bündig ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="af802-116">Vectors and quaternions are not byte aligned in D3DX.</span></span> <span data-ttu-id="af802-117">Wenn Sie Vektoren und Quaternionen mit D3DX Math-Funktionen verwenden, verwenden \_ Sie declspec (align (16)), um Byte ausgerichtete Vektoren und Quaternionen zu generieren, da Sie erheblich besser funktionieren.</span><span class="sxs-lookup"><span data-stu-id="af802-117">When using vectors and quaternions with D3DX math functions, use \_declspec(align(16)) to generate byte aligned vectors and quaternions, because they will perform significantly better.</span></span> <span data-ttu-id="af802-118">Die Definition von \_ declspec wird hier dargestellt.</span><span class="sxs-lookup"><span data-stu-id="af802-118">The definition of \_declspec is shown here.</span></span>


```
#define D3DX_ALIGN16 __declspec(align(16))
```



<span data-ttu-id="af802-119">Andere Compiler interpretieren **D3DXMATRIXA16** als [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="af802-119">Other compilers interpret **D3DXMATRIXA16** as [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span> <span data-ttu-id="af802-120">Die Verwendung dieser Struktur für einen Compiler, der die Matrix nicht tatsächlich ausgerichtet, kann problematisch sein, da Sie keine Fehler verfügbar macht, die die Ausrichtung ignorieren.</span><span class="sxs-lookup"><span data-stu-id="af802-120">Using this structure on a compiler that does not actually align the matrix can be problematic because it will not expose bugs that ignore alignment.</span></span> <span data-ttu-id="af802-121">Wenn sich z. b. ein **D3DXMATRIXA16** -Objekt innerhalb einer Struktur oder Klasse befindet, wird eine [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) möglicherweise mit einer dichten Verpackung ausgeführt (wobei 16-Byte-Begrenzungen ignoriert werden).</span><span class="sxs-lookup"><span data-stu-id="af802-121">For example, if a **D3DXMATRIXA16** object is inside a structure or class, a [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) might be done with tight packing (ignoring 16-byte boundaries).</span></span> <span data-ttu-id="af802-122">Dies würde zu Buildunterbrechungen führen, wenn der Compiler einige aufeinander folgende Matrizen hinzufügen würde.</span><span class="sxs-lookup"><span data-stu-id="af802-122">This would cause build breaks if the compiler were to sometime add matrix aligning.</span></span>

### <a name="d3dxmatrixa16-extensions"></a><span data-ttu-id="af802-123">D3DXMATRIXA16-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="af802-123">D3DXMATRIXA16 Extensions</span></span>

<span data-ttu-id="af802-124">**D3DXMATRIXA16** verfügt über die folgenden C++-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="af802-124">**D3DXMATRIXA16** has the following C++ extensions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="af802-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af802-125">Requirements</span></span>



| <span data-ttu-id="af802-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af802-126">Requirement</span></span> | <span data-ttu-id="af802-127">Wert</span><span class="sxs-lookup"><span data-stu-id="af802-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af802-128">Header</span><span class="sxs-lookup"><span data-stu-id="af802-128">Header</span></span><br/> | <dl> <span data-ttu-id="af802-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="af802-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af802-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af802-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af802-131">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="af802-131">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
