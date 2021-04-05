---
title: MCI_PLAY Befehl (MMSYSTEM. h)
description: Der Befehl MCI \_ Play signalisiert dem Gerät, mit dem Übertragen von Ausgabedaten zu beginnen. CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- MCI_PLAY Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_PLAY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f985a8d5d6be7ad42702afc898b3aaf437ef320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859310"
---
# <a name="mci_play-command"></a>MCI- \_ Wiedergabe Befehl

Der Befehl MCI \_ Play signalisiert dem Gerät, mit dem Übertragen von Ausgabedaten zu beginnen. CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PLAY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_PLAY_PARMS ) lpPlay
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

<span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpplay*
</dt> <dd>

Zeiger auf eine [**MCI- \_ Wiedergabe- \_ Parametern**](mci-play-parms.md) -Struktur. (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags gelten für alle Geräte, die die MCI-Wiedergabe unterstützen \_ :

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von
</dt> <dd>

Ein Start Speicherort ist im **dwfrom** -Member der von *lpplay* identifizierten Struktur enthalten. Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben. Wenn MCI \_ from nicht angegeben wird, wird der Start Speicherort standardmäßig auf die aktuelle Position festgelegt.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu
</dt> <dd>

Eine Endposition ist im **dwto** -Member der von *lpplay* identifizierten Struktur enthalten. Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ \_ Format Flag zum Festlegen \_ der Uhrzeit der MCI- \_ Menge angegeben. Wenn MCI \_ in nicht angegeben wird, wird die Endposition standardmäßig auf das Ende des Mediums festgelegt.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>MCI \_ DGV- \_ Wiedergabe \_ Wiederholen
</dt> <dd>

Die Wiedergabe sollte am Anfang wieder gestartet werden, wenn das Ende des Inhalts erreicht ist.

</dd> <dt>

<span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI \_ DGV- \_ Wiedergabe \_ Rückgängigmachen
</dt> <dd>

Wiedergabe sollte in umgekehrter Reihenfolge erfolgen.

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>MCI- \_ MCIAVI- \_ Wiedergabe \_ Fenster
</dt> <dd>

Die Wiedergabe sollte in dem Fenster erfolgen, das einer Geräte Instanz zugeordnet ist (Standardeinstellung). (Dieses Flag ist für MCIAVI spezifisch. DRV.)

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI- \_ MCIAVI \_ Play \_ Fullscreen
</dt> <dd>

Bei der Wiedergabe sollte eine voll Bild Anzeige verwendet werden. Verwenden Sie dieses Flag nur bei der Wiedergabe von komprimierten oder 8-Bit-Dateien.

</dd> </dl>

Für Digital Video-Geräte verweist *lpplay* auf eine [**MCI- \_ DGV \_ - \_ Wiedergabe**](/previous-versions//dd743396(v=vs.85)) Elementstruktur.

Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>MCI \_ VCR- \_ Wiedergabe \_ bei
</dt> <dd>

Der **dwat** -Member der-Struktur, die von *lpplay* identifiziert wird, enthält einen Zeitpunkt, zu dem der gesamte Befehl beginnt, oder, wenn das Gerät über die Position des Geräts erreicht wird, die durch den [MCI \_](mci-cue.md) -Hinweis Befehl angegeben wird.

</dd> <dt>

<span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>MCI \_ VCR- \_ Wiedergabe \_ umkehren
</dt> <dd>

Wiedergabe sollte in umgekehrter Reihenfolge erfolgen.

</dd> <dt>

<span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>MCI- \_ VCR- \_ Wiedergabe Überprüfung \_
</dt> <dd>

Die Wiedergabe sollte so schnell wie möglich sein, während die Videoausgabe erhalten bleibt.

</dd> </dl>

Bei VCR-Geräten verweist *lpplay* auf eine [**MCI- \_ VCR-Wiedergabe- \_ \_ Parametern**](mci-vcr-play-parms.md) -Struktur.

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp " **Videodisk** " verwendet:

<dl> <dt>

<span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI- \_ VD- \_ Wiedergabe \_ schnell
</dt> <dd>

Spielen Sie schnell.

</dd> <dt>

<span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI-VD-wieder \_ \_ Gabe \_ umkehren
</dt> <dd>

Wiedergabe in umgekehrter Reihenfolge.

</dd> <dt>

<span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>MCI- \_ VD- \_ Wiedergabe \_ Scan
</dt> <dd>

Schnelles Scannen.

</dd> <dt>

<span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI-VD-wieder \_ \_ Gabe \_ langsam
</dt> <dd>

Spielen Sie langsam.

</dd> <dt>

<span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>MCI- \_ VD- \_ Wiedergabe \_ Geschwindigkeit
</dt> <dd>

Die Wiedergabegeschwindigkeit ist im **dwspeed** -Member in der von *lpplay* identifizierten Struktur enthalten.

</dd> </dl>

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

 

