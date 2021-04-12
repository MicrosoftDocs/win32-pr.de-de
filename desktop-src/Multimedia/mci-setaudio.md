---
title: MCI_SETAUDIO Befehl (MMSYSTEM. h)
description: Der MCI \_ setaudiobefehl legt Werte fest, die mit Audiowiedergabe und-Erfassung verknüpft sind. Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- MCI_SETAUDIO Befehl Windows-Multimedia
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
ms.openlocfilehash: 20605ff78c62a8e688778692d5ca8f8e1342a968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213736"
---
# <a name="mci_setaudio-command"></a>MCI \_ setaudiobefehl

Der MCI \_ setaudiobefehl legt Werte fest, die mit Audiowiedergabe und-Erfassung verknüpft sind. Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*
</dt> <dd>

Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpsetaudiodatei*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden Flags gelten für den **Digitalvideo** -Gerätetyp:

<dl> <dt>

<span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI \_ DGV \_ \_ setaudioalg
</dt> <dd>

Der **lpstrinalgorithmus** -Member der Struktur, die von *lpsetaudioidentifiziert* wird, enthält die Adresse eines Puffers, der den Namen eines Audiokomprimierungs Algorithmus enthält. Der Komprimierungs Algorithmus wird von nachfolgenden [MCI- \_ Reserve](mci-reserve.md) -oder [MCI- \_ Daten Satz](mci-record.md) Befehlen verwendet. Die verfügbaren Algorithmen sind Geräte abhängig. Wenn der Algorithmus nicht mit dem aktuellen Dateiformat kompatibel ist, wird das Dateiformat in das Standardformat für den Algorithmus geändert.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI \_ DGV \_ \_ setaudioclocktime
</dt> <dd>

Die angegebene Zeit wird in Millisekunden angegeben und ist die absolute Zeit bei der Verwendung mit MCI \_ DGV \_ \_ setaudioover. (Diese Zeit ist nicht im Schritt der Wiedergabe des Arbeitsbereichs.)

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>MCI- \_ DGV \_ - \_ setaudioeingabe
</dt> <dd>

Ändert das Flag für das Bass-, Treble-oder volumenflag, sodass es sich auf das Eingabe Signal auswirkt und ändert, was aufgezeichnet wird. Wenn möglich, ist dies der Standardwert, wenn die Eingabe überwacht wird.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>MCI- \_ DGV \_ - \_ setaudioelement
</dt> <dd>

Eine audiokonstante wird im **dwitem** -Member der-Struktur angegeben, die von *lpsetaudioangegeben* wird. Die Konstante identifiziert den Wert, der festgelegt wird. Die folgenden Konstanten sind definiert:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI \_ DGV \_ \_ setaudioavgbytespersec
</dt> <dd>

Die durchschnittliche Anzahl von Bytes wird im **dwValue** -Member der-Struktur angegeben, die durch *lpsetaudiobezeichnet* wird. Mit diesem Wert wird die durchschnittliche Anzahl von Bytes pro Sekunde für die Wiedergabe oder Aufzeichnung im PCM (Pulse Code Modulation) und ADPCM (Adaptive Differential Pulse Code Modulation)-Formate festgelegt. Die Datei wird in diesem Format gespeichert.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI \_ DGV \_ \_ setaudiobass
</dt> <dd>

Der Wert für "audiolow Frequency" wird als Faktor im **dwValue** -Member der durch " *lpsetaudio"* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI \_ DGV \_ \_ setaudiobitspersample
</dt> <dd>

Die Anzahl der Bits pro Stichprobe wird im **dwValue** -Member der Struktur angegeben, die durch *lpsetaudiobezeichnet* wird. Mit diesem Wert wird die Anzahl der Bits pro Stichprobe festgelegt oder im PCM-Format aufgezeichnet. Die Datei wird in diesem Format gespeichert.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI \_ DGV \_ \_ setaudioblockalign
</dt> <dd>

Die Datenblock Ausrichtung wird im **dwValue** -Member der-Struktur angegeben, die durch *lpsetaudiobezeichnet* wird. Dieser Wert legt die Ausrichtung von Datenblöcken relativ zum Anfang der Eingabe Wellenform Daten fest.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI \_ DGV \_ \_ setaudiosamplespersec
</dt> <dd>

Die Samplingrate wird im **dwValue** -Member der-Struktur angegeben, die durch *lpsetaudiobezeichnet* wird. Dieser Wert legt die Stichprobenrate für die Wiedergabe und Aufzeichnung mit den PCM-und ADPCM-Algorithmen fest. Die Datei wird in diesem Format gespeichert.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>MCI- \_ DGV \_ - \_ setaudioquelle
</dt> <dd>

