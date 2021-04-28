---
description: 'ID3DXRenderToSurface::OnLostDevice-Methode: Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.'
ms.assetid: 8962236d-4801-46a3-9944-a7c4ad762882
title: ID3DXRenderToSurface::OnLostDevice-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 772b678dc4260954c2e03c13d7259565cd896bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093113"
---
# <a name="id3dxrendertosurfaceonlostdevice-method"></a>ID3DXRenderToSurface::OnLostDevice-Methode

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

Diese Methode sollte immer dann aufgerufen werden, wenn das Gerät verloren geht oder bevor der Benutzer [**IDirect3DDevice9::Reset aufruft.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) Selbst wenn das Gerät nicht tatsächlich verloren gegangen ist, ist ID3DXRenderToSurface::OnLostDevice für die Freigabe von Zustandsblocks und anderen Ressourcen verantwortlich, die möglicherweise freigegeben werden müssen, bevor das Gerät zurück gesetzt wird. Daher kann das Schriftartobjekt vor dem Aufruf von **IDirect3DDevice9::Reset** und id3DXRenderToSurface::OnResetDevice nicht erneut verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 
