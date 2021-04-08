---
title: WM_MENUCHAR Meldung (Winuser. h)
description: Wird gesendet, wenn ein Menü aktiv ist und der Benutzer eine Taste drückt, die keiner mnetmonischen oder Zugriffstaste entspricht. Diese Meldung wird an das Fenster gesendet, das das Menü besitzt.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a278e4a1b4333631741a6a542318a8a55e40b512
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743832"
---
# <a name="wm_menuchar-message"></a>WM- \_ menuchar-Meldung

Wird gesendet, wenn ein Menü aktiv ist und der Benutzer eine Taste drückt, die keiner mnetmonischen oder Zugriffstaste entspricht. Diese Meldung wird an das Fenster gesendet, das das Menü besitzt.


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das nieder wertige Wort gibt den Zeichencode an, der dem vom Benutzer gedrückten Schlüssel entspricht.

Das höchst wertige Wort gibt den aktiven Menütyp an. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                 | Bedeutung                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ Popup**</dt> <dt>0x00000010l</dt> </dl>       | Ein Dropdown Menü, ein Untermenü oder ein Kontextmenü.<br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ Sysmenu**</dt> <dt>0x00002000l</dt> </dl> | Das Fenstermenü.<br/>                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das aktive Menü.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung, die diese Nachricht verarbeitet, sollte einen der folgenden Werte im höherwertigen Wort des Rückgabewerts zurückgeben.



| Rückgabecode/-wert                                                                                                                                  | BESCHREIBUNG                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNC \_ Schließen**</dt> Sie <dt>1</dt> . </dl>   | Informiert das System, dass es das aktive Menü schließen soll.<br/>                                                                                                                      |
| <dl> <dt>**MNC \_**</dt> <dt>2</dt> ausführen </dl> | Informiert das System, dass es das im nieder wertigen Wort des Rückgabewerts angegebene Element auswählen soll. Das Besitzer Fenster empfängt eine [**WM- \_ Befehls**](wm-command.md) Meldung.<br/> |
| <dl> <dt>**MNC \_**</dt> <dt>0</dt> ignorieren </dl>  | Informiert das System darüber, dass das vom Benutzer gedrückte Zeichen verworfen und auf dem System Sprecher ein kurzes Signal erstellt werden sollte.<br/>                                                       |
| <dl> <dt>**MNC \_**</dt> <dt>3</dt> auswählen </dl>  | Informiert das System, dass es das im nieder wertigen Wort des Rückgabewerts angegebene Element auswählen soll. <br/>                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Das nieder wertige Wort wird ignoriert, wenn das höchst wertige Wort 0 oder 1 enthält.

Eine Anwendung sollte diese Nachricht verarbeiten, wenn eine Zugriffstaste verwendet wird, um ein Menü Element auszuwählen, das eine Bitmap anzeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Licher**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

