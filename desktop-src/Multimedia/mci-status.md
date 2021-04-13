---
title: MCI_STATUS Befehl (MMSYSTEM. h)
description: Der MCI- \_ Status Befehl ruft Informationen zu einem MCI-Gerät ab. Alle Geräte erkennen diesen Befehl. Informationen werden im dwreturn-Member der Struktur zurückgegeben, die durch den lpstatus-Parameter identifiziert wird.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- MCI_STATUS Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_STATUS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86553ac759a362c1ea4abb53a47d0e9376cbc526
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2021
ms.locfileid: "104350689"
---
# <a name="mci_status-command"></a>Befehl "MCI- \_ Status"

> [!NOTE]
> Bias-freie Kommunikation Microsoft unterstützt eine unterschiedlichste und inklusive Umgebung.  In diesem Dokument sind Verweise auf das Wort "Slave" vorhanden. Im [Stil Handbuch von Microsoft für die Bias-Free-Kommunikation](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) wird dies als ausschließendes Wort erkannt.  Dieser Wortlaut wird verwendet, da es sich zurzeit um den in den Befehlen verwendeten Wortlaut handelt. Aus Konsistenz Gründen enthält dieses Dokument dieses Wort. Wenn dieses Wort in den Befehlen geändert wird, korrigieren wir dieses Dokument als Ausrichtung.

Der MCI- \_ Status Befehl ruft Informationen zu einem MCI-Gerät ab. Alle Geräte erkennen diesen Befehl. Informationen werden im **dwreturn** -Member der Struktur zurückgegeben, die durch den *lpstatus* -Parameter identifiziert wird.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STATUS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_STATUS_PARMS) lpStatus
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

<span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpstatus*
</dt> <dd>

