---
title: MCM_GETMINREQRECT Meldung (kommstrg. h)
description: Ruft die Mindestgröße ab, die erforderlich ist, um einen vollen Monat in einem Monatskalender-Steuerelement anzuzeigen. Sie können diese Nachricht explizit oder mit dem monthcal \_ getminreqrect-Makro senden.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- Windows-Steuerelemente für MCM_GETMINREQRECT Meldung
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
ms.openlocfilehash: ac6b2e2b16a70841836a277ffe55e030a6d6a241
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476071"
---
# <a name="mcm_getminreqrect-message"></a>MCM \_ getminreqrect-Meldung

Ruft die Mindestgröße ab, die erforderlich ist, um einen vollen Monat in einem Monatskalender-Steuerelement anzuzeigen. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getminreqrect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die Informationen zu umschließenden Rechtecks empfängt. Dieser Parameter muss eine gültige Adresse sein und darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, und *LPARAM* empfängt bei erfolgreicher Ausführung die entsprechenden umgebenden Informationen. Andernfalls gibt die Meldung 0 (null) zurück.

## <a name="remarks"></a>Bemerkungen

Die mindestens erforderliche Fenstergröße für ein Monatskalender-Steuerelement hängt von der aktuell ausgewählten Schriftart, den Steuerelement Stilen, den Systemmetriken und den regionalen Einstellungen ab. Wenn eine Anwendung etwas ändert, das sich auf die minimale Fenstergröße auswirkt, oder eine [**WM- \_ settingchange**](/windows/desktop/winmsg/wm-settingchange) -Nachricht verarbeitet, sollte Sie **MCM \_ getminreqrect** senden, um die neue Mindestgröße zu ermitteln.

> [!Note]  
> Das von **MCM \_ getminreqrect** zurückgegebene Rechteck enthält nicht die Breite der "Today"-Zeichenfolge, wenn es vorhanden ist. Wenn der [**MCS- \_ notoday**](month-calendar-control-styles.md) -Stil nicht festgelegt ist, sollte Ihre Anwendung auch das Rechteck abrufen, das die Zeichen folgen Breite "Today" definiert, indem eine [**MCM \_ getmaxchanwidth**](mcm-getmaxtodaywidth.md) -Nachricht gesendet wird. Verwenden Sie die größere der beiden Rechtecke, um sicherzustellen, dass die "Today"-Zeichenfolge nicht abgeschnitten wird.

 

Die **oberen** und **linken** Member der Struktur, auf die von *LPARAM* verwiesen wird, sind immer 0 (null). Die **Rechte** und **untersten** Elemente stellen den minimalen *CX* -und *CY* -Member dar, der für das Steuerelement erforderlich ist

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

