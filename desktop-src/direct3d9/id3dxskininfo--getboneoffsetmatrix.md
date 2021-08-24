---
description: Ruft die Offsetmatrix ab.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: ID3DXSkinInfo::GetBoneOffsetMatrix-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d10586fc9d4008ebd22b7edf2fa955628ffa0ab703ef70ed06cb2f2cb1fd8d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492300"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a>ID3DXSkinInfo::GetBoneOffsetMatrix-Methode

Ruft die Offsetmatrix ab.

## <a name="syntax"></a>Syntax


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Besen* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Nummernnummer des 50-00-

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **LPD3DXMATRIX**](d3dxmatrix.md)**

Gibt einen Zeiger auf die Offsetmatrix zurück. Geben Sie diesen Zeiger nicht frei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[**GetNumBones**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
