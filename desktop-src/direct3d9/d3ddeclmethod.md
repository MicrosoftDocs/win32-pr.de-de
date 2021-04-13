---
description: Definiert die Scheitelpunkt Deklarations Methode, bei der es sich um einen vordefinierten Vorgang handelt, der vom Mosaik Prozess (oder einer beliebigen prozeduralen Geometrie Routine auf den Scheitelpunkt Daten während des Mosaik Vorgangs) ausgeführt wird.
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: D3DDECLMETHOD-Enumeration (D3D9Types. h)
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
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354386"
---
# <a name="d3ddeclmethod-enumeration"></a>D3DDECLMETHOD-Enumeration

Definiert die Scheitelpunkt Deklarations Methode, bei der es sich um einen vordefinierten Vorgang handelt, der vom Mosaik Prozess (oder einer beliebigen prozeduralen Geometrie Routine auf den Scheitelpunkt Daten während des Mosaik Vorgangs) ausgeführt wird.

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

<span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD \_ Standard**
</dt> <dd>

Standardwert. Der Mosaik Dienst kopiert die Scheitelpunkt Daten (Spline-Daten für Patches) unverändert und ohne zusätzliche Berechnungen. Wenn der Mosaik Prozess verwendet wird, wird dieses Element interpoliert. Andernfalls werden Scheitelpunkt Daten in das Eingabe Register kopiert. Der Eingabe-und Ausgabetyp kann ein beliebiger Wert sein, aber immer derselbe Typ.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ partialu**
</dt> <dd>

Berechnet den Tangens an einem Punkt des Rechtecks oder Dreiecks Patches in der U-Richtung. Der Eingabetyp kann einer der folgenden sein:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ float4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Der Ausgabetyp ist immer D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ partialv**
</dt> <dd>

Berechnet den Tangens an einem Punkt des Rechtecks oder Dreiecks Patches in der V-Richtung. Der Eingabetyp kann einer der folgenden sein:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ float4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Der Ausgabetyp ist immer D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ crossuv**
</dt> <dd>

Berechnet den normalen an einem Punkt des Rechtecks oder Dreiecks Patches, indem das Kreuz Produkt von zwei Tangenten übernommen wird. Der Eingabetyp kann einer der folgenden sein:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ float4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Der Ausgabetyp ist immer D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD \_ -UV**
</dt> <dd>

Kopieren Sie die U-V-Werte an einem Punkt des Rechtecks oder Dreiecks Patches. Dies führt zu einem 2D-float-Wert. Der Eingabetyp muss auf D3DDECLTYPE nicht \_ verwendet werden. Der Ausgabedatentyp lautet immer D3DDECLTYPE \_ FLOAT2. Der Eingabestream und Offset werden ebenfalls nicht verwendet (muss jedoch auf 0 festgelegt werden).

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD- \_ Suche**
</dt> <dd>

Suchen Sie eine Verschiebungs Zuordnung. Der Eingabetyp kann einer der folgenden sein:

-   D3DDECLTYPE \_ FLOAT2
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ float4

Nur die x-und y-Komponenten werden für die Textur kartogramm-Suche verwendet. Der Ausgabetyp ist immer D3DDECLTYPE \_ FLOAT1. Das Gerät muss die Verschiebungs Zuordnung unterstützen. Weitere Informationen zur Verschiebungs Zuordnung finden Sie unter [Verschiebungs Zuordnung (Direct3D 9)](displacement-mapping.md). Diese Konstante wird nur von der programmierbaren Pipeline für n-Patchdaten unterstützt, wenn n-Patches aktiviert sind.

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ lookuppresampling**
</dt> <dd>

Suchen Sie eine Verschiebungs Zuordnung mit präsampling. Der Eingabetyp muss auf D3DDECLTYPE nicht \_ verwendet werden. der streamindex und der Streamoffset müssen auf 0 festgelegt werden. Der Ausgabetyp für diesen Vorgang lautet immer D3DDECLTYPE \_ FLOAT1. Das Gerät muss die Verschiebungs Zuordnung unterstützen. Weitere Informationen zur Verschiebungs Zuordnung finden Sie unter [Verschiebungs Zuordnung (Direct3D 9)](displacement-mapping.md). Diese Konstante wird nur von der programmierbaren Pipeline für n-Patchdaten unterstützt, wenn n-Patches aktiviert sind. Diese Methode kann nur mit D3DDECLUSAGE Sample verwendet werden \_ .

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Mosaik Prozess untersucht die-Methode, um zu bestimmen, welche Daten während des Mosaik Prozesses aus den Scheitelpunkt Daten berechnet werden sollen. Für Mesh-Daten sollte der Standardwert verwendet werden. Patches können jeden der anderen implementierten Typen verwenden.

Vertex-Daten werden mit einem Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Strukturen deklariert. Jedes Element im Array enthält eine Scheitelpunkt Deklarations Methode.

Neben der Verwendung von D3DDECLMETHOD \_ Default kann ein normales Mesh \_ die D3DDECLMETHOD Lookup-Methode und die D3DDECLMETHOD \_ lookuppresampling-Methode verwenden, wenn N-Patches aktiviert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




