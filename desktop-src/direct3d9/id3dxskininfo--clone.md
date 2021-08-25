---
description: Klont ein Skininformationsobjekt.
ms.assetid: 82d0a78a-95f3-4b09-bc1a-b4bc663e0850
title: ID3DXSkinInfo::Clone-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Clone
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19a07c3d29c4c73b423ec5d93e2eda549243a00ff7ee3570cca9b9699fbd1be2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893300"
---
# <a name="id3dxskininfoclone-method"></a>ID3DXSkinInfo::Clone-Methode

Klont ein Skininformationsobjekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [in, out] LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppSkinInfo* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Adresse eines Zeigers auf ein [**ID3DXSkinInfo-Objekt,**](id3dxskininfo.md) das das geklonte Objekt enthält, wenn die Methode erfolgreich ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 




