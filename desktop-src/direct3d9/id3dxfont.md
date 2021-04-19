---
description: Die ID3DXFont-Schnittstelle kapselt die Texturen und Ressourcen, die erforderlich sind, um eine bestimmte Schriftart auf einem bestimmten Gerät zu Rendering.
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: ID3DXFont-Schnittstelle (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b3919e4198feddbe4ac193f58f63d48753aa94d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355839"
---
# <a name="id3dxfont-interface"></a>ID3DXFont-Schnittstelle

Die ID3DXFont-Schnittstelle kapselt die Texturen und Ressourcen, die erforderlich sind, um eine bestimmte Schriftart auf einem bestimmten Gerät zu Rendering.

## <a name="members"></a>Member

Die **ID3DXFont** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXFont** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXFont** -Schnittstelle verfügt über diese Methoden.



| Methode                                                    | BESCHREIBUNG                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText**](id3dxfont--drawtext.md)                   | Zeichnet formatierten Text. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.<br/>                                                                                                                                                               |
| [**GetDC**](id3dxfont--getdc.md)                         | Gibt ein Handle für einen Anzeigegeräte Kontext (DC) zurück, der über den Schriftart Satz verfügt.<br/>                                                                                                                                                           |
| [**GetDesc**](id3dxfont--getdesc.md)                     | Ruft eine Beschreibung des aktuellen Schriftart Objekts ab. Getdescw und getdesca sind mit dieser Methode identisch, mit dem Unterschied, dass ein Zeiger an eine [**D3DXFONT \_**](d3dxfont-desc.md) -oder **D3DXFONT- \_ DeScA** -Struktur zurückgegeben wird.<br/> |
| [**GetDevice**](id3dxfont--getdevice.md)                 | Ruft das Direct3D-Gerät ab, das dem Schriftart Objekt zugeordnet ist.<br/>                                                                                                                                                                     |
| [**Getglyphdata**](id3dxfont--getglyphdata.md)           | Gibt Informationen über die Platzierung und die Ausrichtung eines Symbols in einer Zeichen Zelle zurück.<br/>                                                                                                                                            |
| [**GetTextMetrics**](id3dxfont--gettextmetrics.md)       | Ruft Schriftart Eigenschaften ab, die in einer [**TextMetric**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) -Struktur identifiziert werden. Diese Methode unterstützt die ANSI-und Unicode-Compilereinstellungen.<br/>                                                                       |
| [**OnLostDevice**](id3dxfont--onlostdevice.md)           | Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.<br/>                                              |
| [**OnResetDevice**](id3dxfont--onresetdevice.md)         | Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.<br/>                                                                                                                                                                    |
| [**Preloadcharacter**](id3dxfont--preloadcharacters.md) | Lädt eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.<br/>                                                                                                                               |
| [**Präloadglyphen**](id3dxfont--preloadglyphs.md)         | Lädt eine Reihe von Symbolen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.<br/>                                                                                                                                   |
| [**PreloadText**](id3dxfont--preloadtext.md)             | Lädt formatierten Text in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.<br/>                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Die **ID3DXFont** -Schnittstelle wird durch Aufrufen von [**D3DXCreateFont**](d3dxcreatefont.md) oder [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md)abgerufen.

Der LPD3DXFONT-Typ wird als Zeiger auf die **ID3DXFont** -Schnittstelle definiert.


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
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

 

 
