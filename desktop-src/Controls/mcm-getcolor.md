---
title: MCM_GETCOLOR (Commctrl.h)
description: Ruft die Farbe für einen bestimmten Teil eines Monatskalender-Steuerelements ab. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ GetColor-Makros senden.
ms.assetid: 6c30ad0d-7584-402a-9c27-3c12c49c87f3
keywords:
- MCM_GETCOLOR meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- MCM_GETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254b140e801f4d4440c9b292999e5c8f91175a30750b08bfd30abd6afd84f73d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062090"
---
# <a name="mcm_getcolor-message"></a>MCM \_ GETCOLOR-Nachricht

Ruft die Farbe für einen bestimmten Teil eines Monatskalender-Steuerelements ab. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ GetColor-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wert vom Typ **int,** der an gibt, welche Monatskalenderfarbe abgerufen werden soll. Die folgenden Werte sind möglich:



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**\_MCSC-HINTERGRUND**</dt> </dl>       | Ruft die Zwischenmonate angezeigte Hintergrundfarbe ab.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Ruft die im Monat angezeigte Hintergrundfarbe ab.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**\_MCSC-TEXT**</dt> </dl>                         | Ruft die Farbe ab, die zum Anzeigen von Text innerhalb eines Monats verwendet wird.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Ruft die im Titel des Kalenders angezeigte Hintergrundfarbe ab.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TITLETEXT**</dt> </dl>          | Ruft die Farbe ab, die zum Anzeigen von Text im Titel des Kalenders verwendet wird.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Ruft die Farbe ab, die verwendet wird, um Kopfzeilentag und Nachtagstext anzuzeigen. Header und nachfolgende Tage sind die Tage aus den vorherigen und folgenden Monaten, die im Kalender des aktuellen Monats angezeigt werden.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **COLORREF-Wert** zurück, der bei Erfolg die Farbeinstellung für den angegebenen Teil des Monatskalender-Steuerelements darstellt. Andernfalls gibt diese Meldung -1 zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





