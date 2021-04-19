---
description: Erstellen Sie einen UV-Atlas für ein Mesh.
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: D3DXUVAtlasPartition-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 707a503832a4fd66ab2e8d9346587d11544a885c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361861"
---
# <a name="d3dxuvatlaspartition-function"></a>D3DXUVAtlasPartition-Funktion

Erstellen Sie einen UV-Atlas für ein Mesh.

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

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein Eingabe Mesh (siehe [**ID3DXMesh**](id3dxmesh.md)), das die Objekt Geometrie zum Berechnen des Atlas enthält. Das Mesh muss mindestens Positionsdaten und 2D-Texturkoordinaten enthalten.

</dd> <dt>

*dwmaxchartnumber* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die maximale Anzahl von Diagrammen, in die das Mesh partitioniert werden soll. Siehe Hinweise zu den Partitionierungs Modi. Verwenden Sie 0, um D3DX zu sagen, dass der Atlas auf der Grundlage von Stretch parametrisiert werden soll.

</dd> <dt>

*"f"* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Umfang der zulässigen Streckung. 0 bedeutet, dass keine Streckung zulässig ist, 1 bedeutet, dass eine beliebige Streckung verwendet werden kann.

</dd> <dt>

*dwtextureindex* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

NULL basierter Texturkoordinaten Index, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.

</dd> <dt>

*PDW-ency* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Ein Zeiger auf ein Array von Ereignisdaten mit 3 DWords pro Gesicht, das angibt, welche Dreiecke nebeneinander zueinander stehen (siehe [**ID3DXBaseMesh:: generatefaceency**](id3dxbasemesh--generateadjacency.md)).

</dd> <dt>

*pdwfalseedges* 
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Ein Array mit 3 DWords pro Gesicht. Jedes Gesicht gibt an, ob ein Rand false ist oder nicht. Ein nicht-false-Rand wird durch-1 angegeben. ein falscher Rand wird durch einen beliebigen anderen Wert angegeben. Dies ermöglicht die Parametrisierung eines Netzes von Quads, bei dem die Ränder in der Mitte der einzelnen Quad nicht abgeschnitten werden.

</dd> <dt>

*pfimtarray* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Ein Zeiger auf ein Array von integrierten metriktensoren, das beschreibt, wie ein Dreieck gestreckt wird (siehe [integratedmetrictensor](using-uvatlas.md)).

</dd> <dt>

*pCallback* \[ in\]
</dt> <dd>

Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Ein Zeiger auf eine Rückruffunktion (siehe [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)), die zum Überwachen des Fortschritts nützlich ist.

</dd> <dt>

" *schcallbackfrequency* \[ " in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Geben Sie an, wie oft D3DX den Rückruf aufruft. ein angemessener Standardwert ist 0,0001 f.

</dd> <dt>

*pusercontent* \[ in\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übermittelt wird. wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Geben Sie die Qualität der Diagramme an, die durch Kombinieren von mindestens einem [**D3DXUVATLAS**](./d3dxuvatlas.md) -Flags generiert werden.

</dd> <dt>

*ppmeshout* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Zeiger auf das erstellte Mesh mit dem Atlas (siehe [**ID3DXMesh**](id3dxmesh.md)).

</dd> <dt>

*pfacepartitionierung* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Ein Zeiger auf ein Array der letzten Gesichts Partitionierungs Daten. Jedes Element enthält ein DWORD pro Gesicht (siehe [**ID3DXBuffer**](id3dxbuffer.md)).

</dd> <dt>

*ppvertexrematexray* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ein Zeiger auf ein Array von neu zugeordnete Vertices. Jedes Array Element identifiziert den ursprünglichen Vertex, von dem jeder abschließende Scheitelpunkt stammt (wenn der Scheitelpunkt während der Neuzuordnung aufgeteilt wurde). Jedes Array Element enthält ein DWORD pro Scheitelpunkt.

</dd> <dt>

*pppartitionresultadjacency* 
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle. Dieser Puffer enthält ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Ausgabe Mesh angeben. Dieser Parameter darf nicht **null** sein, da er für den nachfolgenden Aufrufen von D3DXUVAtlasPack () erforderlich ist.

</dd> <dt>

*pfmaxstretchout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Ein Zeiger auf den maximalen streckungs Wert, der vom Atlas-Algorithmus generiert wird. Der Bereich liegt zwischen 0,0 und 1,0.

</dd> <dt>

*pdwnumcharout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die Anzahl der Diagramme, die vom Atlas-Algorithmus erstellt wurden. Wenn dwmaxchartnumber zu niedrig ist, gibt dieser Parameter die Mindestanzahl von Diagrammen zurück, die zum Erstellen eines Atlas erforderlich ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK; andernfalls ist der Wert D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

D3DXUVAtlasPartition ähnelt [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), mit der Ausnahme, dass D3DXUVAtlasPartition den abschließenden Verpackungs Schritt nicht ausführt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Command-Line Tool für UV-Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)
</dt> </dl>

 

 