Zeiger auf eine [**MCI \_ - \_ statusparametstruktur**](mci-status-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Standard-und Befehls spezifischen Flags gelten für alle Geräte, die den MCI-Status unterstützen \_ :

<dl> <dt>

<span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>MCI- \_ Status \_ Element
</dt> <dd>

Gibt an, dass der **dwitem** -Member der durch *lpstatus* identifizierten Struktur eine Konstante enthält, die das abzurufende Status Element angibt. Die folgenden Konstanten definieren, welches Status Element im **dwreturn** -Member der-Struktur zurückgegeben werden soll:

MCI- \_ Status, \_ aktueller \_ Titel

Der **dwreturn** -Member wird auf die aktuelle Nachverfolgung festgelegt. MCI verwendet kontinuierliche Nachverfolgung.

MCI- \_ Status \_ Länge

Der **dwreturn** -Member ist auf die Gesamt Medien Länge festgelegt.

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI- \_ Status \_ Modus
</dt> <dd>

Der **dwreturn** -Member ist auf den aktuellen Modus des Geräts festgelegt. Die Modi umfassen Folgendes:

-   MCI- \_ Modus \_ nicht \_ bereit
-   MCI- \_ Modus anhalten \_
-   MCI- \_ Modus \_ abspielen
-   MCI- \_ Modus wird \_ beendet
-   MCI- \_ Modus \_ geöffnet
-   MCI- \_ Modus- \_ Datensatz
-   MCI- \_ Modus- \_ Suche

</dd> <dt>

<span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>MCI- \_ Status \_ Anzahl \_ von \_ Spuren
</dt> <dd>

Der **dwreturn** -Member ist auf die Gesamtzahl der Wiedergabe baren Spuren festgelegt.

</dd> <dt>

<span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>MCI- \_ Status \_ Position
</dt> <dd>

Der **dwreturn** -Member wird auf die aktuelle Position festgelegt.

</dd> <dt>

<span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>MCI- \_ Status ist \_ bereit
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät bereit ist. Andernfalls wird **false** festgelegt.

</dd> <dt>

<span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>MCI- \_ Status \_ Zeit \_ Format
</dt> <dd>

Der **dwreturn** -Member wird auf das aktuelle Zeitformat des Geräts festgelegt. Zu den Zeitformaten gehören:

-   MCI- \_ Format ( \_ Bytes)
-   MCI- \_ Formatierungs \_ Frames
-   MCI- \_ Format \_ HMS
-   MCI- \_ Format ( \_ Millisekunden)
-   MCI- \_ Format \_ MSF
-   MCI- \_ Format \_ Beispiele
-   MCI- \_ Format- \_ TMSF

</dd> <dt>

<span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>MCI- \_ Status \_ Start
</dt> <dd>

Ruft die Anfangsposition des Mediums ab. Um die Anfangsposition abzurufen, kombinieren Sie dieses Flag mit dem MCI \_ \_ -Status Element, und legen Sie das **dwitem** -Member der durch *lpstatus* identifizierten Struktur auf die MCI- \_ Status Position fest \_ .

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>MCI- \_ Track
</dt> <dd>

Gibt an, dass ein Status Nachverfolgung-Parameter im **dwtrack** -Member der durch *lpstatus* identifizierten Struktur enthalten ist. Sie müssen dieses Flag mit der MCI- \_ Status \_ Position oder den MCI- \_ Status \_ Längen Konstanten verwenden. Bei Verwendung mit der MCI- \_ Status \_ Position erhält die MCI- \_ Verfolgung die Anfangs Position des angegebenen Titels. Bei Verwendung mit der MCI- \_ Status \_ Länge erhält die MCI-nach \_ Verfolgung die Länge des angegebenen Titels. MCI verwendet kontinuierliche Nachverfolgung.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp **CDAudio** verwendet. Diese Konstanten werden im **lengertem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.

<dl> <dt>

<span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>MCI- \_ CDA- \_ \_ Statustyp \_ Verfolgung
</dt> <dd>

Der **dwreturn** -Member ist auf einen der folgenden Werte festgelegt:

-   MCI \_ \_ -CDA \_ -trackaudiodatei
-   MCI-CDA-nach \_ \_ Verfolgung \_ anderer

Um dieses Flag zu verwenden, muss das MCI \_ -trackflag festgelegt werden, und das **dwtrack** -Element der durch *lpstatus* identifizierten Struktur muss eine gültige Nachverfolgung enthalten.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI- \_ Status \_ Medien \_ vorhanden
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn die Medien in das Gerät eingefügt werden. Andernfalls wird **false** festgelegt.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>MCI \_ DGV- \_ Status \_ diskspace
</dt> <dd>

Der **lpstraudrive** -Member der Struktur, die von *lpstatus* identifiziert wird, gibt ein Laufwerk oder in einigen Implementierungen einen Pfad an. Der MCI- \_ Status Befehl gibt die ungefähre Menge an Speicherplatz zurück, die durch den [MCI- \_ Reserve](mci-reserve.md) Befehl im **dwreturn** -Member der durch *lpstatus* identifizierten Struktur abgerufen werden kann. Der Speicherplatz wird in Einheiten des aktuellen Zeit Formats gemessen.

</dd> <dt>

<span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>MCI- \_ DGV- \_ Status \_ Eingabe
</dt> <dd>

Die vom **lengertem** -Member der durch *lpstatus* identifizierte-Konstante gilt für die Eingabe.

</dd> <dt>

<span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>MCI- \_ DGV- \_ Status \_ Links
</dt> <dd>

Die vom **lengertem** -Member der durch *lpstatus* identifizierte-Konstante gilt für den linken Audiokanal.

</dd> <dt>

<span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>MCI \_ DGV- \_ Status \_ nominell
</dt> <dd>

Die durch den **lengertem** -Member der-Struktur angegebene Konstante, die von *lpstatus* identifiziert wird, fordert den nominalen Wert anstelle des aktuellen Werts an.

</dd> <dt>

<span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>MCI- \_ DGV- \_ Status \_ Ausgabe
</dt> <dd>

Die vom **lengertem** -Member der durch *lpstatus* identifizierte-Konstante gilt für die Ausgabe.

</dd> <dt>

<span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>MCI- \_ DGV- \_ Status \_ Daten Satz
</dt> <dd>

Die für das MCI \_ DGV-statusraten-Flag zurückgegebene Frame Rate \_ \_ \_ ist die für die Komprimierung verwendete Rate.

</dd> <dt>

<span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>MCI \_ DGV- \_ Status \_ Referenz
</dt> <dd>

Der **dwreturn** -Member der Struktur, die von *lpstatus* identifiziert wird, gibt das nächste Keyframe-Bild zurück, das dem im **dwreference** -Member angegebenen Frame vorangestellt ist.

</dd> <dt>

<span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>MCI- \_ DGV- \_ Status \_ Recht
</dt> <dd>

Die vom **lengertem** -Member der durch *lpstatus* identifizierte-Konstante gilt für den richtigen Audiokanal.

</dd> </dl>

Die folgenden Konstanten werden mit dem **Digitalvideo** -Gerätetyp im **dwitem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.

<dl> <dt>

<span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>MCI \_ \_ -AVI \_ -Status- \_ audioumbrüche
</dt> <dd>

Der **dwreturn** -Member gibt an, wie oft der Audioteil der letzten AVI-Sequenz abgebrochen wurde. Das System zählt immer dann eine audiopause, wenn versucht wird, Audiodaten in den Gerätetreiber zu schreiben und feststellt, dass der Treiber bereits alle verfügbaren Daten wiedergegeben hat. Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.

</dd> <dt>

<span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>MCI \_ AVI- \_ Status \_ Frames \_ übersprungen
</dt> <dd>

Der **dwreturn** -Member gibt die Anzahl der Frames zurück, die beim Abspielen der letzten AVI-Sequenz nicht gezeichnet wurden. Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.

</dd> <dt>

<span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>MCI \_ AVI \_ Status \_ Letzte \_ Wiedergabe \_ Geschwindigkeit
</dt> <dd>

Der **dwreturn** -Member gibt einen Wert zurück, der angibt, wie genau die tatsächliche Wiedergabezeit der letzten AVI-Sequenz mit der Ziel Wiedergabezeit übereinstimmt. Der Wert 1000 gibt an, dass die Zielzeit und die tatsächliche zeitgleich sind. Der Wert 2000 gibt z. b. an, dass die AVI-Sequenz zweimal so lange gedauert hat, wie Sie vorhanden sein sollte. Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>MCI \_ DGV \_ \_ -statusaudiodatei
</dt> <dd>

Der **dwreturn** -Member gibt MCI \_ on oder MCI \_ aus, abhängig von der aktuellen MCI \_ Set \_ -Audiooption für den [MCI \_ Set](mci-set.md) -Befehl. Sie gibt MCI \_ für zurück, wenn entweder oder beide Redner aktiviert sind, andernfalls MCI \_ .

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>MCI \_ \_ -DGV \_ -Status- \_ Audioeingabe
</dt> <dd>

Der **dwreturn** -Member gibt die ungefähre sofortige Audioebene des analogen Audiosignals zurück. Ein Wert größer als 1000 impliziert, dass eine clippingverzerrung vorliegt. Einige Geräte können diesen Wert nur beim Aufzeichnen von Audiodaten bestimmen. Diesem Statuswert ist kein zugeordneter **MCI- \_ Satz** oder [MCI \_ -setaudiobefehl](mci-setaudio.md) zugeordnet. Dieser Wert bezieht sich auf die MCI-Wave-Status Ebene des Waveform-audiobefehls, die jedoch anders normalisiert ist \_ \_ \_ .

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>MCI \_ \_ -DGV \_ -Status- \_ audiodatensatz
</dt> <dd>

Der **dwreturn** -Member gibt MCI \_ on oder MCI off zurück, wobei \_ der Status des MCI \_ DGV \_ \_ setaudiodatensatz-Flags des **MCI \_ setaudiobefehls** festgelegt wird.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>MCI \_ \_ -DGV \_ -statusaudioquelle \_
</dt> <dd>

Der **dwreturn** -Member gibt die aktuelle audiodigitalisierungs Quelle zurück:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MCI- \_ DGV \_ - \_ setaudiodurchschnitt
</dt> <dd>

Gibt den Durchschnitt des linken und rechten Audiokanals an.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ \_ setaudiolinks
</dt> <dd>

Gibt den linken Audiokanal an.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ \_ setaudioright
</dt> <dd>

Gibt den richtigen Audiokanal an.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ DGV \_ \_ setaudiostereo
</dt> <dd>

Gibt Stereo an.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>MCI \_ \_ -DGV \_ -statusaudiostream \_
</dt> <dd>

Der **dwreturn** -Member gibt die aktuelle audiostreamnummer zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI \_ DGV- \_ Status \_ avgbytespersec
</dt> <dd>

Der **dwreturn** -Member gibt die durchschnittliche Anzahl der Bytes zurück, die pro Sekunde für die Aufzeichnung verwendet werden.

</dd> <dt>

<span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>MCI \_ DGV- \_ Status- \_ Bass
</dt> <dd>

Der **dwreturn** -Member gibt die aktuelle audiobass-Ebene zurück. Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>MCI \_ DGV- \_ Status \_ BitsPerPel
</dt> <dd>

Das **dwreturn** -Element gibt die Anzahl der Bits pro Pixel zurück, die zum Speichern von aufgezeichneten oder aufgezeichneten Daten verwendet werden.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI \_ DGV- \_ Status \_ BitsPerSample
</dt> <dd>

Das **dwreturn** -Element gibt die Anzahl der Bits pro Stichprobe zurück, die vom Gerät für die Aufzeichnung verwendet werden. Dies gilt nur für Geräte, die das PCM-Format unterstützen.

</dd> <dt>

<span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI- \_ DGV- \_ Status \_ BlockAlign
</dt> <dd>

Der **dwreturn** -Member gibt die Ausrichtung von Datenblöcken relativ zum Anfang der Eingabe Wellenform zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>MCI- \_ DGV- \_ Status \_ Helligkeit
</dt> <dd>

Der **dwreturn** -Member gibt die aktuelle videohelligkeits Ebene zurück. Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.

</dd> <dt>

<span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>MCI \_ DGV- \_ Status \_ Farbe
</dt> <dd>

Der **dwreturn** -Member gibt die aktuelle Farb Ebene zurück. Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.

</dd> <dt>

<span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>MCI- \_ DGV- \_ Status \_ Kontrast
</dt> <dd>

Der **dwreturn** -Member gibt die aktuelle Kontrast Ebene zurück. Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI \_ DGV- \_ Status \_ Dateiformat
</dt> <dd>

Der **dwreturn** -Member gibt das aktuelle Dateiformat für die Aufzeichnung oder Speicherung zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MCI- \_ DGV- \_ Status \_ Datei \_ Modus
</dt> <dd>

Der **dwreturn** -Member gibt den Status des Datei Vorgangs zurück:

MCI- \_ DGV- \_ dateimodusbearbeitung \_ \_

Wird beim Ausschneiden, kopieren, löschen, einfügen und rückgängig-Vorgängen zurückgegeben.

MCI- \_ DGV- \_ Datei \_ Modus im \_ Leerlauf

Wird zurückgegeben, wenn die Datei für den nächsten Vorgang bereit ist.

MCI- \_ DGV- \_ Datei \_ Modus wird \_ geladen

Wird beim Laden der Datei zurückgegeben.

MCI- \_ DGV- \_ Datei \_ Modus \_ Speichern

Wird zurückgegeben, während die Datei gespeichert wird.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>MCI- \_ DGV- \_ Status \_ Datei \_ Abschluss
</dt> <dd>

Der **dwreturn** -Member gibt den geschätzten Prozentsatz für das Laden, speichern, erfassen, Ausschneiden, kopieren, löschen, einfügen oder Rückgängig-Vorgang aus. (Anwendungen können dies verwenden, um einen visuellen Indikator für den Fortschritt bereitzustellen.) Dieses Flag wird nicht von allen Digital-Video-Geräten unterstützt.

</dd> <dt>

<span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>MCI- \_ DGV- \_ Status \_ Vorwärts
</dt> <dd>

Der **dwreturn** -Member gibt **true** zurück, wenn die Geräte Richtung vorwärts oder das Gerät nicht wiedergegeben wird.

</dd> <dt>

<span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>MCI \_ DGV- \_ Status- \_ Frame \_ Rate
</dt> <dd>

Das **dwreturn** -Element muss mit dem MCI \_ DGV- \_ Status " \_ nominell", dem MCI \_ DGV- \_ Status \_ Daten Satz oder beidem verwendet werden. Bei der Verwendung mit dem MCI \_ DGV- \_ Status \_ Daten Satz wird die aktuelle für die Aufzeichnung verwendete Frame Rate zurückgegeben. Bei Verwendung mit dem MCI \_ DGV \_ \_ -Statusdaten Satz und dem MCI \_ DGV-Status " \_ \_ nominell" wird die nominale Frame Rate zurückgegeben, die dem Eingabe Videosignal zugeordnet ist. Bei Verwendung mit \_ dem nominalen MCI DGV- \_ Status \_ wird die der Datei zugeordnete nominale Frame Rate zurückgegeben. In allen Fällen werden die Einheiten in Frames pro Sekunde multipliziert mit 1000.

</dd> <dt>

<span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>MCI \_ DGV- \_ Status \_ Gamma
</dt> <dd>

Der **dwreturn** -Member gibt den aktuellen Gamma Wert zurück. Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.

</dd> <dt>

<span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI- \_ DGV- \_ Status- \_ hpal
</dt> <dd>

Der **dwreturn** -Member gibt den ASCII-Dezimalwert für das aktuelle Palettenhandle zurück. Das Handle ist im nieder wertigen Wort des zurückgegebenen Werts enthalten.

</dd> <dt>

<span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>MCI \_ DGV- \_ Status- \_ HWND
</dt> <dd>

Der **dwreturn** -Member gibt den ASCII-Dezimalwert für das aktuelle explizite oder Standardfenster Handle zurück, das dieser Gerätetreiber Instanz zugeordnet ist. Das Handle ist im nieder wertigen Wort des zurückgegebenen Werts enthalten.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>MCI- \_ DGV- \_ Status \_ Schlüssel \_ Farbe
</dt> <dd>

Der **dwreturn** -Member gibt den aktuellen Schlüssel Farbwert zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>MCI- \_ DGV- \_ Status \_ Schlüssel \_ Index
</dt> <dd>

Der **dwreturn** -Member gibt den aktuellen Schlüssel Index Wert zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>Monitor für den MCI- \_ DGV- \_ Status \_
</dt> <dd>

Der **dwreturn** -Member gibt eine Konstante zurück, die die Quelle der aktuellen Präsentation angibt. Die folgenden Konstanten sind definiert:

MCI- \_ DGV- \_ Monitor \_ Datei

Eine Datei ist die Quelle.

MCI- \_ DGV- \_ Monitor \_ Eingabe

Die Eingabe ist die Quelle.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>MCI \_ DGV- \_ Status \_ Monitor- \_ Methode
</dt> <dd>

Der **dwreturn** -Member gibt eine Konstante zurück, die die für die Eingabe Überwachung verwendete Methode angibt. Die folgenden Konstanten sind definiert:

MCI \_ DGV- \_ Methode \_ Direct

Direkte Eingabe Überwachung.

MCI \_ DGV- \_ Methoden \_ Beitrag

Überwachung nach der Eingabe.

MCI \_ DGV- \_ Methode \_ vor

Überwachung vor der Eingabe.

</dd> <dt>

<span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MCI- \_ DGV- \_ Status \_ Pausen \_ Modus
</dt> <dd>

Der **dwreturn** -Member gibt die Wiedergabe des MCI \_ -Modus zurück, \_ Wenn das Gerät während der Wiedergabe angehalten wurde, und gibt den MCI- \_ Modus- \_ Datensatz zurück Der Befehl gibt die nicht anwendbare mcierr- \_ \_ Funktion als Fehlerrückgabe zurück, wenn das Gerät nicht angehalten wurde.

</dd> <dt>

<span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI \_ DGV- \_ Status \_ SamplesPerSecond
</dt> <dd>

Das **dwreturn** -Element gibt die Anzahl der Stichproben pro Sekunde zurück, die aufgezeichnet wurden.

</dd> <dt>

<span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI \_ DGV- \_ Status \_ Suche \_ genau
</dt> <dd>

Der **dwreturn** -Member gibt **true** oder **false** zurück, um anzugeben, ob das Such genaue Format festgelegt ist. (Anwendungen können dieses Format mithilfe des Befehls [MCI Set \_ ](mci-set.md) mit dem Flag MCI \_ DGV \_ Set \_ Seek exakt festlegen \_ .)

</dd> <dt>

<span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>MCI \_ DGV- \_ Status \_ Schärfe
</dt> <dd>

Der **dwreturn** -Member gibt die aktuelle Schärfe Ebene zurück. Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.

</dd> <dt>

<span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>MCI- \_ DGV- \_ Status \_ Größe
</dt> <dd>

Der **dwreturn** -Member gibt die ungefähre Wiedergabedauer von komprimierten Daten zurück, die der reservierte Arbeitsbereich enthalten wird. Die Dauer Einheiten liegen im aktuellen Zeitformat vor. Wenn kein reservierter Speicherplatz vorhanden ist, wird NULL zurückgegeben. Die zurückgegebene Größe ist ungefähre Werte, da der genaue Speicherplatz für komprimierte Daten im allgemeinen erst vorhergesagt werden kann, nachdem die Daten komprimiert wurden.

</dd> <dt>

<span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI- \_ DGV- \_ Status ( \_ SMPTE)
</dt> <dd>

Der **dwreturn** -Member gibt den SMPTE-Zeit Code zurück, der der aktuellen Position im Arbeitsbereich zugeordnet ist.

</dd> <dt>

<span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>MCI \_ DGV- \_ Status \_ Geschwindigkeit
</dt> <dd>

Der **dwreturn** -Member gibt die aktuelle Wiedergabegeschwindigkeit zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>MCI- \_ DGV- \_ Status \_ weiterhin \_ Fileformat
</dt> <dd>

Der **dwreturn** -Member gibt das aktuelle Dateiformat für den [MCI- \_ Erfassungs](mci-capture.md) Befehl zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>MCI \_ DGV- \_ Status \_ tint
</dt> <dd>

Der **dwreturn** -Member gibt die aktuelle Video-Tönungs-Ebene zurück. Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.

</dd> <dt>

<span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI- \_ DGV- \_ Status \_ Treble
</dt> <dd>

Der **dwreturn** -Member gibt die aktuelle audiotreble-Ebene zurück. Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.

</dd> <dt>

<span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>MCI- \_ DGV- \_ Status \_ nicht gespeichert
</dt> <dd>

Der **dwreturn** -Member gibt **true** zurück, wenn im Arbeitsbereich aufgezeichnete Daten verloren gehen, die als Ergebnis eines [MCI \_](mci-close.md)-Schließ Vorgangs, einer [MCI- \_ Auslastung](mci-load.md), eines [MCI-Daten \_ Satzes](mci-record.md), einer [MCI- \_ Reserve](mci-reserve.md), eines [MCI- \_ Ausschnitts](mci-cut.md), einer [MCI- \_ Delete](mci-delete.md)-oder einer [MCI \_](mci-paste.md) -Befehls Der Member gibt andernfalls **false** zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>Video zum MCI- \_ DGV- \_ Status \_
</dt> <dd>

Der **dwreturn** -Member gibt MCI in zurück, \_ Wenn das Video aktiviert ist, oder \_ Wenn es deaktiviert ist.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>MCI- \_ DGV- \_ Status- \_ Video \_ Daten Satz
</dt> <dd>

Der **dwreturn** -Member gibt MCI \_ on oder MCI \_ Off zurück und gibt den Status an, der vom MCI \_ DGV \_ setvideo-Datensatz- \_ Flag des Befehls [MCI \_ setvideo](mci-setvideo.md) festgelegt wird.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>MCI- \_ DGV- \_ Status- \_ Video \_ Quelle
</dt> <dd>

Der **dwreturn** -Member gibt eine Konstante zurück, die den Typ der Videoquelle angibt, die vom MCI \_ DGV \_ setvideo \_ Source-Flag des **MCI \_ setvideo** -Befehls festgelegt wurde.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI \_ DGV- \_ Status \_ Video \_ src \_ NUM
</dt> <dd>

Der **dwreturn** -Member gibt die Zahl innerhalb seines Typs der derzeit aktiven Videoeingabe Quelle zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>MCI- \_ DGV- \_ Status- \_ \_ Videostream
</dt> <dd>

Der **dwreturn** -Member gibt die aktuelle videostreamnummer zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>MCI \_ DGV \_ - \_ statusvolume
</dt> <dd>

Der **dwreturn** -Member gibt den Durchschnitt des Volumes an den linken und den rechten Redner zurück. Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>MCI- \_ DGV- \_ Status \_ Fenster \_ sichtbar
</dt> <dd>

Der **dwreturn** -Member gibt **true** zurück, wenn das Fenster nicht ausgeblendet ist.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>MCI- \_ DGV- \_ Status \_ Fenster \_ minimiert
</dt> <dd>

Der **dwreturn** -Member gibt **true** zurück, wenn das Fenster minimiert wird.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>MCI- \_ DGV- \_ Status \_ Fenster \_ maximiert
</dt> <dd>

Der **dwreturn** -Member gibt **true** zurück, wenn das Fenster maximiert ist.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI- \_ Status \_ Medien \_ vorhanden
</dt> <dd>

Der **dwreturn** -Member gibt **true** zurück.

</dd> </dl>

Für Digital Video-Geräte zeigt der *lpstatus* -Parameter auf eine [**MCI \_ DGV- \_ statusparameterstruktur \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) .

Die folgenden zusätzlichen Flags werden beim **Sequencer** -Gerätetyp verwendet. Diese Konstanten werden im **lengertem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.

<dl> <dt>

<span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI- \_ \_ Statustyp "Status \_ "
</dt> <dd>

Der **dwreturn** -Member wird auf einen der folgenden Werte festgelegt, der den aktuellen Divisions Typ einer Sequenz angibt:

-   MCI \ \_ \_ div \_ ppqn
-   MCI \ \_ \_ div \_ SMPTE \_ 24
-   MCI Server \_ \_ div \_ SMPTE \_ 25
-   MCI Server \_ \_ div \_ SMPTE \_ 30
-   MCI-Server \ \_ \_ div \_ SMPTE \_ 30drop

</dd> <dt>

<span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MCI- \_ \_ Status \_ Master
</dt> <dd>

Der **dwreturn** -Member ist auf den für den Master Vorgang verwendeten Synchronisierungstyp festgelegt.

</dd> <dt>

<span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>Status Offset für MCI- \_ \_ Status \_
</dt> <dd>

Der **dwreturn** -Member wird auf den aktuellen SMPTE-Offset einer Sequenz festgelegt.

</dd> <dt>

<span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>MCI- \_ \_ \_ Statusport
</dt> <dd>

Der **dwreturn** -Member wird für den aktuellen Port, der von der Sequenz verwendet wird, auf den-ID-Geräte Bezeichner festgelegt

</dd> <dt>

<span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI- \_ \_ Status- \_ Slave
</dt> <dd>

Der **dwreturn** -Member ist auf den Synchronisierungstyp festgelegt, der für den untergeordneten Vorgang verwendet

</dd> <dt>

<span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI- \_ \_ Status \_ Tempo
</dt> <dd>

Der **dwreturn** -Member wird auf das aktuelle Tempo einer MIDI-Sequenz in Beats pro Minute für ppqn-Dateien oder Frames pro Sekunde für SMPTE-Dateien festgelegt.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI- \_ Status \_ Medien \_ vorhanden
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn die Medien in das Gerät eingefügt werden. Andernfalls wird **false** festgelegt.

</dd> </dl>

Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet. Diese Konstanten werden im **lengertem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI- \_ Status \_ Medien \_ vorhanden
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn die Medien in das Gerät eingefügt werden. Andernfalls wird **false** festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>MCI- \_ VCR- \_ Status assemblierungsdatensatz \_ \_
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn der Assemblierungs Modus auf Andernfalls wird **false** festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>Monitor für den MCI \_ -VCR \_ \_ -Status \_
</dt> <dd>

Der **dwreturn** -Member wird auf eine Konstante festgelegt, die den derzeit ausgewählten audiomonitortyp angibt.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>MCI \_ \_ -VCR \_ -Status- \_ audiomonitor- \_ Nummer
</dt> <dd>

Das **dwreturn** -Element wird auf die Nummer des aktuell ausgewählten audiomonitortyps festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>MCI \_ \_ -VCR \_ -statusaudiodatensatz \_
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn Audiodaten aufgezeichnet werden, wenn der nächste Datensatz-Befehl angegeben wird. Andernfalls wird **false** festgelegt. Wenn Sie MCI \_ Track im *dwFlags* -Parameter dieses Befehls angeben, enthält **dwtrack** den Track, auf den diese Abfrage angewendet wird.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>MCI \_ VCR \_ \_ - \_ statusaudioquelle
</dt> <dd>

Der **dwreturn** -Member wird auf eine Konstante festgelegt, die den aktuellen audioquellentyp angibt.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>MCI \_ \_ -VCR \_ -Status- \_ \_ audioquellnummer
</dt> <dd>

Der **dwreturn** -Member wird auf die Nummer des derzeit ausgewählten audioquelltyps festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>MCI \_ VCR \_ - \_ statusuhr
</dt> <dd>

Der **dwreturn** -Member ist auf den aktuellen Uhrwert festgelegt, und zwar in den Schritten der gesamten Uhr.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>MCI \_ VCR \_ - \_ statusclock- \_ ID
</dt> <dd>

Der **dwreturn** -Member ist auf eine Zahl festgelegt, die die verwendete Uhr eindeutig beschreibt.

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>MCI \_ VCR- \_ Status- \_ counter- \_ Format
</dt> <dd>

Das **dwreturn** -Element wird auf eine Konstante festgelegt, die das aktuelle Leistungs Muster beschreibt. Weitere Informationen finden Sie unter MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>Auflösung des MCI \_ VCR- \_ Status \_ Zählers \_
</dt> <dd>

Der **dwreturn** -Member ist auf eine Konstante festgelegt, die die Auflösung des Zählers beschreibt, und ist einer der folgenden Werte:

-   MCI- \_ VCR- \_ counter- \_ \_ Frames: der Counter hat eine Auflösung von Frames.
-   MCI- \_ VCR- \_ counter- \_ \_ Sekunden: der Counter hat eine Auflösung von Sekunden.
-   Wert des MCI- \_ VCR- \_ Status \_ Zählers \_ : das **dwreturn** -Element wird im aktuellen Zeit-/Uhrzeitformat auf den aktuellen Lesezeichen Wert festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>MCI- \_ VCR- \_ Status- \_ Frame \_ Rate
</dt> <dd>

Der **dwreturn** -Member wird auf die aktuelle systemeigene Framerate des Geräts festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>MCI- \_ VCR- \_ Status \_ Index
</dt> <dd>

Der **dwreturn** -Member ist auf eine Konstante festgelegt, die den aktuellen Inhalt der Bildschirm Anzeige beschreibt und eine der folgenden Elemente ist:

-   MCI- \_ VCR- \_ Index Indikator \_
-   Datum des MCI- \_ VCR- \_ Indexes \_
-   MCI- \_ VCR- \_ Index \_ Zeit
-   MCI- \_ VCR- \_ Index \_ Zeit Code

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>MCI \_ VCR- \_ Status \_ Index \_ on
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn die Bildschirm Anzeige auf ON festgelegt ist. Andernfalls wird **false** festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>MCI- \_ VCR- \_ \_ statusmedientyp \_
</dt> <dd>

Der **dwreturn** -Member ist auf einen der folgenden Elemente festgelegt:

-   MCI \_ VCR- \_ Medien \_ 8mm
-   MCI \_ VCR- \_ Medien \_ Hi8
-   MCI \_ VCR \_ Media \_ VHS
-   MCI \_ VCR- \_ Medien \_ SVHS
-   MCI \_ VCR- \_ Medien \_ Beta
-   MCI \_ VCR- \_ Medien ( \_ edbeta)
-   anderes MCI \_ VCR- \_ Medium \_

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>MCI- \_ VCR- \_ Status \_ Nummer
</dt> <dd>

Das **dwnumber** -Element wird auf die logische gatewaynummer festgelegt, wenn Sie dieses Flag mit dem MCI \_ VCR- \_ Status-Tuner- \_ \_ kanalflag verwenden.

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>MCI \_ \_ -VCR \_ -Status Anzahl \_ von \_ \_ Audiospuren
</dt> <dd>

Das **dwreturn** -Element wird auf die Anzahl der Audiospuren festgelegt, die unabhängig ausgewählt werden können.

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>MCI \_ VCR- \_ Status \_ Anzahl \_ von \_ Video \_ Spuren
</dt> <dd>

Das **dwreturn** -Element wird auf die Anzahl der Videospuren festgelegt, die unabhängig ausgewählt werden können.

</dd> <dt>

<span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>MCI \_ VCR- \_ Status \_ Pause \_ Timeout
</dt> <dd>

Der **dwreturn** -Member wird auf die maximale Dauer eines Pause-Befehls in Millisekunden festgelegt. Der Rückgabewert 0 (null) gibt an, dass kein Timeout auftritt.

</dd> <dt>

<span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>MCI \_ VCR- \_ Status \_ Wiedergabe \_ Format
</dt> <dd>

Der **dwreturn** -Member ist auf einen der folgenden Elemente festgelegt:

-   MCI \_ VCR- \_ Format \_ EP
-   MCI \_ VCR- \_ Format- \_ LP
-   anderes MCI \_ VCR- \_ Format \_
-   MCI \_ VCR- \_ Format \_ SP

</dd> <dt>

<span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>Dauer des MCI \_ VCR- \_ Status \_ Postroll \_
</dt> <dd>

Der **dwreturn** -Member wird auf die Länge des Videobands festgelegt, das nach dem Ende der Position im aktuellen Zeitformat wiedergegeben wird. Dies ist erforderlich, um den VCR-Band Transport von einem Befehl zum Anhalten oder anhalten zu unterbrechen.

</dd> <dt>

<span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>MCI- \_ VCR- \_ Status \_ Einschalten \_
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn die Stromversorgung ist. Andernfalls wird **false** festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>Dauer der Vorabversion des MCI \_ VCR- \_ Status \_ \_
</dt> <dd>

Das **dwreturn** -Element wird auf die Länge des Videobands festgelegt, das vor dem Start Ende im aktuellen Zeitformat wiedergegeben wird. Dies ist erforderlich, um die VCR-Ausgabe zu stabilisieren.

</dd> <dt>

<span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>MCI \_ VCR- \_ Status \_ Daten Satz \_ Format
</dt> <dd>

Der **dwreturn** -Member ist auf einen der folgenden Elemente festgelegt:

-   MCI \_ VCR- \_ Format \_ EP
-   MCI \_ VCR- \_ Format- \_ LP
-   anderes MCI \_ VCR- \_ Format \_
-   MCI \_ VCR- \_ Format \_ SP

</dd> <dt>

<span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>MCI- \_ VCR- \_ Status \_ Geschwindigkeit
</dt> <dd>

Der **dwreturn** -Member ist auf die aktuelle Geschwindigkeit festgelegt. Weitere Informationen finden Sie unter MCI \_ VCR \_ Set \_ Speed-Flag des Befehls [MCI \_ Set](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MCI- \_ VCR- \_ Status \_ Zeit \_ Modus
</dt> <dd>

Der **dwreturn** -Member ist auf einen der folgenden Elemente festgelegt:

-   MCI- \_ VCR- \_ Zeit ( \_ Counter)
-   MCI- \_ VCR- \_ Zeit \_ Erkennung
-   MCI- \_ VCR- \_ Zeit ( \_ Timecode)

Weitere Informationen finden Sie im MCI \_ VCR \_ Set \_ time Mode- \_ Flag des Befehls [MCI \_ Set](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>MCI- \_ VCR- \_ Status- \_ \_ Zeittyp
</dt> <dd>

Das **dwreturn** -Element wird auf eine Konstante festgelegt, die den verwendeten aktuellen Zeittyp beschreibt (wird von [Play](play.md), [Record](record.md), [Seek](seek.md)usw. verwendet) und ist einer der folgenden:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI- \_ VCR- \_ Zeit ( \_ Counter)
</dt> <dd>

Der Counter-Wert wird verwendet.

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI- \_ VCR- \_ Zeit ( \_ Timecode)
</dt> <dd>

"Timecode" wird verwendet.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>MCI- \_ VCR- \_ Status- \_ Zeit Code \_ vorhanden
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn der Zeitcode an der aktuellen Position im Inhalt vorhanden ist. Andernfalls wird **false** festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>MCI- \_ VCR- \_ Status- \_ Timecode- \_ Datensatz
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn der Zeitcode aufgezeichnet wird, wenn der nächste Datensatz-Befehl angegeben wird. Andernfalls wird **false** festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>MCI- \_ VCR- \_ Status- \_ \_ timecodetyp
</dt> <dd>

Der **dwreturn** -Member ist auf eine Konstante festgelegt, die den Typ des Timecodes beschreibt, der direkt vom Gerät unterstützt wird. es handelt sich um einen der folgenden Werte:

-   MCI \_ VCR \_ Timecode \_ Type \_ None: dieses Gerät verwendet keinen Timecode.
-   MCI- \_ VCR- \_ Timecode \_ Type \_ other: dieses Gerät verwendet einen nicht angegebenen Zeit Code.
-   MCI \_ VCR \_ Timecode \_ Type \_ SMPTE: dieses Gerät verwendet SMPTE-Timecode.
-   MCI \_ VCR \_ Timecode \_ Type \_ SMPTE \_ Drop: dieses Gerät verwendet SMPTE Drop Timecode.

</dd> <dt>

<span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>MCI \_ VCR- \_ Status- \_ \_ Peerkanal
</dt> <dd>

Der **dwreturn** -Member wird auf die aktuelle Channelnummer festgelegt. Wenn Sie die MCI- \_ VCR- \_ Status \_ Nummer im *dwFlags* -Parameter dieses Befehls angeben, enthält **dwnumber** die logische-Tuner-Nummer, für die dieser Befehl gilt.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>Video Monitor für den MCI- \_ VCR- \_ Status \_ \_
</dt> <dd>

Der **dwreturn** -Member wird auf eine Konstante festgelegt, die den derzeit ausgewählten Videomonitor-Typ angibt.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>\_ \_ \_ Video \_ Monitor \_ Nummer für den MCI-VCR-Status
</dt> <dd>

Das **dwreturn** -Element wird auf die Nummer des derzeit ausgewählten Videomonitor Typs festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>\_ \_ \_ Video \_ Daten Satz für den MCI VCR-Status
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Video aufgezeichnet wird, wenn der nächste Datensatz-Befehl angegeben wird. Andernfalls wird **false** festgelegt. Wenn Sie MCI \_ Track im *dwFlags* -Parameter dieses Befehls angeben, enthält **dwtrack** den Track, auf den diese Abfrage angewendet wird.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>MCI \_ VCR- \_ Status- \_ Video \_ Quelle
</dt> <dd>

Der **dwreturn** -Member wird auf eine Konstante festgelegt, die den derzeit ausgewählten Typ der Videoquelle angibt.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>MCI \_ VCR- \_ Status \_ Video- \_ Quell \_ Nummer
</dt> <dd>

Das **dwreturn** -Element wird auf die Nummer des derzeit ausgewählten Videoquellen Typs festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI \_ VCR \_ Status \_ Schreib \_ geschützt
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Medium schreibgeschützt ist. Andernfalls wird **false** festgelegt.

</dd> </dl>

Bei VCR-Geräten verweist der *lpstatus* -Parameter auf eine [**MCI- \_ VCR- \_ statusparameterstruktur \_**](mci-vcr-status-parms.md) .

Wenn Sie das MCI- \_ \_ statuslength-Flag zum Ermitteln der Länge des Mediums verwenden, werden für VCR-Geräte immer zwei Stunden zurückgegeben, es sei denn, die Länge wurde explizit mit dem Befehl [MCI \_ Set](mci-set.md) geändert.

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp " **Overlay** " verwendet. Diese Konstanten werden im **lengertem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.

<dl> <dt>

<span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>MCI \_ OVLY- \_ Status- \_ HWND
</dt> <dd>

Das **dwreturn** -Element wird auf das Handle des Fensters festgelegt, das dem Video Überlagerungs Gerät zugeordnet ist.

</dd> <dt>

<span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>MCI- \_ OVLY- \_ Status \_ Streckung
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn die Streckung aktiviert ist. Andernfalls wird **false** festgelegt.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI- \_ Status \_ Medien \_ vorhanden
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn die Medien in das Gerät eingefügt werden. Andernfalls wird **false** festgelegt.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp " **Videodisk** " verwendet. Diese Konstanten werden im **lengertem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI- \_ Status \_ Medien \_ vorhanden
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn die Medien in das Gerät eingefügt werden. Andernfalls wird **false** festgelegt.

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI- \_ Status \_ Modus
</dt> <dd>

Der **dwreturn** -Member ist auf den aktuellen Modus des Geräts festgelegt. Videodisk-Geräte können \_ \_ \_ zusätzlich zu den Konstanten, die von jedem Gerät zurückgegeben werden können, die MCI-VD-Modus-Konstante zurückgeben, wie mit dem *dwFlags* -Parameter dokumentiert.

</dd> <dt>

<span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>MCI- \_ VD- \_ Status- \_ Festplatten \_ Größe
</dt> <dd>

Der **dwreturn** -Member wird auf die Größe der geladenen CD in Zoll (8 oder 12) festgelegt.

</dd> <dt>

<span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>MCI- \_ VD- \_ Status \_ Vorwärts
</dt> <dd>

Der **dwreturn** -Member wird bei der Wiedergabe auf **true** festgelegt. Andernfalls wird **false** festgelegt.

Dieses Flag wird vom MCI-Videodisk-Gerät nicht unterstützt.

</dd> <dt>

<span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>MCI- \_ VD- \_ \_ statusmedientyp \_
</dt> <dd>

Der **dwreturn** -Member ist auf den Medientyp des eingefügten Mediums festgelegt. Die folgenden Medientypen können zurückgegeben werden:

MCI- \_ VD- \_ Medien- \_ CAV

MCI- \_ VD- \_ Medien- \_ CLV

anderes MCI- \_ VD- \_ Medium \_

</dd> <dt>

<span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>MCI- \_ VD- \_ Status \_ Seite
</dt> <dd>

Der **dwreturn** -Member ist auf 1 oder 2 festgelegt, um anzugeben, welche Seite der Festplatte geladen wird. Dieses Flag wird nicht von allen Videodisk-Geräten unterstützt.

</dd> <dt>

<span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>MCI- \_ VD- \_ Status \_ Geschwindigkeit
</dt> <dd>

Der **dwreturn** -Member wird auf die Wiedergabegeschwindigkeit in Frames pro Sekunde festgelegt. Die mcipionr. DRV-Gerätetreiber gibt eine nicht unterstützte mcierr- \_ \_ Funktion zurück.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **waveaudiogerätetyp** verwendet. Diese Konstanten werden im **lengertem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.

<dl> <dt>

<span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI \_ Wave \_ Formattag
</dt> <dd>

Das **dwreturn** -Element wird auf das aktuelle Formattag festgelegt, das für die Wiedergabe, Aufzeichnung und Speicherung verwendet wird.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI- \_ Wave- \_ Eingabe
</dt> <dd>

Der **dwreturn** -Member ist auf das für die Aufzeichnung verwendete Wave-Eingabegerät festgelegt. Wenn kein Gerät verwendet wird und kein Gerät explizit festgelegt wurde, lautet die Fehlerrückgabe mcierr \_ Wave \_ inputunspezifi.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI- \_ Wave- \_ Ausgabe
</dt> <dd>

Der **dwreturn** -Member ist auf das für die Wiedergabe verwendete Wave-Ausgabegerät festgelegt. Wenn kein Gerät verwendet wird und kein Gerät explizit festgelegt wurde, lautet die Fehlerrückgabe mcierr \_ Wave \_ outputunspezifi.

</dd> <dt>

<span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>MCI- \_ Wave- \_ Status \_ avgbytespersec
</dt> <dd>

Das **dwreturn** -Element wird auf die aktuellen Bytes pro Sekunde festgelegt, die zum Abspielen, aufzeichnen und Speichern verwendet werden.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>MCI- \_ Wave- \_ Status- \_ BitsPerSample
</dt> <dd>

Das **dwreturn** -Element wird auf die aktuellen Bits pro Beispiel festgelegt, die zum Abspielen, aufzeichnen und Speichern von PCM-formatierten Daten verwendet werden.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>MCI- \_ Wellen \_ Status \_ BlockAlign
</dt> <dd>

Das **dwreturn** -Element wird auf die aktuelle Block Ausrichtung festgelegt, die zum Abspielen, aufzeichnen und Speichern verwendet wird.

</dd> <dt>

<span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>MCI- \_ Wellen \_ Status \_ Kanäle
</dt> <dd>

Der **dwreturn** -Member wird auf die aktuelle Kanalanzahl festgelegt, die zum wiedergeben, aufzeichnen und Speichern verwendet wird.

</dd> <dt>

<span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>MCI- \_ Wave- \_ Status \_ Ebene
</dt> <dd>

Der **dwreturn** -Member ist auf den aktuellen Datensatz oder die Wiedergabe Ebene von PCM-formatierten Daten festgelegt. Der Wert wird abhängig von der verwendeten Stichprobengröße als 8-oder 16-Bit-Wert zurückgegeben. Die Rechte-oder Mono-Kanal Ebene wird im nieder wertigen Wort zurückgegeben. Die linke Kanal Ebene wird im höherwertigen Wort zurückgegeben.

</dd> <dt>

<span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>MCI- \_ Wave- \_ Status " \_ samplespersec"
</dt> <dd>

Das **dwreturn** -Element wird auf die aktuellen Stichproben pro Sekunde festgelegt, die zum Abspielen, aufzeichnen und Speichern verwendet werden.

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
</dt> <dt>

[MCI- \_ Ausschneiden](mci-cut.md)
</dt> <dt>

[MCI \_ Löschen](mci-delete.md)
</dt> <dt>

[MCI- \_ Einfügen](mci-paste.md)
</dt> <dt>

[MCI- \_ Reserve](mci-reserve.md)
</dt> <dt>

[MCI- \_ Gruppe](mci-set.md)
</dt> <dt>

[Theater](play.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[einzuholen](seek.md)
</dt> </dl>

 

