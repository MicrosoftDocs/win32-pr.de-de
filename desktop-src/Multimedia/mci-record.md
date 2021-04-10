---
title: MCI_RECORD Befehl (MMSYSTEM. h)
description: Der Befehl MCI- \_ Datensatz startet die Aufzeichnung von der aktuellen Position aus oder von einem angegebenen Speicherort an einen anderen angegebenen Speicherort.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- MCI_RECORD Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_RECORD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cd15974753b8f40abd87b8d93622c090e2a57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104012"
---
# <a name="mci_record-command"></a>Befehl "MCI- \_ Datensatz"

Der Befehl [**MCI- \_ Datensatz**](mci-record-parms.md) startet die Aufzeichnung von der aktuellen Position aus oder von einem angegebenen Speicherort an einen anderen angegebenen Speicherort. VCR-und Waveform-Audiogeräte erkennen diesen Befehl. Obwohl Digital-Video-Geräte und MIDI-Sequencer diesen Befehl ebenfalls erkennen, implementieren die MCIAVI-und mciseq-Treiber Sie nicht.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RECORD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_RECORD_PARMS) lpRecord
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

<span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lprecord*
</dt> <dd>

Zeiger auf eine Struktur des [**MCI- \_ Daten Satz- \_ Parametern**](mci-record-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Dieser Befehl wird von Geräten unterstützt, die " **true** " zurückgeben, wenn Sie den [MCI \_ getdevcaps](mci-getdevcaps.md) -Befehl mit dem MCI \_ getdevcaps-Flag zum Aufzeichnen von Einträgen aufrufen \_ \_ . Für den MCIWave-Treiber werden alle Daten, die nach dem Öffnen einer Datei aufgezeichnet werden, verworfen, wenn die Datei geschlossen wird, ohne Sie zu speichern.

Die folgenden zusätzlichen Flags gelten für alle Geräte, die den MCI-Datensatz unterstützen \_ :

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von
</dt> <dd>

Ein Start Speicherort ist im **dwfrom** -Member der durch *lprecord* identifizierten Struktur enthalten. Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben. Wenn MCI \_ from nicht angegeben wird, wird der Start Speicherort standardmäßig auf die aktuelle Position festgelegt.

</dd> <dt>

<span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>MCI- \_ Datensatz \_ Einfügen
</dt> <dd>

Neu aufgezeichnete Informationen sollten eingefügt oder in die vorhandenen Daten eingefügt werden. Von einigen Geräten wird dies möglicherweise nicht unterstützt. Wenn dies unterstützt wird, ist dies die Standardeinstellung.

</dd> <dt>

<span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>MCI- \_ Daten Satz \_ Überschreibung
</dt> <dd>

Die Daten sollten vorhandene Daten überschreiben. Die MCIWave. Das drv-Gerät gibt \_ \_ als Antwort auf dieses Flag eine nicht unterstützte mcierr-Funktion zurück.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu
</dt> <dd>

Eine Endposition ist im **dwto** -Member der durch *lprecord* identifizierten Struktur enthalten. Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben. Wenn MCI \_ in nicht angegeben wird, wird die Endposition standardmäßig auf das Ende des Inhalts festgelegt.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>Audiostream für MCI \_ DGV \_ \_ -Datensatz \_
</dt> <dd>

Im **dwaudiostream** -Member der durch *lprecord* identifizierten Struktur ist eine audiostreamnummer enthalten. Wenn Sie dieses Flag weglassen, werden Audiodaten im ersten physischen Stream aufgezeichnet.

</dd> <dt>

<span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>MCI- \_ DGV- \_ Daten Satz \_ Aufbewahrung
</dt> <dd>

Wenn die Aufzeichnung angehalten wird, wird auf dem Bildschirm das letzte Bild angezeigt, und das Video wird erst angezeigt, wenn ein [MCI- \_ Monitor](mci-monitor.md) Befehl ausgegeben wird.

</dd> <dt>

<span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>MCI- \_ DGV- \_ Datensatz- \_ \_ Videostream
</dt> <dd>

Im **dwvideostream** -Member der durch *lprecord* identifizierten Struktur ist eine Video Strom Nummer enthalten. Wenn Sie dieses Flag weglassen, werden die Videodaten im ersten physischen Stream aufgezeichnet.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI- \_ DGV- \_ Rect
</dt> <dd>

Im **RC** -Member der durch *lprecord* identifizierten-Struktur wird ein Rechteck angegeben. Das Rechteck gibt den Bereich der externen Eingabe an, der als Quelle für die komprimierten und gespeicherten Pixel verwendet wird. Dieses Rechteck ist standardmäßig auf das Rechteck festgelegt (oder standardmäßig), das vom MCI \_ DGV \_ Put- \_ videoflag für den Befehl " [MCI \_ Put](mci-put.md) " angegeben wird. Wenn Sie anders festgelegt ist als das Video Rechteck, wird angezeigt, was nicht angezeigt wird.

</dd> </dl>

Für Digital Video-Geräte verweist *lprecord* auf eine [**MCI- \_ DGV \_ - \_ Daten Satz**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) Struktur.

Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>MCI- \_ VCR- \_ Datensatz \_ unter
</dt> <dd>

Der **dwat** -Member der durch *lprecord* identifizierten Struktur enthält einen Zeitpunkt, zu dem der gesamte Befehl beginnt, oder, wenn das Gerät gecuht wird, wenn das Gerät die vom Befehl angegebenen Position erreicht.

</dd> <dt>

<span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>MCI \_ VCR- \_ Daten Satz \_ initialisieren
</dt> <dd>

Suchen Sie das Gerät nach dem Start des Mediums, beginnen Sie mit dem Aufzeichnen von leeren Videos und Audiodaten, und notieren Sie sich, wenn möglich.

</dd> </dl>

Für VCR-Geräte verweist *lprecord* auf eine [**MCI- \_ VCR- \_ Daten Satz \_**](mci-vcr-record-parms.md) Struktur.

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

 

