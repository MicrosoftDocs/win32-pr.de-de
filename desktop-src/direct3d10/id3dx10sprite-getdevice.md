---
description: Rufen Sie das Gerät ab, das dem Sprite-Objekt zugeordnet ist.
ms.assetid: 9119b232-22c8-4b05-b584-ce176370ca97
title: ID3DX10Sprite::GetDevice-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 13513b6fcd2bdb952eda17f10cc81406ff484a20dce3f690d43dd3b5c28eb08f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634250"
---
# <a name="id3dx10spritegetdevice-method"></a>ID3DX10Sprite::GetDevice-Methode

Rufen Sie das Gerät ab, das dem Sprite-Objekt zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDevice* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Adresse eines Zeigers auf eine ID3D10Device-Schnittstelle, die das Direct3D-Geräteobjekt darstellt, das dem Sprite-Objekt zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Durch aufrufen dieser Methode wird die interne Verweisanzahl für die ID3D10Device-Schnittstelle erhöht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