Eine-Konstante, die die Quelle der Audioeingabe angibt, ist im **dwValue** -Member der-Struktur enthalten, die von *lpsetaudioidentifiziert* wird. Für die Audioeingabequellen sind die folgenden Konstanten definiert:

MCI \_ DGV \_ \_ setaudioquelle \_ Durchschnitt

Der Durchschnitt der linken und rechten Audiokanäle.

MCI- \_ DGV \_ - \_ setaudioquelle \_ Links

Linker Audiokanal.

MCI \_ DGV \_ \_ setaudioquelle \_ Rechts

Rechter Audiokanal.

MCI \_ DGV \_ \_ setaudioquelle \_ Stereo

Stereo.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>MCI- \_ DGV \_ - \_ setaudiostream
</dt> <dd>

Ein Audiodatenstrom wird im **dwValue** -Member der-Struktur angegeben, die durch *lpsetaudiobezeichnet* wird. Der ganzzahlige Wert gibt den Audiostream an, der vom Arbeitsbereich wiedergegeben wird. Wenn der Stream nicht angegeben wird, wird der erste physisch verschachtelte Audiostream wiedergegeben.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI \_ DGV \_ \_ setaudiotreble
</dt> <dd>

Der Wert für die hohe Frequenz Frequenz ist als Faktor im **dwValue** -Member der durch *lpsetaudioangabe* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>MCI- \_ DGV \_ - \_ setaudiovolume
</dt> <dd>

Die Audioebene für einen oder beide Audiokanäle wird als Faktor im **dwValue** -Member der Struktur angegeben, die durch *lpsetaudiobezeichnet* wird. Wenn das linke und das Rechte Volume auf unterschiedliche Werte festgelegt wurden, ist das Verhältnis von Links zu rechter Volume ungefähr unverändert.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ \_ setaudiolinks
</dt> <dd>

Aktiviert den linken Audiokanal bei Verwendung mit MCI, der \_ auf festgelegt ist \_ . Deaktiviert den linken Audiokanal bei Verwendung mit aktiviertem MCI \_ \_ . Wenn dieses Flag mit der Kombination aus MCI \_ DGV \_ \_ setaudiovalue und MCI \_ DGV \_ setaudiovolume verwendet wird \_ , wird das Volume des linken Audiokanals festgelegt. Wenn dieses Flag mit MCI \_ DGV \_ setaudioquelle verwendet wird \_ , gibt es den linken Audiokanal als Quelle für den audioeingabedigitalisierer an.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ DGV \_ \_ setaudioover
</dt> <dd>

Ein Übergangs Längen Parameter ist im **dwover** -Member der Struktur enthalten, die von *lpsetaudioidentifiziert* wird. Der Längen Wert gibt an, wie lange (in Einheiten des aktuellen Zeit Formats) benötigt wird, um eine Änderung vorzunehmen, bei der ein Faktor verwendet wird. Wenn dieses Flag nicht verwendet wird, treten Änderungen sofort auf.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI \_ DGV \_ \_ setaudioqualität
</dt> <dd>

Der **lpstrauquality** -Member der Struktur, die von *lpsetaudioidentifiziert* wird, enthält eine Adresse eines Puffers, der die Audioqualität definiert. Eine Text Zeichenfolge innerhalb des Puffers gibt die Merkmale des Audiokomprimierungs Algorithmus an.

Das MCI \_ DGV \_ \_ setaudioalg-Flag kann verwendet werden, um einen Qualitäts Deskriptor für den angegebenen Algorithmus auszuwählen. Wenn dieses Flag weggelassen wird, wird der aktuelle Algorithmus verwendet.

Welche Algorithmen und Deskriptornamen verfügbar sind, hängt vom Gerät ab. Jedes Gerät bietet eine Dokumentation für die verfügbaren Algorithmen und eine Beschreibung der anwendbaren Deskriptornamen. Mit dem [MCI- \_ Qualitäts](mci-quality.md) Befehl können zusätzliche Deskriptornamen definiert werden.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>MCI- \_ DGV \_ - \_ setaudiodatensatz
</dt> <dd>

Gibt an, ob Audiodaten von der Aufzeichnung eingeschlossen oder ausgeschlossen werden. In Kombination mit MCI \_ , das auf festgelegt \_ ist, werden Audiodaten aufgezeichnet. In Kombination mit der Deaktivierung von MCI \_ \_ werden Audiodaten ausgeschlossen. Der Standardwert enthält Audiodaten.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ \_ setaudioright
</dt> <dd>

