---
title: MM_MCINOTIFY (Mmsystem.h)
description: Die MM \_ MCINOTIFY-Meldung benachrichtigt eine Anwendung, dass ein MCI-Gerät einen Vorgang abgeschlossen hat. MCI-Geräte senden diese Nachricht nur, wenn das MCI \_ NOTIFY-Flag verwendet wird.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- MM_MCINOTIFY-Nachricht Windows Multimedia
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
ms.openlocfilehash: fc03ab0406542472871f35ca3ff619d4d9a6f35725b9322a4c11bc73bc29a5aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807510"
---
# <a name="mm_mcinotify-message"></a>MM \_ MCINOTIFY-Nachricht

Die **MM \_ MCINOTIFY-Meldung** benachrichtigt eine Anwendung, dass ein MCI-Gerät einen Vorgang abgeschlossen hat. MCI-Geräte senden diese Nachricht nur, wenn das MCI \_ NOTIFY-Flag verwendet wird.


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Grund für die Benachrichtigung. Die folgenden Werte sind definiert:



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCI \_ NOTIFY \_ ABORTED    | Das Gerät hat einen Befehl empfangen, der verhindert, dass die aktuellen Bedingungen zum Initiieren der Rückruffunktion erfüllt sind. Wenn ein neuer Befehl den aktuellen Befehl unterbricht und auch eine Benachrichtigung an fordert, sendet das Gerät nur diese Nachricht und nicht MCI \_ NOTIFY \_ SUPERSEDED. |
| \_MCI-BENACHRICHTIGUNGSFEHLER \_    | Ein Gerätefehler ist aufgetreten, während das Gerät den Befehl ausgeführt hat.                                                                                                                                                                                                            |
| MCI \_ NOTIFY \_ SUCCESSFUL | Die Bedingungen, die die Rückruffunktion initiieren, sind erfüllt.                                                                                                                                                                                                                 |
| MCI \_ NOTIFY \_ SUPERSEDED | Das Gerät hat einen weiteren Befehl mit dem Flag "notify" empfangen, und die aktuellen Bedingungen zum Initiieren der Rückruffunktion wurden ersetzt.                                                                                                                           |



 

</dd> <dt>

<span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*
</dt> <dd>

Bezeichner des Geräts, das die Rückruffunktion initiiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Weitere Informationen zum MCI \_ NOTIFY-Flag finden Sie unter Das [Benachrichtigungsflag](the-notify-flag.md).

Ein Gerät gibt das MCI \_ NOTIFY \_ SUCCESSFUL-Flag mit **MM \_ MCINOTIFY** zurück, wenn die Aktion für einen Befehl abgeschlossen ist. Ein CD-Audiogerät verwendet dieses Flag z. B. für die Benachrichtigung für den Wiedergabebefehl [**(**](play.md) [**MCI \_ PLAY**](mci-play.md)), wenn die Wiedergabe des Geräts abgeschlossen ist. Der **Wiedergabebefehl** ist nur erfolgreich, wenn er die angegebene Endposition erreicht oder das Ende des Mediums erreicht. Ebenso geben die Befehle [**seek**](seek.md) ( [**MCI \_ SEEK**](mci-seek.md)) und [**record**](record.md) ( MCI RECORD ) erst dann [**MCI \_ NOTIFY**](mci-record.md)SUCCESSFUL zurück, wenn sie die angegebene Endposition erreichen oder das Ende des \_ \_ Mediums erreichen.

Ein Gerät gibt das MCI \_ NOTIFY \_ ABORTED-Flag mit MM **\_ MCINOTIFY** nur dann zurück, wenn es einen Befehl empfängt, der verhindert, dass die Benachrichtigungsbedingungen erfüllt werden. Beispielsweise würde der [**Befehl play**](play.md) die Benachrichtigung  für einen vorherigen Wiedergabebefehl nicht abbrechen, vorausgesetzt, der neue Befehl ändert weder die Wiedergaberichtung noch die Endposition. Die [**Such-**](seek.md) [**und Datensatzbefehle**](record.md) verhalten sich ähnlich. MCI sendet auch nicht MCI NOTIFY ABORTED, wenn die Wiedergabe oder Aufzeichnung mit dem Befehl \_ \_ [**pause**](pause.md) [**(MCI \_ PAUSE**](mci-pause.md)) angehalten wird. Durch senden [**des Befehls resume**](resume.md) ( [**MCI \_ RESUME**](mci-resume.md)) können die Rückrufbedingungen weiterhin erfüllt werden.

Wenn Ihre Anwendung eine Benachrichtigung für einen Befehl an fordert, überprüfen Sie die Fehler zurückgegebenen [**mciSendString-**](/previous-versions//dd757161(v=vs.85)) oder [**mciSendCommand-Funktionen.**](/previous-versions//dd757160(v=vs.85)) Wenn bei diesen Funktionen ein Fehler auftritt und ein Wert ungleich 0 (null) zurückgegeben wird, wird von MCI keine Benachrichtigung für den Befehl festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Nachrichten](mci-messages.md)
</dt> <dt>

[**pause**](pause.md)
</dt> <dt>

[**Spielen**](play.md)
</dt> <dt>

[**Aufzeichnung**](record.md)
</dt> <dt>

[**Fortsetzen**](resume.md)
</dt> <dt>

[**Suchen**](seek.md)
</dt> </dl>

 

