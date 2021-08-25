---
description: Identifiziert die beabsichtigte Verwendung von Scheitelpunktdaten.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: D3DDECLUSAGE-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 707a5b7b886ac9366733e1b17322ac61c7d9703cb6ef8ac1e095cf1300fd508d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857510"
---
# <a name="d3ddeclusage-enumeration"></a>D3DDECLUSAGE-Enumeration

Identifiziert die beabsichtigte Verwendung von Scheitelpunktdaten.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGE \_ POSITION**
</dt> <dd>

Positionsdaten im Bereich von (-1,-1) bis (1,1). Verwenden Sie D3DDECLUSAGE POSITION mit einem Verwendungsindex von 0, um die nicht übersetzte Position für die Vertexverarbeitung fester Funktionen und den \_ n-Patch-Mosaik anzugeben. Verwenden Sie D3DDECLUSAGE POSITION mit dem Verwendungsindex 1, um die nicht übersetzte Position im Vertex-Shader der festen Funktion für die \_ Vertex-Optimierung anzugeben.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ BLENDWEIGHT**
</dt> <dd>

Mischen von Gewichtungsdaten. Verwenden Sie D3DDECLUSAGE BLENDWEIGHT mit einem Verwendungsindex von 0, um die Beimischungsgewichtungen anzugeben, die bei indizierten und nicht indizierten \_ Vertexmischungen verwendet werden.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ BLENDINDICES**
</dt> <dd>

Mischen von Indizierungsdaten. Verwenden Sie D3DDECLUSAGE BLENDINDICES mit einem Nutzungsindex von 0, um Matrixindizes für indiziertes \_ Paletten-Skinning anzugeben.

</dd> <dt>

<span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ NORMAL**
</dt> <dd>

Normale Scheitelpunktdaten. Verwenden Sie D3DDECLUSAGE NORMAL mit einem Nutzungsindex von 0, um Scheitelpunktnormals für die Vertexverarbeitung fester Funktionen und den \_ n-Patch-Mosaik anzugeben. Verwenden Sie D3DDECLUSAGE NORMAL mit dem Verwendungsindex 1, um Scheitelpunktnormwerte für die Vertexverarbeitung fester Funktionen für \_ vertex tweening anzugeben.

</dd> <dt>

<span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ PSIZE**
</dt> <dd>

Punktgrößendaten. Verwenden Sie D3DDECLUSAGE PSIZE mit einem Nutzungsindex von 0, um das Punktgrößenattribut anzugeben, das von der Setup-Engine des Rasterizers verwendet wird, um einen Punkt in ein Quader für die \_ Punkt-Sprite-Funktionalität zu erweitern.

</dd> <dt>

<span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ TEXCOORD**
</dt> <dd>

Texturkoordinatendaten. Verwenden Sie D3DDECLUSAGE TEXCOORD, n, um Texturkoordinaten in der Vertexverarbeitung fester Funktionen und in Pixel-Shadern vor \_ PS \_ 3 \_ 0 anzugeben. Diese können verwendet werden, um benutzerdefinierte Daten zu übergeben.

</dd> <dt>

<span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE \_ TANGENT**
</dt> <dd>

Vertex tangent-Daten.

</dd> <dt>

<span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE \_ BINORMAL**
</dt> <dd>

Binormale Vertexdaten.

</dd> <dt>

<span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ TESSFACTOR**
</dt> <dd>

Einzelner positiver Gleitkommawert. Verwenden Sie D3DDECLUSAGE TESSFACTOR mit einem Nutzungsindex von 0, um einen Mosaikfaktor anzugeben, der in der Mosaikeinheit verwendet wird, um die Rate des Mosaiks zu \_ steuern. Weitere Informationen zum Datentyp finden Sie unter D3DDECLTYPE \_ FLOAT1.

</dd> <dt>

<span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE \_ POSITIONT**
</dt> <dd>

Vertexdaten enthalten transformierte Positionsdaten im Bereich von (0,0) bis (Viewportbreite, Viewporthöhe). Verwenden Sie D3DDECLUSAGE \_ POSITIONT mit einem Nutzungsindex von 0, um die transformierte Position anzugeben. Wenn eine Deklaration festgelegt wird, die diese enthält, führt die Pipeline keine Scheitelpunktverarbeitung durch.

</dd> <dt>

<span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**D3DDECLUSAGE \_ COLOR**
</dt> <dd>

Scheitelpunktdaten enthalten diffuse oder speculare Farben. Verwenden Sie D3DDECLUSAGE COLOR mit einem Nutzungsindex von 0, um die diffuse Farbe im Vertex-Shader der festen Funktion und den Pixel-Shadern vor \_ PS \_ 3 \_ 0 anzugeben. Verwenden Sie D3DDECLUSAGE COLOR mit dem Nutzungsindex 1, um die Specularfarbe im Vertex-Shader der festen Funktion und pixel-Shader vor \_ PS \_ 3 \_ 0 anzugeben.

</dd> <dt>

<span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE \_ ALLE**
</dt> <dd>

Scheitelpunktdaten enthalten Daten. Verwenden Sie D3DDECLUSAGEBLEND mit einem Nutzungsindex von 0, um einen Blendwert anzugeben, der nach Abschluss der Pixelschattierung \_ verwendet wird. Dies gilt für Pixel-Shader vor Version ps \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE \_ DEPTH**
</dt> <dd>

Scheitelpunktdaten enthalten Tiefendaten.

</dd> <dt>

<span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**D3DDECLUSAGE-BEISPIEL \_**
</dt> <dd>

Scheitelpunktdaten enthalten Samplerdaten. Verwenden Sie D3DDECLUSAGE SAMPLE mit einem Nutzungsindex von 0, um den Verschiebungswert anzugeben, \_ nach dem sie suchen möchten. Sie kann nur mit D3DDECLUSAGE \_ LOOKUPPRESAMPLED oder D3DDECLUSAGE \_ LOOKUP verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Scheitelpunktdaten werden mit einem Array von [**D3DVERTEXELEMENT9-Strukturen**](d3dvertexelement9.md) deklariert. Jedes Element im Array enthält einen Verwendungstyp.

Weitere Informationen zu Scheitelpunktdeklarationen finden Sie unter [Vertexdeklaration (Direct3D 9).](vertex-declaration.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[Scheitelpunktdeklaration (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 




