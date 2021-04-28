---
description: 'D3DXSHPRTCompSuperCluster-Funktion: Wird mit komprimierten Ergebnissen der Scheitelpunktversion des PRT-Simulators (Precomputed Radiance Transfer) verwendet.'
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: D3DXSHPRTCompSuperCluster-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c22c8a3a14fd8af3e9104889b421068c7ff1457
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117858"
---
# <a name="d3dxshprtcompsupercluster-function"></a>D3DXSHPRTCompSuperCluster-Funktion

Wird mit komprimierten Ergebnissen der Scheitelpunktversion des PRT-Simulators (Precomputed Radiance Transfer) verwendet. Generiert "Supercluster", bei denen es sich um Gruppen von Clustern handelt, die im gleichen Zeichnen-Aufruf gezeichnet werden können. Ein gieriger Algorithmus, der die Überzeichnung minimiert, wird verwendet, um die Cluster zu gruppieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pClusterIDs* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf numVerts-Cluster-IDs (extrahiert aus einem komprimierten Puffer)

</dd> <dt>

*pScene* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein Gitternetz, das eine zusammengesetzte Szene darstellt, die an den Simulator übergeben wird. Siehe [**ID3DXMesh.**](id3dxmesh.md)

</dd> <dt>

*MaxNumClusters* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Maximale Anzahl von Clustern, die pro Supercluster zugeordnet sind.

</dd> <dt>

*NumClusters* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der im Simulator berechneten Cluster.

</dd> <dt>

*pSClusterIDs* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array der Länge *NumClusters*. Enthält den Index des Superclusters, dem der entsprechende Cluster zugewiesen wurde.

</dd> <dt>

*pNumSCs* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Anzahl der zugeordneten Supercluster.

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

 

 
