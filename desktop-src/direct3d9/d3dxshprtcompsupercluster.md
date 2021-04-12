---
description: Wird mit komprimierten Ergebnissen der vertexversion des PRT-Simulators (preberechneten Radiance Transfer) verwendet.
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: D3DXSHPRTCompSuperCluster-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 1daf25dddfaf738ecc2fed9605429a19170177ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354707"
---
# <a name="d3dxshprtcompsupercluster-function"></a>D3DXSHPRTCompSuperCluster-Funktion

Wird mit komprimierten Ergebnissen der vertexversion des PRT-Simulators (preberechneten Radiance Transfer) verwendet. Generiert "Super Cluster", bei denen es sich um Gruppen von Clustern handelt, die im selben zeichnen-Befehl gezeichnet werden können. Ein gieriger Algorithmus, der Alphablendings minimiert, wird zum Gruppieren der Cluster verwendet.

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

*pclusterids* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Zeiger auf eine num}-Cluster-IDs (aus einem komprimierten Puffer extrahiert)

</dd> <dt>

*pscene* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ein Zeiger auf ein Mesh, das die an den Simulator übergebenen Verbund Szene darstellt. Siehe [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*Maxnumclusters* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Maximale Anzahl von Clustern, die pro Super Cluster zugewiesen sind.

</dd> <dt>

*Numclusters* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Cluster, die im Simulator berechnet wurden.

</dd> <dt>

*psclusterids* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array der Länge *numclusters*. Enthält den Index des Super Clusters, dem der entsprechende Cluster zugewiesen wurde.

</dd> <dt>

*pnumscs* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Anzahl der zugewiesenen Super Cluster.

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

 

 
