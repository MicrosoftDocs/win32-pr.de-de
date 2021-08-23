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
ms.openlocfilehash: a2ab3d030a2bf4c037b72e07244694c20ab7e94fb5c70f75ff0eb37e4205f70f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407870"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a>D3DXMATRIXA16-Struktur (D3dx9math.h)

Eine 4x4-, 16-Byte-ausgerichtete Matrix, die Methoden und Operatorüberladungen enthält.

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

Die Komponente (i, j) der Matrix, wobei i die Zeilennummer und j die Spaltennummer ist. 34 bedeutet z. \_ B. das gleiche wie \[ a₃₄ \] , die Komponente in der dritten Zeile und vierten Spalte.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine 16-Byte-ausgerichtete Matrix, die von mathematischen D3DX-Funktionen verwendet wird, wurde für eine verbesserte Leistung auf Intel Pentium 4-Prozessoren optimiert. Matrizen werden unabhängig davon ausgerichtet, wo sie erstellt werden: auf dem Programmstapel, im Heap oder im globalen Bereich. Die Ausrichtung erfolgt mit \_ \_ declspec(align(16)), die nur mit Visual C++ .NET und mit Visual C++ 6.0 funktioniert, wenn das Prozessorpaket installiert ist. Leider gibt es keine Möglichkeit, das Prozessorpaket zu erkennen, sodass die Byteausrichtung standardmäßig nur mit Visual C++ .NET aktiviert ist.

Vektoren und Quaternionen werden in D3DX nicht bytebündig ausgerichtet. Wenn Sie Vektoren und Quaternionen mit mathematischen D3DX-Funktionen verwenden, verwenden Sie \_ declspec(align(16)), um bytebündige Vektoren und Quaternionen zu generieren, da sie erheblich besser funktionieren. Die Definition von \_ declspec ist hier dargestellt.


```
#define D3DX_ALIGN16 __declspec(align(16))
```



Andere Compiler interpretieren D3DXMATRIXA16 als D3DXMATRIX. Die Verwendung dieser Struktur auf einem Compiler, der die Matrix nicht tatsächlich ausrichtet, kann problematisch sein, da sie keine Fehler verfügbar macht, die die Ausrichtung ignorieren. Wenn sich z. B. ein D3DXMATRIXA16-Objekt innerhalb einer Struktur oder Klasse befindet, kann ein [**Memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) mit engem Komprimieren durchgeführt werden (wobei 16-Byte-Grenzen ignoriert werden). Dies würde zu Buildunterbrechungen führen, wenn der Compiler irgendwann eine Matrixausrichtung hinzufügen würde.

### <a name="d3dxmatrixa16"></a>D3DXMATRIXA16

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
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXMATRIX**](d3dxmatrix.md)
</dt> </dl>

 

 
