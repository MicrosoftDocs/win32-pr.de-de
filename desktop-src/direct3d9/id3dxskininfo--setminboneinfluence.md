---
description: Legt den minimalen Einfluss auf Dies fest. Einflusswerte, die kleiner als diese sind, werden ignoriert.
ms.assetid: 9af19c9e-bb6e-4f93-973f-5c38f88eea3d
title: ID3DXSkinInfo::SetMinBoneInfluence-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetMinBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: abe9f1d7f9c54b9c3086160b974e2bc7dc659eb6dae3ff647f059627ff3ef145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747480"
---
# <a name="id3dxskininfosetminboneinfluence-method"></a>ID3DXSkinInfo::SetMinBoneInfluence-Methode

Legt den minimalen Einfluss auf Dies fest. Einflusswerte, die kleiner als diese sind, werden ignoriert.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMinBoneInfluence(
  [in] FLOAT MinInfl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MinInfl* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Minimaler Einflusswert. Einflusswerte, die kleiner als diese sind, werden ignoriert.

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
</dt> <dt>

[**ID3DXSkinInfo::GetMinBoneInfluence**](id3dxskininfo--getminboneinfluence.md)
</dt> </dl>

 

 
