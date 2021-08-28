---
description: 'D3DXUVAtlasPartition-Funktion: Erstellen Sie einen UV-Atlas für ein Gitternetz.'
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
ms.openlocfilehash: e34c5b9fe69129cb60c604cbde1fc6bcb4df8e442b7ea29bc55cec44911505e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096126"
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

Die maximale Anzahl von Diagrammen, in die das Netz partitioniert werden soll. Weitere Informationen finden Sie in den Hinweisen zu den Partitionierungsmodi. Verwenden Sie 0, um D3DX mitzuteilen, dass der Atlas basierend auf Stretch parametrisiert werden soll.

</dd> <dt>

*fMaxStretch* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Die zulässige Menge an Stretching. 0 bedeutet, dass kein Stretching zulässig ist, 1 bedeutet, dass eine beliebige Menge an Stretching verwendet werden kann.

</dd> <dt>

*dwTextureIndex* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Nullbasierter Texturkoordinatenindex, der angibt, welche Menge von Texturkoordinaten verwendet werden soll.

</dd> <dt>

*pdwAdjazenz* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ein Zeiger auf ein Array von Adjazenzdaten mit 3 DWORDs pro Gesicht, der angibt, welche Dreiecke nebeneinander liegen (siehe [**ID3DXBaseMesh::GenerateAdencyency**](id3dxbasemesh--generateadjacency.md)).

</dd> <dt>

*pdwFalseEdges* 
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ein Array mit 3 DWORDS pro Gesicht. Jedes Gesicht gibt an, ob ein Rand false ist oder nicht. Ein nicht falscher Rand wird durch -1 angegeben, ein falscher Rand durch einen anderen Wert. Dies ermöglicht die Parametrisierung eines Gitternetzes von Quads, wobei die Ränder in der Mitte jedes Quaders nicht geschnitten werden.

</dd> <dt>

*pfIMTArray* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ein Zeiger auf ein Array integrierter Metrik tensors, der beschreibt, wie ein Dreieck gestreckt wird (siehe [IntegratedMetricTensor](using-uvatlas.md)).

</dd> <dt>

*pCallback* \[ In\]
</dt> <dd>

Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Ein Zeiger auf eine Rückruffunktion (siehe [LPD3DXUVATLASCB),](lpd3dxuvatlascb.md)die für die Überwachung des Fortschritts nützlich ist.

</dd> <dt>

*fCallbackFrequency* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Geben Sie an, wie oft D3DX den Rückruf aufruft. ein sinnvoller Standardwert ist 0,0001f.

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

Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle.**](id3dxbuffer.md) Dieser Puffer enthält ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Ausgabegitternetz angeben. Dieser Parameter darf nicht **NULL** sein, da er für den nachfolgenden Aufruf von D3DXUVAtlasPack() erforderlich ist.

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

## <a name="remarks"></a>Hinweise

D3DXUVAtlasPartition ähnelt [**D3DXUVAtlasCreate,**](d3dxuvatlascreate.md)mit der Ausnahme, dass D3DXUVAtlasPartition den letzten Komprimierungsschritt nicht ausführt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[UVAtlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)
</dt> </dl>

 

 
