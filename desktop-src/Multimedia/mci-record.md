---
title: MCI_RECORD Befehl (Mmsystem.h)
description: Der MCI \_ RECORD-Befehl beginnt mit der Aufzeichnung von der aktuellen Position oder von einem angegebenen Speicherort an einem anderen angegebenen Speicherort.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- MCI_RECORD Befehl Windows Multimedia
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
ms.openlocfilehash: 327b9ed9b138b581bec17d8bfcfe19ae67bb07d59be2781af54e22a85e2133c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803451"
---
# <a name="mci_record-command"></a>MCI \_ RECORD-Befehl

Der [**MCI \_ RECORD-Befehl**](mci-record-parms.md) beginnt mit der Aufzeichnung von der aktuellen Position oder von einem angegebenen Speicherort an einem anderen angegebenen Speicherort. VCR- und Waveform-Audiogeräte erkennen diesen Befehl. Obwohl digital-video-Geräte und GIGABYTE-Sequencer diesen Befehl ebenfalls erkennen, implementieren die MCIAVI- und MCISEQ-Treiber ihn nicht.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsmeldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder, für Digital Video- und VCR-Geräte, MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*
</dt> <dd>

Zeiger auf eine [**MCI \_ RECORD \_ PARMS-Struktur.**](mci-record-parms.md) (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Dieser Befehl wird von Geräten unterstützt, die **TRUE** zurückgeben, wenn Sie den [MCI \_ GETDEVCAPS-Befehl](mci-getdevcaps.md) mit dem \_ MCI GETDEVCAPS \_ CAN \_ RECORD-Flag aufrufen. Für den MCIWAVE-Treiber werden alle Nach dem Öffnen einer Datei aufgezeichneten Daten verworfen, wenn die Datei geschlossen wird, ohne sie zu speichern.

Die folgenden zusätzlichen Flags gelten für alle Geräte, die MCI \_ RECORD unterstützen:

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Eine Startposition ist im **dwFrom-Member** der durch *lpRecord* identifizierten Struktur enthalten. Die den Positionswerten zugewiesenen Einheiten werden mit dem MCI \_ SET \_ TIME \_ FORMAT-Flag des [MCI \_ SET-Befehls](mci-set.md) angegeben. Wenn MCI \_ FROM nicht angegeben ist, wird die Startposition standardmäßig auf die aktuelle Position festgelegt.

</dd> <dt>

<span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>MCI \_ RECORD \_ INSERT
</dt> <dd>

Neu aufgezeichnete Informationen sollten in die vorhandenen Daten eingefügt oder eingefügt werden. Einige Geräte unterstützen dies möglicherweise nicht. Wenn dies unterstützt wird, ist dies die Standardeinstellung.

</dd> <dt>

<span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>MCI \_ RECORD \_ OVERWRITE
</dt> <dd>

Daten sollten vorhandene Daten überschreiben. The MCIWAVE. Das DRV-Gerät gibt MCIERR \_ UNSUPPORTED \_ FUNCTION als Reaktion auf dieses Flag zurück.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Eine Endposition ist im **dwTo-Member** der durch *lpRecord* identifizierten Struktur enthalten. Die den Positionswerten zugewiesenen Einheiten werden mit dem MCI \_ SET \_ TIME \_ FORMAT-Flag des [MCI \_ SET-Befehls](mci-set.md) angegeben. Wenn MCI \_ TO nicht angegeben ist, wird der Endspeicherort standardmäßig auf das Ende des Inhalts festgelegt.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **Gerätetyp digitalvideo** verwendet:

<dl> <dt>

<span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>MCI \_ DGV \_ RECORD \_ AUDIO \_ STREAM
</dt> <dd>

Eine Audiostreamnummer ist im **dwAudioStream-Member** der durch *lpRecord* identifizierten Struktur enthalten. Wenn Sie dieses Flag weglassen, werden Audiodaten im ersten physischen Stream aufgezeichnet.

</dd> <dt>

<span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>MCI \_ DGV \_ RECORD \_ HOLD
</dt> <dd>

Wenn die Aufzeichnung beendet wird, wird das letzte Bild auf dem Bildschirm angezeigt, und das Video wird erst wieder angezeigt, wenn ein [MCI \_ MONITOR-Befehl](mci-monitor.md) ausgegeben wurde.

</dd> <dt>

<span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>MCI \_ DGV \_ RECORD \_ VIDEO \_ STREAM
</dt> <dd>

Eine Videostreamnummer ist im **dwVideoStream-Member** der durch *lpRecord* identifizierten Struktur enthalten. Wenn Sie dieses Flag weglassen, werden Videodaten im ersten physischen Stream aufgezeichnet.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT
</dt> <dd>

Ein Rechteck wird im **rc-Member** der durch *lpRecord* identifizierten Struktur angegeben. Das Rechteck gibt den Bereich der externen Eingabe an, der als Quelle für die komprimierten und gespeicherten Pixel verwendet wird. Dieses Rechteck wird standardmäßig auf das Rechteck festgelegt (oder standardmäßig festgelegt), das vom MCI \_ DGV \_ PUT \_ VIDEO-Flag für den [MCI \_ PUT-Befehl](mci-put.md) angegeben wird. Wenn es anders als das Videorechteck festgelegt ist, wird nicht angezeigt, was aufgezeichnet wird.

</dd> </dl>

Für Digitalvideogeräte zeigt *lpRecord* auf eine [**MCI \_ DGV \_ RECORD \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms)

Die folgenden zusätzlichen Flags werden mit dem **Vcr-Gerätetyp** verwendet:

<dl> <dt>

<span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>MCI \_ VCR \_ RECORD \_ AT
</dt> <dd>

Der **dwAt-Member** der von *lpRecord* identifizierten Struktur enthält einen Zeitpunkt, zu dem der gesamte Befehl beginnt, oder , wenn das Gerät angekuppelt wird, wenn das Gerät den von der Position erreicht, die vom Cue-Befehl angegeben wird.

</dd> <dt>

<span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>INITIALISIEREN DES \_ MCI-VCR-DATENSATZES \_ \_
</dt> <dd>

Suchen Sie das Gerät bis zum Anfang des Mediums, beginnen Sie mit der Aufzeichnung leerer Videos und Audiodaten, und zeichnen Sie nach Möglichkeit den Zeitcode auf.

</dd> </dl>

Für VCR-Geräte zeigt *lpRecord* auf eine [**MCI \_ VCR \_ RECORD \_ PARMS-Struktur.**](mci-vcr-record-parms.md)

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

 

