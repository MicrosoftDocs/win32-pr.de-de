---
title: DTM_SETMCCOLOR Meldung (kommstrg. h)
description: Legt die Farbe für einen bestimmten Teil des Monats Kalenders innerhalb eines DTP-Steuer Elements fest. Sie können diese Nachricht explizit senden oder das DateTime- \_ setmonthcalcolor-Makro verwenden.
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- Windows-Steuerelemente für DTM_SETMCCOLOR Meldung
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
ms.openlocfilehash: 2e496abb4dd28b040dd4a8035073ffa32a3f3847
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742561"
---
# <a name="dtm_setmccolor-message"></a>DTM- \_ Nachricht "Abmeldung"

Legt die Farbe für einen bestimmten Teil des Monats Kalenders innerhalb eines DTP-Steuer Elements fest. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ setmonthcalcolor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Wert vom Typ **int** , der angibt, welche Monatskalender Farbe festgelegt werden soll. Die folgenden Werte sind möglich:



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**MCSC- \_ Hintergrund**</dt> </dl>       | Legen Sie die zwischen den Monaten angezeigte Hintergrundfarbe fest.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ monthbk**</dt> </dl>                | Legen Sie die im Monat angezeigte Hintergrundfarbe fest.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**MCSC- \_ Text**</dt> </dl>                         | Legen Sie die Farbe fest, mit der Text innerhalb eines Monats angezeigt wird.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ titlebk**</dt> </dl>                | Legen Sie die im Titel des Kalenders angezeigte Hintergrundfarbe fest.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TitleText**</dt> </dl>          | Legen Sie die Farbe fest, die verwendet wird, um Text innerhalb des Kalender Titels anzuzeigen.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC- \_ trailingtext**</dt> </dl> | Legen Sie die Farbe fest, die verwendet wird, um den Header Tag und den nachfolgenden Tag Header und nachfolgende Tage sind die Tage aus den vorherigen und den nächsten Monaten, die im Kalender des aktuellen Monats angezeigt werden.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein **COLORREF** -Wert, der die Farbe darstellt, die für den angegebenen Bereich des Monats Kalenders festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **COLORREF** -Wert zurück, der die vorherige Farbeinstellung für den angegebenen Teil des Monatskalender-Steuer Elements darstellt, wenn erfolgreich. Andernfalls gibt die Meldung-1 zurück.

## <a name="remarks"></a>Bemerkungen

Wenn visuelle Stile aktiviert sind, hat diese Meldung keine Auswirkung, es sei denn, *wParam* ist ein MCSC- \_ Hintergrund.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





