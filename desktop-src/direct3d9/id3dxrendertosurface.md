---
description: Die ID3DXRenderToSurface-Schnittstelle wird verwendet, um den Renderingvorgang für-Oberflächen zu generalisieren.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: ID3DXRenderToSurface-Schnittstelle (D3dx9core. h)
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
ms.openlocfilehash: 577e729e4e1a510dd24dc981b2b90bdca27dc0f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355826"
---
# <a name="id3dxrendertosurface-interface"></a>ID3DXRenderToSurface-Schnittstelle

Die ID3DXRenderToSurface-Schnittstelle wird verwendet, um den Renderingvorgang für-Oberflächen zu generalisieren.

## <a name="members"></a>Member

Die **ID3DXRenderToSurface** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXRenderToSurface** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXRenderToSurface** -Schnittstelle verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginScene**](id3dxrendertosurface--beginscene.md)       | Beginnt eine Szene.<br/>                                                                                                                                                                      |
| [**EndScene**](id3dxrendertosurface--endscene.md)           | Beendet eine Szene.<br/>                                                                                                                                                                        |
| [**GetDesc**](id3dxrendertosurface--getdesc.md)             | Ruft die Parameter der Renderoberfläche ab.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertosurface--getdevice.md)         | Ruft das Direct3D-Gerät ab, das der Renderoberfläche zugeordnet ist.<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertosurface--onlostdevice.md)   | Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.<br/> |
| [**OnResetDevice**](id3dxrendertosurface--onresetdevice.md) | Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.<br/>                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Oberflächen können auf verschiedene Arten verwendet werden, z.b. Renderingziele, Offscreen-Rendering oder Rendering in Texturen.

Eine Oberfläche kann mithilfe eines separaten Viewports konfiguriert werden, indem die [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md) -Methode verwendet wird, um eine benutzerdefinierte Renderansicht bereitzustellen. Wenn es sich bei der-Oberfläche nicht um ein Renderziel handelt, wird ein kompatibles Renderziel verwendet, und das Ergebnis wird auf die-Oberfläche am Ende der Szene kopiert.

Die **ID3DXRenderToSurface** -Schnittstelle wird durch Aufrufen der [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) -Funktion abgerufen.

Der LPD3DXRENDERTOSURFACE-Typ wird als Zeiger auf die **ID3DXRenderToSurface** -Schnittstelle definiert.


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
