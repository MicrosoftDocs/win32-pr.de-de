---
description: Ruft die Attribute des Patches ab.
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: 'ID3DXPatchMesh:: getpatchinfo-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetPatchInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70308857aa66551ed371dbe511acb6bd2d211bfb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364371"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a>ID3DXPatchMesh:: getpatchinfo-Methode

Ruft die Attribute des Patches ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPatchInfo(
  [out, retval] LPD3DXPATCHINFO PatchInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Patchinfo* \[ Out, retval\]
</dt> <dd>

Typ: **[ **LPD3DXPATCHINFO**](d3dxpatchinfo.md)**

Ein Zeiger auf die Strukturen, die die Patchattribute enthalten. Weitere Informationen zu Patch-Attributen finden Sie unter [**D3DXPATCHINFO**](d3dxpatchinfo.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 




