---
title: MCI_PAUSE Befehl (MMSYSTEM. h)
description: Der MCI- \_ anhaltebefehl hält die aktuelle Aktion an. CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: c4d0b0a2-cd7b-4641-a318-eb4b4e88b70f
keywords:
- MCI_PAUSE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_PAUSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076397ca9ab770d6f9c23cc5b64853bdd2f07ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739824"
---
# <a name="mci_pause-command"></a>MCI-Befehl "anhalten" \_

Der MCI- \_ anhaltebefehl hält die aktuelle Aktion an. CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk und Waveform-Audiogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PAUSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpPause
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

<span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lppause*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Der Unterschied zwischen den [MCI- \_ Stopps](mci-stop.md) und den MCI-anhaltebefehlen \_ hängt vom Gerät ab. Wenn möglich, hält MCI anhalten \_ den Geräte Vorgang an, aber das Gerät kann sofort wieder aufgenommen werden. Bei den mcicda-, mciseq-und mcipionr-Treibern funktioniert der MCI- \_ anhaltebefehl genauso wie der Befehl zum Stoppen von MCI \_ .

Für Digital Video-Geräte zeigt der *lppause* -Parameter auf eine [**MCI \_ DGV \_ - \_ Pause**](/previous-versions//dd743395(v=vs.85)) -Parameter-Struktur.

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

 

