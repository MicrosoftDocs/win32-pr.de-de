---
title: MCI_STATUS Befehl (Mmsystem.h)
description: Der \_ MCI-Befehl STATUS ruft Informationen zu einem MCI-Gerät ab. Dieser Befehl wird von allen Geräten erkannt. Informationen werden im dwReturn-Member der Struktur zurückgegeben, die durch den lpStatus-Parameter identifiziert wird.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- MCI_STATUS-Befehl Windows Multimedia
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
ms.openlocfilehash: 9905000c718ff70435ec91bf86bf7a77d14379ed7ca557eaa85fb0df594196c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784280"
---
# <a name="mci_status-command"></a>Befehl "MCI \_ STATUS"

> [!NOTE]
> Bias-free Communication Microsoft unterstützt eine vielfältige und inklusionsbasierte Umgebung.  In diesem Dokument gibt es Verweise auf das Wort "slave". Microsoft Style [Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) erkennt dies als Ausschlusswort.  Diese Formulierung wird verwendet, da sie derzeit in den Befehlen verwendet wird. Zur Konsistenz enthält dieses Dokument dieses Wort. Wenn dieses Wort in den Befehlen geändert wird, korrigieren wir dieses Dokument so, dass es ausgerichtet ist.

Der \_ MCI-Befehl STATUS ruft Informationen zu einem MCI-Gerät ab. Dieser Befehl wird von allen Geräten erkannt. Informationen werden im **dwReturn-Member der** Struktur zurückgegeben, die durch den *lpStatus-Parameter identifiziert* wird.

Um diesen Befehl zu senden, rufen Sie die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsnachricht empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder bei Digitalvideo- und VCR-Geräten MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*
</dt> <dd>

