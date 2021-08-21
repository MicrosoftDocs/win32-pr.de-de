---
description: Die ID3DXFont-Schnittstelle kapselt die Texturen und Ressourcen, die zum Rendern einer bestimmten Schriftart auf einem bestimmten Gerät erforderlich sind.
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: ID3DXFont-Schnittstelle (D3dx9core.h)
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
ms.openlocfilehash: f05322ef2d7898f0025154989e9ac09ab8355025d8ad1ed94034fb25da66592f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493651"
---
# <a name="id3dxfont-interface"></a>ID3DXFont-Schnittstelle

Die ID3DXFont-Schnittstelle kapselt die Texturen und Ressourcen, die zum Rendern einer bestimmten Schriftart auf einem bestimmten Gerät erforderlich sind.

## <a name="members"></a>Member

Die **ID3DXFont-Schnittstelle erbt** von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXFont** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXFont-Schnittstelle** verfügt über diese Methoden.



| Methode                                                    | Beschreibung                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Drawtext**](id3dxfont--drawtext.md)                   | Zeichnet formatierten Text. Diese Methode unterstützt ANSI- und Unicode-Zeichenfolgen.<br/>                                                                                                                                                               |
| [**GetDC**](id3dxfont--getdc.md)                         | Gibt ein Handle für einen Anzeigegerätekontext (DC) zurück, für den die Schriftart festgelegt ist.<br/>                                                                                                                                                           |
| [**GetDesc**](id3dxfont--getdesc.md)                     | Ruft eine Beschreibung des aktuellen Schriftartobjekts ab. GetDescW und GetDescA sind mit dieser Methode identisch, mit der Ausnahme, dass ein Zeiger auf eine [**D3DXFONT \_ DESCW-**](d3dxfont-desc.md) bzw. **D3DXFONT \_ DESCA-Struktur** zurückgegeben wird.<br/> |
| [**GetDevice**](id3dxfont--getdevice.md)                 | Ruft das Direct3D-Gerät ab, das dem Schriftartobjekt zugeordnet ist.<br/>                                                                                                                                                                     |
| [**GetGlyphData**](id3dxfont--getglyphdata.md)           | Gibt Informationen zur Platzierung und Ausrichtung eines Glyphen in einer Zeichenzelle zurück.<br/>                                                                                                                                            |
| [**GetTextMetrics**](id3dxfont--gettextmetrics.md)       | Ruft Schriftartmerkmale ab, die in einer [**TEXTMETRIC-Struktur**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) identifiziert werden. Diese Methode unterstützt ANSI- und Unicode-Compilereinstellungen.<br/>                                                                       |
| [**OnLostDevice**](id3dxfont--onlostdevice.md)           | Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen freizugeben und alle Zustandsblöcke zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurückgesetzt wird.<br/>                                              |
| [**OnResetDevice**](id3dxfont--onresetdevice.md)         | Verwenden Sie diese Methode, um Ressourcen erneut zu erhalten und den Anfangszustand zu speichern.<br/>                                                                                                                                                                    |
| [**PreloadCharacters**](id3dxfont--preloadcharacters.md) | Lädt eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderns auf dem Gerät zu verbessern.<br/>                                                                                                                               |
| [**PreloadGlyphs**](id3dxfont--preloadglyphs.md)         | Lädt eine Reihe von Glyphen in den Videospeicher, um die Effizienz des Renderns auf dem Gerät zu verbessern.<br/>                                                                                                                                   |
| [**PreloadText**](id3dxfont--preloadtext.md)             | Lädt formatierten Text in den Videospeicher, um die Effizienz des Renderns auf dem Gerät zu verbessern. Diese Methode unterstützt ANSI- und Unicode-Zeichenfolgen.<br/>                                                                                        |



 

## <a name="remarks"></a>Hinweise

Die **ID3DXFont-Schnittstelle** wird durch Aufrufen von [**D3DXCreateFont**](d3dxcreatefont.md) oder [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md)abgerufen.

Der LPD3DXFONT-Typ wird als Zeiger auf die **ID3DXFont-Schnittstelle** definiert.


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
