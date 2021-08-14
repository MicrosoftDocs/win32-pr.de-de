---
description: 'ID3DXEffect::OnLostDevice-Methode: Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen freizugeben und alle Zustandsblöcke zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurückgesetzt wird.'
ms.assetid: f56925d8-17f7-44c5-a371-3cde41804613
title: ID3DXEffect::OnLostDevice-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnLostDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d198cb06461fc377933f2dc90c1e3fb687559ef7b83cc7becd9f04bdf1b78d1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521216"
---
# <a name="id3dxeffectonlostdevice-method"></a>ID3DXEffect::OnLostDevice-Methode

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

Diese Methode sollte immer dann aufgerufen werden, wenn das Gerät verloren geht oder bevor der Benutzer [**IDirect3DDevice9::Reset**](/windows/desktop/api)aufruft. Auch wenn das Gerät nicht verloren gegangen ist, ist **ID3DXEffect::OnLostDevice** für das Freigeben von Zustandssperren und anderen Ressourcen verantwortlich, die vor dem Zurücksetzen des Geräts freigegeben werden müssen. Daher kann das Schriftartobjekt nicht erneut verwendet werden, bevor **IDirect3DDevice9::Reset** und dann [**ID3DXEffect::OnResetDevice**](id3dxeffect--onresetdevice.md)aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