Aktiviert den richtigen Audiokanal bei Verwendung mit MCI, der \_ auf festgelegt ist \_ . Deaktiviert den richtigen Audiokanal bei Verwendung mit aktiviertem MCI \_ \_ . Wenn dieses Flag mit der Kombination aus MCI \_ DGV \_ \_ setaudiovalue und MCI \_ DGV \_ setaudiovolume verwendet wird \_ , wird das Volume des richtigen Audiokanals festgelegt.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>MCI- \_ DGV \_ - \_ setaudiowert
</dt> <dd>

Im **dwValue** -Member der-Struktur, die durch *lpsetaudiobezeichnet* wird, wird ein Wert angegeben. Die Bedeutung des Werts wird durch die Konstante angegeben, die für das MCI- \_ DGV \_ -setaudioelementflag definiert ist \_ .

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI- \_ festgelegt \_
</dt> <dd>

Deaktiviert den angegebenen Audiokanal.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ festgelegt \_ auf
</dt> <dd>

Aktiviert den angegebenen Audiokanal.

</dd> <dt>

<span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>MCI- \_ \_ setaudioausgabe
</dt> <dd>

Ändert das Flag für das Bass-, Treble-oder volumenflag, sodass nur das geübte Signal geändert wird und nicht das, was aufgezeichnet wird. Wenn möglich, ist dies der Standardwert, wenn die Eingabe überwacht wird.

</dd> </dl>

Für Digital Video-Geräte zeigt der *lpsetaudioparameter* auf eine [**MCI \_ DGV- \_ setaudioparameterstruktur \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) .

Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>MCI- \_ VCR \_ - \_ setaudiodatensatz
</dt> <dd>

Legt die Audioaufzeichnung auf ein oder aus fest, das in Verbindung mit einem der folgenden Flags verwendet wird:

MCI \_ festgelegt \_ auf

Audioaufzeichnung in.

MCI- \_ festgelegt \_

Audioaufzeichnung aus. Möglicherweise ist es erforderlich, zuerst die Assemblierung zu deaktivieren (mit dem Befehl [MCI \_ ](mci-set.md) -Befehl, bei dem das \_ Flag assemblierungsdatensatz für MCI VCR \_ fest \_ \_ gelegt ist), bevor die Audioaufzeichnung ausgeschaltet werden kann.

MCI- \_ Track

Der **dwtrack** -Member der-Struktur, die von *lpsetaudioidentifiziert* wird, gibt an, welcher Titel vom Befehl betroffen ist.

MCI \_ VCR \_ - \_ setaudioquelle

Legt die Audioquelle fest. Dieses Flag muss mit dem MCI \_ VCR \_ - \_ setaudioflag zum Markieren von verwendet werden.

MCI \_ VCR \_ - \_ setaudiomonitor

Legt den audioquellmonitor fest. Dieses Flag muss mit dem MCI \_ VCR \_ - \_ setaudioflag zum Markieren von verwendet werden.

MCI \_ VCR \_ \_ setaudioto

Der **dwto** -Member der Struktur, die von *lpsetaudioidentifiziert* wird, enthält eine Konstante, die den Typ der Eingabe oder der überwachten Eingabe beschreibt. Dabei muss es sich um einen der folgenden handeln:

<dl> <dd>

MCI \_ VCR- \_ src- \_ \_ typtuner

Typ: Tuner

</dd> <dd>

MCI \_ VCR- \_ src- \_ \_ typzeile

Der Typ ist "Line".

</dd> <dd>

MCI \_ VCR \_ src \_ Type \_ aux

Typ ist "Hilfstyp".

</dd> <dd>

MCI \_ VCR- \_ src- \_ Typ \_ generisch

Der Typ ist generisch.

</dd> <dd>

MCI \_ VCR- \_ src- \_ Typ \_ stumm schalten

Typ ist stumm. Dies kann nur mit dem MCI \_ VCR \_ \_ setaudioquellflag verwendet werden.

</dd> <dd>

Ausgabe des MCI- \_ VCR- \_ src- \_ Typs \_

Der Typ ist "Output".

</dd> <dd>

MCI \_ VCR \_ - \_ setaudionummer

Der dwnumber-Member der Struktur, die von lpsetaudioidentifiziert wird, enthält die Audioeingabe (des Typs, der im dwto-Member angegeben ist), der verwendet werden soll.

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Bei VCR-Geräten verweist der *lpsetaudioparameter* auf eine [**MCI \_ VCR- \_ setaudioparameterstruktur \_**](mci-vcr-setaudio-parms.md) .

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

 

