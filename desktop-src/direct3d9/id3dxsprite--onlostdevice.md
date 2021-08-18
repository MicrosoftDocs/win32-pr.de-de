---
description: 'ID3DXSprite::OnLostDevice-Methode: Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen freizugeben und alle Zustandsblöcke zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurückgesetzt wird.'
ms.assetid: 60028f18-21fe-428b-9bee-d5359671da81
title: ID3DXSprite::OnLostDevice-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8431fd8b7c8e106e6eca1b28498befb828c67880d173bd5141e771885cbab1a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985199"
---
# <a name="id3dxspriteonlostdevice-method"></a>ID3DXSprite::OnLostDevice-Methode

Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen freizugeben und alle Zustandsblöcke zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurückgesetzt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Diese Methode sollte immer dann aufgerufen werden, wenn das Gerät verloren geht oder bevor der Benutzer [**IDirect3DDevice9::Reset**](/windows/desktop/api)aufruft. Auch wenn das Gerät nicht verloren gegangen ist, ist **ID3DXSprite::OnLostDevice** für das Freigeben von Zustandssperren und anderen Ressourcen verantwortlich, die vor dem Zurücksetzen des Geräts freigegeben werden müssen. Daher kann das Schriftartobjekt nicht erneut verwendet werden, bevor **IDirect3DDevice9::Reset** und dann [**ID3DXSprite::OnResetDevice**](id3dxsprite--onresetdevice.md)aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




