---
description: Führt ein einheitliches Mosaik basierend auf der Mosaik Ebene aus.
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: 'ID3DXPatchMesh:: tttellate-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Tessellate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b94b79a9decd2f44fa1675e257a2401e2ae8f7a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373550"
---
# <a name="id3dxpatchmeshtessellate-method"></a>ID3DXPatchMesh:: Tess-Methode

Führt ein einheitliches Mosaik basierend auf der Mosaik Ebene aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ftess Level* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Mosaik Ebene. Dies ist die Anzahl der Scheitel Punkte, die zwischen vorhandenen Vertices eingeführt wurden. Der Bereich dieses float-Parameters ist 0 < ftess Level <= 32.

</dd> <dt>

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Resultierende Mosaik Gitter. Siehe [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird effizienter durchgeführt, wenn das patchmesh mit [**ID3DXPatchMesh:: optimiert**](id3dxpatchmesh--optimize.md)optimiert wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
