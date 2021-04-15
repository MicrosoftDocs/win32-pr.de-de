---
title: DTM_GETMCCOLOR Meldung (kommstrg. h)
description: Ruft die Farbe für einen angegebenen Teil des Monats Kalenders innerhalb eines DTP-Steuer Elements ab. Sie können diese Nachricht explizit senden oder das "DateTime \_ getmonthcalcolor"-Makro verwenden.
ms.assetid: 892e8c23-f0d0-4fd6-98ed-39592c4d316f
keywords:
- Windows-Steuerelemente für DTM_GETMCCOLOR Meldung
topic_type:
- apiref
api_name:
- DTM_GETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690c461c5bccbd050fb3d698d1a41c6d1e513944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479463"
---
# <a name="dtm_getmccolor-message"></a>DTM \_ getmccolor-Nachricht

Ruft die Farbe für einen angegebenen Teil des Monats Kalenders innerhalb eines DTP-Steuer Elements ab. Sie können diese Nachricht explizit senden oder das " [**DateTime \_ getmonthcalcolor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) "-Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Wert vom Typ **int** , der angibt, welche Monatskalender Farbe abgerufen werden soll. Die folgenden Werte sind möglich:



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**MCSC- \_ Hintergrund**</dt> </dl>       | Rufen Sie die zwischen Monaten angezeigte Hintergrundfarbe ab.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ monthbk**</dt> </dl>                | Rufen Sie die im Monat angezeigte Hintergrundfarbe ab.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**MCSC- \_ Text**</dt> </dl>                         | Ruft die Farbe ab, die zum Anzeigen von Text innerhalb eines Monats verwendet wird.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ titlebk**</dt> </dl>                | Ruft die im Titel des Kalenders angezeigte Hintergrundfarbe ab.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TitleText**</dt> </dl>          | Ruft die Farbe ab, die zum Anzeigen von Text innerhalb des Kalender Titels verwendet wird.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC- \_ trailingtext**</dt> </dl> | Ruft die Farbe ab, die zum Anzeigen des Header Tags und des nachfolgenden Tages Textes verwendet wird Header und nachfolgende Tage sind die Tage aus den vorherigen und den nächsten Monaten, die im Kalender des aktuellen Monats angezeigt werden.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **COLORREF** -Wert zurück, der die Farbeinstellung für den angegebenen Teil des Monatskalender-Steuer Elements darstellt, wenn erfolgreich. Die Meldung gibt-1 zurück, wenn dies nicht gelingt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





