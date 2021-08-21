---
description: Ruft das Gerät ab, das dem Sprite-Objekt zugeordnet ist.
ms.assetid: 9ce18623-893e-4395-bdf7-8d16a641a557
title: ID3DXSprite::GetDevice-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 396558e2a3dc6c267ae4da6fe10a257d93e758cca5aa5d80bd1f40c01ce5ee25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094042"
---
# <a name="id3dxspritegetdevice-method"></a>ID3DXSprite::GetDevice-Methode

Ruft das Gerät ab, das dem Sprite-Objekt zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDevice* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

Adresse eines Zeigers auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Direct3D-Geräteobjekt darstellt, das dem Sprite-Objekt zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

Durch aufrufen dieser Methode wird die interne Verweisanzahl für die [**IDirect3DDevice9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) erhöht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 
