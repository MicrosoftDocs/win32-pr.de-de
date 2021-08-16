---
title: MCI_SETAUDIO Befehl (Mmsystem.h)
description: Der MCI \_ SETAUDIO-Befehl legt Werte fest, die der Audiowiedergabe und -erfassung zugeordnet sind. DigitalVideo- und VCR-Geräte erkennen diesen Befehl.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- MCI_SETAUDIO Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SETAUDIO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b882209b8a9debc2c01e4f5c6f852d418c1a5cd321a764af022d19c58fe32a21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803397"
---
# <a name="mci_setaudio-command"></a>MCI \_ SETAUDIO-Befehl

Der MCI \_ SETAUDIO-Befehl legt Werte fest, die der Audiowiedergabe und -erfassung zugeordnet sind. DigitalVideo- und VCR-Geräte erkennen diesen Befehl.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETAUDIO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetAudio
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

MCI \_ NOTIFY, MCI \_ WAIT oder MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*
</dt> <dd>

Zeiger auf eine [**GENERISCHE \_ MCI-PARMS-Struktur. \_**](mci-generic-parms.md) (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden Flags gelten für den **Gerätetyp digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI \_ DGV \_ SETAUDIO \_ ALG
</dt> <dd>

Der **lpstrAlgorithm-Member** der von *lpSetAudio* identifizierten Struktur enthält eine Adresse eines Puffers, der den Namen eines Audiokomprimierungsalgorithmus enthält. Der Komprimierungsalgorithmus wird von nachfolgenden [MCI \_ RESERVE-](mci-reserve.md) oder [MCI \_ RECORD-Befehlen](mci-record.md) verwendet. Die verfügbaren Algorithmen sind geräteabhängig. Wenn der Algorithmus nicht mit dem aktuellen Dateiformat kompatibel ist, wird das Dateiformat in das Standardformat für den Algorithmus geändert.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI \_ DGV \_ SETAUDIO \_ CLOCKTIME
</dt> <dd>

Die angegebene Zeit beträgt in Millisekunden und ist die absolute Zeit, wenn sie mit MCI \_ DGV \_ SETAUDIO OVER verwendet \_ wird. (Dieses Mal ist die Wiedergabe des Arbeitsbereichs nicht schrittweise.)

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>MCI \_ DGV \_ SETAUDIO \_ INPUT
</dt> <dd>

Ändert das Kennzeichen für Denker, Treble oder Lautstärke, sodass es sich auf das Eingabesignal auswirkt und ändert, was aufgezeichnet wird. Wenn möglich, ist dies die Standardeinstellung beim Überwachen der Eingabe.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>MCI \_ DGV \_ SETAUDIO \_ ITEM
</dt> <dd>

Eine Audiokonstante wird im **dwItem-Member** der durch *lpSetAudio* identifizierten Struktur angegeben. Die Konstante identifiziert den Wert, der festgelegt wird. Die folgenden Konstanten werden definiert:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI \_ DGV \_ SETAUDIO \_ AVGBYTESPERSEC
</dt> <dd>

Die durchschnittliche Anzahl von Bytes wird im **dwValue-Member** der durch *lpSetAudio* identifizierten Struktur angegeben. Dieser Wert legt die durchschnittliche Anzahl von Bytes pro Sekunde für die Wiedergabe oder Aufzeichnung in den Formaten PCM (Pulse Code Bytes) und ADPCM (Adaptive Differential Pulse Code Code) fest. Die Datei wird in diesem Format gespeichert.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI \_ DGV \_ SETAUDIO \_ HEXADEZI
</dt> <dd>

Die niedrige Audiofrequenzebene wird als Faktor im **dwValue-Member** der durch *lpSetAudio* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI \_ DGV \_ SETAUDIO \_ BITSPERSAMPLE
</dt> <dd>

Die Anzahl der Bits pro Stichprobe wird im **dwValue-Member** der durch *lpSetAudio* identifizierten Struktur angegeben. Dieser Wert legt die Anzahl der Bits pro wiedergegebener oder aufgezeichneter Stichprobe im PCM-Format fest. Die Datei wird in diesem Format gespeichert.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI \_ DGV \_ SETAUDIO \_ BLOCKALIGN
</dt> <dd>

Die Datenblockausrichtung wird im **dwValue-Member** der durch *lpSetAudio* identifizierten Struktur angegeben. Dieser Wert legt die Ausrichtung von Datenblöcken relativ zum Anfang der Eingabe von Wellenformdaten fest.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI \_ DGV \_ SETAUDIO \_ SAMPLESPERSEC
</dt> <dd>

Die Abtastrate wird im **dwValue-Member** der durch *lpSetAudio* identifizierten Struktur angegeben. Dieser Wert legt die Abtastrate für die Wiedergabe und Aufzeichnung mit den ALGORITHMEN PCM und ADPCM fest. Die Datei wird in diesem Format gespeichert.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>MCI \_ DGV \_ SETAUDIO \_ SOURCE
</dt> <dd>

Eine Konstante, die die Quelle der Audioeingabe angibt, ist im **dwValue-Member** der struktur enthalten, die durch *lpSetAudio* identifiziert wird. Die folgenden Konstanten werden für die Audioeingabequellen definiert:

MCI \_ DGV \_ SETAUDIO \_ SOURCE \_ AVERAGE

Der Durchschnitt der linken und rechten Audiokanäle.

MCI \_ DGV \_ SETAUDIO \_ SOURCE \_ LEFT

Linker Audiokanal.

MCI \_ DGV \_ SETAUDIO \_ SOURCE \_ RIGHT

Richtiger Audiokanal.

MCI \_ DGV \_ SETAUDIO \_ SOURCE \_ STEREO

Stereo.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>MCI \_ DGV \_ SETAUDIO \_ STREAM
</dt> <dd>

Ein Audiostream wird im **dwValue-Member** der durch *lpSetAudio* identifizierten Struktur angegeben. Der ganzzahlige Wert gibt den Audiostream an, der aus dem Arbeitsbereich wiedergegeben wird. Wenn der Stream nicht angegeben ist, wird der erste physisch verschachtelte Audiodatenstrom wiedergegeben.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI \_ DGV \_ SETAUDIO \_ TREBLE
</dt> <dd>

Die hochfrequente Audioebene wird als Faktor im **dwValue-Member** der durch *lpSetAudio* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>MCI \_ DGV \_ SETAUDIO \_ VOLUME
</dt> <dd>

Die Audioebene für einen oder beide Audiokanäle wird als Faktor im **dwValue-Member** der struktur angegeben, die durch *lpSetAudio* identifiziert wird. Wenn das linke und das rechte Volume auf unterschiedliche Werte festgelegt wurden, ist das Verhältnis von volume von links nach rechts ungefähr unverändert.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ SETAUDIO \_ LEFT
</dt> <dd>

Aktiviert den linken Audiokanal bei Verwendung mit MCI \_ SET \_ ON. Deaktiviert den linken Audiokanal bei Verwendung mit MCI \_ SET \_ OFF. Wenn dieses Flag mit der Kombination aus MCI \_ DGV \_ SETAUDIO \_ VALUE und MCI \_ DGV \_ SETAUDIO VOLUME verwendet \_ wird, wird die Lautstärke des linken Audiokanals festgelegt. Wenn dieses Flag mit MCI \_ DGV \_ SETAUDIO SOURCE verwendet \_ wird, gibt es den linken Audiokanal als Quelle für den Audioeingabedigitalisierer an.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ DGV \_ SETAUDIO \_ OVER
</dt> <dd>

Ein Parameter für die Übergangslänge ist im **dwOver-Member** der durch *lpSetAudio* identifizierten Struktur enthalten. Der Längenwert gibt an, wie lange (in Einheiten des aktuellen Zeitformats) es dauern soll, eine Änderung vorzunehmen, die einen Faktor verwendet. Wenn dieses Flag nicht verwendet wird, treten sofort Änderungen auf.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI \_ DGV \_ SETAUDIO \_ QUALITY
</dt> <dd>

Der **lpstrQuality-Member** der von *lpSetAudio* identifizierten Struktur enthält eine Adresse eines Puffers, der die Audioqualität definiert. Eine Textzeichenfolge innerhalb des Puffers gibt die Merkmale des Audiokomprimierungsalgorithmus an.

Das MCI \_ DGV \_ SETAUDIO \_ ALG-Flag kann verwendet werden, um einen Qualitätsdeskriptor für den angegebenen Algorithmus auszuwählen. Wenn dieses Flag ausgelassen wird, wird der aktuelle Algorithmus verwendet.

Die verfügbaren Algorithmen und Deskriptornamen hängen vom Gerät ab. Jedes Gerät stellt Dokumentation für die verfügbaren Algorithmen und eine Beschreibung der entsprechenden Deskriptornamen bereit. Der [MCI \_ QUALITY-Befehl](mci-quality.md) kann zusätzliche Deskriptornamen definieren.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>MCI \_ DGV \_ SETAUDIO \_ RECORD
</dt> <dd>

Gibt an, ob die Aufzeichnung Audiodaten ein- oder ausschließt. In Kombination mit MCI \_ SET \_ ON werden Audiodaten aufgezeichnet. In Kombination mit MCI \_ SET \_ OFF werden Audiodaten ausgeschlossen. Die Standardeinstellung umfasst Audiodaten.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ RIGHT
</dt> <dd>

Aktiviert den richtigen Audiokanal bei Verwendung mit MCI \_ SET \_ ON. Deaktiviert den richtigen Audiokanal bei Verwendung mit MCI \_ SET \_ OFF. Wenn dieses Flag mit der Kombination aus MCI \_ DGV \_ SETAUDIO \_ VALUE und MCI \_ DGV \_ SETAUDIO VOLUME verwendet \_ wird, wird die Lautstärke des richtigen Audiokanals festgelegt.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>MCI \_ DGV \_ SETAUDIO-WERT \_
</dt> <dd>

Ein Wert wird im **dwValue-Member** der -Struktur angegeben, die durch *lpSetAudio identifiziert wird.* Die Bedeutung des Werts wird durch die Konstante angegeben, die für das MCI \_ DGV \_ SETAUDIO \_ ITEM-Flag definiert ist.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ SET \_ OFF
</dt> <dd>

Deaktiviert den angegebenen Audiokanal.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ SET \_ ON
</dt> <dd>

Aktiviert den angegebenen Audiokanal.

</dd> <dt>

<span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>MCI \_ SETAUDIO-AUSGABE \_
</dt> <dd>

Ändert das Flag "1", "Treble" oder "Volume", sodass nur das abgespielte Signal und nicht das aufgezeichnete Signal verändert wird. Wenn möglich, ist dies die Standardeinstellung bei der Überwachung der Eingabe.

</dd> </dl>

Bei Digitalvideogeräten verweist *der lpSetAudio-Parameter* auf eine [**MCI \_ DGV \_ SETAUDIO \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa)

Die folgenden zusätzlichen Flags werden mit dem **vcr-Gerätetyp** verwendet:

<dl> <dt>

<span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>MCI \_ VCR \_ SETAUDIO \_ RECORD
</dt> <dd>

Legt die Audioaufzeichnung auf ein oder aus fest, die in Verbindung mit einem der folgenden Flags verwendet wird:

MCI \_ SET \_ ON

Audioaufzeichnung ein.

MCI \_ SET \_ OFF

Audioaufzeichnung deaktiviert. Möglicherweise ist es erforderlich, zuerst die Assembleraufzeichnung zu deaktivieren (mithilfe des [Befehls MCI \_ SET,](mci-set.md) bei dem das MCI VCR SET ASSEMBLE RECORD-Flag auf off festgelegt ist), bevor die Audioaufzeichnung deaktiviert werden \_ \_ \_ \_ kann.

MCI \_ TRACK

Der **dwTrack-Member** der durch *lpSetAudio* identifizierten Struktur gibt an, welche Spur vom Befehl betroffen ist.

MCI \_ VCR \_ SETAUDIO \_ SOURCE

Legt die Audioquelle fest. Dieses Flag muss mit dem MCI \_ VCR \_ SETAUDIO \_ TO-Flag verwendet werden.

MCI \_ VCR \_ SETAUDIO \_ MONITOR

Legt den Audioquellenmonitor fest. Dieses Flag muss mit dem MCI \_ VCR \_ SETAUDIO \_ TO-Flag verwendet werden.

MCI \_ VCR \_ SETAUDIO \_ AUF

Der **dwTo-Member** der durch *lpSetAudio* identifizierten Struktur enthält eine Konstante, die den Typ der Eingabe oder der überwachten Eingabe beschreibt. Dies muss einer der folgenden Sein:

<dl> <dd>

MCI \_ VCR \_ SRC \_ TYPE \_ TUNER

Typ: Tuner

</dd> <dd>

MCI \_ VCR \_ SRC \_ TYPE \_ LINE

Typ: zeile

</dd> <dd>

MCI \_ VCR \_ SRC \_ TYPE \_ AUX

Der Typ ist "auxiliary".

</dd> <dd>

MCI \_ VCR \_ SRC \_ TYPE \_ GENERIC

Der Typ ist generisch.

</dd> <dd>

MCI \_ VCR \_ SRC \_ TYPE \_ MUTE

Der Typ ist stumm. Dies kann nur mit dem MCI \_ VCR \_ SETAUDIO \_ SOURCE-Flag verwendet werden.

</dd> <dd>

AUSGABE DES MCI \_ \_ VCR-SRC-TYPS \_ \_

Typ: Ausgabe

</dd> <dd>

MCI \_ VCR \_ SETAUDIO \_ NUMBER

Der dwNumber-Member der durch lpSetAudio identifizierten Struktur enthält die Audioeingabe (des im dwTo-Member angegebenen Typs), die verwendet werden soll.

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Bei VCR-Geräten verweist *der lpSetAudio-Parameter* auf eine [**MCI \_ VCR \_ SETAUDIO \_ PARMS-Struktur.**](mci-vcr-setaudio-parms.md)

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

 

