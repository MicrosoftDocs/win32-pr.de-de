---
title: MCM_SETCOLOR (Commctrl.h)
description: Legt die Farbe für einen bestimmten Teil eines Monatskalender-Steuerelements fest. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ SetColor-Makros senden.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- MCM_SETCOLOR von Windows Steuerelementen
topic_type:
- apiref
api_name:
- MCM_SETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0915f78ad2dc666d6476cebb51be4f8b8c6102cb1433da59af7b9a1342deedc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697150"
---
# <a name="mcm_setcolor-message"></a>MCM \_ SETCOLOR-Meldung

Legt die Farbe für einen bestimmten Teil eines Monatskalender-Steuerelements fest. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ SetColor-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wert vom Typ **int,** der an gibt, welche Monatskalenderfarbe festgelegt werden soll. Die folgenden Werte sind möglich:



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**\_MCSC-HINTERGRUND**</dt> </dl>       | Legen Sie die Hintergrundfarbe fest, die zwischen Monaten angezeigt wird.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Legen Sie die Hintergrundfarbe fest, die innerhalb des Monats angezeigt wird.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**\_MCSC-TEXT**</dt> </dl>                         | Legen Sie die Farbe fest, die zum Anzeigen von Text innerhalb eines Monats verwendet wird.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Legen Sie die Hintergrundfarbe fest, die im Titel des Kalenders angezeigt wird.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TITLETEXT**</dt> </dl>          | Legen Sie die Farbe fest, die zum Anzeigen von Text im Titel des Kalenders verwendet wird.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Legen Sie die Farbe fest, die zum Anzeigen von Kopfzeilentag- und Nachtagtext verwendet wird. Header und nachfolgende Tage sind die Tage aus den vorherigen und folgenden Monaten, die im Kalender des aktuellen Monats angezeigt werden.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF-Wert,**](/windows/desktop/gdi/colorref) der die Farbe darstellt, die für den angegebenen Bereich des Monatskalenders festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [**COLORREF-Wert**](/windows/desktop/gdi/colorref) zurück, der bei Erfolg die vorherige Farbeinstellung für den angegebenen Teil des Monatskalender-Steuerelements darstellt. Andernfalls ist die Rückgabe -1.

## <a name="remarks"></a>Hinweise

Wenn visuelle Stile aktiv sind, hat diese Meldung keine Auswirkungen, es sei *denn, wParam* ist MCSC \_ BACKGROUND.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

