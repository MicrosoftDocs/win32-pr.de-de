---
description: Definiert Einstellungen, die für Gitter-Tangensframeberechnungen verwendet werden.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: D3DXTANGENT-Enumeration (D3dx9mesh.h)
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
ms.openlocfilehash: 5d6e57d2027a7366ec2b82ac7bd82aae4275d489c17f1922684e3ca6232be940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749770"
---
# <a name="d3dxtangent-enumeration"></a>D3DXTANGENT-Enumeration

Definiert Einstellungen, die für Gitter-Tangensframeberechnungen verwendet werden.

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

<span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ WRAP \_ U**
</dt> <dd>

Texturkoordinatenwerte in u-Richtung liegen zwischen 0 und 1. In diesem Fall wird ein Texturkoordinatensatz ausgewählt, der den Umkreis des Dreiecks minimiert. Weitere [Informationen finden Sie unter Texturumbruch (Direct3D 9).](texture-wrapping.md)

</dd> <dt>

<span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ WRAP \_ V**
</dt> <dd>

Texturkoordinatenwerte in v-Richtung liegen zwischen 0 und 1. In diesem Fall wird ein Texturkoordinatensatz ausgewählt, der den Umkreis des Dreiecks minimiert. Weitere [Informationen finden Sie unter Texturumbruch (Direct3D 9).](texture-wrapping.md)

</dd> <dt>

<span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ WRAP \_ UV**
</dt> <dd>

Texturkoordinatenwerte in Sie- und v-Richtung liegen zwischen 0 und 1. In diesem Fall wird ein Texturkoordinatensatz ausgewählt, der den Umkreis des Dreiecks minimiert. Weitere [Informationen finden Sie unter Texturumbruch (Direct3D 9).](texture-wrapping.md)

</dd> <dt>

<span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ DONT \_ NORMALIZE \_ PARTIALS**
</dt> <dd>

Normalisieren Sie partielle Ableitungen nicht in Bezug auf Texturkoordinaten. Wenn dies nicht normalisiert ist, ist die Skala der partiellen Ableitungen proportional zur Skala des 3D-Modells dividiert durch die Skala des Dreiecks im Raum (u, v). Dieser Skalierungswert gibt ein Maß dafür an, wie viel die Textur in einer bestimmten Richtung gestreckt wird. Die resultierende Vektorlänge ist eine gewichtete Summe der Längen der partiellen Ableitungen.

</dd> <dt>

<span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ DONT \_ ORTHOGONALIZE**
</dt> <dd>

Transformieren Sie Texturkoordinaten nicht in orthogonale kartesische Koordinaten. Schließen Sich gegenseitig aus mit D3DXTANGENT \_ ORTHOGONALIZE \_ FROM you und \_ D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ V.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ V**
</dt> <dd>

Berechnen Sie die partielle Ableitung in Bezug auf Texturkoordinate v unabhängig für jeden Scheitelpunkt, und berechnen Sie dann die partielle Ableitung in Bezug auf Sie als Kreuzprodukt der partiellen Ableitung in Bezug auf v und den normalen Vektor. Schließen sich gegenseitig aus mit D3DXTANGENT \_ DONT \_ ORTHOGONALIZE und D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U**
</dt> <dd>

Berechnen Sie die partielle Ableitung in Bezug auf die Texturkoordinate u unabhängig für jeden Scheitelpunkt, und berechnen Sie dann die partielle Ableitung in Bezug auf v als Kreuzprodukt des normalen Vektors und der partiellen Ableitung in Bezug auf Sie. Schließen Sich gegenseitig aus mit D3DXTANGENT \_ DONT \_ ORTHOGONALIZE und D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ V.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT \_ GEWICHTUNG \_ NACH \_ BEREICH**
</dt> <dd>

Gewichten Sie die Richtung des berechneten normalen oder partiellen abgeleiteten Vektors pro Scheitelpunkt entsprechend den Bereichen der Dreiecke, die an diesen Scheitelpunkt angefügt sind. Schließen sie sich mit D3DXTANGENT \_ WEIGHT \_ EQUAL gegenseitig aus.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT \_ WEIGHT \_ EQUAL**
</dt> <dd>

Berechnen Sie einen Normalvektor mit Einheitenlänge für jedes Dreieck des Eingabegitters. Schließen sich mit D3DXTANGENT \_ WEIGHT BY AREA gegenseitig \_ \_ aus.

</dd> <dt>

<span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ WIND \_ CW**
</dt> <dd>

Scheitelungen werden im Uhrzeigersinn um jedes Dreieck herum geordnet. Die berechnete normaler Vektorrichtung wird daher um 180 Grad von der Richtung umgekehrt, die mithilfe der umgekehrten Scheitelpunkt reihenfolge berechnet wird.

</dd> <dt>

<span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ \_ NORMALS BERECHNEN**
</dt> <dd>

Berechnen Sie den normalen Vektor pro Scheitelpunkt für jedes Dreieck des Eingabegitters, und ignorieren Sie alle normalen Vektoren, die bereits im Eingabegitternetz vorhanden sind.

</dd> <dt>

<span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ GENERATE AN ORT UND \_ \_ STELLE**
</dt> <dd>

Die Ergebnisse werden im ursprünglichen Eingabegitter gespeichert, und das Ausgabegitternetz wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




