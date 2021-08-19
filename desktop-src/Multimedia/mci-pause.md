---
title: MCI_PAUSE Befehl (Mmsystem.h)
description: Der \_ MCI-Befehl PAUSE hält die aktuelle Aktion an. CD-Audio- und Digitalvideogeräte, DIE SEQUENCEr-, VCR-, videodisc- und waveform-audio-Geräte erkennen diesen Befehl.
ms.assetid: c4d0b0a2-cd7b-4641-a318-eb4b4e88b70f
keywords:
- MCI_PAUSE-Befehl Windows Multimedia
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
ms.openlocfilehash: 2c2318a10e7b03bf89d616bd6ff2373cdf785b0bb4015ab4b308ead57d7f9223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803498"
---
# <a name="mci_pause-command"></a>MCI \_ PAUSE-Befehl

Der \_ MCI-Befehl PAUSE hält die aktuelle Aktion an. CD-Audio- und Digitalvideogeräte, DIE SEQUENCEr-, VCR-, videodisc- und waveform-audio-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsnachricht empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder bei Digitalvideo- und VCR-Geräten MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*
</dt> <dd>

Zeiger auf eine [**MCI \_ GENERIC \_ PARMS-Struktur.**](mci-generic-parms.md) (Geräte mit erweiterten Befehlssätzen ersetzen diese Struktur möglicherweise durch eine gerätespezifische Struktur.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Der Unterschied zwischen den [Befehlen MCI \_ STOP](mci-stop.md) und MCI \_ PAUSE hängt vom Gerät ab. Wenn möglich, hält MCI PAUSE den Gerätebetrieb an, lässt das Gerät aber bereit, die Wiedergabe \_ sofort wieder aufzunehmen. Mit den Treibern MCICDA, MCISEQ und MCIPIONR funktioniert der MCI PAUSE-Befehl genauso \_ wie der MCI \_ STOP-Befehl.

Bei Digitalvideogeräten verweist der *lpPause-Parameter* auf eine [**MCI \_ DGV \_ PAUSE \_ PARMS-Struktur.**](/previous-versions//dd743395(v=vs.85))

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

[MCI-Befehle](mci-commands.md)
</dt> </dl>

 

