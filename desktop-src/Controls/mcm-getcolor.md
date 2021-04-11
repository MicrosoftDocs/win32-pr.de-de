---
title: MCM_GETCOLOR Meldung (kommstrg. h)
description: Ruft die Farbe für einen angegebenen Teil eines Monatskalender-Steuer Elements ab. Sie können diese Nachricht explizit oder mit dem monthcal \_ GetColor-Makro senden.
ms.assetid: 6c30ad0d-7584-402a-9c27-3c12c49c87f3
keywords:
- Windows-Steuerelemente für MCM_GETCOLOR Meldung
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
ms.openlocfilehash: 932b457bd1ddd870fd84facdb540e31188825504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105458"
---
# <a name="mcm_getcolor-message"></a>MCM- \_ GetColor-Meldung

Ruft die Farbe für einen angegebenen Teil eines Monatskalender-Steuer Elements ab. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) -Makro senden.

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

Gibt einen **COLORREF** -Wert zurück, der die Farbeinstellung für den angegebenen Teil des Monatskalender-Steuer Elements darstellt, wenn erfolgreich. Andernfalls gibt diese Meldung-1 zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





