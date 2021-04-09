---
description: Die ID3DXSprite-Schnittstelle stellt eine Reihe von Methoden bereit, die das Zeichnen von Sprites mithilfe von Microsoft Direct3D vereinfachen.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: ID3DXSprite-Schnittstelle (D3dx9core. h)
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
ms.openlocfilehash: 3703132cd8a0f7744119d9b8cb5d9d48f260094c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870135"
---
# <a name="id3dxsprite-interface"></a>ID3DXSprite-Schnittstelle

Die ID3DXSprite-Schnittstelle stellt eine Reihe von Methoden bereit, die das Zeichnen von Sprites mithilfe von Microsoft Direct3D vereinfachen.

## <a name="members"></a>Member

Die **ID3DXSprite** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXSprite** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXSprite** -Schnittstelle verfügt über diese Methoden.



| Methode                                                | BESCHREIBUNG                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Starten**](id3dxsprite--begin.md)                   | Bereitet ein Gerät zum Zeichnen von Sprites vor.<br/>                                                                                                                                                                            |
| [**Draw**](id3dxsprite--draw.md)                     | Fügt der Liste der im Batch verarbeiteten Sprites ein Sprite hinzu.<br/>                                                                                                                                                                     |
| [**ENDE**](id3dxsprite--end.md)                       | Ruft [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) auf und stellt den Gerätezustand vor dem Aufrufen von [**ID3DXSprite:: begin**](id3dxsprite--begin.md) wieder her.<br/>                                            |
| [**Leerung**](id3dxsprite--flush.md)                   | Erzwingt, dass alle Batch-Sprites an das Gerät übermittelt werden. Gerätezustände verbleiben nach dem letzten [**ID3DXSprite:: begin**](id3dxsprite--begin.md)-Rückruf. Die Liste der im Batch verarbeiteten Sprites wird dann gelöscht.<br/> |
| [**GetDevice**](id3dxsprite--getdevice.md)           | Ruft das Gerät ab, das dem Sprite-Objekt zugeordnet ist.<br/>                                                                                                                                                           |
| [**GetTransform**](id3dxsprite--gettransform.md)     | Ruft die Sprite-Transformation ab.<br/>                                                                                                                                                                                        |
| [**OnLostDevice**](id3dxsprite--onlostdevice.md)     | Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.<br/>                              |
| [**OnResetDevice**](id3dxsprite--onresetdevice.md)   | Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.<br/>                                                                                                                                                   |
| [**SetTransform**](id3dxsprite--settransform.md)     | Legt die Sprite-Transformation fest.<br/>                                                                                                                                                                                        |
| [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) | Legt die linke Seite "World-View Transform" für ein Sprite fest. Ein Aufrufe dieser Methode ist vor dem abgleichen oder Sortieren von Sprites erforderlich.<br/>                                                                                 |
| [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) | Legt die von rechts ausgebene World-View-Transformation für ein Sprite fest. Ein Aufrufe dieser Methode ist vor dem abgleichen oder Sortieren von Sprites erforderlich.<br/>                                                                                |



 

## <a name="remarks"></a>Bemerkungen

Die **ID3DXSprite** -Schnittstelle wird durch Aufrufen der [**D3DXCreateSprite**](d3dxcreatesprite.md) -Funktion abgerufen.

Die Anwendung ruft in der Regel zuerst [**ID3DXSprite:: begin**](id3dxsprite--begin.md)auf und ermöglicht so die Kontrolle über den Geräte Rendering, die Alpha Mischung und die Sprite-Transformation und-Sortierung. Nennen Sie dann für jedes Sprite, das angezeigt werden soll, [**ID3DXSprite::D RAW**](id3dxsprite--draw.md). **ID3DXSprite::D RAW** kann wiederholt aufgerufen werden, um eine beliebige Anzahl von Sprites zu speichern. Um die Batch Verarbeitung für das Gerät anzuzeigen, müssen Sie [**ID3DXSprite:: End**](id3dxsprite--end.md) oder [**ID3DXSprite:: Flush**](id3dxsprite--flush.md)aufrufen.

Der LPD3DXSPRITE-Typ wird als Zeiger auf die **ID3DXSprite** -Schnittstelle definiert.


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
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

 

 