Zeiger auf eine [**MCI \_ STATUS \_ PARMS-Struktur.**](mci-status-parms.md) (Geräte mit erweiterten Befehlssätzen ersetzen diese Struktur möglicherweise durch eine gerätespezifische Struktur.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden zusätzlichen standard- und befehlsspezifischen Flags gelten für alle Geräte, die MCI \_ STATUS unterstützen:

<dl> <dt>

<span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>\_MCI-STATUSELEMENT \_
</dt> <dd>

Gibt an, **dass das dwItem-Element** der durch *lpStatus* identifizierten Struktur eine Konstante enthält, die angibt, welches Statuselement erhalten werden soll. Die folgenden Konstanten definieren, welches Statuselement im **dwReturn-Element** der -Struktur zurückgeben werden soll:

MCI \_ STATUS \_ CURRENT \_ TRACK

Das **dwReturn-Member** wird auf die aktuelle Tracknummer festgelegt. MCI verwendet fortlaufende Tracknummern.

\_MCI-STATUSLÄNGE \_

Das **dwReturn-Member** wird auf die Mediengesumme festgelegt.

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_MCI-STATUSMODUS \_
</dt> <dd>

Das **dwReturn-Mitglied** ist auf den aktuellen Modus des Geräts festgelegt. Die Modi umfassen Folgendes:

-   \_MCI-MODUS \_ NICHT \_ BEREIT
-   PAUSE IM \_ \_ MCI-MODUS
-   WIEDERGABE IM \_ \_ MCI-MODUS
-   BEENDEN DES \_ \_ MCI-MODUS
-   \_MCI-MODUS \_ GEÖFFNET
-   \_ \_ MCI-MODUSDATENSATZ
-   MCI \_ MODE \_ SEEK

</dd> <dt>

<span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>\_MCI-STATUSNUMMER \_ \_ DER \_ SPUREN
</dt> <dd>

Das **dwReturn-Member** wird auf die Gesamtzahl der wiedersetzbaren Spuren festgelegt.

</dd> <dt>

<span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>\_MCI-STATUSPOSITION \_
</dt> <dd>

Das **dwReturn-Member** wird auf die aktuelle Position festgelegt.

</dd> <dt>

<span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>\_MCI-STATUS \_ BEREIT
</dt> <dd>

Das **dwReturn-Mitglied** ist auf **TRUE festgelegt,** wenn das Gerät bereit ist. andernfalls ist **sie auf FALSE** festgelegt.

</dd> <dt>

<span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>\_ \_ MCI-STATUSZEITFORMAT \_
</dt> <dd>

Das **dwReturn-Member** wird auf das aktuelle Zeitformat des Geräts festgelegt. Die Zeitformate umfassen Folgendes:

-   BYTES IM \_ \_ MCI-FORMAT
-   \_ \_ MCI-FORMATFRAMES
-   \_MCI-FORMAT \_ HMS
-   \_MCI-FORMAT \_ IN MILLISEKUNDEN
-   MSF IM \_ \_ MCI-FORMAT
-   \_ \_ MCI-FORMATBEISPIELE
-   MCI \_ FORMAT \_ TMSF

</dd> <dt>

<span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>MCI \_ STATUS \_ START
</dt> <dd>

Erhält die Anfangsposition des Mediums. Um die Anfangsposition zu erhalten, kombinieren Sie dieses Flag mit MCI STATUS ITEM, und legen Sie das \_ \_ **dwItem-Element** der durch *lpStatus* identifizierten Struktur auf MCI \_ STATUS POSITION \_ fest.

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>MCI \_ TRACK
</dt> <dd>

Gibt an, dass ein Statusverfolgungsparameter im **dwTrack-Member** der durch *lpStatus identifizierten Struktur enthalten ist.* Sie müssen dieses Flag mit den Konstanten MCI \_ STATUS \_ POSITION oder MCI STATUS LENGTH \_ \_ verwenden. Bei Verwendung mit MCI \_ STATUS \_ POSITION erhält MCI TRACK die \_ Anfangsposition der angegebenen Spur. Bei Verwendung mit MCI \_ STATUS \_ LENGTH erhält MCI TRACK die Länge der \_ angegebenen Spur. MCI verwendet fortlaufende Tracknummern.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **cdaudio-Gerätetyp** verwendet. Diese Konstanten werden im **dwItem-Member** der -Struktur verwendet, auf die der *lpStatus-Parameter* zeigt, wenn MCI STATUS ITEM für den \_ \_ *dwFlags-Parameter angegeben* wird.

<dl> <dt>

<span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>MCI \_ CDA \_ STATUS \_ TYPE \_ TRACK
</dt> <dd>

Das **dwReturn-Member** wird auf einen der folgenden Werte festgelegt:

-   MCI \_ CDA \_ TRACK \_ AUDIO
-   MCI \_ CDA \_ TRACK \_ OTHER

Um dieses Flag verwenden zu können, muss das MCI TRACK-Flag festgelegt werden, und das dwTrack-Member der durch lpStatus identifizierten Struktur muss \_ eine gültige Tracknummer enthalten.  

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_MCI-STATUSMEDIEN \_ \_ VORHANDEN
</dt> <dd>

Das **dwReturn-Member** ist auf **TRUE festgelegt,** wenn das Medium in das Gerät eingefügt wird. andernfalls ist **sie auf FALSE** festgelegt.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **Gerätetyp digitalvideo** verwendet:

<dl> <dt>

<span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>MCI \_ DGV \_ STATUS \_ DISKSPACE
</dt> <dd>

Der **lpstrDrive-Member** der durch *lpStatus* identifizierten Struktur gibt ein Laufwerk oder in einigen Implementierungen einen Pfad an. Der Befehl MCI STATUS gibt die ungefähre Menge an Speicherplatz zurück, die durch den \_ [MCI \_ RESERVE-Befehl](mci-reserve.md) im **dwReturn-Member** der durch lpStatus identifizierten *Struktur erhalten werden konnte.* Der Speicherplatz wird in Einheiten des aktuellen Zeitformats gemessen.

</dd> <dt>

<span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>EINGABE DES \_ MCI-DGV-STATUS \_ \_
</dt> <dd>

Die konstante, die vom **dwItem-Member** der durch *lpStatus* identifizierten Struktur angegeben wird, gilt für die Eingabe.

</dd> <dt>

<span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>MCI \_ DGV \_ STATUS \_ LEFT
</dt> <dd>

Die konstante, die vom **dwItem-Member** der durch *lpStatus* identifizierten Struktur angegeben wird, gilt für den linken Audiokanal.

</dd> <dt>

<span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>MCI \_ DGV \_ STATUS \_ NOMINAL
</dt> <dd>

Die konstante, die vom **dwItem-Member** der durch *lpStatus* identifizierten Struktur angegeben wird, fordert den nominalen Wert anstelle des aktuellen Werts an.

</dd> <dt>

<span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>AUSGABE DES MCI \_ \_ \_ DGV-STATUS
</dt> <dd>

Die konstante, die vom **dwItem-Member** der durch *lpStatus* identifizierten Struktur angegeben wird, gilt für die Ausgabe.

</dd> <dt>

<span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>MCI \_ \_ DGV-STATUSDATENSATZ \_
</dt> <dd>

Die framerate, die für das MCI DGV STATUS FRAME RATE-Flag zurückgegeben \_ \_ \_ \_ wird, ist die Rate, die für die Komprimierung verwendet wird.

</dd> <dt>

<span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>REFERENZ ZUM \_ MCI-DGV-STATUS \_ \_
</dt> <dd>

Der **dwReturn-Member** der durch *lpStatus* identifizierten Struktur gibt das nächste Keyframebild zurück, das dem im **dwReference-Member angegebenen Frame** voraus ist.

</dd> <dt>

<span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>MCI \_ DGV \_ STATUS \_ RIGHT
</dt> <dd>

Die konstante, die vom **dwItem-Member** der durch *lpStatus* identifizierten Struktur angegeben wird, gilt für den richtigen Audiokanal.

</dd> </dl>

Die folgenden Konstanten werden mit dem **Gerätetyp digitalvideo** im **dwItem-Member** der -Struktur verwendet, auf die der *lpStatus-Parameter* zeigt, wenn MCI STATUS ITEM für den \_ \_ *dwFlags-Parameter angegeben* wird.

<dl> <dt>

<span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>AUDIOUNTERBRECHUNGEN DES \_ MCI-AVI-STATUS \_ \_ \_
</dt> <dd>

Das **dwReturn-Member** gibt zurück, wie oft der Audioteil der letzten AVI-Sequenz ausgebrochen ist. Das System zählt eine Audiopause, wenn es versucht, Audiodaten in den Gerätetreiber zu schreiben, und entdeckt, dass der Treiber bereits alle verfügbaren Daten abgespielt hat. Dieses Flag wird nur vom MCIAVI-Treiber für digitale Videos erkannt.

</dd> <dt>

<span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>\_ \_ MCI-AVI-STATUSFRAMES \_ \_ ÜBERSPRUNGEN
</dt> <dd>

Das **dwReturn-Member** gibt die Anzahl der Frames zurück, die nicht gezeichnet wurden, als die letzte AVI-Sequenz abgespielt wurde. Dieses Flag wird nur vom MCIAVI-Treiber für digitale Videos erkannt.

</dd> <dt>

<span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>MCI \_ AVI \_ STATUS \_ LAST \_ PLAY \_ SPEED
</dt> <dd>

Das **dwReturn-Member** gibt einen Wert zurück, der angibt, wie genau die tatsächliche Wiedergabezeit der letzten AVI-Sequenz der Zielspielzeit entspricht. Der Wert 1000 gibt an, dass die Zielzeit und die tatsächliche Zeit identisch waren. Ein Wert von 2000 würde z. B. darauf hindeuten, dass die Wiedergabe der AVI-Sequenz doppelt so lange ge dauern würde, wie sie hätte. Dieses Flag wird nur vom MCIAVI-Treiber für digitale Videos erkannt.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>MCI \_ DGV \_ STATUS \_ AUDIO
</dt> <dd>

Das **dwReturn-Member** gibt MCI ON oder MCI OFF zurück, abhängig von der neuesten MCI SET AUDIO-Option für den \_ \_ \_ \_ [MCI \_ SET-Befehl.](mci-set.md) Sie gibt MCI \_ ON zurück, wenn einer oder beide Sprecher aktiviert sind, andernfalls MCI \_ OFF.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>MCI \_ DGV \_ STATUS \_ AUDIO \_ INPUT
</dt> <dd>

Das **dwReturn-Member** gibt die ungefähre sofortige Audioebene des analogen Audiosignals zurück. Ein Wert größer als 1.000 impliziert eine Clippingverzerrung. Einige Geräte können diesen Wert nur beim Aufzeichnen von Audiodaten bestimmen. Diesem Statuswert ist kein **MCI \_ SET-** oder [MCI \_ SETAUDIO-Befehl](mci-setaudio.md) zugeordnet. Dieser Wert bezieht sich auf den Waveform-Audiobefehl MCI WAVE STATUS LEVEL, normalisiert sich aber \_ \_ \_ anders.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>MCI \_ DGV \_ STATUS \_ AUDIO \_ RECORD
</dt> <dd>

Das **dwReturn-Member** gibt MCI ON oder MCI OFF zurück, das den durch das \_ \_ MCI \_ DGV \_ SETAUDIO RECORD-Flag des \_ **MCI \_ SETAUDIO-Befehls festgelegten Zustand** wiedergibt.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>MCI \_ DGV \_ STATUS \_ AUDIO \_ SOURCE
</dt> <dd>

Das **dwReturn-Member** gibt die aktuelle Audiodisiererquelle zurück:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MCI \_ DGV \_ SETAUDIO \_ AVERAGE
</dt> <dd>

Gibt den Durchschnitt der linken und rechten Audiokanäle an.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ SETAUDIO \_ LEFT
</dt> <dd>

Gibt den linken Audiokanal an.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ RIGHT
</dt> <dd>

Gibt den richtigen Audiokanal an.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ DGV \_ SETAUDIO \_ STEREO
</dt> <dd>

Gibt Stereo an.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>MCI \_ DGV \_ STATUS \_ AUDIO \_ STREAM
</dt> <dd>

Das **dwReturn-Member** gibt die aktuelle Audiostreamnummer zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI \_ DGV \_ STATUS \_ AVGBYTESPERSEC
</dt> <dd>

Das **dwReturn-Member** gibt die durchschnittliche Anzahl von Bytes pro Sekunde zurück, die für die Aufzeichnung verwendet werden.

</dd> <dt>

<span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>MCI \_ DGV \_ STATUS \_ DG
</dt> <dd>

Das **dwReturn-Member** gibt den aktuellen Audiopegel zurück. Verwenden Sie MCI \_ DGV \_ STATUS NOMINAL mit \_ diesem Flag, um den nominalen Wert zu erhalten.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>MCI \_ DGV \_ STATUS \_ BITSPERPEL
</dt> <dd>

Das **dwReturn-Member** gibt die Anzahl der Bits pro Pixel zurück, die zum Speichern erfasster oder aufgezeichneter Daten verwendet werden.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI \_ DGV \_ STATUS \_ BITSPERSAMPLE
</dt> <dd>

Das **dwReturn-Member** gibt die Anzahl der Bits pro Stichprobe zurück, die das Gerät für die Aufzeichnung verwendet. Dies gilt nur für Geräte, die das PCM-Format unterstützen.

</dd> <dt>

<span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI \_ DGV \_ STATUS \_ BLOCKALIGN
</dt> <dd>

Das **dwReturn-Member** gibt die Ausrichtung von Datenblöcken relativ zum Anfang der Eingabe-Wellenform zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>HELLIGKEIT DES MCI \_ \_ \_ DGV-STATUS
</dt> <dd>

Das **dwReturn-Member** gibt die aktuelle Video-Helligkeitsstufe zurück. Verwenden Sie MCI \_ DGV \_ STATUS NOMINAL mit \_ diesem Flag, um den nominalen Wert zu erhalten.

</dd> <dt>

<span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>MCI \_ DGV \_ STATUS \_ COLOR
</dt> <dd>

Das **dwReturn-Member** gibt die aktuelle Farbebene zurück. Verwenden Sie MCI \_ DGV \_ STATUS NOMINAL mit \_ diesem Flag, um den nominalen Wert zu erhalten.

</dd> <dt>

<span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>MCI \_ DGV \_ STATUS \_ CONTRAST
</dt> <dd>

Das **dwReturn-Member** gibt den aktuellen Kontrast zurück. Verwenden Sie MCI \_ DGV \_ STATUS NOMINAL mit \_ diesem Flag, um den nominalen Wert zu erhalten.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI \_ DGV \_ STATUS \_ FILEFORMAT
</dt> <dd>

Das **dwReturn-Member** gibt das aktuelle Dateiformat zum Aufzeichnen oder Speichern zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MCI \_ DGV \_ STATUS \_ FILE \_ MODE
</dt> <dd>

Das **dwReturn-Member** gibt den Status des Dateivorgang zurück:

BEARBEITEN DES MCI \_ \_ \_ DGV-DATEIMODUS \_

Wird während Ausschneide-, Kopier-, Lösch-, Einfüge- und Rückgängig-Vorgängen zurückgegeben.

MCI \_ \_ DGV-DATEIMODUS IM \_ \_ LEERLAUF

Wird zurückgegeben, wenn die Datei für den nächsten Vorgang bereit ist.

LADEN DES MCI \_ \_ \_ DGV-DATEIMODUS \_

Wird zurückgegeben, während die Datei geladen wird.

SPEICHERN DES MCI \_ \_ \_ DGV-DATEIMODUS \_

Wird zurückgegeben, während die Datei gespeichert wird.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>MCI \_ DGV \_ STATUS \_ FILE \_ COMPLETION
</dt> <dd>

Das **dwReturn-Member** gibt den geschätzten Prozentsatz zurück, in dem ein Lade-, Sicherungs-, Erfassungs-, Ausschneide-, Kopier-, Lösch-, Einfüge- oder Rückgängig-Vorgang durchgeführt wurde. (Anwendungen können damit einen visuellen Fortschrittsindikator bereitstellen.) Dieses Flag wird nicht von allen Digitalvideogeräten unterstützt.

</dd> <dt>

<span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>MCI \_ DGV \_ STATUS \_ FORWARD
</dt> <dd>

Das **dwReturn-Member** gibt **TRUE zurück,** wenn die Geräterichtung vorwärts ist oder das Gerät nicht abspielt.

</dd> <dt>

<span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>MCI \_ DGV \_ STATUS \_ FRAME \_ RATE
</dt> <dd>

Das **dwReturn-Member** muss mit MCI \_ DGV \_ STATUS \_ NOMINAL, MCI \_ DGV STATUS RECORD oder \_ \_ beidem verwendet werden. Bei Verwendung mit MCI \_ DGV \_ STATUS RECORD wird die \_ aktuelle Framerate zurückgegeben, die für die Aufzeichnung verwendet wird. Bei Verwendung mit MCI DGV STATUS RECORD und MCI DGV STATUS NOMINAL wird die nominale Bildfrequenz zurückgegeben, die dem \_ \_ \_ Eingabevideosignal zugeordnet \_ \_ \_ ist. Bei Verwendung mit MCI \_ DGV \_ STATUS NOMINAL wird \_ die nominale Framerate zurückgegeben, die der Datei zugeordnet ist. In allen Fällen werden die Einheiten in Frames pro Sekunde multipliziert mit 1000.

</dd> <dt>

<span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>MCI \_ DGV \_ STATUS \_ GAMMA
</dt> <dd>

Das **dwReturn-Member** gibt den aktuellen Gammawert zurück. Verwenden Sie MCI \_ DGV \_ STATUS NOMINAL mit \_ diesem Flag, um den nominalen Wert zu erhalten.

</dd> <dt>

<span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI \_ DGV \_ STATUS \_ HPAL
</dt> <dd>

Das **dwReturn-Member** gibt den ASCII-Dezimalwert für das aktuelle Palettenhand handle zurück. Das Handle ist im niedrigen Wort des zurückgegebenen Werts enthalten.

</dd> <dt>

<span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>MCI \_ DGV \_ STATUS \_ HWND
</dt> <dd>

Das **dwReturn-Member** gibt den ASCII-Dezimalwert für das aktuelle explizite oder Standardfensterhand handle zurück, das dieser Gerätetreiberinstanz zugeordnet ist. Das Handle ist im niedrigen Wort des zurückgegebenen Werts enthalten.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>MCI \_ DGV \_ STATUS \_ KEY \_ COLOR
</dt> <dd>

Das **dwReturn-Member** gibt den aktuellen Schlüsselfarbenwert zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>MCI \_ DGV \_ STATUS \_ KEY \_ INDEX
</dt> <dd>

Das **dwReturn-Member** gibt den aktuellen Schlüsselindexwert zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>MCI \_ DGV \_ STATUS \_ MONITOR
</dt> <dd>

Das **dwReturn-Member** gibt eine Konstante zurück, die die Quelle der aktuellen Präsentation angibt. Die folgenden Konstanten werden definiert:

MCI \_ DGV \_ \_ MONITOR-DATEI

Eine Datei ist die Quelle.

MCI \_ DGV \_ MONITOR \_ INPUT

Die Eingabe ist die Quelle.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>MCI \_ DGV \_ STATUS \_ \_ MONITOR-METHODE
</dt> <dd>

Der **dwReturn-Member gibt** eine Konstante zurück, die die für die Eingabeüberwachung verwendete Methode angibt. Die folgenden Konstanten sind definiert:

DIREKTE MCI \_ \_ \_ DGV-METHODE

Direkte Eingabeüberwachung.

MCI \_ DGV \_ METHOD \_ POST

Überwachung nach der Eingabe.

MCI \_ \_ DGV-METHODE \_ VOR

Überwachung vor der Eingabe.

</dd> <dt>

<span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MCI \_ DGV \_ STATUS \_ PAUSE \_ MODE
</dt> <dd>

Das **dwReturn-Member** gibt MCI MODE PLAY zurück, wenn das Gerät während der Wiedergabe angehalten wurde, und gibt MCI MODE RECORD zurück, wenn das Gerät während der Aufzeichnung \_ angehalten \_ \_ \_ wurde. Der Befehl gibt MCIERR NONAPPLICABLE FUNCTION als Fehlerrückgibt \_ \_ zurück, wenn das Gerät nicht angehalten ist.

</dd> <dt>

<span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI \_ DGV \_ STATUS \_ SAMPLESPERSECOND
</dt> <dd>

Das **dwReturn-Member** gibt die Anzahl der aufgezeichneten Stichproben pro Sekunde zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI \_ DGV \_ STATUS \_ SEEK \_ EXACTLY
</dt> <dd>

Das **dwReturn-Member** gibt **TRUE** oder **FALSE zurück,** was angibt, ob das Suchformat genau festgelegt ist. (Anwendungen können dieses Format festlegen, indem sie den [Befehl MCI \_ SET](mci-set.md) mit dem Flag MCI \_ DGV \_ SET SEEK \_ EXACTLY \_ verwenden.)

</dd> <dt>

<span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>MCI \_ DGV \_ STATUS \_ SHARPNESS
</dt> <dd>

Das **dwReturn-Member** gibt den aktuellen Schärfenpegel zurück. Verwenden Sie MCI \_ DGV \_ STATUS NOMINAL mit \_ diesem Flag, um die nominale Ebene zu erhalten.

</dd> <dt>

<span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>MCI \_ DGV \_ STATUS \_ SIZE
</dt> <dd>

Das **dwReturn-Member** gibt die ungefähre Wiedergabedauer komprimierter Daten zurück, die der reservierte Arbeitsbereich enthält. Die Dauereinheiten liegen im aktuellen Zeitformat vor. Sie gibt 0 (null) zurück, wenn kein reservierter Speicherplatz vorhanden ist. Die zurückgegebene Größe ist ungefähr, da der genaue Speicherplatz für komprimierte Daten im Allgemeinen erst vorhergesagt werden kann, nachdem die Daten komprimiert wurden.

</dd> <dt>

<span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI \_ DGV \_ STATUS \_ SMPTE
</dt> <dd>

Das **dwReturn-Member** gibt den SMPTE-Zeitcode zurück, der der aktuellen Position im Arbeitsbereich zugeordnet ist.

</dd> <dt>

<span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>MCI \_ DGV \_ STATUS \_ SPEED
</dt> <dd>

Das **dwReturn-Member** gibt die aktuelle Wiedergabegeschwindigkeit zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>MCI \_ DGV \_ STATUS \_ STILL \_ FILEFORMAT
</dt> <dd>

Das **dwReturn-Member** gibt das aktuelle Dateiformat für den [MCI \_ CAPTURE-Befehl](mci-capture.md) zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>MCI \_ DGV \_ STATUS \_ TÖN
</dt> <dd>

Das **dwReturn-Member** gibt die aktuelle Videotonebene zurück. Verwenden Sie MCI \_ DGV \_ STATUS NOMINAL mit \_ diesem Flag, um die nominale Ebene zu erhalten.

</dd> <dt>

<span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI \_ DGV \_ STATUS \_ TREBLE
</dt> <dd>

Das **dwReturn-Member** gibt den aktuellen Audio-Treble-Grad zurück. Verwenden Sie MCI \_ DGV \_ STATUS NOMINAL mit \_ diesem Flag, um die nominale Ebene zu erhalten.

</dd> <dt>

<span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>MCI \_ DGV \_ STATUS \_ UNSAVED
</dt> <dd>

Das **dwReturn-Mitglied** gibt **TRUE** zurück, wenn im Arbeitsbereich Aufgezeichnete Daten gespeichert sind, die möglicherweise durch einen [MCI \_ CLOSE-,](mci-close.md) [MCI \_ LOAD-,](mci-load.md) [MCI \_ RECORD-,](mci-record.md) [MCI \_ RESERVE-,](mci-reserve.md) [MCI \_ CUT-,](mci-cut.md) [MCI \_ DELETE-](mci-delete.md)oder [ \_ MCI-PASTE-Befehl](mci-paste.md) verloren gehen. Andernfalls gibt der **Member FALSE** zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>VIDEO ZUM MCI \_ \_ \_ DGV-STATUS
</dt> <dd>

Das **dwReturn-Member** gibt MCI \_ ON zurück, wenn video aktiviert ist, oder MCI \_ OFF, wenn es deaktiviert ist.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>VIDEOAUFZEICHNUNG ZUM MCI \_ \_ \_ DGV-STATUS \_
</dt> <dd>

Das **dwReturn-Member** gibt MCI ON oder MCI OFF zurück, was den durch das \_ \_ MCI \_ DGV SETVIDEO RECORD-Flag des \_ \_ [MCI \_ SETVIDEO-Befehls festgelegten Zustand](mci-setvideo.md) widerspiegelt.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>MCI \_ DGV \_ STATUS \_ VIDEO \_ SOURCE
</dt> <dd>

Das **dwReturn-Member** gibt eine Konstante zurück, die den Typ der Videoquelle angibt, die vom MCI \_ DGV SETVIDEO SOURCE-Flag des \_ \_ **MCI \_ SETVIDEO-Befehls festgelegt** wurde.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI \_ DGV \_ STATUS \_ VIDEO \_ SRC \_ NUM
</dt> <dd>

Das **dwReturn-Member** gibt die Zahl innerhalb des Typs der aktuell aktiven Videoeingabequelle zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>VIDEOSTREAM ZUM MCI \_ \_ \_ DGV-STATUS \_
</dt> <dd>

Das **dwReturn-Member** gibt die aktuelle Videostreamnummer zurück.

</dd> <dt>

<span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>MCI \_ DGV \_ STATUS \_ VOLUME
</dt> <dd>

Das **dwReturn-Member** gibt den Durchschnitt des Volumes an den linken und rechten Lautsprecher zurück. Verwenden Sie MCI \_ DGV \_ STATUS NOMINAL mit \_ diesem Flag, um die nominale Ebene zu erhalten.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>MCI \_ \_ DGV-STATUSFENSTER \_ \_ SICHTBAR
</dt> <dd>

Das **dwReturn-Member** gibt **TRUE zurück,** wenn das Fenster nicht ausgeblendet ist.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>MCI \_ \_ DGV-STATUSFENSTER \_ \_ MINIMIERT
</dt> <dd>

Das **dwReturn-Member** gibt **TRUE zurück,** wenn das Fenster minimiert ist.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>MCI \_ \_ DGV-STATUSFENSTER \_ \_ MAXIMIERT
</dt> <dd>

Das **dwReturn-Member** gibt **TRUE zurück,** wenn das Fenster maximiert ist.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_MCI-STATUSMEDIEN \_ \_ VORHANDEN
</dt> <dd>

Der **dwReturn-Member** gibt **TRUE zurück.**

</dd> </dl>

Bei Digitalvideogeräten verweist *der lpStatus-Parameter* auf eine [**MCI \_ DGV STATUS \_ \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa)

Die folgenden zusätzlichen Flags werden mit dem **Sequencer-Gerätetyp** verwendet. Diese Konstanten werden im **dwItem-Member** der -Struktur verwendet, auf die der *lpStatus-Parameter* zeigt, wenn MCI STATUS ITEM für den \_ \_ *dwFlags-Parameter angegeben* wird.

<dl> <dt>

<span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI \_ SEQ \_ STATUS \_ DIVTYPE
</dt> <dd>

Das **dwReturn-Member** wird auf einen der folgenden Werte festgelegt, der den aktuellen Divisionstyp einer Sequenz angibt:

-   MCI \_ SEQ \_ DIV \_ PPQN
-   MCI \_ SEQ \_ DIV \_ SMPTE \_ 24
-   MCI \_ SEQ \_ DIV \_ SMPTE \_ 25
-   MCI \_ SEQ \_ DIV \_ SMPTE \_ 30
-   MCI \_ SEQ \_ DIV \_ SMPTE \_ 30DROP

</dd> <dt>

<span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MCI \_ SEQ \_ STATUS \_ MASTER
</dt> <dd>

Das **dwReturn-Member** wird auf den Synchronisierungstyp festgelegt, der für den Mastervorgang verwendet wird.

</dd> <dt>

<span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>MCI \_ SEQ \_ STATUS \_ OFFSET
</dt> <dd>

Das **dwReturn-Member** wird auf den aktuellen SMPTE-Offset einer Sequenz festgelegt.

</dd> <dt>

<span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>MCI \_ SEQ \_ STATUS \_ PORT
</dt> <dd>

Das **dwReturn-Member** wird auf die BEZEICHNUNG-Geräte-ID für den aktuellen Port festgelegt, der von der Sequenz verwendet wird.

</dd> <dt>

<span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI \_ SEQ \_ STATUS \_ SLAVE
</dt> <dd>

Das **dwReturn-Member** wird auf den Synchronisierungstyp festgelegt, der für den untergeordneten Vorgang verwendet wird.

</dd> <dt>

<span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI \_ SEQ \_ STATUS \_ TEMPO
</dt> <dd>

Das **dwReturn-Member** wird für PPQN-Dateien auf das aktuelle Tempo einer SEQUENCE-Sequenz in Takten pro Minute oder auf Frames pro Sekunde für SMPTE-Dateien festgelegt.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_MCI-STATUSMEDIEN \_ \_ VORHANDEN
</dt> <dd>

Das **dwReturn-Member** ist auf **TRUE festgelegt,** wenn das Medium auf dem Gerät eingefügt wird. andernfalls ist **sie auf FALSE** festgelegt.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **vcr-Gerätetyp** verwendet. Diese Konstanten werden im **dwItem-Member** der -Struktur verwendet, auf die der *lpStatus-Parameter* zeigt, wenn MCI STATUS ITEM für den \_ \_ *dwFlags-Parameter angegeben* wird.

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_MCI-STATUSMEDIEN \_ \_ VORHANDEN
</dt> <dd>

Das **dwReturn-Member** ist auf **TRUE festgelegt,** wenn das Medium auf dem Gerät eingefügt wird. andernfalls ist **sie auf FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>MCI \_ VCR \_ STATUS \_ ASSEMBLE \_ RECORD
</dt> <dd>

Das **dwReturn-Member** ist auf **TRUE festgelegt,** wenn der Assemblermodus aktiviert ist. andernfalls ist **sie auf FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>MCI \_ VCR \_ STATUS \_ AUDIO \_ MONITOR
</dt> <dd>

Der **dwReturn-Member** wird auf eine Konstante festgelegt, die den aktuell ausgewählten Audiomonitortyp angibt.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>MCI \_ VCR \_ STATUS \_ AUDIO \_ MONITOR \_ NUMBER
</dt> <dd>

Der **dwReturn-Member** wird auf die Nummer des aktuell ausgewählten Audiomonitortyps festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>MCI \_ \_ VCR-STATUSAUDIODATENSATZ \_ \_
</dt> <dd>

Das **dwReturn-Member** ist auf **TRUE festgelegt,** wenn Audiodaten aufgezeichnet werden, wenn der nächste Datensatzbefehl angegeben wird. andernfalls ist **sie auf FALSE** festgelegt. Wenn Sie MCI \_ TRACK im *dwFlags-Parameter* dieses Befehls angeben, enthält **dwTrack** die Spur, für die diese Anfrage gilt.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>MCI \_ VCR \_ STATUS \_ AUDIO \_ SOURCE
</dt> <dd>

Der **dwReturn-Member** wird auf eine Konstante festgelegt, die den aktuellen Audioquellentyp angibt.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>MCI \_ VCR \_ STATUS \_ AUDIO \_ SOURCE \_ NUMBER
</dt> <dd>

Der **dwReturn-Member** wird auf die Nummer des aktuell ausgewählten Audioquellentyps festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>MCI \_ VCR \_ STATUS \_ CLOCK
</dt> <dd>

Das **dwReturn-Member** wird auf den aktuellen Uhrwert in Allen Taktinkrementen festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>MCI \_ VCR \_ STATUS \_ CLOCK \_ ID
</dt> <dd>

Das **dwReturn-Member** wird auf eine Zahl festgelegt, die die verwendete Uhr eindeutig beschreibt.

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>MCI \_ VCR \_ STATUS \_ COUNTER \_ FORMAT
</dt> <dd>

Das **dwReturn-Member** wird auf eine Konstante festgelegt, die das aktuelle Indikatorformat beschreibt. Weitere Informationen finden Sie unter dem MCI \_ SET \_ TIME \_ FORMAT-Flag des [MCI \_ SET-Befehls.](mci-set.md)

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>AUFLÖSUNG DES \_ MCI-VCR-STATUSZÄHLERS \_ \_ \_
</dt> <dd>

Das **dwReturn-Member** wird auf eine Konstante festgelegt, die die Auflösung des Leistungsindikators beschreibt, und ist einer der folgenden Werte:

-   MCI VCR COUNTER RES FRAMES( MCI \_ VCR \_ COUNTER RES \_ \_ FRAMES): Der Leistungsindikator verfügt über die Auflösung von Frames.
-   MCI \_ VCR \_ COUNTER RES \_ \_ SECONDS: Der Leistungsindikator hat eine Auflösung von Sekunden.
-   MCI \_ VCR \_ STATUS COUNTER \_ \_ VALUE:Das **dwReturn-Member** wird im aktuellen Indikatorzeitformat auf den aktuellen Indikatorwert festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>MCI \_ VCR \_ STATUS \_ FRAME \_ RATE
</dt> <dd>

Das **dwReturn-Member** wird auf die aktuelle native Framerate des Geräts festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>\_MCI-VCR-STATUSINDEX \_ \_
</dt> <dd>

Das **dwReturn-Member** ist auf eine Konstante festgelegt, die den aktuellen Inhalt der Anzeige auf dem Bildschirm beschreibt, und ist einer der folgenden:

-   \_MCI-VCR-INDEXZÄHLER \_ \_
-   MCI \_ VCR \_ INDEX \_ DATE
-   \_ \_ MCI-VCR-INDEXZEIT \_
-   MCI \_ VCR \_ INDEX \_ TIMECODE

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>MCI \_ VCR \_ STATUS \_ INDEX \_ ON
</dt> <dd>

Das **dwReturn-Member** ist auf **TRUE festgelegt,** wenn die Anzeige auf dem Bildschirm eintrifft. andernfalls ist **sie auf FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>MEDIENTYP "MCI \_ VCR \_ \_ \_ STATUS"
</dt> <dd>

Das **dwReturn-Member** ist auf eine der folgenden Festgelegt:

-   MCI \_ VCR \_ MEDIA \_ 8MM
-   MCI \_ VCR \_ MEDIA \_ HI8
-   MCI \_ VCR \_ MEDIA \_ VHS
-   MCI \_ VCR \_ MEDIA \_ SVHS
-   MCI \_ VCR \_ MEDIA \_ BETA
-   MCI \_ VCR \_ MEDIA \_ EDBETA
-   MCI \_ VCR \_ MEDIA \_ OTHER

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>\_ \_ MCI-VCR-STATUSNUMMER \_
</dt> <dd>

Das **dwNumber-Member** wird auf die logische Tunernummer festgelegt, wenn Sie dieses Flag mit dem MCI \_ VCR \_ STATUS \_ TUNER \_ CHANNEL-Flag verwenden.

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>MCI \_ VCR STATUS NUMBER OF AUDIO TRACKS (MCI-VCR-STATUSNUMMER \_ DER \_ \_ \_ \_ AUDIOSPUREN)
</dt> <dd>

Das **dwReturn-Member** wird auf die Anzahl der Audiospuren festgelegt, die unabhängig voneinander ausgewählt werden können.

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>MCI \_ VCR \_ STATUS \_ NUMBER \_ OF \_ VIDEO \_ TRACKS
</dt> <dd>

Das **dwReturn-Member** wird auf die Anzahl von Videospuren festgelegt, die unabhängig voneinander ausgewählt werden können.

</dd> <dt>

<span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>MCI \_ VCR \_ STATUS \_ PAUSE \_ TIMEOUT
</dt> <dd>

Das **dwReturn-Member** wird auf die maximale Dauer eines Pausenbefehls in Millisekunden festgelegt. Der Rückgabewert 0 (null) gibt an, dass kein Time out auftritt.

</dd> <dt>

<span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>MCI \_ VCR \_ STATUS \_ PLAY \_ FORMAT
</dt> <dd>

Das **dwReturn-Member** ist auf eine der folgenden Festgelegt:

-   MCI \_ VCR \_ FORMAT \_ EP
-   MCI \_ VCR \_ FORMAT \_ LP
-   MCI \_ VCR \_ FORMAT \_ OTHER
-   MCI \_ VCR \_ FORMAT \_ SP

</dd> <dt>

<span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>MCI \_ VCR \_ STATUS \_ POSTROLL \_ DURATION
</dt> <dd>

Das **dwReturn-Member** wird auf die Länge des Videobands festgelegt, das nach dem Punkt, an dem er beendet wurde, im aktuellen Zeitformat abspielt. Dies ist erforderlich, um den VCR-Bandtransport von einem Stop- oder Pause-Befehl zu unterbrechen.

</dd> <dt>

<span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>MCI \_ VCR \_ STATUS \_ POWER \_ ON
</dt> <dd>

Das **dwReturn-Member** ist auf **TRUE festgelegt,** wenn die Stromversorgung eintrifft. andernfalls ist **sie auf FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>MCI \_ VCR \_ STATUS \_ PREROLL \_ DURATION
</dt> <dd>

Das **dwReturn-Member** wird auf die Länge des Videobands festgelegt, das vor dem Startort im aktuellen Zeitformat abspielt. Dies ist erforderlich, um die VCR-Ausgabe zu stabilisiert.

</dd> <dt>

<span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>\_ \_ MCI-VCR-STATUSDATENSATZFORMAT \_ \_
</dt> <dd>

Das **dwReturn-Member** ist auf eine der folgenden Festgelegt:

-   MCI \_ VCR \_ FORMAT \_ EP
-   MCI \_ VCR \_ FORMAT \_ LP
-   MCI \_ VCR \_ FORMAT \_ OTHER
-   MCI \_ VCR \_ FORMAT \_ SP

</dd> <dt>

<span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>\_ \_ MCI-VCR-STATUSGESCHWINDIGKEIT \_
</dt> <dd>

Das **dwReturn-Member** wird auf die aktuelle Geschwindigkeit festgelegt. Weitere Informationen finden Sie unter dem MCI \_ VCR \_ SET \_ SPEED-Flag des [MCI \_ SET-Befehls.](mci-set.md)

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MCI \_ \_ VCR-STATUSZEITMODUS \_ \_
</dt> <dd>

Das **dwReturn-Member** ist auf eine der folgenden Festgelegt:

-   \_ \_ MCI-VCR-ZEITZÄHLER \_
-   MCI \_ VCR \_ TIME \_ DETECT
-   MCI \_ VCR \_ TIME \_ TIMECODE

Weitere Informationen finden Sie unter dem MCI \_ VCR \_ SET TIME \_ \_ MODE-Flag des [MCI \_ SET-Befehls.](mci-set.md)

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>MCI \_ VCR STATUS TIME TYPE (MCI-VCR-STATUSZEITTYP) \_ \_ \_
</dt> <dd>

Der **dwReturn-Member** wird auf eine Konstante festgelegt, die den aktuellen verwendeten Zeittyp beschreibt (wird von play [,](play.md) [record,](record.md) [seek](seek.md)und so weiter verwendet) und ist eine der folgenden:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_MCI-VCR-ZEITZÄHLER \_ \_
</dt> <dd>

Der Zähler wird verwendet.

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI \_ VCR \_ TIME \_ TIMECODE
</dt> <dd>

Timecode wird verwendet.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>MCI \_ VCR \_ STATUS \_ TIMECODE \_ PRESENT
</dt> <dd>

Das **dwReturn-Member** ist auf **TRUE festgelegt,** wenn der Zeitcode an der aktuellen Position im Inhalt vorhanden ist. andernfalls ist **sie auf FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>MCI \_ VCR \_ STATUS \_ TIMECODE \_ RECORD
</dt> <dd>

Das **dwReturn-Member** ist auf **TRUE festgelegt,** wenn der Zeitcode aufgezeichnet wird, wenn der nächste Datensatzbefehl angegeben wird. andernfalls ist **sie auf FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>\_TIMECODETYP DES MCI-VCR-STATUS \_ \_ \_
</dt> <dd>

Der **dwReturn-Member** ist auf eine Konstante festgelegt, die den Typ des Zeitcodes beschreibt, der direkt vom Gerät unterstützt wird, und ist einer der folgenden:

-   MCI \_ VCR \_ TIMECODE \_ TYPE \_ NONE: Dieses Gerät verwendet keinen Zeitcode.
-   MCI \_ VCR \_ TIMECODE \_ TYPE \_ OTHER: Dieses Gerät verwendet einen nicht angegebenen Zeitcode.
-   MCI \_ VCR \_ TIMECODE \_ TYPE \_ SMPTE: Dieses Gerät verwendet den SMPTE-Zeitcode.
-   MCI \_ VCR \_ TIMECODE \_ TYPE \_ SMPTE DROP: Dieses Gerät verwendet \_ SMPTE Drop Timecode.

</dd> <dt>

<span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>MCI \_ VCR \_ STATUS \_ TUNER \_ CHANNEL
</dt> <dd>

Das **dwReturn-Member** wird auf die aktuelle Kanalnummer festgelegt. Wenn Sie MCI VCR STATUS NUMBER im \_ \_ \_ *dwFlags-Parameter* dieses Befehls angeben, enthält **dwNumber** die logische Tunernummer, für die dieser Befehl gilt.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>VIDEOMONITOR FÜR \_ DEN MCI-VCR-STATUS \_ \_ \_
</dt> <dd>

Das **dwReturn-Element** wird auf eine Konstante festgelegt, die den aktuell ausgewählten Videomonitortyp angibt.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>VIDEOMONITORNUMMER \_ DES MCI-VCR-STATUS \_ \_ \_ \_
</dt> <dd>

Das **dwReturn-Element** wird auf die Nummer des aktuell ausgewählten Videomonitortyps festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>VIDEOAUFZEICHNUNG ZUM \_ MCI-VCR-STATUS \_ \_ \_
</dt> <dd>

Das **dwReturn-Member** ist auf **TRUE festgelegt,** wenn das Video aufgezeichnet wird, wenn der nächste Datensatzbefehl angegeben wird. andernfalls ist **sie auf FALSE** festgelegt. Wenn Sie MCI \_ TRACK im *dwFlags-Parameter* dieses Befehls angeben, enthält **dwTrack** die Spur, für die diese Anfrage gilt.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>VIDEOQUELLE FÜR \_ DEN MCI-VCR-STATUS \_ \_ \_
</dt> <dd>

Das **dwReturn-Element** wird auf eine Konstante festgelegt, die den aktuell ausgewählten Videoquellentyp angibt.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>\_VIDEOQUELLENNUMMER DES MCI-VCR-STATUS \_ \_ \_ \_
</dt> <dd>

Das **dwReturn-Element** wird auf die Nummer des aktuell ausgewählten Videoquellentyps festgelegt.

</dd> <dt>

<span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI \_ VCR \_ STATUS \_ WRITE \_ PROTECTED
</dt> <dd>

Das **dwReturn-Member** ist auf **TRUE festgelegt,** wenn das Medium schreibgeschützt ist. andernfalls ist **sie auf FALSE** festgelegt.

</dd> </dl>

Bei VCR-Geräten verweist *der lpStatus-Parameter* auf eine [**MCI \_ VCR \_ STATUS \_ PARMS-Struktur.**](mci-vcr-status-parms.md)

Wenn Sie das MCI \_ STATUS \_ LENGTH-Flag verwenden, um die Länge des Mediums zu bestimmen, werden für VCR-Geräte immer 2 Stunden zurückgegeben, es sei denn, die Länge wurde mit dem [MCI \_ SET-Befehl](mci-set.md) explizit geändert.

Die folgenden zusätzlichen Flags werden mit dem **Überlagerungsgerätetyp** verwendet. Diese Konstanten werden im **dwItem-Member** der Struktur verwendet, auf die der *lpStatus-Parameter* zeigt, wenn MCI \_ STATUS ITEM für den \_ *dwFlags-Parameter* angegeben wird.

<dl> <dt>

<span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>MCI \_ OVLY \_ STATUS \_ HWND
</dt> <dd>

Der **dwReturn-Member** wird auf das Handle des Fensters festgelegt, das dem Videoüberlagerungsgerät zugeordnet ist.

</dd> <dt>

<span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>MCI \_ OVLY \_ STATUS \_ STRETCH
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn Stretching aktiviert ist. andernfalls ist sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_MCI-STATUSMEDIEN \_ \_ VORHANDEN
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn das Medium in das Gerät eingefügt wird. andernfalls ist sie auf **FALSE** festgelegt.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp **videodisc** verwendet. Diese Konstanten werden im **dwItem-Member** der Struktur verwendet, auf die der *lpStatus-Parameter* zeigt, wenn MCI \_ STATUS ITEM für den \_ *dwFlags-Parameter* angegeben wird.

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_MCI-STATUSMEDIEN \_ \_ VORHANDEN
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn das Medium in das Gerät eingefügt wird. andernfalls ist sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_ \_ MCI-STATUSMODUS
</dt> <dd>

Der **dwReturn-Member** wird auf den aktuellen Modus des Geräts festgelegt. Videodisc-Geräte können die MCI \_ VD \_ MODE \_ PARK-Konstante sowie die Konstanten zurückgeben, die jedes Gerät zurückgeben kann, wie im *dwFlags-Parameter* dokumentiert.

</dd> <dt>

<span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>MCI \_ VD \_ STATUS \_ DISC \_ SIZE
</dt> <dd>

Der **dwReturn-Member** wird auf die Größe des geladenen Datenträgers in Zoll (8 oder 12) festgelegt.

</dd> <dt>

<span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>MCI \_ VD \_ STATUS \_ FORWARD
</dt> <dd>

Das **dwReturn-Element** wird auf **TRUE** festgelegt, wenn es weitergespielt wird. andernfalls ist sie auf **FALSE** festgelegt.

Das MCI-Videodisc-Gerät unterstützt dieses Flag nicht.

</dd> <dt>

<span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>MCI \_ VD \_ STATUS \_ MEDIA \_ TYPE
</dt> <dd>

Der **dwReturn-Member** wird auf den Medientyp des eingefügten Mediums festgelegt. Die folgenden Medientypen können zurückgegeben werden:

MCI \_ VD \_ MEDIA \_ CAV

MCI \_ VD \_ MEDIA \_ CLV

MCI \_ VD \_ MEDIA \_ OTHER

</dd> <dt>

<span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>MCI \_ \_ VD-STATUSSEITE \_
</dt> <dd>

Der **dwReturn-Member** ist auf 1 oder 2 festgelegt, um anzugeben, welche Seite des Datenträgers geladen wird. Nicht alle videodisc-Geräte unterstützen dieses Flag.

</dd> <dt>

<span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>MCI \_ VD \_ STATUS \_ SPEED
</dt> <dd>

Der **dwReturn-Member** wird auf die Wiedergabegeschwindigkeit in Frames pro Sekunde festgelegt. Der MCIPIONR. Der DRV-Gerätetreiber gibt MCIERR \_ UNSUPPORTED \_ FUNCTION zurück.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **Gerätetyp waveaudio** verwendet. Diese Konstanten werden im **dwItem-Member** der Struktur verwendet, auf die der *lpStatus-Parameter* zeigt, wenn MCI \_ STATUS ITEM für den \_ *dwFlags-Parameter* angegeben wird.

<dl> <dt>

<span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI \_ WAVE \_ FORMATTAG
</dt> <dd>

Der **dwReturn-Member** wird auf das aktuelle Formattag festgelegt, das zum Wiedergeben, Aufzeichnen und Speichern verwendet wird.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ INPUT
</dt> <dd>

Der **dwReturn-Member** wird auf das Welleneingabegerät festgelegt, das für die Aufzeichnung verwendet wird. Wenn kein Gerät verwendet wird und kein Gerät explizit festgelegt wurde, wird der Fehler MCIERR \_ WAVE \_ INPUTUNSPECIFIED zurückgegeben.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ \_ WAVE-AUSGABE
</dt> <dd>

Der **dwReturn-Member** wird auf das Wellenausgabegerät festgelegt, das für die Wiedergabe verwendet wird. Wenn kein Gerät verwendet wird und kein Gerät explizit festgelegt wurde, wird der Fehler MCIERR \_ WAVE \_ OUTPUTUNSPECIFIED zurückgegeben.

</dd> <dt>

<span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>MCI \_ WAVE \_ STATUS \_ AVGBYTESPERSEC
</dt> <dd>

Der **dwReturn-Member** wird auf die aktuellen Bytes pro Sekunde festgelegt, die zum Wiedergeben, Aufzeichnen und Speichern verwendet werden.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>MCI \_ WAVE \_ STATUS \_ BITSPERSAMPLE
</dt> <dd>

Der **dwReturn-Member** wird auf die aktuellen Bits pro Stichprobe festgelegt, die zum Wiedergeben, Aufzeichnen und Speichern pcm-formatierter Daten verwendet werden.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>MCI \_ WAVE \_ STATUS \_ BLOCKALIGN
</dt> <dd>

Der **dwReturn-Member** wird auf die aktuelle Blockausrichtung festgelegt, die zum Wiedergeben, Aufzeichnen und Speichern verwendet wird.

</dd> <dt>

<span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>MCI \_ WAVE \_ STATUS \_ CHANNELS
</dt> <dd>

Der **dwReturn-Member** wird auf die aktuelle Kanalanzahl festgelegt, die zum Wiedergeben, Aufzeichnen und Speichern verwendet wird.

</dd> <dt>

<span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>MCI \_ WAVE \_ STATUS \_ LEVEL
</dt> <dd>

Der **dwReturn-Member** wird auf die aktuelle Aufzeichnungs- oder Wiedergabeebene von PCM-formatierten Daten festgelegt. Der Wert wird abhängig von der verwendeten Stichprobengröße als 8- oder 16-Bit-Wert zurückgegeben. Die rechte oder Monokanalebene wird im Wort mit niedriger Reihenfolge zurückgegeben. Die linke Kanalebene wird im Hochordnungswort zurückgegeben.

</dd> <dt>

<span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>MCI \_ WAVE \_ STATUS \_ SAMPLESPERSEC
</dt> <dd>

Der **dwReturn-Member** wird auf die aktuellen Stichproben pro Sekunde festgelegt, die zum Wiedergeben, Aufzeichnen und Speichern verwendet werden.

</dd> </dl>

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
</dt> <dt>

[MCI \_ CUT](mci-cut.md)
</dt> <dt>

[MCI \_ DELETE](mci-delete.md)
</dt> <dt>

[\_MCI-EINFÜGE](mci-paste.md)
</dt> <dt>

[MCI \_ RESERVE](mci-reserve.md)
</dt> <dt>

[MCI \_ SET](mci-set.md)
</dt> <dt>

[Spielen](play.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[Suchen](seek.md)
</dt> </dl>

 

