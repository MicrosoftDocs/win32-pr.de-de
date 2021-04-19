---
title: MCI_SET Befehl (MMSYSTEM. h)
description: Der MCI- \_ set-Befehl legt Geräteinformationen fest. CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk, Video-Overlay und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- MCI_SET Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SET
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1da0da94c0d970b607a29548c773fa9302d26d
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2021
ms.locfileid: "106373393"
---
# <a name="mci_set-command"></a>Befehl "MCI- \_ Set"

> [!NOTE]
> Bias-freie Kommunikation Microsoft unterstützt eine unterschiedlichste und inklusive Umgebung.  In diesem Dokument sind Verweise auf das Wort "Slave" vorhanden. Im [Stil Handbuch von Microsoft für die Bias-Free-Kommunikation](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) wird dies als ausschließendes Wort erkannt.  Dieser Wortlaut wird verwendet, da es sich zurzeit um den in den Befehlen verwendeten Wortlaut handelt. Aus Konsistenz Gründen enthält dieses Dokument dieses Wort. Wenn dieses Wort in den Befehlen geändert wird, korrigieren wir dieses Dokument als Ausrichtung.

Der MCI- \_ set-Befehl legt Geräteinformationen fest. CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk, Video-Overlay und Waveform-Audiogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SET, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SET_PARMS) lpSet
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

<span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpset*
</dt> <dd>

