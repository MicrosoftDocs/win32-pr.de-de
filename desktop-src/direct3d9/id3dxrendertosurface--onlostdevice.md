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
ms.openlocfilehash: 9073cfbc4c51b04049f39d5788b7538f768cebc82ac1036a5fdf1901f2418412
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492410"
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

## <a name="remarks"></a>Hinweise

Diese Methode sollte immer dann aufgerufen werden, wenn das Gerät verloren geht oder bevor der Benutzer [**IDirect3DDevice9::Reset aufruft.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) Selbst wenn das Gerät nicht tatsächlich verloren gegangen ist, ist ID3DXRenderToSurface::OnLostDevice für die Freigabe von Zustandsblocks und anderen Ressourcen verantwortlich, die möglicherweise freigegeben werden müssen, bevor das Gerät zurück gesetzt wird. Daher kann das Schriftartobjekt vor dem Aufruf von **IDirect3DDevice9::Reset** und id3DXRenderToSurface::OnResetDevice nicht erneut verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 
