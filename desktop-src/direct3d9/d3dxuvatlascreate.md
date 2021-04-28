---
description: 'D3DXUVAtlasCreate-Funktion: Erstellen sie einen UV-Atlas für ein Gitter.'
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: D3DXUVAtlasCreate-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasCreate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f382e7d59f3a5b5db8ba3cfd65ba6cc1a11e86d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117828"
---
# <a name="d3dxuvatlascreate-function"></a>D3DXUVAtlasCreate-Funktion

Erstellen Sie einen UV-Atlas für ein Gitter.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXUVAtlasCreate(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        UINT            dwWidth,
  _In_        UINT            dwHeight,
  _In_        FLOAT           fGutter,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContext,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    *ppFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein Eingabegittermodell (siehe [**ID3DXMesh),**](id3dxmesh.md)das die Objektgeometrie zum Berechnen des Atlas enthält. Das Gitternetz muss mindestens Positionsdaten und 2D-Texturkoordinaten enthalten.

</dd> <dt>

*dwMaxChartNumber* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die maximale Anzahl von Diagrammen, in die das Gitternetz partitioniert werden soll. Siehe Hinweise zu den Partitionierungsmodi. Verwenden Sie 0, um D3DX zu informieren, dass der Atlas basierend auf stretch parametrisiert werden soll.

</dd> <dt>

*fMaxStretch* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Die zulässige Stretchingmenge. 0 bedeutet, dass kein Stretching zulässig ist, 1 bedeutet, dass eine beliebige Menge an Stretching verwendet werden kann.

</dd> <dt>

*dwWidth* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Texturbreite.

</dd> <dt>

*dwHeight* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Texturhöhe.

</dd> <dt>

*fGutter* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der mindeste Abstand zwischen zwei Diagrammen im Atlas in Texel. Der Bundsteg wird immer um die Breite skaliert. Wenn also ein Bundsteg von 2,5 für eine Textur mit 512 x 512 verwendet wird, beträgt der Mindestabstand zwischen zwei Diagrammen 2,5 /512,0 Texel.

</dd> <dt>

*dwTextureIndex* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Nullbasierter Texturkoordinatenindex, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.

</dd> <dt>

*pdwAdjazenz* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ein Zeiger auf ein Array von Adjazenzdaten. mit 3 DWORDs pro Gesicht, die angeben, welche Dreiecke nebeneinander angeordnet sind (siehe [**ID3DXBaseMesh::GenerateAdencyency**](id3dxbasemesh--generateadjacency.md)).

</dd> <dt>

*pdwFalseEdges* 
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ein Array mit 3 DWORDS pro Gesicht. Jedes Gesicht gibt an, ob ein Rand false ist oder nicht. Ein nicht falscher Rand wird durch -1 angegeben, ein falscher Rand durch einen anderen Wert. Dies ermöglicht die Parametrisierung eines Gitternetzes von Quadern, wobei die Ränder in der Mitte jedes Quaders nicht geschnitten werden.

</dd> <dt>

*pfIMTArray* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ein Zeiger auf ein Array integrierter Metriktensoren, der beschreibt, wie ein Dreieck gestreckt wird (siehe [IntegratedMetricTensor](using-uvatlas.md)).

</dd> <dt>

*pCallback* \[ In\]
</dt> <dd>

Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Ein Zeiger auf eine Rückruffunktion (siehe [LPD3DXUVATLASCB),](lpd3dxuvatlascb.md)die für die Überwachung des Fortschritts nützlich ist.

</dd> <dt>

*fCallbackFrequency* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Geben Sie an, wie oft D3DX den Rückruf aufruft. Ein angemessener Standardwert ist 0,0001f.

</dd> <dt>

*pUserContent* \[ In\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übergeben wird; Wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion enthält.

</dd> <dt>

*dwOptions* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Geben Sie die Qualität der generierten Diagramme an. Siehe [**D3DXUVATLAS**](./d3dxuvatlas.md).

</dd> <dt>

*ppMeshOut* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Zeiger auf das erstellte Gitter mit dem Atlas (siehe [**ID3DXMesh**](id3dxmesh.md)).

</dd> <dt>

*ppFacePartitioning* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ein Zeiger auf ein Array der endgültigen Gesichtspartitionierungsdaten. Jedes Element enthält ein DWORD pro Gesicht (siehe [**ID3DXBuffer**](id3dxbuffer.md)).

</dd> <dt>

*ppVertexRemapArray* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ein Zeiger auf ein Array neu zugeordneter Scheitelpunkte. Jedes Arrayelement identifiziert den ursprünglichen Scheitelpunkt, von dem jeder letzte Scheitelpunkt stammt (wenn der Scheitelpunkt während der Neuzuordnung geteilt wurde). Jedes Arrayelement enthält ein DWORD pro Scheitelpunkt.

</dd> <dt>

*pfMaxStretchOut* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ein Zeiger auf den maximalen Stretchwert, der vom Atlas-Algorithmus generiert wird. Der Bereich liegt zwischen 0,0 und 1,0.

</dd> <dt>

*pdwNumChartsOut* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die Anzahl von Diagrammen, die vom Atlas-Algorithmus erstellt wurden. Wenn dwMaxChartNumber zu niedrig ist, gibt dieser Parameter die mindest erforderliche Anzahl von Diagrammen zurück, um einen Atlas zu erstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Andernfalls ist der Wert D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Bemerkungen

D3DXUVAtlasCreate kann die Meshgeometrie auf zwei Arten partitionieren:

-   Basierend auf der Anzahl der Diagramme
-   Basierend auf dem maximal zulässigen Stretching. Wenn die maximal zulässige Streckung 0 beträgt, befindet sich jedes Dreieck wahrscheinlich in einem eigenen Diagramm.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[UVAtlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)
</dt> </dl>

 

 
