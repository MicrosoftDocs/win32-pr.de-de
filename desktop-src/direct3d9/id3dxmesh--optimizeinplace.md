---
description: Generiert ein Gitternetz mit neu angeordneten Gesichtern und Scheitelpunkten, um die Zeichnungsleistung zu optimieren. Diese Methode ordnet das vorhandene Gitternetz neu an.
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: ID3DXMesh::OptimizeInplace-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0075e7a0b823f0d747859a4717a440e0c244fde76076e4b285c7d1b2a7e78d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120804"
---
# <a name="id3dxmeshoptimizeinplace-method"></a>ID3DXMesh::OptimizeInplace-Methode

Generiert ein Gitternetz mit neu angeordneten Gesichtern und Scheitelpunkten, um die Zeichnungsleistung zu optimieren. Diese Methode ordnet das vorhandene Gitternetz neu an.

## <a name="syntax"></a>Syntax


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus einem oder mehreren [**D3DXMESHOPT-Flags,**](./d3dxmeshopt.md) die den Typ der auszuführenden Optimierung angeben.

</dd> <dt>

*pAdencyencyIn* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Quellgitternetz angibt. Wenn der Rand keine angrenzenden Gesichter hat, wird der Wert 0xffffffff.

</dd> <dt>

*pAdjaencyOut* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im optimierten Netz angibt. Wenn der Rand keine angrenzenden Gesichter hat, wird der Wert 0xffffffff. Wenn der für dieses Argument angegebene Wert **NULL** ist, werden keine Adjazenzdaten zurückgegeben.

</dd> <dt>

*pFaceRemap* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Array von DWORDs (eins pro Gesicht), das das ursprüngliche Gitternetz identifiziert, das den einzelnen Gesichtern im optimierten Gitternetz entspricht. Wenn der für dieses Argument angegebene Wert **NULL** ist, werden keine Gesichtszuordnungsdaten zurückgegeben.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle,**](id3dxbuffer.md) die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitelpunkte den alten Scheitelpunkten zugeordnet werden. Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunktzuordnung ändern müssen. Wenn der für dieses Argument angegebene Wert **NULL** ist, werden keine Vertex-Neuzuordnungsdaten zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Vor dem Ausführen von **ID3DXMesh::OptimizeInplace** muss eine Anwendung einen Adjazenzpuffer generieren, indem [**sie ID3DXBaseMesh::GenerateAdjaency aufruft.**](id3dxbasemesh--generateadjacency.md) Der Adjazenzpuffer enthält Adjazenzdaten, z. B. eine Liste von Kanten und den nebeneinander liegenden Gesichtern.

> [!Note]  
> Diese Methode schlägt fehl, wenn das Gitternetz seinen Scheitelpunktpuffer mit einem anderen Gitternetz teilt, es sei denn, D3DXMESHOPT \_ IGNOREVERTS ist in Flags festgelegt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::Optimize**](id3dxmesh--optimize.md)
</dt> </dl>

 

 
