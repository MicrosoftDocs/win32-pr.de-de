---
description: 'D3DXSHPRTCompSplitMeshSC-Funktion: Wird mit komprimierten Ergebnissen der Scheitelpunktversion des PRT-Simulators (Precomputed Radiance Transfer) verwendet.'
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: D3DXSHPRTCompSplitMeshSC-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e51a86ec9b12992d49364d3a7c614751dacafac3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093898"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a>D3DXSHPRTCompSplitMeshSC-Funktion

Wird mit komprimierten Ergebnissen der Scheitelpunktversion des PRT-Simulators (Precomputed Radiance Transfer) verwendet. Nachdem [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) aufgerufen wurde, kann diese Funktion verwendet werden, um das Gitternetz in eine Gruppe von Gesichtern/Scheitelpunkten pro Supercluster aufzuteilen. Jeder Supercluster enthält alle Gesichter, die einen beliebigen Scheitelpunkt enthalten, der in einem seiner Cluster klassifiziert ist. Alle Scheitelpunkte, die mit dieser Gruppe von Gesichtern verbunden sind, sind auch im zurückgegebenen Array ppVertStatus enthalten, das angibt, ob der Scheitelpunkt zum Supercluster gehört.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pClusterIDs* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

*NumVertices-Cluster-IDs* (aus einem komprimierten Puffer extrahiert)

</dd> <dt>

*NumVertices* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Scheitelpunkte im ursprünglichen Gitternetz.

</dd> <dt>

*NumCs* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl von Clustern (Eingabeparameter für Komprimierung))

</dd> <dt>

*pSClusterIDs* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Array von *NumCs* der Größe, die Supercluster-IDs enthalten.

</dd> <dt>

*NumSCs* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl von Superclustern, die in [**D3DXSHPRTCompSuperCluster zugeordnet sind.**](d3dxshprtcompsupercluster.md)

</dd> <dt>

*pInputIB* \[ In\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Unformatierter Indexpuffer für Mesh. Das Format hängt von *InputIBIs32Bit ab.*

</dd> <dt>

*InputIBIs32Bit* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

True **gibt an,** dass der Indexpuffer auf 32 Bit festgelegt ist. andernfalls 16 Bit.

</dd> <dt>

*NumFaces* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Gesichter im ursprünglichen Gitter (*pInputIB* ist das 3-fache dieser Länge.)

</dd> <dt>

*ppIBData* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Unformatierter Indexpuffer, der die resultierenden geteilten Gesichter enthält. Format, das von *InputIBIs32Bit bestimmt wird.* Zugeordnet nach Funktion.

</dd> <dt>

*pIBDataLength* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Länge von *ppIBData,* zugewiesen in funktion.

</dd> <dt>

*OutputIBIs32Bit* \[ in, out\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

True gibt an, dass ein Ganzzahlarray ohne Vorzeichen zuordnet. andernfalls ordnet ein short-Array ohne Vorzeichen zu.

</dd> <dt>

*ppFaceRemap* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zuordnung jedes Gesichts in *ppIBData* zu ursprünglichen Gesichtern. Die Länge ist \* *pIBDataLength*/3.

</dd> <dt>

*ppVertData* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Neue Scheitelpunktdatenstruktur. Größe von *pVertDataLength.*

</dd> <dt>

*pVertDataLength* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Anzahl der neuen Scheitelpunkte im geteilten Gitternetz. In Funktion zugewiesen.

</dd> <dt>

*pSCClusterList* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Ein Array mit *NumCs* der Länge, in das *pSCData* für jeden Supercluster indiziert *(pClusterIDs-Felder),* \* enthält Cluster, die nach Supercluster sortiert sind.

</dd> <dt>

*pSCData* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***

Struktur pro Supercluster. Enthält Indizes in *ppIBData,* *pSCClusterList* und *ppVertData.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorausberechnungsfunktionen für die Übertragung von Radiance](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
