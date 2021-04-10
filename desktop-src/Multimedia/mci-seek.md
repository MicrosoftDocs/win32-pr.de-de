---
title: MCI_SEEK Befehl (MMSYSTEM. h)
description: Der MCI \_ Seek-Befehl ändert die aktuelle Position im Inhalt so schnell wie möglich.
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- MCI_SEEK Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e34f6fa823092968e74515a885e7a40db9f2d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040297"
---
# <a name="mci_seek-command"></a>Befehl "MCI- \_ Suche"

Der MCI \_ Seek-Befehl ändert die aktuelle Position im Inhalt so schnell wie möglich. Die Video-und Audioausgabe sind während der Suche deaktiviert. Nachdem die Suche beendet wurde, wird das Gerät beendet. CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk und Waveform-Audiogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SEEK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SEEK_PARMS) lpSeek
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

<span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpseek*
</dt> <dd>

Zeiger auf eine [**MCI \_ - \_ Such**](mci-seek-parms.md) Elementstruktur. (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Wenn eine Daten Stichprobengröße für ein Gerät größer als 1 Byte ist (z. b. mit Waveform-audiostereo-Daten), wechselt dieser Befehl zum Anfang des nächsten Beispiels, wenn eine angegebene Position nicht mit dem Anfang eines Beispiels übereinstimmt.

Die folgenden zusätzlichen Flags gelten für alle Geräte, die die MCI-Suche unterstützen \_ :

<dl> <dt>

<span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI \_ - \_ Suche \_ am Ende
</dt> <dd>

Suchen Sie nach dem Ende des Inhalts.

</dd> <dt>

<span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI \_ - \_ Suche \_ starten
</dt> <dd>

Suchen Sie am Anfang des Inhalts.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu
</dt> <dd>

Eine Position ist im **dwto** -Member der durch *lpseek* identifizierten Struktur enthalten. Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben. Verwenden Sie dieses Flag nicht mit der MCI- \_ Suche \_ , um zu \_ \_ starten oder \_ zu \_ starten.

</dd> </dl>

Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI \_ VCR- \_ Suche \_ unter
</dt> <dd>

Der **dwat** -Member der-Struktur, die von *lpseek* identifiziert wird, enthält einen Zeitpunkt, zu dem der gesamte Befehl beginnt.

</dd> <dt>

<span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>MCI- \_ VCR- \_ Such \_ Zeichen
</dt> <dd>

Der **dwmark** -Member der durch *lpseek* identifizierten Struktur enthält die nummerierte Markierung, nach der gesucht werden soll.

</dd> <dt>

<span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>MCI \_ VCR- \_ Suche \_ umkehren
</dt> <dd>

Die Suchrichtung ist umgekehrt. Diese wird nur mit dem Flag "MCI \_ VCR- \_ \_ suchflag" verwendet.

</dd> </dl>

Bei VCR-Geräten verweist der *lpseek* -Parameter auf eine [**MCI- \_ VCR- \_ suchparameterstruktur \_**](mci-vcr-seek-parms.md) .

Das folgende zusätzliche Flag wird für den **Videodisk** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI- \_ VD- \_ Suche \_ umkehren
</dt> <dd>

Die Suchrichtung ist umgekehrt.

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

 

