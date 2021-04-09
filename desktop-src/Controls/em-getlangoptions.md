---
title: EM_GETLANGOPTIONS Meldung (RichEdit. h)
description: Ruft die Options Einstellungen eines Rich-Edit-Steuer Elements für den Eingabemethoden-Editor (IME) und die Unterstützung asiatischer Sprache ab.
ms.assetid: 9fd9d27c-7713-454e-b49f-8ecdba848d2e
keywords:
- Windows-Steuerelemente für EM_GETLANGOPTIONS Meldung
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
ms.openlocfilehash: a27254ccb10093059eb9161410f4e25efdc59306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858690"
---
# <a name="em_getlangoptions-message"></a>EM \_ getlangoptions-Meldung

Ruft die Options Einstellungen eines Rich-Edit-Steuer Elements für den Eingabemethoden-Editor (IME) und die Unterstützung asiatischer Sprache ab.

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

Gibt die Einstellungen der IME-und asiatischen Sprache zurück, die NULL oder mehr der folgenden Werte aufweisen können.



| Rückgabecode                                                                                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Autofont für den IWF \_**</dt> </dl>                    | Wenn dieses Flag festgelegt ist, ändert das Steuerelement automatisch Schriftarten, wenn der Benutzer explizit zu einem anderen Tastaturlayout wechselt. Es ist hilfreich, die **Automatische Offline \_ Schriftart** für universelle Unicode-Schriftarten zu deaktivieren. Diese Option ist standardmäßig aktiviert (1).<br/>                                                                                                                                                                     |
| <dl> <dt>**IMF \_ AutoFontSizeAdjust**</dt> </dl>          | Wenn dieses Flag festgelegt ist, skaliert das Steuerelement Schriftart gebundene Schriftgrößen von der einfügepunktgröße entsprechend dem Skript. Asiatische Schriftarten sind z. b. etwas größer als westliche Schriftarten. Diese Option ist standardmäßig aktiviert (1).<br/>                                                                                                                                                                                              |
| <dl> <dt>**IMF- \_ autokeyboard**</dt> </dl>                | Wenn dieses Flag festgelegt ist, ändert das Steuerelement automatisch das Tastaturlayout, wenn der Benutzer explizit zu einer anderen Schriftart wechselt, oder wenn der Benutzer die Einfügemarke explizit an eine neue Position im Text ändert. Wird automatisch für bidirektionale Steuerelemente aktiviert. Für alle anderen Steuerelemente ist diese standardmäßig deaktiviert. Diese Option ist standardmäßig deaktiviert (0).<br/>                                 |
| <dl> <dt>**IWF \_ disableautobidiautokeyboard**</dt> </dl> | **Windows 8**: Wenn dieses Flag festgelegt ist, verwendet das Steuerelement sprachneutrale Logik für den automatischen Tastatur Wechsel. Diese Option ist standardmäßig deaktiviert (0).<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**IMF- \_ DualFont**</dt> </dl>                    | Wenn dieses Flag festgelegt ist, verwendet das Steuerelement den Dual-Font-Modus. Wird für die Unterstützung asiatischer Sprachen verwendet. Das-Steuerelement verwendet eine englische Schriftart für ASCII-Text und eine asiatische Schriftart für asiatischen Text. Diese Option ist standardmäßig aktiviert (1).<br/>                                                                                                                                                                                                   |
| <dl> <dt>**IMF \_ imealwayssendnotify**</dt> </dl>         | Mit diesem Flag wird gesteuert, wie das Rich Edit-Steuerelement den Client während der IME-Komposition benachrichtigt: <br/> 0: Es werden keine [ \_ Änderungen](en-change.md) an der Änderung vorgenommen [, oder es werden \_ keine Änderungen im](en-selchange.md) unbestimmten Zustand angezeigt. Hiermit wird eine Benachrichtigung gesendet, wenn die endgültige Zeichenfolge empfangen wird. Dies ist die Standardoption.<br/> 1: Senden von [en \_ Change](en-change.md) -und [en \_ selChange](en-selchange.md) -Ereignissen im unbestimmten Zustand.<br/> |
| <dl> <dt>**IWF \_ imecancelcomplete**</dt> </dl>           | Dieses Flag bestimmt, wie das Steuerelement die Kompositions Zeichenfolge eines IME verwendet, wenn der Benutzer es abbricht. Wenn das Flag festgelegt ist, wird die Kompositionszeichenfolge vom Steuerelement verworfen. Wenn das Flag nicht festgelegt ist, verwendet das Steuerelement die Kompositionszeichenfolge als Ergebniszeichenfolge. Diese Option ist standardmäßig deaktiviert (0).<br/>                                                                                                              |
| <dl> <dt>**IWF \_ noimplicitlang**</dt> </dl>              | **Windows 8**: Wenn dieses Flag festgelegt ist, deaktivieren Sie das Markieren von Tastatureingaben mit der Tastatur Sprache, und stellen Sie sicher, dass IDSs der nicht ostasiatischen Sprache mit dem Zeichen Repertoire kompatibel ist. Diese Option ist standardmäßig deaktiviert (0). <br/>                                                                                                                                                                             |
| <dl> <dt>**IMF \_ nokbdlidfixup**</dt> </dl>               | **Windows 8**: Wenn dieses Flag festgelegt ist, deaktiviert das Rich Edit-Steuerelement die stampende Tastatur Sprache auf einem leeren Steuerelement. Diese Option ist standardmäßig deaktiviert (0).<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**Rechtschreibprüfung für den IWF \_**</dt> </dl>               | **Windows 8**: Wenn dieses Flag festgelegt ist, schaltet das Rich Edit-Steuerelement die Rechtschreibprüfung aus. Diese Option ist standardmäßig deaktiviert (0). <br/>                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**IMF- \_ tkbautkorrektur**</dt> </dl>           | **Windows 8**: Wenn dieses Flag festgelegt ist, aktivieren Sie die Tastenkombination AutoCorrect. Diese Option ist standardmäßig deaktiviert (0). <br/>                                                                                                                                                                                                                                                                                                  |
| <dl> <dt>**IMF- \_ tkbvorhersage**</dt> </dl>               | **Windows 10**: wird ignoriert.<br/> **Windows 8**: Wenn dieses Flag festgelegt ist, aktiviert das Rich Edit-Steuerelement die Fingereingabe von Finger Eingaben. Diese Option ist standardmäßig deaktiviert (0). <br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**IMF- \_ uifonts**</dt> </dl>                     | Standard Schriftarten von Benutzeroberflächen verwenden. Diese Option ist standardmäßig deaktiviert (0).<br/>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Das Flag für die **\_ Automatische Schriftart der IMF** ist standardmäßig festgelegt. Die Flags " **\_ autokeyboard** " und " **IMF \_ imecancelcomplete** " sind standardmäßig deaktiviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ setlangoptions**](em-setlangoptions.md)
</dt> <dt>

[**EM \_ SetLimitText**](em-setlimittext.md)
</dt> </dl>

 

 





