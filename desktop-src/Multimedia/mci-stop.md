---
title: MCI_STOP Befehl (MMSYSTEM. h)
description: Der MCI \_ -Befehl "beenden" beendet alle Wiedergabe-und Daten Satz Sequenzen, entlädt alle Wiedergabe Puffer und beendet die Anzeige von Videobildern. CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- MCI_STOP Befehl Windows-Multimedia
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
ms.openlocfilehash: 6ea5f2acbe39b0be64ebc640ae31ceede7591c7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391967"
---
# <a name="mci_stop-command"></a>MCI- \_ Befehl zum Abbrechen

Der MCI \_ -Befehl "beenden" beendet alle Wiedergabe-und Daten Satz Sequenzen, entlädt alle Wiedergabe Puffer und beendet die Anzeige von Videobildern. CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*
</dt> <dd>

Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpstopps*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Der Unterschied zwischen den MCI \_ -Stopps und den [MCI \_ ](mci-pause.md) -anhaltebefehlen hängt vom Gerät ab. Wenn möglich, hält MCI anhalten \_ den Geräte Vorgang an, aber das Gerät kann sofort wieder aufgenommen werden.

Für das CD-Audiogerät setzt MCI \_ die aktuelle Positionsposition auf NULL zurück. im Gegensatz dazu behält die [MCI- \_ Pause](mci-pause.md) die aktuelle Position des Titels bei und geht davon aus, dass die Wiedergabe des Geräts fortgesetzt wird.

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

[MCI-Befehle](mci-commands.md)
</dt> </dl>

 

