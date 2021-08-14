---
title: EM_SETLANGOPTIONS-Nachricht (Richedit.h)
description: Legt Optionen für die Unterstützung des Eingabemethoden-Editors (Input Method Editor, IME) und der Unterstützung für asienisch in einem umfangreichen Bearbeitungssteuerelement fest.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- EM_SETLANGOPTIONS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5984c20273d2daa0a2e39fc6caf6dde88c8b274502a50e1a5e5eb3cca2b6f94c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831201"
---
# <a name="em_setlangoptions-message"></a>EM \_ SETLANGOPTIONS-Meldung

Legt Optionen für die Unterstützung des Eingabemethoden-Editors (Input Method Editor, IME) und der Unterstützung für asienisch in einem umfangreichen Bearbeitungssteuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt die Sprachoptionen an. Eine Liste der möglichen Werte finden Sie unter [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt den Wert 1 zurück.

## <a name="remarks"></a>Hinweise

Die **EM \_ SETLANGOPTIONS-Meldung** steuert Folgendes:

-   Automatische Schriftartbindung.
-   Automatischer Tastaturwechsel.
-   Automatische Anpassung des Schriftgrads.
-   Verwendung von Standardschriftarten der Benutzeroberfläche anstelle von Dokumentstandardschriftarten.
-   Benachrichtigungen an den Client während der IME-Komposition.
-   Wie ime den Kompositionsmodus abbricht.
-   Rechtschreibprüfung, automatische Korrektur und Vorhersage der Touchtastatur.

Diese Meldung legt die Werte aller Sprachoptionsflags fest. Um eine Teilmenge der Flags zu ändern, senden Sie die [**EM \_ GETLANGOPTIONS-Nachricht,**](em-getlangoptions.md) um die aktuellen Optionsflags abzurufen, ändern Sie die zu ändernden Flags, und senden Sie dann die **EM \_ SETLANGOPTIONS-Nachricht** mit dem Ergebnis.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ GETLANGOPTIONS**](em-getlangoptions.md)
</dt> </dl>

 

 





