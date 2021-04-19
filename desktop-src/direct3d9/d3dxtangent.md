---
description: Definiert Einstellungen, die für Gitter Tangens-Frame Berechnungen verwendet werden.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: D3DXTANGENT-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 43e3c5ced0eee3366b85070ce89d19154d048ab4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371908"
---
# <a name="d3dxtangent-enumeration"></a>D3DXTANGENT-Enumeration

Definiert Einstellungen, die für Gitter Tangens-Frame Berechnungen verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ Wrap \_ U**
</dt> <dd>

Texturkoordinaten Werte in der u-Richtung liegen zwischen 0 und 1. In diesem Fall wird ein Texturkoordinaten Satz ausgewählt, der den Umkreis des Dreiecks minimiert. Weitere Informationen finden Sie unter [Textur Wrapping (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ Wrap \_ V**
</dt> <dd>

Texturkoordinaten Werte in der v-Richtung liegen zwischen 0 und 1. In diesem Fall wird ein Texturkoordinaten Satz ausgewählt, der den Umkreis des Dreiecks minimiert. Weitere Informationen finden Sie unter [Textur Wrapping (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ Wrap \_ -UV**
</dt> <dd>

Die Texturkoordinaten Werte in der Richtung und der v-Richtung liegen zwischen 0 und 1. In diesem Fall wird ein Texturkoordinaten Satz ausgewählt, der den Umkreis des Dreiecks minimiert. Weitere Informationen finden Sie unter [Textur Wrapping (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ keine \_ \_ partitionale normalisieren**
</dt> <dd>

Partielle Ableitungen sollten nicht in Bezug auf Texturkoordinaten normalisiert werden. Wenn nicht normalisiert, ist die Skala der partiellen Ableitungen proportional zur Skala des 3D-Modells dividiert durch die Skala des Dreiecks im (u, v)-Raum. Dieser Skalierungs Wert gibt an, wie weit die Textur in eine bestimmte Richtung gestreckt wird. Die resultierende Vektor Länge ist eine gewichtete Summe der Längen der partiellen Ableitungen.

</dd> <dt>

<span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ nicht \_ orthogonalize**
</dt> <dd>

Transformieren Sie keine Texturkoordinaten in orthogonale kartesische Koordinaten. Schließen Sie sich mit D3DXTANGENT \_ orthogonalize \_ von \_ Ihnen und D3DXTANGENT \_ orthogonalize \_ von \_ V gegenseitig aus.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT \_ orthogonalize \_ von \_ V**
</dt> <dd>

Berechnen Sie die partielle Ableitung in Bezug auf die Texturkoordinaten v unabhängig für jeden Scheitelpunkt, und berechnen Sie dann die partielle Ableitung in Bezug auf das Kreuz Produkt der partiellen Ableitung in Bezug auf v und den normalen Vektor. Schließen Sie sich mit D3DXTANGENT \_ dont \_ orthogonalize und D3DXTANGENT \_ orthogonalize aus U gegenseitig \_ aus \_ .

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT \_ orthogonalize \_ von \_ U**
</dt> <dd>

Berechnen Sie die partielle Ableitung in Bezug auf die Textur Koordinate u unabhängig für jeden Scheitelpunkt, und berechnen Sie dann die partielle Ableitung in Bezug auf v als Kreuz Produkt des normalen Vektors und die partielle Ableitung in Bezug auf Sie. Schließen Sie sich mit D3DXTANGENT \_ dont \_ orthogonalize und D3DXTANGENT \_ orthogonalize aus V gegenseitig \_ aus \_ .

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT \_ Gewichtung \_ nach \_ Bereich**
</dt> <dd>

Gewichtet die Richtung des berechneten pro-Vertex-normalen oder partiellen Ableitung-Vektors gemäß den Bereichen der Dreiecke, die an diesen Scheitelpunkt angefügt sind. Schließen Sie sich mit D3DXTANGENT Weight gleich gegenseitig aus \_ \_ .

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT \_ Gewichtung \_ gleich**
</dt> <dd>

Berechnen Sie für jedes Dreieck des Eingabe Netzes einen normalen Vektor mit Einheiten Länge. Schließen Sie sich mit D3DXTANGENT \_ Weight \_ by Area gegenseitig aus \_ .

</dd> <dt>

<span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ Wind \_ CW**
</dt> <dd>

Vertices werden um jedes Dreieck in einer Richtung im Uhrzeigersinn angeordnet. Die berechnete normale Vektor Richtung wird aus der Richtung, die mithilfe der Vertex-Reihenfolge gegen den Uhrzeigersinn berechnet wurde, um 180 Grad

</dd> <dt>

<span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ Berechnen von \_ normalen**
</dt> <dd>

Berechnen Sie den normalen Vertex-Vektor für jedes Dreieck des Eingabe Netzes, und ignorieren Sie alle normalen Vektoren, die bereits im eingabemesh vorhanden sind.

</dd> <dt>

<span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT- \_ Generierung direkt generieren \_ \_**
</dt> <dd>

Die Ergebnisse werden im ursprünglichen eingabemesh gespeichert, und das Ausgabe Mesh wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




