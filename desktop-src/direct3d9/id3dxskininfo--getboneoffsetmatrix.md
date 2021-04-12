---
description: Ruft die markveroffsetmatrix ab.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: 'ID3DXSkinInfo:: getboneoffsetmatrix-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: fce108dc1d0eb08f198ae9375ac35ed149c5e760
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354096"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a>ID3DXSkinInfo:: getboneoffsetmatrix-Methode

Ruft die markveroffsetmatrix ab.

## <a name="syntax"></a>Syntax


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Knochen* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Die Knochen Nummer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **LPD3DXMATRIX**](d3dxmatrix.md)**

Gibt einen Zeiger auf die Knochen Offset Matrix zurück. Diesen Zeiger nicht freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**Setboneoffsetmatrix**](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[**Getnumbones**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
