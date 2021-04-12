---
title: MCI_GETDEVCAPS Befehl (MMSYSTEM. h)
description: Der MCI \_ getdevcaps-Befehl ruft statische Informationen zu einem Gerät ab.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- MCI_GETDEVCAPS Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85abb0354d36979741d0b292dd9def469cec0049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519043"
---
# <a name="mci_getdevcaps-command"></a>MCI \_ getdevcaps-Befehl

Der MCI \_ getdevcaps-Befehl ruft statische Informationen zu einem Gerät ab. Alle Geräte erkennen diesen Befehl. Welche Parameter und Flags für diesen Befehl verfügbar sind, hängt vom ausgewählten Gerät ab. Informationen werden im **dwreturn** -Member der von *lpcapsparms* identifizierten Struktur zurückgegeben.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
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

<span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpcapsparms*
</dt> <dd>

Zeiger auf eine [**MCI \_ getdevcaps \_**](mci-getdevcaps-parms.md) -Parameter Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Standard-und Befehls spezifischen Flags gelten für alle Geräte, die MCI \_ getdevcaps unterstützen:

<dl> <dt>

<span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>MCI \_ getdevcaps- \_ Verbund \_ Gerät
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät Datenspeicher verwendet, das explizit geöffnet und geschlossen werden muss. Andernfalls wird **false** festgelegt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>MCI \_ getdevcaps \_ - \_ Gerätetyp
</dt> <dd>

Der **dwreturn** -Member wird auf einen der Werte festgelegt, die unter [MCI-Gerätetypen](mci-device-types.md)aufgeführt sind.

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ getdevcaps \_ hat \_ Audiodaten
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät über eine Audioausgabe verfügt. Andernfalls wird **false** festgelegt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ getdevcaps \_ hat \_ Video
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät über eine Videoausgabe verfügt. Andernfalls wird **false** festgelegt. Beispielsweise ist der-Member für Geräte, die den Videodisk-Befehlssatz unterstützen, auf **true** festgelegt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI \_ getdevcaps- \_ Element
</dt> <dd>

Gibt an, dass das **dwitem** -Element der MCI-Struktur " [**\_ getdevcaps \_**](mci-getdevcaps-parms.md) " eine der folgenden Konstanten enthält:

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI \_ getdevcaps \_ kann \_ auswerfen
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät die Medien auswerfen kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI \_ getdevcaps kann wiedergegeben werden \_ \_
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät die Medien wiedergeben kann. Andernfalls wird Sie auf " **false**" festgelegt. Wenn ein Gerät den Wert **true** angibt, bedeutet dies, dass das Gerät die Befehle [MCI \_ Pause](mci-pause.md) und [ \_ MCI](mci-stop.md) -Befehl sowie den Befehl [MCI \_ Play](mci-play.md) unterstützt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI \_ getdevcaps \_ kann \_ aufzeichnen
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Gerät eine Aufzeichnung unterstützt. Andernfalls wird Sie auf " **false**" festgelegt. Wenn ein Gerät **true** angibt, bedeutet dies, dass das Gerät die Befehle MCI \_ Anhalten und MCI- \_ Befehl sowie den Befehl [MCI- \_ Datensatz](mci-record.md) unterstützt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI \_ getdevcaps \_ kann \_ Speichern
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät eine Datei speichern kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ getdevcaps \_ verwendet \_ Dateien
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn für das Gerät ein Dateiname erforderlich ist. Andernfalls wird **false** festgelegt. Dateien werden nur von Verbund Geräten verwendet.

</dd> </dl>

Die folgenden Flags können im **dwitem** -Member von [**MCI \_ getdevcaps- \_ Parametern**](mci-getdevcaps-parms.md) für den **Digitalvideo** -Gerätetyp angegeben werden:

<dl> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ getdevcaps \_ kann \_ eingefroren werden
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät Frames Einfrieren kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ getdevcaps \_ kann \_ Sperren
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät gesperrt werden kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI \_ DGV \_ getdevcaps \_ kann \_ umkehren
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Gerät in umgekehrter Reihenfolge wiedergegeben werden kann Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ getdevcaps \_ kann \_ Str \_ werden
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Gerät Eingaben ausdehnen kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI \_ DGV \_ getdevcaps \_ kann \_ gestreckt werden
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät ein Bildstrecken kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI \_ DGV \_ getdevcaps \_ kann \_ Testen
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät Tests ausführen kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ getdevcaps \_ hat \_ weiterhin
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät weiterhin Bilder anzeigen kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ getdevcaps ( \_ Max. \_ Fenster)
</dt> <dd>

Der **dwreturn** -Member ist auf die maximale Anzahl von Fenstern festgelegt, die das Gerät gleichzeitig verarbeiten kann.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>MCI \_ DGV \_ getdevcaps- \_ höchst \_ Rate
</dt> <dd>

Der **dwreturn** -Member wird auf die maximale Wiedergabe Rate für das Gerät in Frames pro Sekunde festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>minimale Rate der MCI \_ DGV- \_ getdevcaps \_ \_
</dt> <dd>

Der **dwreturn** -Member wird auf die minimale Wiedergabe Rate für das Gerät in Frames pro Sekunde festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>MCI \_ DGV \_ getdevcaps- \_ Paletten
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät einen Palettenhandle zurückgeben kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> </dl>

Die folgenden Flags können für den **VCR** -Gerätetyp im Element " **dwitem** " von [**MCI \_ getdevcaps- \_ Parametern**](mci-getdevcaps-parms.md) angegeben werden:

