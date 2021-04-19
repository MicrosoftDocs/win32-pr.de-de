---
description: Gibt die beabsichtigte Verwendung von Vertex-Daten an.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: D3DDECLUSAGE-Enumeration (D3D9Types. h)
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
ms.openlocfilehash: f3997aa38a7a97455b9f36d8afbee896ca9ae937
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361853"
---
# <a name="d3ddeclusage-enumeration"></a>D3DDECLUSAGE-Enumeration

Gibt die beabsichtigte Verwendung von Vertex-Daten an.

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

<span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGE- \_ Position**
</dt> <dd>

Positionieren von Daten im Bereich von (-1,-1) bis (1, 1). Verwenden \_ Sie die D3DDECLUSAGE-Position mit einem Nutzungs Index von 0, um eine nicht transformierte Position für die Vertex-Verarbeitung fester Funktionen und den n-Patch-Mosaik Wert anzugeben. Verwenden \_ Sie die D3DDECLUSAGE-Position mit einem Verwendungs Index von 1, um eine nicht transformierte Position im Scheitelpunkt des fixierten Funktionen für die vertextwiening anzugeben.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ blendweight**
</dt> <dd>

Mischen von Gewichtungsdaten. Verwenden \_ Sie D3DDECLUSAGE blendweight mit einem Nutzungs Index von 0, um die Blend-Gewichtungen anzugeben, die für indizierte und nicht indizierte vertexblending verwendet werden.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ blendindices**
</dt> <dd>

Kombination von Indizes-Daten. Verwenden \_ Sie D3DDECLUSAGE blendindices mit einem Nutzungs Index von 0, um Matrix Indizes für indizierte palettenskinning anzugeben.

</dd> <dt>

<span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ Normal**
</dt> <dd>

Vertex-normale Daten. Verwenden \_ Sie D3DDECLUSAGE normal mit einem Nutzungs Index von 0, um Vertex-Normale für die Vertex-Verarbeitung fester Funktionen und den n-Patch-Mosaik Wert anzugeben. Verwenden \_ Sie D3DDECLUSAGE normal mit einem Nutzungs Index von 1, um Vertex-Normale für die Vertex-Verarbeitung fester Funktionen für vertextwiening anzugeben.

</dd> <dt>

<span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ Psize**
</dt> <dd>

Daten zur Datenpunkt Größe. Verwenden \_ Sie D3DDECLUSAGE Psize mit einem Nutzungs Index von 0, um das Attribut für die Punktgröße anzugeben, das vom Setup Modul des Rasterizers verwendet wird, um einen Punkt für die Punkt Sprite-Funktionalität zu erweitern.

</dd> <dt>

<span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ texcoord**
</dt> <dd>

Texturkoordinaten Daten. Verwenden \_ Sie D3DDECLUSAGE texcoord, n, um Texturkoordinaten in der Vertex-Verarbeitung fester Funktionen und in Pixel-Shader vor PS \_ 3 0 anzugeben \_ . Diese können verwendet werden, um benutzerdefinierte Daten zu übergeben.

</dd> <dt>

<span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE \_ Tangens**
</dt> <dd>

Vertextangens-Daten.

</dd> <dt>

<span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE \_ Binormal**
</dt> <dd>

Vertex-Binormale-Daten.

</dd> <dt>

<span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ Tess Factor**
</dt> <dd>

Einzelner positiver Gleit Komma Wert. Verwenden \_ Sie D3DDECLUSAGE Tess Factor mit einem Nutzungs Index von 0, um einen Mosaik Faktor anzugeben, der in der Mosaik Einheit verwendet wird, um die Rate des Mosaik Prozesses zu steuern. Weitere Informationen zum-Datentyp finden Sie unter D3DDECLTYPE \_ FLOAT1.

</dd> <dt>

<span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE \_ positiont**
</dt> <dd>

Vertex-Daten enthalten transformierte Positionsdaten im Bereich von (0,0) bis (Viewportbreite, VIEWPORTHÖHE). Verwenden \_ Sie D3DDECLUSAGE positiont mit einem Nutzungs Index von 0, um die transformierte Position anzugeben. Wenn eine Deklaration, die diese enthält, festgelegt ist, führt die Pipeline keine Scheitelpunkt Verarbeitung aus.

</dd> <dt>

<span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**D3DDECLUSAGE- \_ Farbe**
</dt> <dd>

Vertex-Daten enthalten diffuses oder Glanz Farben. Verwenden \_ Sie die D3DDECLUSAGE-Farbe mit einem Nutzungs Index von 0, um die diffuse Farbe in den Scheitel Punkten der Fixed-Funktion und die Pixel-Shader vor PS \_ 3 0 anzugeben \_ . Verwenden \_ Sie die D3DDECLUSAGE-Farbe mit einem Verwendungs Index von 1, um die Glanz Farbe im Scheitelpunkt des Scheitel Punkts und die Pixel-Shader vor PS \_ 3 0 anzugeben \_ .

</dd> <dt>

<span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE- \_ Nebel**
</dt> <dd>

Vertex-Daten enthalten Nebel Daten. Verwenden \_ Sie D3DDECLUSAGE Fog mit einem Nutzungs Index von 0, um einen in der nach Abschluss der Pixel Schattierung verwendeten Wert für "Nebel Blend" anzugeben. Dies gilt für Pixel-Shader vor Version PS \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE \_ Tiefe**
</dt> <dd>

Vertex-Daten enthalten Tiefendaten.

</dd> <dt>

<span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**D3DDECLUSAGE- \_ Beispiel**
</dt> <dd>

Vertex-Daten enthalten Samplingdaten. Verwenden \_ Sie D3DDECLUSAGE Sample mit einem Nutzungs Index von 0, um den zu über suchenden Verschiebungs Wert anzugeben. Sie kann nur mit D3DDECLUSAGE \_ lookuppresampling oder D3DDECLUSAGE \_ Lookup verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Vertex-Daten werden mit einem Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Strukturen deklariert. Jedes Element im Array enthält einen Verwendungstyp.

Weitere Informationen zu Vertex-Deklarationen finden Sie unter [Vertex-Deklaration (Direct3D 9)](vertex-declaration.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[Vertex-Deklaration (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 




