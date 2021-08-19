---
title: MCI_GETDEVCAPS Befehl (Mmsystem.h)
description: Der MCI \_ GETDEVCAPS-Befehl ruft statische Informationen zu einem Gerät ab.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- MCI_GETDEVCAPS Befehl Windows Multimedia
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
ms.openlocfilehash: 7798f72405209f9834c3b67f84e57508c58ffc6153bce860b91f089005648905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803952"
---
# <a name="mci_getdevcaps-command"></a>MCI \_ GETDEVCAPS-Befehl

Der MCI \_ GETDEVCAPS-Befehl ruft statische Informationen zu einem Gerät ab. Dieser Befehl wird von allen Geräten erkannt. Welche Parameter und Flags für diesen Befehl verfügbar sind, hängt vom ausgewählten Gerät ab. Informationen werden im **dwReturn-Member** der durch *lpCapsParms identifizierten* Struktur zurückgegeben.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsmeldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder, für Digital Video- und VCR-Geräte, MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*
</dt> <dd>

Zeiger auf eine [**\_ MCI-GETDEVCAPS-PARMS-Struktur. \_**](mci-getdevcaps-parms.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden zusätzlichen standard- und befehlsspezifischen Flags gelten für alle Geräte, die MCI \_ GETDEVCAPS unterstützen:

<dl> <dt>

<span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>MCI \_ GETDEVCAPS \_ COMPOUND \_ DEVICE
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn das Gerät Datenspeicherung verwendet, die explizit geöffnet und geschlossen werden muss. andernfalls ist sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>MCI \_ \_ GETDEVCAPS-GERÄTETYP \_
</dt> <dd>

Der **dwReturn-Member** wird auf einen der Werte festgelegt, die unter [MCI-Gerätetypen](mci-device-types.md)aufgeführt sind.

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ GETDEVCAPS \_ VERFÜGT ÜBER \_ AUDIO
</dt> <dd>

Der **dwReturn-Member** ist auf **TRUE** festgelegt, wenn das Gerät über eine Audioausgabe verfügt. andernfalls ist sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ GETDEVCAPS \_ HAT \_ VIDEO
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn das Gerät über eine Videoausgabe verfügt. andernfalls ist sie auf **FALSE** festgelegt. Beispielsweise wird der Member für Geräte, die den Videodisc-Befehlssatz unterstützen, auf **TRUE** festgelegt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI \_ GETDEVCAPS-ELEMENT \_
</dt> <dd>

Gibt an, dass der **dwItem-Member** der [**MCI \_ GETDEVCAPS \_ PARMS-Struktur**](mci-getdevcaps-parms.md) eine der folgenden Konstanten enthält:

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI \_ GETDEVCAPS \_ KANN \_ AUSWERFEN
</dt> <dd>

Der **dwReturn-Member** ist auf **TRUE** festgelegt, wenn das Gerät das Medium auswerfen kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI \_ GETDEVCAPS \_ KANN WIEDERGEGEBEN \_ WERDEN
</dt> <dd>

Der **dwReturn-Member** ist auf **TRUE** festgelegt, wenn das Gerät die Medien wiedergeben kann. Andernfalls wird sie auf **FALSE** festgelegt. Wenn ein Gerät **TRUE** angibt, impliziert dies, dass das Gerät die Befehle [MCI \_ PAUSE](mci-pause.md) und [MCI \_ STOP](mci-stop.md) sowie den [MCI \_ PLAY-Befehl](mci-play.md) unterstützt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI \_ GETDEVCAPS \_ CAN \_ RECORD
</dt> <dd>

Der **dwReturn-Member** ist auf **TRUE** festgelegt, wenn das Gerät die Aufzeichnung unterstützt. Andernfalls wird sie auf **FALSE** festgelegt. Wenn ein Gerät **TRUE** angibt, impliziert dies, dass das Gerät die Befehle MCI \_ PAUSE und MCI STOP sowie den \_ [MCI \_ RECORD-Befehl](mci-record.md) unterstützt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI \_ GETDEVCAPS \_ KANN GESPEICHERT \_ WERDEN
</dt> <dd>

Das **dwReturn-Element** ist auf **TRUE** festgelegt, wenn das Gerät eine Datei speichern kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ GETDEVCAPS \_ VERWENDET \_ DATEIEN
</dt> <dd>

Das **dwReturn-Element** wird auf **TRUE** festgelegt, wenn das Gerät einen Dateinamen erfordert. andernfalls ist sie auf **FALSE** festgelegt. Nur Verbundgeräte verwenden Dateien.

</dd> </dl>

Die folgenden Flags können im **dwItem-Member** von [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) für den **Digitalvideo-Gerätetyp** angegeben werden:

<dl> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ GETDEVCAPS \_ KANN \_ EINFRIEREN
</dt> <dd>

Der **dwReturn-Member** ist auf **TRUE** festgelegt, wenn das Gerät Frames einfrieren kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ GETDEVCAPS \_ CAN \_ LOCK
</dt> <dd>

Der **dwReturn-Member** ist auf **TRUE** festgelegt, wenn das Gerät gesperrt werden kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI \_ DGV \_ GETDEVCAPS \_ KANN \_ UMKEHREN
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn das Gerät umgekehrt wiedergegeben werden kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ CAN \_ STR \_ IN
</dt> <dd>

Der **dwReturn-Member** ist auf **TRUE** festgelegt, wenn das Gerät Eingaben strecken kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI \_ DGV \_ GETDEVCAPS \_ CAN \_ STRETCH
</dt> <dd>

Das **dwReturn-Element** wird auf **TRUE** festgelegt, wenn das Gerät ein Bild strecken kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI \_ DGV \_ GETDEVCAPS \_ KANN \_ TESTEN
</dt> <dd>

Das **dwReturn-Element** ist auf **TRUE** festgelegt, wenn das Gerät Tests ausführen kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ GETDEVCAPS \_ HAT \_ NOCH
</dt> <dd>

Das **dwReturn-Element** ist auf **TRUE** festgelegt, wenn das Gerät Standbilder anzeigen kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ GETDEVCAPS \_ MAX \_ WINDOWS
</dt> <dd>

Der **dwReturn-Member** wird auf die maximale Anzahl von Fenstern festgelegt, die das Gerät gleichzeitig verarbeiten kann.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>MCI \_ DGV \_ GETDEVCAPS \_ MAXIMUM \_ RATE
</dt> <dd>

Der **dwReturn-Member** wird auf die maximale Wiedergaberate für das Gerät in Frames pro Sekunde festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>MINDESTRATE FÜR MCI \_ DGV \_ GETDEVCAPS \_ \_
</dt> <dd>

Das **dwReturn-Element** wird auf die minimale Wiedergaberate für das Gerät in Frames pro Sekunde festgelegt.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>MCI \_ DGV \_ GETDEVCAPS \_ PALETTEN
</dt> <dd>

Der **dwReturn-Member** ist auf **TRUE** festgelegt, wenn das Gerät ein Palettenhandle zurückgeben kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> </dl>

Die folgenden Flags können im **dwItem-Member** von [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) für den **vcr-Gerätetyp** angegeben werden:

<dl> <dt>

<span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>MCI \_ GETDEVCAPS \_ CLOCK \_ INCREMENT \_ RATE
</dt> <dd>

Das **dwReturn-Element** wird auf die Anzahl der Inkremente pro Sekunde festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI \_ VCR \_ GETDEVCAPS \_ KANN \_ LÄNGE ERKENNEN \_
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn das Gerät die Länge des Mediums erkennen kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI \_ VCR \_ GETDEVCAPS \_ KANN \_ EINFRIEREN
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn das Gerät in der Lage ist, das Ausgabebild einzufrieren. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI \_ VCR \_ GETDEVCAPS \_ KANN \_ QUELLEN ÜBERWACHEN \_
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn das Gerät Quellen überwachen kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI \_ VCR \_ GETDEVCAPS \_ CAN \_ PREROLL
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn das Gerät eine Vorabrolling ermöglicht. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI \_ VCR \_ GETDEVCAPS \_ CAN \_ PREVIEW
</dt> <dd>

Das **dwReturn-Element** wird auf **TRUE** festgelegt, wenn das Gerät vorschaufähig ist. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI \_ VCR \_ GETDEVCAPS \_ KANN \_ UMKEHREN
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn das Gerät umgekehrt wiedergegeben werden kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI \_ VCR \_ GETDEVCAPS \_ KANN \_ TESTEN
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn das Gerät getestet werden kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI \_ VCR \_ GETDEVCAPS \_ HAT \_ UHR
</dt> <dd>

Das **dwReturn-Element** wird auf **TRUE** festgelegt, wenn das Gerät eine externe Uhr unterstützt. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI \_ VCR \_ GETDEVCAPS \_ HAT \_ TIMECODE
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn das Gerät über eine Timecodefunktion verfügt oder diese Funktion unbekannt ist. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>MCI \_ VCR \_ GETDEVCAPS \_ NUMBER \_ OF \_ MARKS
</dt> <dd>

Das **dwReturn-Element** wird auf die Anzahl der Markierungen (99) festgelegt.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI \_ VCR \_ GETDEVCAPS \_ SEEK \_ ACCURACY
</dt> <dd>

Das **dwReturn-Element** wird auf die Suchgenauigkeit des Geräts festgelegt.

</dd> </dl>

Die folgenden Flags können im **dwItem-Member** von [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) für den **Overlaygerätetyp** angegeben werden:

<dl> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ OVLY \_ GETDEVCAPS \_ KANN \_ EINFRIEREN
</dt> <dd>

Das **dwReturn-Element** wird auf **TRUE** festgelegt, wenn das Gerät das Image einfrieren kann. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI \_ OVLY \_ GETDEVCAPS \_ CAN \_ STRETCH
</dt> <dd>

Das **dwReturn-Element** wird auf **TRUE** festgelegt, wenn das Gerät das Bild strecken kann, um den Frame zu füllen. Andernfalls wird sie auf **FALSE** festgelegt.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ GETDEVCAPS \_ MAX \_ WINDOWS
</dt> <dd>

Der **dwReturn-Member** wird auf die maximale Anzahl von Fenstern festgelegt, die das Gerät gleichzeitig verarbeiten kann.

</dd> </dl>

Die folgenden Flags können im **dwItem-Member** von [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) für den **Gerätetyp videodisc** angegeben werden:

<dl> <dt>

<span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI \_ VD \_ GETDEVCAPS \_ KANN \_ UMKEHREN
</dt> <dd>

Der **dwReturn-Member** wird auf **TRUE** festgelegt, wenn der Videodisc-Player umgekehrt wiedergegeben werden kann. Andernfalls wird sie auf **FALSE** festgelegt. Einige Player können CLV-Datenträger in umgekehrter Reihenfolge sowie CAV-Datenträger wiedergeben.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ VD \_ GETDEVCAPS \_ CAV
</dt> <dd>

Gibt in Kombination mit anderen Elementen an, dass die Rückgabeinformationen für videodiscs im CAV-Format gelten. Dies ist die Standardeinstellung, wenn keine videodisc eingefügt wird.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ VD \_ GETDEVCAPS \_ CLV
</dt> <dd>

Gibt in Kombination mit anderen Elementen an, dass die Rückgabeinformationen für videodiscs im CLV-Format gelten.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ FAST \_ RATE
</dt> <dd>

Das **dwReturn-Element** wird auf die standardmäßige schnelle Wiedergaberate in Frames pro Sekunde festgelegt.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ NORMAL \_ RATE
</dt> <dd>

Der **dwReturn-Member** wird auf die normale Wiedergaberate in Frames pro Sekunde festgelegt.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ SLOW \_ RATE
</dt> <dd>

Der **dwReturn-Member** wird auf die standard langsame Wiedergaberate in Frames pro Sekunde festgelegt.

</dd> </dl>

Die folgenden Flags können im **dwItem-Member** von [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) für den **Waveaudio-Gerätetyp** angegeben werden:

<dl> <dt>

<span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>MCI \_ WAVE \_ GETDEVCAPS \_ INPUT
</dt> <dd>

Das **dwReturn-Element** wird auf die Gesamtzahl der Geräte für die Wellenformeingabe (Aufzeichnung) festgelegt.

</dd> <dt>

<span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>MCI \_ WAVE \_ GETDEVCAPS-AUSGABE \_
</dt> <dd>

Das **dwReturn-Element** wird auf die Gesamtzahl der Waveformausgabegeräte (Wiedergabegeräte) festgelegt.

</dd> </dl>

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

 

