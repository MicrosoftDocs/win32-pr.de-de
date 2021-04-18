---
title: QuickInfo-Stile (kommctrl. h)
description: In diesem Abschnitt werden die mit QuickInfo-Steuerelementen verwendeten Steuerelement Stile aufgelistet
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8b89aed88caddceae815414b9f2b4d93a550c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364899"
---
# <a name="tooltip-styles"></a>QuickInfo-Stile

In diesem Abschnitt werden die mit QuickInfo-Steuerelementen verwendeten Steuerelement Stile aufgelistet



| Konstante                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <dt>**TTS \_ alwaystip**</dt> </dl>                | Gibt an, dass das QuickInfo-Steuerelement angezeigt wird, wenn sich der Cursor auf einem Tool befindet, auch wenn das Besitzer Fenster des QuickInfo-Steuer Elements nicht Ohne diesen Stil wird die QuickInfo nur angezeigt, wenn das Besitzer Fenster des Tools aktiv ist.<br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <dt>**TTS-Sprechblase \_**</dt> </dl>                      | [Version 5,80](common-control-versions.md). Gibt an, dass das QuickInfo-Steuerelement die Darstellung einer Zeichenfolge "Sprechblase" mit abgerundeten Ecken und einem Stamm Element anzeigt, das auf das Element zeigt. <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <dt>**TTE \_ Schließen**</dt> </dl>                            | Zeigt die Schaltfläche **Schließen** in der QuickInfo an. Nur gültig, wenn die QuickInfo den Stil der TTS-Sprechblase \_ und einen Titel hat. siehe [**TTM \_ SetTitle**](ttm-settitle.md).<br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <dt>**TTS \_ noanimieren**</dt> </dl>                | [Version 5,80](common-control-versions.md). Deaktiviert die Animation mit verschiebbaren QuickInfo auf Windows 98-und Windows 2000-Systemen. Dieser Stil wird in früheren Systemen ignoriert.<br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <dt>**TTS- \_ nofade**</dt> </dl>                         | [Version 5,80](common-control-versions.md). Deaktiviert die Animation der Ausblend-QuickInfo. <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <dt>**TTS \_ NoPrefix**</dt> </dl>                   | Verhindert, dass das System kaufmännische und Zeichen aus einer Zeichenfolge entfernt oder eine Zeichenfolge mit einem Tabstopp Zeichen beendet. Ohne diesen Stil entfernt das System automatisch kaufmännische und Zeichen und beendet eine Zeichenfolge beim ersten Tabstopp Zeichen. Dies ermöglicht es einer Anwendung, dieselbe Zeichenfolge wie ein Menü Element und als Text in einem QuickInfo-Steuerelement zu verwenden.<br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <dt>**TTS \_ usevisualstyle**</dt> </dl> | Verwendet Hyperlinks mit einem Thema. Mit dem Design werden die Stile für alle Links in der QuickInfo definiert. Dieser Stil erfordert immer \_ die Festlegung von ttf-Parametern. <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a>Bemerkungen

Ein QuickInfo-Steuerelement verfügt immer über die \_ Fenster Stile "WS Popup" und "WS \_ Ex \_ Tool Window", unabhängig davon, ob Sie diese beim Erstellen des Steuer Elements angeben

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





