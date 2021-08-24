---
description: Nimmt ein Gitternetz und gibt ein neues Gitternetz mit Mischungsgewichtungen, Indizes und einer Kombinationstabelle pro Scheitelpunkt zurück. In der Tabelle wird beschrieben, welche Paletten sich auf die Teilmengen des Gitternetzes auswirken.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: ID3DXSkinInfo::ConvertToIndexedBlendedMesh-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9aa2b4bef607197c0f6fea084054d0e4fed1c721388677d45b465aff9c39ce49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790450"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a>ID3DXSkinInfo::ConvertToIndexedBlendedMesh-Methode

Nimmt ein Gitternetz und gibt ein neues Gitternetz mit Mischungsgewichtungen, Indizes und einer Kombinationstabelle pro Scheitelpunkt zurück. In der Tabelle wird beschrieben, welche Paletten sich auf die Teilmengen des Gitternetzes auswirken.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Das Eingabegitternetz. Siehe [**ID3DXMesh.**](id3dxmesh.md)

</dd> <dt>

*Optionen* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Derzeit nicht verwendet.

</dd> <dt>

*paletteSize* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der für das Skinning der Matrixpalette verfügbaren Matrizen.

</dd> <dt>

*pAdencyencyIn* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Adjazenzinformationen für das Eingabegitternetz.

</dd> <dt>

*pAdjaencyOut* \[ In\]
</dt> <dd>

Typ: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Ausgabe von Mesh-Adjazenzinformationen.

</dd> <dt>

*pFaceRemap* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Array von DWORDs ,eins pro Gesicht, das das ursprüngliche Netzgesicht identifiziert, das den einzelnen Gesichtern im gemischten Gitternetz entspricht. Wenn der für dieses Argument angegebene Wert **NULL** ist, werden keine Gesichtszuordnungsdaten zurückgegeben.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle,**](id3dxbuffer.md) die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitelpunkte den alten Scheitelpunkten zugeordnet werden. Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunktzuordnung ändern müssen. Dieser Parameter ist optional. **NULL** kann verwendet werden.

</dd> <dt>

*pMaxVertexInfl* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf ein DWORD, das die maximale Anzahl von Durchlässigkeitsfaktoren enthält, die pro Scheitelpunkt für diese Skinningmethode erforderlich sind.

</dd> <dt>

*pNumBoneCombinations* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf die Anzahl der Pfeile in der Kombinationstabelle für Diess.

</dd> <dt>

*ppBoneCombinationTable* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf die Verbundtabelle. Die Daten sind in einer [**D3DXBONECOMBINATION-Struktur**](d3dxbonecombination.md) organisiert.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Zeiger auf das neue Gitternetz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Jedes Element in den Neuzuordnungsarrays gibt den vorherigen Index für diese Position an. Wenn sich beispielsweise ein Scheitelpunkt an Position 3 befand, aber an Position 5 neu zugeordnet wurde, enthält das fünfte Element von pVertexRemap 3.

Diese Methode wird nicht auf Hardware ausgeführt, die keine Vertexmischung mit festen Funktionen unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
