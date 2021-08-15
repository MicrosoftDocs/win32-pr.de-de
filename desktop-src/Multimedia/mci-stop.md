---
title: MCI_STOP Befehl (Mmsystem.h)
description: Der Befehl MCI STOP beendet alle Wiedergabe- und Aufzeichnungssequenzen, entlädt alle Wiedergabepuffer und beendet die \_ Anzeige von Videobildern. CD-Audio, digital-video, KEYBOARD sequencer, videodisc, VCR und waveform-audio-Geräte erkennen diesen Befehl.
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- MCI_STOP-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_STOP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02830dde544e025447cb72df6ff3720857985384ff6bd074c5e0718b114697c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374602"
---
# <a name="mci_stop-command"></a>MCI \_ STOP-Befehl

Der Befehl MCI STOP beendet alle Wiedergabe- und Aufzeichnungssequenzen, entlädt alle Wiedergabepuffer und beendet die \_ Anzeige von Videobildern. CD-Audio, digital-video, KEYBOARD sequencer, videodisc, VCR und waveform-audio-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STOP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsnachricht empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder für Digitalvideo- und VCR-Geräte MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*
</dt> <dd>

Zeiger auf eine [**MCI \_ GENERIC \_ PARMS-Struktur.**](mci-generic-parms.md) (Geräte mit erweiterten Befehlssätzen ersetzen diese Struktur möglicherweise durch eine gerätespezifische Struktur.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Der Unterschied zwischen den Befehlen MCI \_ STOP und [MCI \_ PAUSE](mci-pause.md) hängt vom Gerät ab. Wenn möglich, hält MCI PAUSE den Gerätebetrieb an, lässt das Gerät aber bereit, die Wiedergabe \_ sofort wieder aufzunehmen.

Für das CD-Audiogerät setzt MCI STOP die aktuelle Trackposition auf 0 zurück. Im Gegensatz dazu behält MCI PAUSE die aktuelle Trackposition bei und erwartet, dass das Gerät wieder abgespielt \_ wird. [ \_ ](mci-pause.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehle](mci-commands.md)
</dt> </dl>

 

