---
description: Wird mit komprimierten Ergebnissen der vertexversion des PRT-Simulators (preberechneten Radiance Transfer) verwendet.
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: D3DXSHPRTCompSplitMeshSC-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 18742d12b6e1ae106dcf832baccccb2416465880
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394098"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a>D3DXSHPRTCompSplitMeshSC-Funktion

Wird mit komprimierten Ergebnissen der vertexversion des PRT-Simulators (preberechneten Radiance Transfer) verwendet. Nachdem [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) aufgerufen wurde, kann diese Funktion verwendet werden, um das Mesh in eine Gruppe von Gesichtern/Scheitel Punkten pro Super Cluster aufzuteilen. Jeder Super Cluster enthält alle Gesichter, die alle in einem ihrer Cluster klassifizierten Scheitel Punkte enthalten. Alle Scheitel Punkte, die mit dieser Gruppe von Gesichtern verbunden sind, sind auch im zurückgegebenen Array ppvertstatus enthalten, das angibt, ob der Scheitelpunkt zu dem Super Cluster gehört.

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

*pclusterids* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

*Numvertices* Cluster-IDs (aus einem komprimierten Puffer extrahiert)

</dd> <dt>

*Numvertices* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Scheitel Punkte im ursprünglichen Mesh.

</dd> <dt>

*Numcs* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl von Clustern (Eingabeparameter für die Komprimierung.)

</dd> <dt>

*psclusterids* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Array von Größen- *numcs* , das Super Cluster-IDs enthalten wird.

</dd> <dt>

*Numscs* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md)zugeordneten Super Cluster.

</dd> <dt>

*pinputib* \[ in\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Unformatierten Index Puffer für Mesh. Das Format ist abhängig von *InputIBIs32Bit*.

</dd> <dt>

*InputIBIs32Bit* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

**True** gibt an, dass der Index Puffer auf 32 Bit festgelegt ist. Andernfalls 16 Bit.

</dd> <dt>

*Numerische Werte* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Gesichter im ursprünglichen Mesh (*pinputib* ist dreimal so lang).

</dd> <dt>

*ppibdata* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Unformatierten Index Puffer, der die sich ergebenden geteilten Gesichter enthält. Das von *InputIBIs32Bit* festgelegte Format. Zugeordnet von Funktion.

</dd> <dt>

*pibdatalength* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Länge der in der Funktion zugewiesenen *ppibdata*.

</dd> <dt>

*OutputIBIs32Bit* \[ in, out\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Wenn **true**, wird ein ganzzahliges Array ohne Vorzeichen zugeordnet. Andernfalls weist ein unsigniertes kurzes Array zu.

</dd> <dt>

*ppfakeremap* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zuordnung von jedem Gesicht in *ppibdata* zu ursprünglichen Gesichtern. Länge ist \* *pibdatalength*/3.

</dd> <dt>

*ppvertdata* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Neue Vertex-Datenstruktur. Größe von *pvertdatalength*.

</dd> <dt>

*pvertdatalength* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Anzahl der neuen Scheitel Punkte in geteiltem Mesh. Zugewiesen in-Funktion.

</dd> <dt>

*pscclusterlist* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Ein Array von Längen- *numcs* , in das *pscdata* indiziert (*pclusterids* - \* Felder) für jeden Supercluster, enthält nach Supercluster sortierte Cluster.

</dd> <dt>

*pscdata* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***

Struktur pro Super Cluster. Enthält Indizes in " *ppibdata*", " *pscclusterlist*" und " *ppvertdata*".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Voraus berechnete Strahlungs Übertragungsfunktionen](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
