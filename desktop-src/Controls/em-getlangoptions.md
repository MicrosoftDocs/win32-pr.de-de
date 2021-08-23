---
title: EM_GETLANGOPTIONS Nachricht (Richedit.h)
description: Ruft die Optionseinstellungen eines Rich Edit-Steuerelements für die Unterstützung des Eingabemethoden-Editors (IME) und der asiatischen Sprache ab.
ms.assetid: 9fd9d27c-7713-454e-b49f-8ecdba848d2e
keywords:
- EM_GETLANGOPTIONS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e3fa3602259ff0b754c79c69d91048c68c60b2703d4cd06a7da4630fcdf646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800200"
---
# <a name="em_getlangoptions-message"></a>EM \_ GETLANGOPTIONS-Nachricht

Ruft die Optionseinstellungen eines Rich Edit-Steuerelements für die Unterstützung des Eingabemethoden-Editors (IME) und der asiatischen Sprache ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die IME- und Asiatisch-Spracheinstellungen zurück, die null oder mehr der folgenden Werte sein können.



| Rückgabecode                                                                                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ÜBER DIE \_ AUTOFONT-FUNKTION**</dt> </dl>                    | Wenn dieses Flag festgelegt ist, ändert das Steuerelement automatisch Schriftarten, wenn der Benutzer explizit zu einem anderen Tastaturlayout wechselt. Es ist hilfreich, **DEN \_ AUTOFONT-Code** für universelle Unicode-Schriftarten zu deaktivieren. Diese Option ist standardmäßig aktiviert (1).<br/>                                                                                                                                                                     |
| <dl> <dt>**VERÄRKUNG \_ AUTOFONTSIZEADJUST**</dt> </dl>          | Wenn dieses Flag festgelegt ist, skaliert das Steuerelement schriftgebundene Schriftgrade von der Einfügemarke entsprechend dem Skript. Beispielsweise sind asiatische Schriftarten etwas größer als westländische Schriftarten. Diese Option ist standardmäßig aktiviert (1).<br/>                                                                                                                                                                                              |
| <dl> <dt>**ÜBER DIE \_ AUTOKEYBOARD-LEISTE**</dt> </dl>                | Wenn dieses Flag festgelegt ist, ändert das Steuerelement automatisch das Tastaturlayout, wenn der Benutzer explizit in eine andere Schriftart wechselt oder wenn der Benutzer die Einfügemarke explizit an eine neue Position im Text ändert. Wird für bidirektionale Steuerelemente automatisch aktiviert. Für alle anderen Steuerelemente ist sie standardmäßig deaktiviert. Diese Option ist standardmäßig deaktiviert (0).<br/>                                 |
| <dl> <dt>**DISABLE \_ DISABLEAUTOBIDIAUTOKEYBOARD**</dt> </dl> | **Windows 8:** Wenn dieses Flag festgelegt ist, verwendet das Steuerelement sprachneutrale Logik für den automatischen Tastaturwechsel. Diese Option ist standardmäßig deaktiviert (0).<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**ÜBER \_ DIE DUALFONT-FUNKTION**</dt> </dl>                    | Wenn dieses Flag festgelegt ist, verwendet das Steuerelement den Dual-Font-Modus. Wird für die Unterstützung der asiatischen Sprache verwendet. Das -Steuerelement verwendet eine englische Schriftart für ASCII-Text und eine asiatische Schriftart für asiatisch-Text. Diese Option ist standardmäßig aktiviert (1).<br/>                                                                                                                                                                                                   |
| <dl> <dt>**IMF \_ IMEALWAYSSENDNOTIFY**</dt> </dl>         | Dieses Flag steuert, wie das Rich Edit-Steuerelement den Client während der IME-Komposition benachrichtigt: <br/> 0: Keine [EN \_ CHANGE-](en-change.md) oder [EN \_ SELCHANGE-Benachrichtigungen](en-selchange.md) während des unbestimmten Zustands. Senden Sie eine Benachrichtigung, wenn die endgültige Zeichenfolge eingeht. Dies ist die Standardoption.<br/> 1: Senden von [EN \_ CHANGE-](en-change.md) und [EN \_ SELCHANGE-Ereignissen](en-selchange.md) während des unbestimmten Zustands.<br/> |
| <dl> <dt>**IMF \_ IMECANCELCOMPLETE**</dt> </dl>           | Dieses Flag bestimmt, wie das Steuerelement die Kompositionszeichenfolge einer IME verwendet, wenn der Benutzer sie abbricht. Wenn das Flag festgelegt ist, wird die Kompositionszeichenfolge vom Steuerelement verworfen. Wenn das Flag nicht festgelegt ist, verwendet das Steuerelement die Kompositionszeichenfolge als Ergebniszeichenfolge. Diese Option ist standardmäßig deaktiviert (0).<br/>                                                                                                              |
| <dl> <dt>**DIE \_ NOIMPLICITLANG-SPRACHE**</dt> </dl>              | **Windows 8**: Wenn dieses Flag festgelegt ist, deaktivieren Sie das Stempeln von Tastatureingaben mit der Tastatursprache, und stellen Sie sicher, dass nicht ostasiatische Sprach-IDs mit dem Zeichengeschrift kompatibel sind. Diese Option ist standardmäßig deaktiviert (0). <br/>                                                                                                                                                                             |
| <dl> <dt>**\_KBDLIDFIXUP**</dt> </dl>               | **Windows 8**: Wenn dieses Flag festgelegt ist, deaktiviert das Rich Edit-Steuerelement das Stamping der Tastatursprache für ein leeres Steuerelement. Diese Option ist standardmäßig deaktiviert (0).<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**\_SPELLCHECKING (RECHTSCHREIBPRÜFUNG)**</dt> </dl>               | **Windows 8:** Wenn dieses Flag festgelegt ist, aktiviert das Rich Edit-Steuerelement die Rechtschreibprüfung. Diese Option ist standardmäßig deaktiviert (0). <br/>                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**\_VERZWEIGUNG TKBAUTOCORRECTION**</dt> </dl>           | **Windows 8:** Wenn dieses Flag festgelegt ist, aktivieren Sie die automatische Bildschirmkorrektur der Touchtastatur. Diese Option ist standardmäßig deaktiviert (0). <br/>                                                                                                                                                                                                                                                                                                  |
| <dl> <dt>**SPRECHUNG \_ TKBPREDICTION**</dt> </dl>               | **Windows 10**: Ignoriert.<br/> **Windows 8**: Wenn dieses Flag festgelegt ist, ermöglicht das Rich Edit-Steuerelement die Vorhersage der Tastatureingabe. Diese Option ist standardmäßig deaktiviert (0). <br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**UIFONTS FÜR DIE \_ UIFONTS**</dt> </dl>                     | Verwenden Sie Standardschriftarten der Benutzeroberfläche. Diese Option ist standardmäßig deaktiviert (0).<br/>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Hinweise

Das **FLAG FÜR \_ AUTOFONT** IST standardmäßig festgelegt. Die FLAGS **\_ IMECANCELCOMPLETE und IMECANCELCOMPLETE** sind standardmäßig gelöscht. **\_**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ SETLANGOPTIONS**](em-setlangoptions.md)
</dt> <dt>

[**EM \_ SETLIMITTEXT**](em-setlimittext.md)
</dt> </dl>

 

 





