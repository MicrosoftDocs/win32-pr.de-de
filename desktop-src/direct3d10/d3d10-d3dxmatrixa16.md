---
description: 'D3DXMATRIXA16-Struktur (D3DX10Math.h): Eine 4x4-Matrix mit 16-Byte-Ausrichtung, die Methoden und Operatorüberladungen enthält.'
ms.assetid: d9e9c1cc-7555-4011-a4b4-8cce20404841
title: D3DXMATRIXA16-Struktur (D3DX10Math.h)
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
ms.openlocfilehash: 4953b51cdd09cdbcac4855bd423ce37dda5b979e06153589b5b2ded21004b3ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853400"
---
# <a name="d3dxmatrixa16-structure-d3dx10mathh"></a>D3DXMATRIXA16-Struktur (D3DX10Math.h)

Eine 4x4- und 16-Byte-ausgerichtete Matrix, die Methoden und Operatorüberladungen enthält.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a>Member

<dl> <dt>

**\_Ij**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Komponente (i, j) der Matrix, wobei i die Zeilennummer und j die Spaltennummer ist. 34 bedeutet \_ z. B. dasselbe wie a₃₄ , die Komponente in der \[ dritten Zeile und vierten \] Spalte.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine 16-Byte-ausgerichtete Matrix wurde bei Verwendung durch mathematische D3DX-Funktionen für eine verbesserte Leistung auf Intel Pentium 4-Prozessoren optimiert. Matrizen werden unabhängig davon ausgerichtet, wo sie erstellt werden: im Programmstapel, im Heap oder im globalen Bereich. Die Ausrichtung erfolgt \_ \_ mithilfe von declspec(align(16)), das nur mit Visual C++ .NET und mit Visual C++ 6.0 funktioniert, wenn das Prozessorpaket installiert ist. Leider gibt es keine Möglichkeit, das Prozessorpaket zu erkennen, sodass die Byteausrichtung standardmäßig nur mit Visual C++ .NET aktiviert ist.

Vektoren und Quaternionen sind in D3DX nicht bytebündig ausgerichtet. Wenn Sie Vektoren und Quaternionen mit mathematischen D3DX-Funktionen verwenden, verwenden Sie \_ declspec(align(16)), um bytebündige Vektoren und Quaternionen zu generieren, da sie eine deutlich bessere Leistung erzielen. Die Definition von \_ declspec wird hier gezeigt.


```
#define D3DX_ALIGN16 __declspec(align(16))
```



Andere Compiler interpretieren **D3DXMATRIXA16** als [**D3DXMATRIX**](d3d10-d3dxmatrix.md). Die Verwendung dieser Struktur für einen Compiler, der die Matrix nicht tatsächlich ausrichtet, kann problematisch sein, da sie keine Fehler verfügbar macht, die die Ausrichtung ignorieren. Wenn sich ein **D3DXMATRIXA16-Objekt** beispielsweise in einer Struktur oder Klasse befindet, kann ein [Memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) mit enger Packung (ignorieren von 16-Byte-Begrenzungen) erfolgen. Dies würde zu Buildunterbrechungen führen, wenn der Compiler irgendwann eine Matrix-Ausrichtung hinzufügen würde.

### <a name="d3dxmatrixa16-extensions"></a>D3DXMATRIXA16-Erweiterungen

**D3DXMATRIXA16 verfügt** über die folgenden C++-Erweiterungen.


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
| Header<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
