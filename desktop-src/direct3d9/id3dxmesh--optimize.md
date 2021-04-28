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
ms.openlocfilehash: debec1c0ee54e612ab0de832dbc5c2481dcefad8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093308"
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

*Flags* \[in\]
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

Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle,**](id3dxbuffer.md) die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitelpunkte den alten Scheitelpunkten zugeordnet werden. Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunktzuordnung ändern müssen.

</dd> <dt>

*ppOptMesh* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das optimierte Gitternetz darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Bemerkungen

Diese Methode generiert ein neues Gitternetz. Vor dem Ausführen von Optimize muss eine Anwendung einen Adjazenzpuffer generieren, indem [**ID3DXBaseMesh::GenerateAdjaency**](id3dxbasemesh--generateadjacency.md)aufgerufen wird. Der Adjazenzpuffer enthält Adjazenzdaten, z. B. eine Liste von Kanten und den nebeneinander liegenden Gesichtern.

Diese Methode ist der [**ID3DXBaseMesh::CloneMesh-Methode**](id3dxbasemesh--clonemesh.md) sehr ähnlich, mit der Ausnahme, dass sie beim Generieren des neuen Klons des Gitternetzes Optimierungen ausführen kann. Das Ausgabegitternetz erbt alle Erstellungsparameter des Eingabegitters.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
