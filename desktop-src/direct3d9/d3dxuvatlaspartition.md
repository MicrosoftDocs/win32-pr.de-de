---
description: 'D3DXUVAtlasPartition-Funktion: Erstellen sie einen UV-Atlas für ein Gitternetz.'
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: D3DXUVAtlasPartition-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPartition
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 63df6bbcc1b811b9617796bc6e7e51af2dfdca56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117798"
---
# <a name="d3dxuvatlaspartition-function"></a>D3DXUVAtlasPartition-Funktion

Erstellen Sie einen UV-Atlas für ein Gitternetz.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXUVAtlasPartition(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContent,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    pFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
              LPD3DXBUFFER    *ppPartitionResultAdjacency,
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

Die maximale Anzahl von Diagrammen, in die das Gitternetz partitioniert werden soll. Weitere Informationen finden Sie in den Hinweisen zu den Partitionierungsmodi. Verwenden Sie 0, um D3DX mitzuteilen, dass der Atlas basierend auf Stretch parametrisiert werden soll.

</dd> <dt>

*fMaxStretch* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Die zulässige Menge an Stretching. 0 bedeutet, dass kein Stretching zulässig ist, 1 bedeutet, dass eine beliebige Menge an Stretching verwendet werden kann.

</dd> <dt>

*dwTextureIndex* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Nullbasierter Texturkoordinatenindex, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.

</dd> <dt>

*pdwAdjacency* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ein Zeiger auf ein Array von Adjacency-Daten mit 3 DWORDs pro Gesicht, der angibt, welche Dreiecke nebeneinander liegen (siehe [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).

</dd> <dt>

*pdwFalseEdges* 
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ein Array mit 3 DWORDS pro Gesicht. Jedes Gesicht gibt an, ob ein Rand false ist oder nicht. Ein nicht falscher Rand wird durch -1 angegeben, ein falscher Rand wird durch einen anderen Wert angegeben. Dies ermöglicht die Parametrisierung eines Gitters von Quadern, bei dem die Ränder in der Mitte jedes Quader nicht ausgeschnitten werden.

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

Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übergeben wird; wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.

</dd> <dt>

*dwOptions* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Geben Sie die Qualität der Diagramme an, die durch Kombinieren eines oder mehrerer [**D3DXUVATLAS-Flags**](./d3dxuvatlas.md) generiert werden.

</dd> <dt>

*ppMeshOut* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Zeiger auf das erstellte Gitternetz mit dem Atlas (siehe [**ID3DXMesh**](id3dxmesh.md)).

</dd> <dt>

*pFacePartitioning* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Ein Zeiger auf ein Array der endgültigen Gesichtspartitionierungsdaten. Jedes Element enthält ein DWORD pro Gesicht (siehe [**ID3DXBuffer**](id3dxbuffer.md)).

</dd> <dt>

*ppVertexRemapArray* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ein Zeiger auf ein Array neu zugeordneter Scheitelpunkte. Jedes Arrayelement identifiziert den ursprünglichen Scheitelpunkt, von dem jeder letzte Scheitelpunkt stammt (wenn der Scheitelpunkt während der Neuzuordnung geteilt wurde). Jedes Arrayelement enthält ein DWORD pro Scheitelpunkt.

</dd> <dt>

*ppPartitionResultAdjaency* 
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle.**](id3dxbuffer.md) Dieser Puffer enthält ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Ausgabegitternetz angeben. Dieser Parameter darf nicht **NULL sein,** da der nachfolgende Aufruf von D3DXUVAtlasPack() dies erfordert.

</dd> <dt>

*pfMaxStretchOut* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ein Zeiger auf den maximalen Streckungswert, der vom Atlas-Algorithmus generiert wird. Der Bereich liegt zwischen 0,0 und 1,0.

</dd> <dt>

*pdwNumChartsOut* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die Anzahl von Diagrammen, die vom Atlas-Algorithmus erstellt wurden. Wenn dwMaxChartNumber zu niedrig ist, gibt dieser Parameter die Mindestanzahl von Diagrammen zurück, die zum Erstellen eines Atlas erforderlich sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D OK, andernfalls ist der Wert \_ D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Bemerkungen

D3DXUVAtlasPartition ähnelt [**D3DXUVAtlasCreate,**](d3dxuvatlascreate.md)mit der Ausnahme, dass D3DXUVAtlasPartition den letzten Füllschritt nicht übernimmt.

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

 

 