<dl> <dt>

<span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>MCI \_ getdevcaps- \_ Takt \_ Inkrement- \_ Rate
</dt> <dd>

Der **dwreturn** -Member wird auf die Anzahl der Inkremente pro Sekunde festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI \_ VCR \_ getdevcaps \_ kann \_ die \_ Länge erkennen
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät die Länge des Mediums erkennen kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI \_ VCR \_ getdevcaps \_ kann \_ eingefroren werden.
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät das Ausgabe Bild Einfrieren kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI \_ VCR \_ getdevcaps \_ kann \_ Quellen überwachen \_
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät Quellen überwachen kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI \_ VCR \_ getdevcaps \_ kann \_ vorab
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät über ein vorab Element verfügen kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI \_ VCR \_ getdevcaps \_ kann eine \_ Vorschau anzeigen
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät Vorschau Versionen unterstützt. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI \_ VCR \_ getdevcaps \_ kann \_ umkehren
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Gerät in umgekehrter Reihenfolge wiedergegeben werden kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI \_ VCR \_ getdevcaps \_ kann \_ Testen
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät getestet werden kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI \_ VCR \_ getdevcaps \_ hat \_ Clock
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät eine externe Uhr unterstützt. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI \_ VCR \_ getdevcaps \_ hat \_ Timecode
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Gerät über eine Zeitcode-Funktion verfügt oder wenn diese Funktion unbekannt ist. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>MCI \_ VCR \_ getdevcaps- \_ Anzahl \_ von \_ Markierungen
</dt> <dd>

Der **dwreturn** -Member wird auf die Anzahl der Markierungen (99) festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI \_ VCR \_ getdevcaps- \_ Such \_ Genauigkeit
</dt> <dd>

Der **dwreturn** -Member ist auf die Such Genauigkeit des Geräts festgelegt.

</dd> </dl>

Die folgenden Flags können im **dwitem** -Member von [**MCI \_ getdevcaps- \_ Parametern**](mci-getdevcaps-parms.md) für den **Überlagerungs** Gerätetyp angegeben werden:

<dl> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ OVLY \_ getdevcaps \_ kann \_ eingefroren werden.
</dt> <dd>

Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät das Image Einfrieren kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI \_ OVLY \_ getdevcaps \_ kann \_ gestreckt werden
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Gerät das Bild zum Ausfüllen des Frames Strecken kann. Andernfalls wird Sie auf " **false**" festgelegt.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ getdevcaps ( \_ Max. \_ Fenster)
</dt> <dd>

Der **dwreturn** -Member ist auf die maximale Anzahl von Fenstern festgelegt, die das Gerät gleichzeitig verarbeiten kann.

</dd> </dl>

Die folgenden Flags können im **dwitem** -Member von [**MCI \_ getdevcaps- \_ Parametern**](mci-getdevcaps-parms.md) für den **Videodisk** -Gerätetyp angegeben werden:

<dl> <dt>

<span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI- \_ VD- \_ getdevcaps \_ können \_ umkehren
</dt> <dd>

Der **dwreturn** -Member ist auf **true** festgelegt, wenn der Videodisk-Player in umgekehrter Richtung wiedergegeben werden kann Andernfalls wird Sie auf " **false**" festgelegt. Einige Spieler können CLV-Scheiben in umgekehrter Reihenfolge und in den CAV-Bild Platten wiedergeben.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI- \_ VD \_ getdevcaps- \_ CAV
</dt> <dd>

Gibt bei Kombination mit anderen Elementen an, dass die Rückgabe Informationen auf Videodisks im CAV-Format gelten. Dies ist die Standardeinstellung, wenn keine Video Disk eingefügt wird.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ VD \_ getdevcaps \_ CLV
</dt> <dd>

Gibt bei Kombination mit anderen Elementen an, dass die Rückgabe Informationen auf Videodisks im CLV-Format zutreffen.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>schnelle Rate der MCI- \_ VD- \_ getdevcaps \_ \_
</dt> <dd>

Das **dwreturn** -Element wird auf die standardmäßige schnelle Wiedergabe Rate in Frames pro Sekunde festgelegt.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>MCI- \_ VD- \_ getdevcaps- \_ Normal \_ Rate
</dt> <dd>

Der **dwreturn** -Member wird auf die normale Wiedergabe Rate in Frames pro Sekunde festgelegt.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>langsame MCI- \_ VD- \_ getdevcaps- \_ \_ Rate
</dt> <dd>

Der **dwreturn** -Member ist auf die standardmäßige langsame Wiedergabe Rate in Frames pro Sekunde festgelegt.

</dd> </dl>

Die folgenden Flags können im **dwitem** -Member von [**MCI \_ getdevcaps- \_ Parametern**](mci-getdevcaps-parms.md) für den **waveaudiogerätetyp** angegeben werden:

<dl> <dt>

<span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>MCI- \_ Wave \_ getdevcaps- \_ Eingabe
</dt> <dd>

Das **dwreturn** -Element wird auf die Gesamtzahl der Wellenform-Eingabegeräte (Aufzeichnung) festgelegt.

</dd> <dt>

<span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>MCI- \_ Wave \_ getdevcaps- \_ Ausgabe
</dt> <dd>

Der **dwreturn** -Member ist auf die Gesamtzahl der Wellen Geräte-Ausgabegeräte (Wiedergabe) festgelegt.

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

 

