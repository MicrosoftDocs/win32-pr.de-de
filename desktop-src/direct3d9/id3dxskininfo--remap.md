---
description: Aktualisiert die Informationen zu den Informationen zu den Daten, die nach dem erneuten ordnen der Scheitel Punkte entsprechen Diese Methode sollte aufgerufen werden, wenn der Ziel Vertex-Puffer extern neu angeordnet wurde.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: 'ID3DXSkinInfo:: remap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 657cf0977592a8e19e68b8aeb950c62d404e7cdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354974"
---
# <a name="id3dxskininforemap-method"></a>ID3DXSkinInfo:: remap-Methode

Aktualisiert die Informationen zu den Informationen zu den Daten, die nach dem erneuten ordnen der Scheitel Punkte entsprechen Diese Methode sollte aufgerufen werden, wenn der Ziel Vertex-Puffer extern neu angeordnet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Numvertices* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der zu neuumwandenden Scheitel Punkte.

</dd> <dt>

*pvertexremap* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Array von DWords, dessen Länge durch numvertices angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Jedes Element in pvertexremap gibt den vorherigen Scheitelpunkt Index für diese Position an. Wenn sich z. b. ein Scheitelpunkt an Position 3, aber an Position 5 neu zugeordnet wurde, sollte das fünfte Element von pvertexremap 3 enthalten. Das von [**ID3DXMesh:: optimiert**](id3dxmesh--optimize.md) zurückgegebene Vertex-neuumwandlungs Array kann verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
