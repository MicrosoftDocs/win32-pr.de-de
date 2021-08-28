---
title: MCM_GETMINREQRECT Nachricht (Commctrl.h)
description: Ruft die mindest erforderliche Größe ab, um einen vollständigen Monat in einem Monatskalender-Steuerelement anzuzeigen. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ GetMinReqRect-Makros senden.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- MCM_GETMINREQRECT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- MCM_GETMINREQRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 575636837b1485de62dd5e603a0dea38455c4c99926c13f3bd05101fe2a27eca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062050"
---
# <a name="mcm_getminreqrect-message"></a>MCM \_ GETMINREQRECT-Nachricht

Ruft die mindest erforderliche Größe ab, um einen vollständigen Monat in einem Monatskalender-Steuerelement anzuzeigen. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ GetMinReqRect-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die umgebende Rechteckinformationen empfängt. Dieser Parameter muss eine gültige Adresse sein und darf nicht **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, und *lParam* empfängt bei Erfolg die entsprechenden Begrenzungsinformationen. Andernfalls gibt die Nachricht 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Die mindestens erforderliche Fenstergröße für ein Monatskalender-Steuerelement hängt von der aktuell ausgewählten Schriftart, den steuerelementstilen, Systemmetriken und regionalen Einstellungen ab. Wenn eine Anwendung änderungen, die sich auf die minimale Fenstergröße auswirken, oder eine [**WM \_ SETTINGCHANGE-Nachricht**](/windows/desktop/winmsg/wm-settingchange) verarbeitet, sollte **MCM \_ GETMINREQRECT** gesendet werden, um die neue Mindestgröße zu bestimmen.

> [!Note]  
> Das von **MCM \_ GETMINREQRECT** zurückgegebene Rechteck enthält nicht die Breite der Zeichenfolge "Today", sofern vorhanden. Wenn der [**\_ MCS-FORMATVORLAGENSTIL**](month-calendar-control-styles.md) nicht festgelegt ist, sollte Ihre Anwendung auch das Rechteck abrufen, das die Zeichenfolgenbreite "Today" definiert, indem eine [**MCM \_ GETMAXTODAYWIDTH-Nachricht**](mcm-getmaxtodaywidth.md) gesendet wird. Verwenden Sie das größere der beiden Rechtecke, um sicherzustellen, dass die Zeichenfolge "Today" nicht abgeschnitten wird.

 

Die **oberen** und **linken** Elemente der Struktur, auf die *von lParam* gezeigt wird, sind immer 0 (null). Die **rechten** und **unteren** Member stellen die minimalen *cx-* und *cy-Elemente* dar, die für das Steuerelement erforderlich sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

