---
description: Stellt die folgenden Operator Überladungen und Typumwandlungen für D3DXCOLOR-Strukturen bereit.
ms.assetid: 89780c6f-c78b-4ebe-876a-6dbc37b598ef
title: D3DXCOLOR Extensions (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 7f457332f371b2c452a465c5b831774488301c6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870147"
---
# <a name="d3dxcolor-extensions"></a><span data-ttu-id="eadcd-103">D3DXCOLOR-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="eadcd-103">D3DXCOLOR Extensions</span></span>

<span data-ttu-id="eadcd-104">Stellt die folgenden Operator Überladungen und Typumwandlungen für [**D3DXCOLOR**](d3dxcolor.md) -Strukturen bereit.</span><span class="sxs-lookup"><span data-stu-id="eadcd-104">Supplies the following operator overloads and type casts for [**D3DXCOLOR**](d3dxcolor.md) structures.</span></span>

``` syntax
typedef struct D3DXCOLOR
{
#ifdef __cplusplus
public:
    D3DXCOLOR() {}
    D3DXCOLOR( DWORD argb );
    D3DXCOLOR( CONST FLOAT * );
    D3DXCOLOR( CONST D3DXFLOAT16 * );
    D3DXCOLOR( CONST D3DCOLORVALUE& );
    D3DXCOLOR( FLOAT r, FLOAT g, FLOAT b, FLOAT a );

    // casting
    operator DWORD () const;

    operator FLOAT* ();
    operator CONST FLOAT* () const;

    operator D3DCOLORVALUE* ();
    operator CONST D3DCOLORVALUE* () const;

    operator D3DCOLORVALUE& ();
    operator CONST D3DCOLORVALUE& () const;

    // assignment operators
    D3DXCOLOR& operator += ( CONST D3DXCOLOR& );
    D3DXCOLOR& operator -= ( CONST D3DXCOLOR& );
    D3DXCOLOR& operator *= ( FLOAT );
    D3DXCOLOR& operator /= ( FLOAT );

    // unary operators
    D3DXCOLOR operator + () const;
    D3DXCOLOR operator - () const;

    // binary operators
    D3DXCOLOR operator + ( CONST D3DXCOLOR& ) const;
    D3DXCOLOR operator - ( CONST D3DXCOLOR& ) const;
    D3DXCOLOR operator * ( FLOAT ) const;
    D3DXCOLOR operator / ( FLOAT ) const;

    friend D3DXCOLOR operator * ( FLOAT, CONST D3DXCOLOR& );

    BOOL operator == ( CONST D3DXCOLOR& ) const;
    BOOL operator != ( CONST D3DXCOLOR& ) const;

#endif //__cplusplus
    FLOAT r, g, b, a;
} D3DXCOLOR, *LPD3DXCOLOR;
```

<span data-ttu-id="eadcd-105">Abgeleitete Typen: \* LPD3DXCOLOR</span><span class="sxs-lookup"><span data-stu-id="eadcd-105">Derived types: \*LPD3DXCOLOR</span></span>

## <a name="members"></a><span data-ttu-id="eadcd-106">Member</span><span class="sxs-lookup"><span data-stu-id="eadcd-106">Members</span></span>

<span data-ttu-id="eadcd-107">Weitere Informationen zu Strukturmembern finden Sie unter [**D3DXCOLOR**](d3dxcolor.md).</span><span class="sxs-lookup"><span data-stu-id="eadcd-107">For more information about structure members, refer to [**D3DXCOLOR**](d3dxcolor.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eadcd-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eadcd-108">Remarks</span></span>

<span data-ttu-id="eadcd-109">Operator Überladungen und Typumwandlungen für diese Struktur werden in d3dx9math. INL implementiert.</span><span class="sxs-lookup"><span data-stu-id="eadcd-109">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

> [!Note]  
> <span data-ttu-id="eadcd-110">Der D3DXCOLOR ()-Konstruktor stürzt zur Laufzeit ab, wenn Sie ihn in Microsoft Visual Studio 2010 mit der [Compileroption Lauf Zeit Fehlerüberprüfungen (/RTCc)](/previous-versions/visualstudio/visual-studio-2010/8wtf2dfz(v=vs.100)) im Debugmodus ausführen.</span><span class="sxs-lookup"><span data-stu-id="eadcd-110">The D3DXCOLOR() constructor crashes at runtime when you run it in debug mode in Microsoft Visual Studio 2010 with the [Run-Time Error Checks (/RTCc)](/previous-versions/visualstudio/visual-studio-2010/8wtf2dfz(v=vs.100)) compiler option.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eadcd-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eadcd-111">Requirements</span></span>



| <span data-ttu-id="eadcd-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eadcd-112">Requirement</span></span> | <span data-ttu-id="eadcd-113">Wert</span><span class="sxs-lookup"><span data-stu-id="eadcd-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eadcd-114">Header</span><span class="sxs-lookup"><span data-stu-id="eadcd-114">Header</span></span><br/> | <dl> <span data-ttu-id="eadcd-115"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="eadcd-115"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eadcd-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eadcd-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eadcd-117">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="eadcd-117">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
