---
description: Die ID3DX10Font-Schnittstelle kapselt die Texturen und Ressourcen, die zum Rendern einer bestimmten Schriftart auf einem bestimmten Gerät benötigt werden.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: ID3DX10Font-Schnittstelle (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b40230aa983154f9bfc85b3ffb0f08f713b00213259d18bb9b160374b670795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540346"
---
# <a name="id3dx10font-interface"></a>ID3DX10Font-Schnittstelle

Die ID3DX10Font-Schnittstelle kapselt die Texturen und Ressourcen, die zum Rendern einer bestimmten Schriftart auf einem bestimmten Gerät benötigt werden.

## <a name="members"></a>Member

Die **ID3DX10Font-Schnittstelle erbt** von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10Font** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10Font-Schnittstelle** verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Drawtext**](id3dx10font-drawtext.md)                   | Zeichnen von formatiertem Text. Diese Methode unterstützt ANSI- und Unicode-Zeichenfolgen.<br/>                                                                        |
| [**GetDC**](id3dx10font-getdc.md)                         | Gibt ein Handle an einen Anzeigegerätekontext (DC) zurück, auf dem die Schriftart festgelegt ist.<br/>                                                            |
| [**GetDesc**](id3dx10font-getdesc.md)                     | Abrufen einer Beschreibung des aktuellen Schriftartobjekts.<br/>                                                                                              |
| [**GetDevice**](id3dx10font-getdevice.md)                 | Rufen Sie das Direct3D-Gerät ab, das dem Schriftartobjekt zugeordnet ist.<br/>                                                                              |
| [**GetGlyphData**](id3dx10font-getglyphdata.md)           | Gibt Informationen zur Platzierung und Ausrichtung eines Glyphens in einer Zeichenzelle zurück.<br/>                                                     |
| [**GetTextMetrics**](id3dx10font-gettextmetrics.md)       | Abrufen von Schriftartmerkmalen.<br/>                                                                                                             |
| [**PreloadCharacters**](id3dx10font-preloadcharacters.md) | Laden Sie eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderns auf dem Gerät zu verbessern.<br/>                                        |
| [**PreloadGlyphs**](id3dx10font-preloadglyphs.md)         | Laden Sie eine Reihe von Glyphen in den Videospeicher, um die Effizienz des Renderns auf dem Gerät zu verbessern.<br/>                                            |
| [**PreloadText**](id3dx10font-preloadtext.md)             | Laden Sie formatierten Text in den Videospeicher, um die Effizienz des Renderns auf dem Gerät zu verbessern. Diese Methode unterstützt ANSI- und Unicode-Zeichenfolgen.<br/> |



 

## <a name="remarks"></a>Hinweise

Die ID3DX10Font-Schnittstelle wird durch Aufrufen von [**D3DX10CreateFont**](d3dx10createfont.md) oder [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md)abgerufen.

Der LPD3DX10FONT-Typ wird als Zeiger auf die ID3DX10Font-Schnittstelle definiert.


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
