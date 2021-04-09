---
title: MM_MCINOTIFY Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm mcinotify benachrichtigt eine Anwendung, dass ein MCI-Gerät einen Vorgang abgeschlossen hat. MCI-Geräte senden diese Nachricht nur, wenn das MCI- \_ Benachrichtigungs Kennzeichen verwendet wird.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- MM_MCINOTIFY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MCINOTIFY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ee62c4a2b6e17bf5ad6d719dcb7d6e992a2f2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104709"
---
# <a name="mm_mcinotify-message"></a>MM- \_ mcinotifismeldung

Die Meldung **mm \_ mcinotify** benachrichtigt eine Anwendung, dass ein MCI-Gerät einen Vorgang abgeschlossen hat. MCI-Geräte senden diese Nachricht nur, wenn das MCI- \_ Benachrichtigungs Kennzeichen verwendet wird.


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Der Grund für die Benachrichtigung. Die folgenden Werte sind definiert:



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCI- \_ Benachrichtigung \_ abgebrochen    | Das Gerät hat einen Befehl empfangen, der verhindert hat, dass die aktuellen Bedingungen zum Initiieren der Rückruffunktion erfüllt werden. Wenn ein neuer Befehl den aktuellen Befehl unterbricht und auch eine Benachrichtigung anfordert, sendet das Gerät nur diese Nachricht, nicht jedoch die \_ MCI-Benachrichtigung. \_ |
| MCI- \_ Benachrichtigungs \_ Fehler    | Gerätefehler beim Ausführen des Befehls durch das Gerät.                                                                                                                                                                                                            |
| MCI- \_ Benachrichtigung \_ erfolgreich | Die Bedingungen, die die Rückruffunktion initiieren, wurden erfüllt.                                                                                                                                                                                                                 |
| MCI- \_ Benachrichtigung \_ abgelöst | Das Gerät hat einen weiteren Befehl mit dem festgelegten Flag "Benachrichtigen" erhalten, und die aktuellen Bedingungen zum Initiieren der Rückruffunktion wurden abgelöst.                                                                                                                           |



 

</dd> <dt>

<span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*ldevid*
</dt> <dd>

Der Bezeichner des Geräts, das die Rückruffunktion initiiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zum MCI- \_ Benachrichtigungs Kennzeichen finden Sie [unter dem notify-Flag](the-notify-flag.md).

Ein Gerät gibt das MCI \_ - \_ Flag zum Benachrichtigen von Benachrichtigungen mit **mm \_ mcinotify** zurück, wenn die Aktion für einen Befehl abgeschlossen ist. Beispielsweise verwendet ein CD-Audiogerät dieses Flag für die Benachrichtigung für den [**Wiedergabe**](play.md) Befehl ( [**MCI \_ Play**](mci-play.md)), wenn die Wiedergabe des Geräts abgeschlossen ist. Der **Wiedergabe** Befehl ist nur erfolgreich, wenn er die angegebene Endposition erreicht oder das Ende des Mediums erreicht. Auf ähnliche Weise wird die MCI-Benachrichtigung durch die Befehle [**Seek**](seek.md) ( [**MCI \_ Seek**](mci-seek.md)) und [**Record**](record.md) ( [**MCI- \_ Datensatz**](mci-record.md)) nicht erfolgreich zurückgegeben, \_ \_ bis die angegebene Endposition erreicht oder das Ende des Mediums erreicht wurde.

Ein Gerät gibt das MCI \_ - \_ Flag zum Benachrichtigen von Benachrichtigungen mit mm- **\_ mcinotifinur** dann zurück, wenn es einen Befehl empfängt, der verhindert, dass die Benachrichtigungs Bedingungen erfüllt werden. Beispielsweise würde der [**Wiedergabe**](play.md) Befehl die Benachrichtigung für einen vorherigen **Wiedergabe** Befehl nicht abbrechen, vorausgesetzt, dass der neue Befehl die Wiedergabe Richtung nicht ändert oder die Endposition ändert. Die [**Such**](seek.md) -und [**Daten Satz**](record.md) Befehle Verhalten sich ähnlich. MCI sendet auch keine MCI- \_ Benachrichtigung, \_ die abgebrochen wird, wenn die Wiedergabe oder Aufzeichnung mit dem Befehl [**Pause**](pause.md) ( [**MCI- \_ Pause**](mci-pause.md)) angehalten wird. Durch das Senden des Befehls [**Resume**](resume.md) ( [**MCI \_ Resume**](mci-resume.md)) können die Rückruf Bedingungen weiterhin erfüllt werden.

Wenn Ihre Anwendung eine Benachrichtigung für einen Befehl anfordert, überprüfen Sie die Fehlerrückgabe der Funktionen [**mciSendString**](/previous-versions//dd757161(v=vs.85)) oder [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Wenn diese Funktionen auf einen Fehler stoßen und einen Wert ungleich 0 (null) zurückgeben, wird von MCI keine Benachrichtigung für den Befehl festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Nachrichten](mci-messages.md)
</dt> <dt>

[**Brechung**](pause.md)
</dt> <dt>

[**Theater**](play.md)
</dt> <dt>

[**Aufnahme**](record.md)
</dt> <dt>

[**zusetzen**](resume.md)
</dt> <dt>

[**einzuholen**](seek.md)
</dt> </dl>

 