Zeiger auf eine Struktur für einen [**MCI- \_ Satz von \_ Parametern**](mci-set-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags gelten für alle Geräte, die die MCI-Gruppe unterstützen \_ :

<dl> <dt>

<span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI \_ \_ -Set-Audiodatei
</dt> <dd>

Im dwaudiomember der durch *lpset* identifizierten Struktur ist eine audiokanalnummer enthalten. Dieses Flag muss verwendet werden, wenn MCI \_ \_ auf on oder MCI Set Off festgelegt ist \_ \_ . Verwenden Sie eine der folgenden Konstanten, um die Kanalnummer anzugeben:

</dd> <dt>

<span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI \_ Set \_ \_ audioall
</dt> <dd>

Alle audiochannels.

</dd> <dt>

<span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI \_ \_ -Set-Audiodatei \_ Links
</dt> <dd>

Linker Kanal.

</dd> <dt>

<span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI \_ \_ - \_ audiorecht festlegen
</dt> <dd>

Rechter Kanal.

</dd> <dt>

<span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>MCI- \_ Einrichtung wurde \_ \_ geschlossen
</dt> <dd>

Schließt die Medien Abdeckung (sofern vorhanden).

</dd> <dt>

<span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI- \_ fest \_ gelegungstür \_ geöffnet
</dt> <dd>

Öffnet die Medien Abdeckung (sofern vorhanden).

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI- \_ festgelegt \_
</dt> <dd>

Deaktiviert das angegebene Video oder den Audiokanal.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ festgelegt \_ auf
</dt> <dd>

Aktiviert das angegebene Video oder den Audiokanal.

</dd> <dt>

<span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>MCI- \_ fest \_ gelegzeit \_ Format
</dt> <dd>

Ein Zeitformat Parameter ist im **dwtimeformat** -Member der durch *lpset* identifizierten Struktur enthalten. Die folgenden Flags werden mit diesem Flag verwendet:

</dd> <dt>

<span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>MCI- \_ Format ( \_ Bytes)
</dt> <dd>

In einem PCM-Datenformat (Pulse Code-Modulation) ändert die Beschreibung für das Zeitelement in Bytes für die Eingabe oder Ausgabe. Wird vom **waveaudiogerätetyp** erkannt.

</dd> <dt>

<span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>MCI- \_ Formatierungs \_ Frames
</dt> <dd>

In nachfolgenden Befehlen werden Frames verwendet. Wird von den Gerätetypen **Digitalvideo**, **VCR** und **Videodisc** erkannt.

</dd> <dt>

<span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>MCI- \_ Format \_ HMS
</dt> <dd>

Ändert das Uhrzeit Format in Stunden, Minuten und Sekunden. Wird von den Gerätetypen **VCR** und **Videodisk** erkannt.

</dd> <dt>

<span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>MCI- \_ Format ( \_ Millisekunden)
</dt> <dd>

Ändert das Zeitformat in Millisekunden. Wird von allen Gerätetypen erkannt.

</dd> <dt>

<span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>MCI- \_ Format \_ MSF
</dt> <dd>

Ändert das Zeitformat in Minuten, Sekunden und Frames. Wird von den Gerätetypen **CDAudio** und **VCR** erkannt.

</dd> <dt>

<span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>MCI- \_ Format \_ Beispiele
</dt> <dd>

Ändert das Uhrzeit Format in Samplings für Eingabe oder Ausgabe. Wird vom **waveaudiogerätetyp** erkannt.

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI \_ \_ -Format SMPTE \_ 24, MCI \_ \_ -Format SMPTE \_ 25 und MCI- \_ Format \_ SMPTE \_ 30
</dt> <dd>

Legt das Zeitformat auf 24, 25 und 30 Frame-SMPTE (Struktur von Bewegungsbild-und Fernseh Technikern) fest. Wird von den- **Sequencer** -und **VCR** -Gerätetypen erkannt.

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI- \_ Format \_ SMPTE \_ 30drop
</dt> <dd>

Legt das Zeitformat auf 30 Drop-Frame-SMPTE fest. Wird von den- **Sequencer** -und **VCR** -Gerätetypen erkannt.

</dd> <dt>

<span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>MCI- \_ Format- \_ TMSF
</dt> <dd>

Ändert das Zeitformat in nachverfolgt, Minuten, Sekunden und Frames. (MCI verwendet kontinuierliche Nachverfolgung.) Wird von den Gerätetypen **CDAudio** und **VCR** erkannt.

</dd> <dt>

<span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>MCI- \_ Set- \_ Video
</dt> <dd>

Legt das Videosignal ein oder aus. Dieses Flag muss verwendet werden, wenn MCI \_ \_ auf on oder MCI \_ \_ Off Off festgelegt ist. Geräte, die nicht über Video verfügen, geben eine nicht unterstützte mcierr- \_ \_ Funktion zurück.

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI \_ DGV \_ Set \_ File Format
</dt> <dd>

Ein Dateiformat Parameter ist im **dwfileformat** -Member der durch *lpset* identifizierten Struktur enthalten. Für Digital Video-Geräte wird das Dateiformat für Befehle zum Speichern oder erfassen verwendet. Wenn der Wert nicht angegeben wird, wird standardmäßig ein Gerätetreiber definiertes Format festgelegt. Wenn das angegebene Dateiformat mit dem aktuell ausgewählten Algorithmus und der ausgewählten Qualität in Konflikt steht, werden diese in die Standardwerte für das Dateiformat geändert. Die folgenden Dateiformat Konstanten sind definiert:

</dd> <dt>

<span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ DGV \_ FF \_ AVI
</dt> <dd>

AVI-Format.

</dd> <dt>

<span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ avss
</dt> <dd>

Avss-Format.

</dd> <dt>

<span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI \_ DGV \_ FF \_ DIB
</dt> <dd>

DIB-Format.

</dd> <dt>

<span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ DGV \_ FF \_ jff
</dt> <dd>

Jff-Format.

</dd> <dt>

<span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI \_ DGV \_ FF \_ JPEG
</dt> <dd>

JPEG-Format.

</dd> <dt>

<span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI \_ DGV \_ FF \_ MPEG
</dt> <dd>

MPEG-Format.

</dd> <dt>

<span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ rdib
</dt> <dd>

RLE-DIB-Format.

</dd> <dt>

<span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ DGV \_ FF \_ rjpeg
</dt> <dd>

Rjpeg-Format.

</dd> <dt>

<span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI- \_ DGV- \_ Set- \_ Suche \_ genau
</dt> <dd>

Legt das für die Positionierung verwendete Format fest. Dieses Flag muss verwendet werden, wenn MCI \_ \_ auf on oder MCI Set Off festgelegt ist \_ \_ . Wenn MCI \_ für festgelegt \_ wird, wird durch die Wiedergabe oder Aufzeichnung genau auf den Frame zugegriffen, der mit dem MCI- \_ Flag from angegeben wurde. Dadurch kann es zu einer zusätzlichen Verzögerung kommen, wenn der angeforderte Frame kein Keyframe ist. Wenn MCI \_ \_ auf OFF festgelegt ist, sucht das Gerät nach einem Key-Frame-Bild, das dem angeforderten Frame vorangestellt wird. Bei einigen Dateien und Geräten ist dies möglicherweise der erste Frame der Datei. Der Standardwert für dieses Flag ist Geräte abhängig.

</dd> <dt>

<span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>MCI- \_ DGV- \_ festgelegte \_ Geschwindigkeit
</dt> <dd>

Ein Geschwindigkeitsparameter ist im **dwspeed** -Member der durch *lpset* identifizierten Struktur enthalten. Die Geschwindigkeit wird als Verhältnis zwischen der nominalen Frame Rate und der gewünschten Frame Rate angegeben, bei der die nominale frametrate als 1000 festgelegt wird. Die halbe Geschwindigkeit ist 500, und die doppelte Geschwindigkeit ist 2000. Der zulässige Geschwindigkeitsbereich ist auch abhängig vom Gerät und möglicherweise von der Datei.

</dd> <dt>

<span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>MCI- \_ DGV- \_ Satz \_ weiterhin
</dt> <dd>

Bei Verwendung mit MCI \_ DGV \_ Set \_ FileFormat legt die MCI- \_ Gruppe das für Aufzeichnungs Befehle verwendete Dateiformat fest.

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Für Digital Video-Geräte verweist der *lpset* -Parameter auf eine [**MCI- \_ DGV- \_ Set \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) -Parameter Struktur.

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp des **Sequencers** verwendet:

<dl> <dt>

<span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI-Format für das Setup- \_ \_ Format \_
</dt> <dd>

Legt das Zeitformat auf die Zeiger Einheiten des Titels fest.

</dd> <dt>

<span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI \_ Seq- \_ Satz \_ Master
</dt> <dd>

Legt den Sequencer als Quelle der Synchronisierungs Daten fest und gibt an, dass der Synchronisierungstyp im **dwmaster** -Member der durch *lpset* identifizierten Struktur angegeben wird. Mcisq gibt eine nicht unterstützte mcierr- \_ \_ Funktion zurück. Die folgenden Konstanten sind für den Synchronisierungstyp definiert:

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ -Integration \_
</dt> <dd>

Vom Sequencer werden Synchronisierungs Daten im Format "MIDI" gesendet.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI- \_ \_ SMPTE
</dt> <dd>

Vom Sequencer werden Synchronisierungs Daten im SMPTE-Format gesendet.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI-nicht verfügbar \_ \_
</dt> <dd>

Vom Sequencer werden keine Synchronisierungs Daten gesendet.

</dd> <dt>

<span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>MCI \_ Seq- \_ Satz \_ Offset
</dt> <dd>

Ändert den SMPTE-Offset einer Sequenz in den, der vom **dwOffset** -Member der durch *lpset* identifizierten-Struktur angegeben wird. Dies wirkt sich nur auf Sequenzen mit einem SMPTE-Divisions Typ aus.

</dd> <dt>

<span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>MCI \_ Seq- \_ Set- \_ Port
</dt> <dd>

Legt den Ausgabe-MIDI-Port einer Sequenz auf die fest, die durch den Typ der MIDI-Gerätekennung im **dwport** -Member der durch *lpset* identifizierten Struktur angegeben wird. Das Gerät schließt den vorherigen Port (sofern vorhanden) und versucht, den neuen Port zu öffnen und zu verwenden. Wenn dies nicht möglich ist, wird ein Fehler zurückgegeben, und der zuvor verwendete Port (sofern vorhanden) wird erneut geöffnet. Für die Ports sind die folgenden Konstanten definiert:

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI-nicht verfügbar \_ \_
</dt> <dd>

Schließt den zuvor verwendeten Port (sofern vorhanden). Der Sequencer verhält sich genau so, als ob ein Port geöffnet wäre, es sei denn, es wird eine MIDI-Nachricht gesendet.

</dd> <dt>

<span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>MIDI- \_ Mapper
</dt> <dd>

Legt den Port fest, der für den MIDI-Mapper geöffnet ist.

</dd> <dt>

<span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI \_ Seq \_ Set \_ Slave
</dt> <dd>

Legt fest, dass der Sequencer Synchronisierungs Daten empfängt, und gibt an, dass der Synchronisierungstyp im **dwslave** -Member der durch *lpset* identifizierten Struktur angegeben wird. Mcisq gibt eine nicht unterstützte mcierr- \_ \_ Funktion zurück. Die folgenden Konstanten sind für den Synchronisierungstyp definiert:

</dd> <dt>

<span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>MCI- \_ \_ Datei
</dt> <dd>

Der Sequencer wird so festgelegt, dass die Synchronisierungs Daten in der-Datei mit der Datei

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ -Integration \_
</dt> <dd>

Legt fest, dass der Sequencer Daten zur Datensynchronisierung empfängt.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI-nicht verfügbar \_ \_
</dt> <dd>

Legt fest, dass der Sequencer Synchronisierungs Daten in einem MIDI-Stream ignoriert.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI- \_ \_ SMPTE
</dt> <dd>

Legt fest, dass der Sequencer SMPTE-Synchronisierungs Daten empfängt.

</dd> <dt>

<span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI \_ Seq- \_ Set- \_ Tempo
</dt> <dd>

Ändert das Tempo der MIDI-Sequenz in, das vom **dwtempo** -Member der-Struktur angegeben wird, auf die von *lpset* gezeigt wird. Für Sequenzen mit dem Divisions Datentyp ppqn wird das Tempo in Beats pro Minute angegeben; für Sequenzen mit dem Divisions Typ SMPTE wird das Tempo in Frames pro Sekunde angegeben.

</dd> </dl>

Für Sequencer-Geräte verweist der *lpset* -Parameter auf eine [**MCI \_ Seq \_ Set \_**](mci-seq-set-parms.md) -Parameter Struktur.

Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>MCI \_ VCR \_ Set \_ \_ assemblierungsdatensatz
</dt> <dd>

Legt fest, dass das Gerät im Assemblierungs-oder Einfügemodus aufgezeichnet wird (wenn assembliert ist, INSERT auf ON festgelegt ist und umgekehrt). Verwenden Sie mit einem der folgenden Flags:

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ festgelegt \_ auf
</dt> <dd>

Legt den assemblierungsdatensatz auf fest und schaltet INSERT-Datensatz aus. Zeichnet alle Video-, Audio-und Zeit Leitzahl-Spuren auf.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI- \_ festgelegt \_
</dt> <dd>

Setzt assemblierungsdatensatz aus und schaltet INSERT-Datensatz ein. Wenn assemblierungsdatensatz auf OFF festgelegt ist, können einzelne Titel von Video, Audiodaten und Zeitcode für die Aufzeichnung ausgewählt werden.

</dd> <dt>

<span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>MCI \_ VCR- \_ festgelegte \_ Uhr
</dt> <dd>

Der **dwclock** -Member der durch *lpset* identifizierten Struktur enthält die neue Uhrzeit.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>MCI \_ VCR- \_ Satz-gegen-Satz- \_ \_ forma
</dt> <dd>

Der **dwcounter Format** -Member der durch *lpset* identifizierten-Struktur enthält eine-Konstante, die das neue vom Status Indikator zu verwendende Indikator Zeitformat angibt. Eine Liste gültiger Konstanten finden Sie unter MCI- \_ festgelegter \_ Zeit \_ Format in der Liste der zusätzlichen Flags für diesen Befehl.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>MCI \_ VCR \_ festlegen \_ des \_ Leistungs Zählers
</dt> <dd>

Der **dwcountervalue** -Member der durch *lpset* identifizierten Struktur enthält den neuen Indikator Wert.

</dd> <dt>

<span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>MCI- \_ VCR- \_ Satz \_ Index
</dt> <dd>

Der **dwIndex** -Member der durch *lpset* identifizierten Struktur enthält eine Konstante, die den Inhalt der Bildschirm Anzeige angibt und einen der folgenden Werte aufweisen muss:

</dd> <dt>

<span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>MCI- \_ VCR- \_ Index Indikator \_
</dt> <dd>

Zeigt den Counter an.

</dd> <dt>

<span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>Datum des MCI- \_ VCR- \_ Indexes \_
</dt> <dd>

Zeigt das Datum an.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>MCI- \_ VCR- \_ Index \_ Zeit
</dt> <dd>

Zeigt die Uhrzeit an.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>MCI- \_ VCR- \_ Index \_ Zeit Code
</dt> <dd>

Zeigt Timecode an.

Weitere Informationen finden Sie unter dem [MCI- \_ Index](mci-index.md) Befehl.

</dd> <dt>

<span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>MCI \_ VCR \_ Set \_ Pause \_ Timeout
</dt> <dd>

Der **dwpausetimeout** -Member der durch *lpset* identifizierten Struktur enthält die maximale Dauer eines Pause-Befehls in Millisekunden.

</dd> <dt>

<span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>MCI \_ VCR \_ Festlegen der \_ Postroll \_ Dauer
</dt> <dd>

Der **dwpostrollduration** -Member der Struktur, die von *lpset* identifiziert wird, enthält die videtape-Länge im aktuellen Zeitformat, die zum Bremsen des VCR-Transports erforderlich ist, wenn ein Befehl zum Beenden oder anhalten ausgegeben wird.

</dd> <dt>

<span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>MCI \_ VCR \_ Set \_ Power
</dt> <dd>

Legt den einschalten oder deaktivieren fest. Muss mit einem der folgenden Flags verwendet werden:

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI- \_ festgelegt \_
</dt> <dd>

Schaltet ausschalten.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ festgelegt \_ auf
</dt> <dd>

Schaltet Einschalten ein.

</dd> <dt>

<span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>Dauer der Vorabversion von MCI \_ VCR \_ festgelegt \_ \_
</dt> <dd>

Der **dwprerollduration** -Member der Struktur, die von *lpset* identifiziert wird, enthält die im aktuellen Zeitformat für die Stabilisierung der VCR-Ausgabe erforderliche videobandlänge.

</dd> <dt>

<span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>MCI \_ VCR \_ - \_ Daten Satz \_ Format festlegen
</dt> <dd>

Der **dwrecordformat** -Member der-Struktur, die von *lpset* identifiziert wird, enthält eine-Konstante, die die Daten Satz Geschwindigkeit beschreibt. diese muss eine der folgenden sein:

</dd> <dt>

<span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>MCI \_ VCR- \_ Format \_ EP
</dt> <dd>

Datensätze mit langsamer Geschwindigkeit.

</dd> <dt>

<span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>MCI \_ VCR- \_ Format- \_ LP
</dt> <dd>

Datensätze mit mittlerer und langsamer Geschwindigkeit.

</dd> <dt>

<span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI \_ VCR- \_ Format \_ SP
</dt> <dd>

Datensätze mit Standardgeschwindigkeit.

</dd> <dt>

<span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>MCI \_ VCR- \_ festgelegte \_ Geschwindigkeit
</dt> <dd>

Der **dwspeed** -Member der Struktur, die von *lpset* identifiziert wird, enthält die neue Geschwindigkeitseinstellung, wobei 1000 eine normale Geschwindigkeit, 2000 die doppelte Geschwindigkeit und 500 eine halbe Geschwindigkeit ist usw.

</dd> <dt>

<span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>MCI \_ VCR \_ festlegen \_ der \_ Bandlänge
</dt> <dd>

Der **dwtapelength** -Member der durch *lpset* identifizierten Struktur enthält die neue Bandlänge, vorausgesetzt, die Bandlänge ist nicht erkennbar.

</dd> <dt>

<span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MCI \_ VCR- \_ festgelegte \_ Zeit \_ Modus
</dt> <dd>

Der **dwtimemode** -Member der durch *lpset* identifizierten Struktur enthält eine Konstante, die den neuen Positions Zeit Modus angibt. Die folgenden Konstanten sind gültig:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI- \_ VCR- \_ Zeit ( \_ Counter)
</dt> <dd>

Erzwingt, dass das Gerät den Counter exklusiv verwendet.

</dd> <dt>

<span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>MCI- \_ VCR- \_ Zeit \_ Erkennung
</dt> <dd>

Jedes Mal, wenn ein neues Videoband in das Gerät eingefügt wird oder sich der Modus von nicht bereit in bereit befindet, sollte das Gerät versuchen, festzustellen, ob auf dem Videoband Zeitcode verfügbar ist. Wenn Zeitcode verfügbar ist, verwenden Sie Zeitcode in allen nachfolgenden Befehlen, die Positionen angeben. Andernfalls verwenden Sie den-Wert.

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI- \_ VCR- \_ Zeit ( \_ Timecode)
</dt> <dd>

Erzwingt die ausschließliche Verwendung von Zeitcode durch das Gerät.

</dd> <dt>

<span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>MCI \_ VCR-Set-nach \_ \_ Verfolgung
</dt> <dd>

Optimiert die Geschwindigkeit des VCR-Band Transports mit einer fein Anpassung und muss mit einem der folgenden Flags verwendet werden:

</dd> <dt>

<span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>MCI \_ VCR \_ Plus
</dt> <dd>

Erhöht die Band Transportgeschwindigkeit.

</dd> <dt>

<span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI \_ VCR \_ minus
</dt> <dd>

Verringert die Band Transportgeschwindigkeit.

</dd> <dt>

<span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>MCI- \_ VCR- \_ zurück Setzung
</dt> <dd>

Gibt die nach Verfolgungs Anpassung zu 0 (null) zurück.

</dd> </dl>

Bei VCR-Geräten verweist der *lpset* -Parameter auf eine [**MCI- \_ VCR- \_ Set \_**](mci-vcr-set-parms.md) -Parameter Struktur.

Das folgende zusätzliche Flag wird für den **Videodisk** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>MCI- \_ VD- \_ Format \_ Verfolgung
</dt> <dd>

Ändert das Zeitformat in nachverfolgt. MCI verwendet kontinuierliche Nachverfolgung.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **waveaudiogerätetyp** verwendet:

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI- \_ Wave- \_ Eingabe
</dt> <dd>

Legt die Eingabe fest, die für die Aufzeichnung in den **Winput** -Member der durch *lpset* identifizierten Struktur verwendet wird.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI- \_ Wave- \_ Ausgabe
</dt> <dd>

Legt die Ausgabe fest, die für die Wiedergabe mit dem **woutput** -Member der durch *lpset* identifizierten Struktur verwendet wird.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI- \_ Wellen \_ Satz \_ anyinput
</dt> <dd>

Alle mit dem aktuellen Format kompatiblen Wellen Eingaben können für die Aufzeichnung verwendet werden.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI- \_ Wellen \_ Satz \_ anyoutput
</dt> <dd>

Alle mit dem aktuellen Format kompatiblen Wellen Ausgaben können für die Wiedergabe verwendet werden.

</dd> <dt>

<span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI- \_ Wellen \_ Satz \_ avgbytespersec
</dt> <dd>

Legt die Bytes pro Sekunde fest, die zum wiedergeben, aufzeichnen und speichern in dem **navgbytespersec** -Member der durch *lpset* identifizierten Struktur verwendet werden.

</dd> <dt>

<span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>MCI- \_ Wellen \_ Satz \_ BitsPerSample
</dt> <dd>

Legt die Bits pro Stichprobe fest, die zum wiedergeben, aufzeichnen und Speichern des **nbitspersample** -Members des PCM-Datenformats verwendet werden, das von *lpset* identifiziert wird.

</dd> <dt>

<span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI- \_ Wellen \_ Satz \_ BlockAlign
</dt> <dd>

Legt die Block Ausrichtung fest, die zum Abspielen, aufzeichnen und speichern in dem **nBlockAlign** -Member der durch *lpset* identifizierten Struktur verwendet wird.

</dd> <dt>

<span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>MCI- \_ Wellen \_ Satz \_ Kanäle
</dt> <dd>

Die Anzahl der Kanäle wird im **nchannels** -Member der durch *lpset* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>MCI- \_ Wellen \_ Satz \_ Formattag
</dt> <dd>

Legt den Formattyp fest, der zum Abspielen, aufzeichnen und speichern im **wformattag** -Member der durch *lpset* identifizierten Struktur verwendet wird. Durch angeben \_ des Wave-Formats \_ PCM wird das Format in PCM geändert.

</dd> <dt>

<span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>MCI- \_ Wellen \_ Satz \_ samplespersec
</dt> <dd>

Legt die Stichproben pro Sekunde fest, die für die Wiedergabe, Aufzeichnung und Speicherung in dem **nsamplespersec** -Member der durch *lpset* identifizierten Struktur verwendet werden.

</dd> </dl>

Bei Waveform-Audiogeräten verweist der *lpset* -Parameter auf eine [**MCI- \_ Wellen \_ Satz \_**](mci-wave-set-parms.md) -Parameter Struktur.

Wenn die Datei zum Speichern der Daten erstellt wird, werden mehrere Eigenschaften von Waveform-Audiodaten definiert. Diese Eigenschaften beschreiben, wie die Daten innerhalb der Datei strukturiert sind und nicht geändert werden können, wenn die Aufzeichnung beginnt. Die folgenden Eigenschaften werden in der folgenden Liste von Flags identifiziert:

-   MCI- \_ Wellen \_ Satz \_ avgbytespersec
-   MCI- \_ Wellen \_ Satz \_ BitsPerSample
-   MCI- \_ Wellen \_ Satz \_ BlockAlign
-   MCI- \_ Wellen \_ Satz \_ Kanäle
-   MCI- \_ Wellen \_ Satz \_ Formattag
-   MCI- \_ Wellen \_ Satz \_ samplespersec

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

 

