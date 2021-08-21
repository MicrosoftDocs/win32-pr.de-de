---
description: Definiert die Scheitelpunktdeklarationsmethode, bei der es sich um einen vordefinierten Vorgang handelt, der vom Mosaikator (oder einer beliebigen prozeduralen Geometrieroutine für die Scheitelpunktdaten während des Mosaiks) ausgeführt wird.
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: D3DDECLMETHOD-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f34700666ecb830470e58a3f3389cd6207be68403e612f50ddafc841dd839ed2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565060"
---
# <a name="d3ddeclmethod-enumeration"></a>D3DDECLMETHOD-Enumeration

Definiert die Scheitelpunktdeklarationsmethode, bei der es sich um einen vordefinierten Vorgang handelt, der vom Mosaikator (oder einer beliebigen prozeduralen Geometrieroutine für die Scheitelpunktdaten während des Mosaiks) ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD \_ DEFAULT**
</dt> <dd>

Standardwert. Der Mosaikator kopiert die Scheitelpunktdaten (Splinedaten für Patches) ohne zusätzliche Berechnungen. Wenn der Mosaikator verwendet wird, wird dieses Element interpoliert. Andernfalls werden Scheitelpunktdaten in das Eingaberegister kopiert. Der Eingabe- und Ausgabetyp kann ein beliebiger Wert sein, ist aber immer derselbe Typ.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ PARTIALU**
</dt> <dd>

Berechnet den Tangens an einem Punkt auf dem Rechteck oder Dreieckspatch in U-Richtung. Der Eingabetyp kann einer der folgenden Sein:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Der Ausgabetyp ist immer D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ PARTIALV**
</dt> <dd>

Berechnet den Tangens an einem Punkt auf dem Rechteck oder Dreieckspatch in V-Richtung. Der Eingabetyp kann einer der folgenden Sein:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Der Ausgabetyp ist immer D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ CROSSUV**
</dt> <dd>

Berechnet die Normalität an einem Punkt auf dem Rechteck oder Dreieckspatch, indem das Kreuzprodukt aus zwei Tangenten verwendet wird. Der Eingabetyp kann einer der folgenden Sein:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Der Ausgabetyp ist immer D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD \_ UV**
</dt> <dd>

Kopieren Sie die U-, V-Werte an einem Punkt auf dem Rechteck oder Dreieckspatch. Dies führt zu einem 2D-Gleitkommawert. Der Eingabetyp muss auf D3DDECLTYPE \_ UNUSED festgelegt werden. Der Ausgabedatentyp ist immer D3DDECLTYPE \_ FLOAT2. Der Eingabestream und der Offset werden ebenfalls nicht verwendet (müssen jedoch auf 0 festgelegt werden).

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD \_ LOOKUP**
</dt> <dd>

Suchen Sie eine Verschiebungskarte. Der Eingabetyp kann einer der folgenden Sein:

-   D3DDECLTYPE \_ FLOAT2
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4

Nur die X- und Y-Komponenten werden für die Texturzuordnungssuche verwendet. Der Ausgabetyp ist immer D3DDECLTYPE \_ FLOAT1. Das Gerät muss die Zuordnung von Verschiebungen unterstützen. Weitere Informationen zur Verschiebungszuordnung finden Sie unter [Verschiebungszuordnung (Direct3D 9).](displacement-mapping.md) Diese Konstante wird nur von der programmierbaren Pipeline für N-Patch-Daten unterstützt, wenn N-Patches aktiviert sind.

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ LOOKUPPRESAMPLED**
</dt> <dd>

Suchen Sie eine vorsampelte Verschiebungskarte. Der Eingabetyp muss auf D3DDECLTYPE \_ UNUSED festgelegt werden. Der Streamindex und der Streamoffset müssen auf 0 festgelegt werden. Der Ausgabetyp für diesen Vorgang ist immer D3DDECLTYPE \_ FLOAT1. Das Gerät muss die Zuordnung von Verschiebungen unterstützen. Weitere Informationen zur Verschiebungszuordnung finden Sie unter [Verschiebungszuordnung (Direct3D 9).](displacement-mapping.md) Diese Konstante wird nur von der programmierbaren Pipeline für N-Patch-Daten unterstützt, wenn N-Patches aktiviert sind. Diese Methode kann nur mit D3DDECLUSAGE SAMPLE verwendet \_ werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Mosaikator untersucht die -Methode, um zu bestimmen, welche Daten während des Mosaiks aus den Scheitelpunktdaten berechnet werden sollen. Gitternetzdaten sollten den Standardwert verwenden. Patches können jeden der anderen implementierten Typen verwenden.

Scheitelpunktdaten werden mit einem Array von [**D3DVERTEXELEMENT9-Strukturen**](d3dvertexelement9.md) deklariert. Jedes Element im Array enthält eine Vertexdeklarationsmethode.

Zusätzlich zur Verwendung von D3DDECLMETHOD \_ DEFAULT kann ein normales Gitternetz die Methoden D3DDECLMETHOD \_ LOOKUP und D3DDECLMETHOD \_ LOOKUPPRESAMPLED verwenden, wenn N-Patches aktiviert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




