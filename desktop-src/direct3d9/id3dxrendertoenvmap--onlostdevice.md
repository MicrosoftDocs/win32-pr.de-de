---
description: 'ID3DXRenderToEnvMap::OnLostDevice-Methode: Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.'
ms.assetid: 76dcf5f3-0d2f-4388-9b75-c4dbd1c74982
title: ID3DXRenderToEnvMap::OnLostDevice-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88f27c259262eb7abb57246e547ad66866bb3dcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107198"
---
# <a name="id3dxrendertoenvmaponlostdevice-method"></a>ID3DXRenderToEnvMap::OnLostDevice-Methode

Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

Diese Methode sollte immer dann aufgerufen werden, wenn das Gerät verloren geht oder bevor der Benutzer [**IDirect3DDevice9::Reset aufruft.**](/windows/desktop/api) Selbst wenn das Gerät nicht tatsächlich verloren gegangen ist, ist **ID3DXRenderToEnvMap::OnLostDevice** für die Freigabe von Zustandsblocks und anderen Ressourcen verantwortlich, die möglicherweise vor dem Zurücksetzen des Geräts freigegeben werden müssen. Daher kann das Schriftartobjekt vor dem Aufruf von **IDirect3DDevice9::Reset** und [**id3DXRenderToEnvMap::OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md)nicht erneut verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




