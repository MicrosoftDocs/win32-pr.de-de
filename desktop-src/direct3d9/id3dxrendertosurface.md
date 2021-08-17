---
description: Die ID3DXRenderToSurface-Schnittstelle wird verwendet, um den Renderingprozess auf Oberflächen zu generalisieren.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: ID3DXRenderToSurface-Schnittstelle (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 238e1870fd5bf1832ffbb3b5c3a5a49533ef122277a4000bafdbaa10112b4528
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729506"
---
# <a name="id3dxrendertosurface-interface"></a>ID3DXRenderToSurface-Schnittstelle

Die ID3DXRenderToSurface-Schnittstelle wird verwendet, um den Renderingprozess auf Oberflächen zu generalisieren.

## <a name="members"></a>Member

Die **ID3DXRenderToSurface-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXRenderToSurface** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXRenderToSurface-Schnittstelle** verfügt über diese Methoden.



| Methode                                                       | Beschreibung                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginScene**](id3dxrendertosurface--beginscene.md)       | Startet eine Szene.<br/>                                                                                                                                                                      |
| [**EndScene**](id3dxrendertosurface--endscene.md)           | Beendet eine Szene.<br/>                                                                                                                                                                        |
| [**GetDesc**](id3dxrendertosurface--getdesc.md)             | Ruft die Parameter der Renderoberfläche ab.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertosurface--getdevice.md)         | Ruft das Direct3D-Gerät ab, das der Renderoberfläche zugeordnet ist.<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertosurface--onlostdevice.md)   | Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.<br/> |
| [**OnResetDevice**](id3dxrendertosurface--onresetdevice.md) | Verwenden Sie diese Methode, um Ressourcen erneut zu erhalten und den Anfangszustand zu speichern.<br/>                                                                                                                      |



 

## <a name="remarks"></a>Hinweise

Oberflächen können auf unterschiedliche Weise verwendet werden, einschließlich Renderziele, Off-Screen-Rendering oder Rendern in Texturen.

Eine Oberfläche kann mithilfe eines separaten Viewports mithilfe der [**ID3DXRenderToSurface::BeginScene-Methode**](id3dxrendertosurface--beginscene.md) konfiguriert werden, um eine benutzerdefinierte Renderansicht zur Verfügung zu stellen. Wenn die Oberfläche kein Renderziel ist, wird ein kompatibles Renderziel verwendet, und das Ergebnis wird auf die Oberfläche am Ende der Szene kopiert.

Die **ID3DXRenderToSurface-Schnittstelle** wird durch Aufrufen der [**D3DXCreateRenderToSurface-Funktion**](d3dxcreaterendertosurface.md) erhalten.

Der LPD3DXRENDERTOSURFACE-Typ ist als Zeiger auf die **ID3DXRenderToSurface-Schnittstelle** definiert.


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
