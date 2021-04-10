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
# <a name="d3dxmatrixa16-structure-d3dx10mathh"></a>D3DXMATRIXA16-Struktur (D3DX10Math. h)

Eine 4 x 4-Matrix mit 16 Bytes, die Methoden und Operator Überladungen enthält.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a>Member

<dl> <dt>

**\_angesprochenen**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Komponente (i, j) der Matrix, bei der es sich um die Zeilennummer und j um die Spaltennummer handelt. 34 bedeutet beispielsweise, dass das \_ gleiche wie \[ ein ₃ ₄ \] , die Komponente in der dritten Zeile und vierten Spalte ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bei der Verwendung durch D3DX Math-Funktionen wurde eine aus 16 Bytes ausgerichtete Matrix optimiert, um die Leistung von Intel Pentium 4-Prozessoren zu verbessern. Matrizen werden unabhängig von ihrem Speicherort ausgerichtet: auf dem Programm Stapel, im Heap oder im globalen Gültigkeitsbereich. Die Ausrichtung erfolgt mithilfe \_ \_ von "declspec (align (16))", die mit Visual C++ .net und nur mit Visual C++ 6,0 funktioniert, wenn das Prozessor Paket installiert ist. Leider gibt es keine Möglichkeit, das Prozessor Paket zu erkennen, sodass die Byte Ausrichtung standardmäßig nur mit Visual C++ .NET aktiviert ist.

Vektoren und Quaternionen sind in D3DX nicht Byte bündig ausgerichtet. Wenn Sie Vektoren und Quaternionen mit D3DX Math-Funktionen verwenden, verwenden \_ Sie declspec (align (16)), um Byte ausgerichtete Vektoren und Quaternionen zu generieren, da Sie erheblich besser funktionieren. Die Definition von \_ declspec wird hier dargestellt.


```
#define D3DX_ALIGN16 __declspec(align(16))
```



Andere Compiler interpretieren **D3DXMATRIXA16** als [**D3DXMATRIX**](d3d10-d3dxmatrix.md). Die Verwendung dieser Struktur für einen Compiler, der die Matrix nicht tatsächlich ausgerichtet, kann problematisch sein, da Sie keine Fehler verfügbar macht, die die Ausrichtung ignorieren. Wenn sich z. b. ein **D3DXMATRIXA16** -Objekt innerhalb einer Struktur oder Klasse befindet, wird eine [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) möglicherweise mit einer dichten Verpackung ausgeführt (wobei 16-Byte-Begrenzungen ignoriert werden). Dies würde zu Buildunterbrechungen führen, wenn der Compiler einige aufeinander folgende Matrizen hinzufügen würde.

### <a name="d3dxmatrixa16-extensions"></a>D3DXMATRIXA16-Erweiterungen

**D3DXMATRIXA16** verfügt über die folgenden C++-Erweiterungen.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
