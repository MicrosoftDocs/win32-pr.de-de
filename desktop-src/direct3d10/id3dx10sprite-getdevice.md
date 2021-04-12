---
description: Rufen Sie das Gerät ab, das dem Sprite-Objekt zugeordnet ist.
ms.assetid: 9119b232-22c8-4b05-b584-ce176370ca97
title: 'ID3DX10Sprite:: getdevice-Methode (d3dx10. h)'
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
ms.openlocfilehash: d4e7a3c6ebfcbcb83aaaed6273ea321b33a44ce1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356116"
---
# <a name="id3dx10spritegetdevice-method"></a>ID3DX10Sprite:: getdevice-Methode

Rufen Sie das Gerät ab, das dem Sprite-Objekt zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppdevice* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Adresse eines Zeigers auf eine ID3D10Device-Schnittstelle, die das Direct3D-Geräte Objekt darstellt, das dem Sprite-Objekt zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Durch Aufrufen dieser Methode wird der interne Verweis Zähler in der ID3D10Device-Schnittstelle vergrößert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




