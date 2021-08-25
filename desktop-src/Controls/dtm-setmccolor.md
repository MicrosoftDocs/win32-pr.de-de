---
title: DTM_SETMCCOLOR (Commctrl.h)
description: Legt die Farbe für einen bestimmten Teil des Monatskalenders innerhalb eines DTP-Steuerelements (Date and Time Picker) fest. Sie können diese Nachricht explizit senden oder das \_ DateTime-Makro SetMonthCalColor verwenden.
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- DTM_SETMCCOLOR von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- DTM_SETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5154c2e450f5ef3c12c85fe3307f37958fea807226ab436241038c9ad639d4dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877820"
---
# <a name="dtm_setmccolor-message"></a>SMS \_ SETMCCOLOR-Meldung

Legt die Farbe für einen bestimmten Teil des Monatskalenders innerhalb eines DTP-Steuerelements (Date and Time Picker) fest. Sie können diese Nachricht explizit senden oder das [**\_ DateTime-Makro SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Wert vom Typ **int,** der an gibt, welche Monatskalenderfarbe festgelegt werden soll. Die folgenden Werte sind möglich:



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**\_MCSC-HINTERGRUND**</dt> </dl>       | Legen Sie die Hintergrundfarbe fest, die zwischen Monaten angezeigt wird.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Legen Sie die Hintergrundfarbe fest, die innerhalb des Monats angezeigt wird.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**\_MCSC-TEXT**</dt> </dl>                         | Legen Sie die Farbe fest, die zum Anzeigen von Text innerhalb eines Monats verwendet wird.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Legen Sie die Hintergrundfarbe fest, die im Titel des Kalenders angezeigt wird.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TITLETEXT**</dt> </dl>          | Legen Sie die Farbe fest, die zum Anzeigen von Text im Titel des Kalenders verwendet wird.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Legen Sie die Farbe fest, die verwendet wird, um Kopfzeilentag- und Nachtagstext anzuzeigen. Header und nachfolgende Tage sind die Tage aus den vorherigen und folgenden Monaten, die im Kalender des aktuellen Monats angezeigt werden.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein **COLORREF-Wert,** der die Farbe darstellt, die für den angegebenen Bereich des Monatskalenders festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **COLORREF-Wert** zurück, der bei Erfolg die vorherige Farbeinstellung für den angegebenen Teil des Monatskalender-Steuerelements darstellt. Andernfalls gibt die Meldung -1 zurück.

## <a name="remarks"></a>Hinweise

Wenn visuelle Stile aktiviert sind, hat diese Meldung keine Auswirkungen, es sei *denn, wParam* ist MCSC \_ BACKGROUND.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





