---
title: EM_SETLANGOPTIONS Meldung (RichEdit. h)
description: Legt Optionen für den Eingabemethoden-Editor (IME) und die Unterstützung für asiatische Sprachen in einem Rich Edit-Steuerelement fest.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- Windows-Steuerelemente für EM_SETLANGOPTIONS Meldung
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
ms.openlocfilehash: 2e5095c599dfa78740ce4cb081e4d52c33b2debd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949776"
---
# <a name="em_setlangoptions-message"></a>EM \_ setlangoptions-Meldung

Legt Optionen für den Eingabemethoden-Editor (IME) und die Unterstützung für asiatische Sprachen in einem Rich Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt die Sprachoptionen an. Eine Liste möglicher Werte finden Sie unter [**EM \_ getlangoptions**](em-getlangoptions.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt den Wert 1 zurück.

## <a name="remarks"></a>Bemerkungen

Die **\_ gesetlangoptions** -Nachricht steuert Folgendes:

-   Automatische Schriftart Bindung.
-   Automatischer Tastatur Wechsel.
-   Automatische Anpassung der Schriftart Größe.
-   Verwendung von Standard Schriftarten von Benutzeroberflächen anstelle von Dokument Standard Schriftarten.
-   Benachrichtigungen an den Client während der IME-Komposition.
-   Gibt an, wie IME den Kompositions Modus abbricht.
-   Rechtschreibprüfungs-, AutoCorrect-und Berührungs Tastatur Vorhersage.

Diese Meldung legt die Werte aller sprachflags fest. Um eine Teilmenge der Flags zu ändern, senden Sie die [**EM \_ getlangoptions**](em-getlangoptions.md) -Nachricht, um die aktuellen Options-Flags zu erhalten, ändern Sie die Flags, die Sie ändern müssen, und senden Sie dann die **EM \_ setlangoptions** -Nachricht mit dem Ergebnis.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ getlangoptions**](em-getlangoptions.md)
</dt> </dl>

 

 





