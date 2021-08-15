---
title: WM_MENUCHAR Meldung (Winuser.h)
description: Wird gesendet, wenn ein Menü aktiv ist und der Benutzer eine Taste drückt, die keiner mnemonic- oder accelerator-Taste entspricht. Diese Meldung wird an das Fenster gesendet, das das Menü besitzt.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR Meldung Menüs und andere Ressourcen
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
ms.openlocfilehash: 5d276418636857fb7ce76159111b8e8b24519235823225fccb68fa1523b4137d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869609"
---
# <a name="wm_menuchar-message"></a>WM \_ MENUCHAR-Meldung

Wird gesendet, wenn ein Menü aktiv ist und der Benutzer eine Taste drückt, die keiner mnemonic- oder accelerator-Taste entspricht. Diese Meldung wird an das Fenster gesendet, das das Menü besitzt.


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt den Zeichencode an, der der taste entspricht, die der Benutzer gedrückt hat.

Das Wort in hoher Reihenfolge gibt den aktiven Menütyp an. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                 | Bedeutung                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ POPUP**</dt> <dt>0x00000010L</dt> </dl>       | Ein Dropdownmenü, ein Untermenü oder ein Kontextmenü.<br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt> </dl> | Das Fenstermenü.<br/>                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das aktive Menü.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung, die diese Nachricht verarbeitet, sollte einen der folgenden Werte im Hochordnungswort des Rückgabewerts zurückgeben.



| Rückgabecode/-wert                                                                                                                                  | BESCHREIBUNG                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNC \_ CLOSE**</dt> <dt>1</dt> </dl>   | Informiert das System darüber, dass das aktive Menü geschlossen werden soll.<br/>                                                                                                                      |
| <dl> <dt>**MNC \_ EXECUTE**</dt> <dt>2</dt> </dl> | Informiert das System darüber, dass das im Wort mit niedriger Reihenfolge des Rückgabewerts angegebene Element ausgewählt werden soll. Das Besitzerfenster empfängt eine [**WM \_ COMMAND-Meldung.**](wm-command.md)<br/> |
| <dl> <dt>**MNC \_ IGNORE**</dt> <dt>0</dt> </dl>  | Informiert das System, dass es das Zeichen verwerfen soll, das der Benutzer gedrückt hat, und erstellt einen kurzen Signalton auf dem Systemlautser.<br/>                                                       |
| <dl> <dt>**MNC \_ SELECT**</dt> <dt>3</dt> </dl>  | Informiert das System darüber, dass das im Wort mit niedriger Reihenfolge des Rückgabewerts angegebene Element ausgewählt werden soll. <br/>                                                                       |



 

## <a name="remarks"></a>Hinweise

Das Wort mit niedriger Reihenfolge wird ignoriert, wenn das Wort in hoher Reihenfolge 0 oder 1 enthält.

Eine Anwendung sollte diese Meldung verarbeiten, wenn eine Zugriffstaste verwendet wird, um ein Menüelement auszuwählen, das eine Bitmap anzeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

