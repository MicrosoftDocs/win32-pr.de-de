---
description: Die ID3DXSprite-Schnittstelle stellt eine Reihe von Methoden bereit, die das Zeichnen von Sprites mit Microsoft Direct3D vereinfachen.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: ID3DXSprite-Schnittstelle (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d5786096fb9c38188d73d613fd11efd97c2401e9f8ae9c7eb4a05dfe1dc1e6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729246"
---
# <a name="id3dxsprite-interface"></a>ID3DXSprite-Schnittstelle

Die ID3DXSprite-Schnittstelle stellt eine Reihe von Methoden bereit, die das Zeichnen von Sprites mit Microsoft Direct3D vereinfachen.

## <a name="members"></a>Member

Die **ID3DXSprite-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXSprite** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXSprite-Schnittstelle** verfügt über diese Methoden.



| Methode                                                | Beschreibung                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Starten**](id3dxsprite--begin.md)                   | Bereitet ein Gerät für das Zeichnen von Sprites vor.<br/>                                                                                                                                                                            |
| [**Draw**](id3dxsprite--draw.md)                     | Fügt der Liste der Batch-Sprites einen Sprite hinzu.<br/>                                                                                                                                                                     |
| [**Ende**](id3dxsprite--end.md)                       | Ruft [**ID3DXSprite::Flush**](id3dxsprite--flush.md) auf und stellt den Zustand des Geräts wieder her, wie er vor dem Aufruf von [**ID3DXSprite::Begin**](id3dxsprite--begin.md) war.<br/>                                            |
| [**Leerung**](id3dxsprite--flush.md)                   | Erzwingt, dass alle Batch-Sprites an das Gerät übermittelt werden. Gerätezustände bleiben unverändert nach dem letzten Aufruf von [**ID3DXSprite::Begin**](id3dxsprite--begin.md). Die Liste der Batch-Sprites wird dann gelöscht.<br/> |
| [**GetDevice**](id3dxsprite--getdevice.md)           | Ruft das Gerät ab, das dem Sprite-Objekt zugeordnet ist.<br/>                                                                                                                                                           |
| [**GetTransform**](id3dxsprite--gettransform.md)     | Ruft die Spritetransformation ab.<br/>                                                                                                                                                                                        |
| [**OnLostDevice**](id3dxsprite--onlostdevice.md)     | Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen freizugeben und alle Zustandsblöcke zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurückgesetzt wird.<br/>                              |
| [**OnResetDevice**](id3dxsprite--onresetdevice.md)   | Verwenden Sie diese Methode, um Ressourcen erneut zu erhalten und den Anfangszustand zu speichern.<br/>                                                                                                                                                   |
| [**SetTransform**](id3dxsprite--settransform.md)     | Legt die Spritetransformation fest.<br/>                                                                                                                                                                                        |
| [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) | Legt die Linkshänder-Weltansichtstransformation für einen Sprite fest. Vor dem Aufstellen oder Sortieren von Sprites ist ein Aufruf dieser Methode erforderlich.<br/>                                                                                 |
| [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) | Legt die rechtshändige Weltansichtstransformation für einen Sprite fest. Vor dem Aufstellen oder Sortieren von Sprites ist ein Aufruf dieser Methode erforderlich.<br/>                                                                                |



 

## <a name="remarks"></a>Hinweise

Die **ID3DXSprite-Schnittstelle** wird durch Aufrufen der [**D3DXCreateSprite-Funktion**](d3dxcreatesprite.md) abgerufen.

Die Anwendung ruft in der Regel zuerst [**ID3DXSprite::Begin**](id3dxsprite--begin.md)auf, was die Steuerung des Geräterenderingzustands, der Alphamischung und der Spritetransformation und -sortierung ermöglicht. Rufen Sie dann für jedes anzuzeigende Sprite [**ID3DXSprite::D raw**](id3dxsprite--draw.md)auf. **ID3DXSprite::D raw** kann wiederholt aufgerufen werden, um eine beliebige Anzahl von Sprites zu speichern. Um die Batch-Sprites auf dem Gerät anzuzeigen, rufen [**Sie ID3DXSprite::End**](id3dxsprite--end.md) oder [**ID3DXSprite::Flush auf.**](id3dxsprite--flush.md)

Der LPD3DXSPRITE-Typ wird als Zeiger auf die **ID3DXSprite-Schnittstelle** definiert.


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
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

 

 
