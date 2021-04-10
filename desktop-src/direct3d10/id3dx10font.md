---
description: Die ID3DX10Font-Schnittstelle kapselt die Texturen und Ressourcen, die erforderlich sind, um eine bestimmte Schriftart auf einem bestimmten Gerät zu Rendering.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: ID3DX10Font-Schnittstelle (d3dx10. h)
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
ms.openlocfilehash: 7d7c9fb1daa0934b5e6b3147f60803be5c0b5c07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219534"
---
# <a name="id3dx10font-interface"></a>ID3DX10Font-Schnittstelle

Die ID3DX10Font-Schnittstelle kapselt die Texturen und Ressourcen, die erforderlich sind, um eine bestimmte Schriftart auf einem bestimmten Gerät zu Rendering.

## <a name="members"></a>Member

Die **ID3DX10Font** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DX10Font** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10Font** -Schnittstelle verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText**](id3dx10font-drawtext.md)                   | Formatierten Text zeichnen. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.<br/>                                                                        |
| [**GetDC**](id3dx10font-getdc.md)                         | Gibt ein Handle für einen Anzeigegeräte Kontext (DC) zurück, für den die Schriftart festgelegt ist.<br/>                                                            |
| [**GetDesc**](id3dx10font-getdesc.md)                     | Eine Beschreibung des aktuellen Schriftart Objekts erhalten.<br/>                                                                                              |
| [**GetDevice**](id3dx10font-getdevice.md)                 | Rufen Sie das Direct3D-Gerät ab, das dem Schriftart Objekt zugeordnet ist.<br/>                                                                              |
| [**Getglyphdata**](id3dx10font-getglyphdata.md)           | Gibt Informationen über die Platzierung und Ausrichtung eines Symbols in einer Zeichen Zelle zurück.<br/>                                                     |
| [**GetTextMetrics**](id3dx10font-gettextmetrics.md)       | Rufen Sie Schriftart Eigenschaften ab.<br/>                                                                                                             |
| [**Preloadcharacter**](id3dx10font-preloadcharacters.md) | Laden Sie eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.<br/>                                        |
| [**Präloadglyphen**](id3dx10font-preloadglyphs.md)         | Laden Sie eine Reihe von Symbolen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.<br/>                                            |
| [**PreloadText**](id3dx10font-preloadtext.md)             | Laden Sie formatierten Text in den Videospeicher, um die Effizienz beim Rendern auf das Gerät zu verbessern. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die ID3DX10Font-Schnittstelle wird durch Aufrufen von [**D3DX10CreateFont**](d3dx10createfont.md) oder [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md)abgerufen.

Der LPD3DX10FONT-Typ wird als Zeiger auf die ID3DX10Font-Schnittstelle definiert.


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
