---
description: Definiert einen Scheitelpunkt Deklarations Datentyp.
ms.assetid: 993fc7e4-4752-4bce-82d0-0a034fdc69c0
title: D3DDECLTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3edb3f936772a7265c627f10eeb7aeb4f461701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354377"
---
# <a name="d3ddecltype-enumeration"></a>D3DDECLTYPE-Enumeration

Definiert einen Scheitelpunkt Deklarations Datentyp.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDECLTYPE { 
  D3DDECLTYPE_FLOAT1     = 0,
  D3DDECLTYPE_FLOAT2     = 1,
  D3DDECLTYPE_FLOAT3     = 2,
  D3DDECLTYPE_FLOAT4     = 3,
  D3DDECLTYPE_D3DCOLOR   = 4,
  D3DDECLTYPE_UBYTE4     = 5,
  D3DDECLTYPE_SHORT2     = 6,
  D3DDECLTYPE_SHORT4     = 7,
  D3DDECLTYPE_UBYTE4N    = 8,
  D3DDECLTYPE_SHORT2N    = 9,
  D3DDECLTYPE_SHORT4N    = 10,
  D3DDECLTYPE_USHORT2N   = 11,
  D3DDECLTYPE_USHORT4N   = 12,
  D3DDECLTYPE_UDEC3      = 13,
  D3DDECLTYPE_DEC3N      = 14,
  D3DDECLTYPE_FLOAT16_2  = 15,
  D3DDECLTYPE_FLOAT16_4  = 16,
  D3DDECLTYPE_UNUSED     = 17
} D3DDECLTYPE, *LPD3DDECLTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE \_ FLOAT1**
</dt> <dd>

Der float-Wert einer Komponente wurde auf (float, 0, 0, 1) erweitert.

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE \_ FLOAT2**
</dt> <dd>

Der float-Wert für zwei Komponenten wurde auf (float, float, 0, 1) erweitert.

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE \_ FLOAT3**
</dt> <dd>

Der float-Wert von drei Komponenten wurde auf (float, float, float, 1) erweitert.

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE \_ float4**
</dt> <dd>

Der float-Wert von vier Komponenten wurde auf (float, float, float, float) erweitert.

</dd> <dt>

<span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE \_ D3DCOLOR**
</dt> <dd>

Vier Komponenten, gepackte, nicht signierte bytes, die 0 bis 1 Bereich zugeordnet sind. Input ist ein [**D3DCOLOR**](d3dcolor.md) -Wert, der auf RGBA-Reihenfolge erweitert wird.

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE \_ UBYTE4**
</dt> <dd>

Ein Byte mit vier Komponenten, ohne Vorzeichen.

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE \_ SHORT2**
</dt> <dd>

Two-Component, signed Short erweitert auf (Wert, Wert, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE \_ SHORT4**
</dt> <dd>

4-Component, signed Short erweitert auf (Wert, Wert, Wert, Wert).

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE \_ UBYTE4N**
</dt> <dd>

Ein 4-Byte-Byte, bei dem jedes Byte durch Dividieren durch 255.0 f normalisiert wird.

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE \_ SHORT2N**
</dt> <dd>

Normalized, Two-Component, signed Short, erweitert auf (First Short/32767.0, Second Short/32767.0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE \_ SHORT4N**
</dt> <dd>

Normalized, 4-Component, signed Short, erweitert auf (First Short/32767.0, Second Short/32767.0, dritte Short/32767.0, Fourth Short/32767.0).

</dd> <dt>

<span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE \_ USHORT2N**
</dt> <dd>

Normalized, Two-Component, Ganzzahl ohne Vorzeichen Short, erweitert auf (First Short/65535.0, Short Short/65535.0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE \_ USHORT4N**
</dt> <dd>

Normalized, 4-Component, Ganzzahl ohne Vorzeichen Short, erweitert auf (First Short/65535.0, Second Short/65535.0, dritte Short/65535.0, Fourth Short/65535.0).

</dd> <dt>

<span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE \_ UDEC3**
</dt> <dd>

Drei Komponenten, nicht signiertes, 10 10 10-Format, erweitert auf (Wert, Wert, Wert, 1).

</dd> <dt>

<span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE \_ DEC3N**
</dt> <dd>

Drei Komponenten, signiert, 10 10 10-Format normalisiert und erweitert auf (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**
</dt> <dd>

Zwei-Komponenten-16-Bit-Gleit Komma, erweitert auf (Wert, Wert, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**
</dt> <dd>

Vier-Komponenten, 16-Bit-Gleit Komma, erweitert auf (Wert, Wert, Wert, Wert).

</dd> <dt>

<span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE nicht \_ verwendet**
</dt> <dd>

Das typanfeld in der Deklaration wird nicht verwendet. Dies ist für die Verwendung mit D3DDECLMETHOD \_ UV und D3DDECLMETHOD \_ lookuppresampling vorgesehen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Vertex-Daten werden mit einem Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Strukturen deklariert. Jedes Element im Array enthält einen Scheitelpunkt Deklarations Datentyp.

Verwenden Sie das DirectX Caps Viewer-Tool (DXCapsViewer.exe), um zu sehen, welche Typen auf Ihrem Gerät unterstützt werden. Sie können dieses Tool aus dem DirectX SDK erhalten. Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DDECLMETHOD**](./d3ddeclmethod.md)
</dt> </dl>

 

 
