---
description: 'ID3DXMesh::Optimize-Methode: Generiert ein neues Gitternetz mit neu angeordneten Gesichtern und Scheitelungen, um die Zeichnungsleistung zu optimieren.'
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: ID3DXMesh::Optimize-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4ea03bcaaab492ec09dd24ec93c6a9c9ca393c1399b05e12096a8ba1f4f9aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493100"
---
# <a name="id3dxmeshoptimize-method"></a>ID3DXMesh::Optimize-Methode

Generiert ein neues Gitternetz mit neu angeordneten Gesichtern und Scheitelungen, um die Zeichnungsleistung zu optimieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt den Typ der durchzuführenden Optimierung an. Dieser Parameter kann auf eine Kombination aus mindestens einem Flag von [**D3DXMESHOPT**](./d3dxmeshopt.md) und [**D3DXMESH**](./d3dxmesh.md) festgelegt werden (außer D3DXMESH \_ 32BIT, D3DXMESH \_ IB WRITEONLY und \_ D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pAdjacencyIn* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Quellgitter angibt. Wenn der Rand keine angrenzenden Gesichter hat, wird der Wert 0xffffffff. Siehe Hinweise.

</dd> <dt>

*pAdjacencyOut* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im optimierten Gitter angibt. Wenn der Rand keine angrenzenden Gesichter hat, wird der Wert 0xffffffff.

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Array von DWORDs pro Gesicht, das das ursprüngliche Gitternetzgesicht identifiziert, das jedem Gesicht im optimierten Gitter entspricht. Wenn der für dieses Argument angegebene Wert **NULL ist,** werden keine Gesichtszuordnungsdaten zurückgegeben.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle,**](id3dxbuffer.md) die ein DWORD für jeden Scheitelpunkt enthält, das angibt, wie die neuen Scheitelpunkte den alten Scheitelpunkte zuordnen. Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunktzuordnung ändern müssen.

</dd> <dt>

*ppOptMesh* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das optimierte Gitternetz darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Methode generiert ein neues Gitter. Vor dem Ausführen von Optimize muss eine Anwendung durch Aufrufen von [**ID3DXBaseMesh::GenerateAdjacency einen Adjacency-Puffer generieren.**](id3dxbasemesh--generateadjacency.md) Der Adjacency-Puffer enthält Adjacency-Daten, z. B. eine Liste von Kanten und die nebeneinander liegenden Gesichter.

Diese Methode ist der [**ID3DXBaseMesh::CloneMesh-Methode**](id3dxbasemesh--clonemesh.md) sehr ähnlich, mit der Ausnahme, dass sie beim Generieren des neuen Klons des Gitters optimierungen kann. Das Ausgabegitternetz erbt alle Erstellungsparameter des Eingabegitters.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
