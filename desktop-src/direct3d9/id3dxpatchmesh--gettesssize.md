---
description: Ruft die Größe des Mosaik Netzes ab, wenn eine Mosaik Ebene angegeben ist.
ms.assetid: 86d1d1a0-1934-40e9-bff9-6c435d1e5183
title: 'ID3DXPatchMesh:: gettesssize-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetTessSize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef23f46baca7e05005cee83f6ca765b9a5214b8b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050944"
---
# <a name="id3dxpatchmeshgettesssize-method"></a>ID3DXPatchMesh:: gettesssize-Methode

Ruft die Größe des Mosaik Netzes ab, wenn eine Mosaik Ebene angegeben ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTessSize(
  [in]  FLOAT fTessLevel,
  [in]  DWORD Adaptive,
  [out] DWORD *NumTriangles,
  [out] DWORD *NumVertices
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ftess Level* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Mosaik Ebene.

</dd> <dt>

*Adaptive* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Adaptive Mosaik. Legen Sie für das adaptive Mosaik diesen Wert auf **true** fest, und legen Sie ftess Level auf den maximalen Mosaik Wert fest. Dies führt zu der maximalen Netzgröße, die für das adaptive Mosaik erforderlich ist.

</dd> <dt>

*Numdreiecke* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die Anzahl der vom Mosaik Gitter generierten Dreiecke.

</dd> <dt>

*Numvertices* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die Anzahl der Scheitel Punkte, die vom Mosaik Gitter generiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Diese Methode setzt ein einheitliches Mosaik voraus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
