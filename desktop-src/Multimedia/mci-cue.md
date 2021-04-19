---
title: MCI_CUE Befehl (MMSYSTEM. h)
description: Der MCI-Hinweis \_ Befehl gibt ein Gerät an, sodass die Wiedergabe oder Aufzeichnung mit minimaler Verzögerung beginnt. Mit Digital Video-, VCR-und Waveform-Audiogeräten wird dieser Befehl erkannt.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- MCI_CUE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8463c68f304fe216049568e0df518cbe1d0090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344691"
---
# <a name="mci_cue-command"></a>MCI-Hinweis \_ Befehl

Der MCI-Hinweis \_ Befehl gibt ein Gerät an, sodass die Wiedergabe oder Aufzeichnung mit minimaler Verzögerung beginnt. Mit Digital Video-, VCR-und Waveform-Audiogeräten wird dieser Befehl erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
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

<span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpcue*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>MCI \_ DGV-Hinweis \_ \_ Eingabe
</dt> <dd>

Eine Digital Video-Instanz sollte sich auf die Aufzeichnung vorbereiten. Wenn die Anwendung keinen Speicherplatz reserviert hat, reserviert das Gerät den Speicherplatz mithilfe seiner Standardparameter. Die Anwendung kann dieses Flag weglassen, wenn die aktuelle Präsentations Quelle bereits die externe Eingabe ist. (Dieses Flag hat keine Auswirkung auf die Auswahl der Präsentations Quelle.)

</dd> <dt>

<span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI \_ DGV-Hinweis \_ \_ noshow
</dt> <dd>

Eine Digital Video-Instanz sollte sich auf die Wiedergabe des Frames vorbereiten, der mit dem Befehl angegeben wurde, ohne ihn anzuzeigen. Wenn dieses Flag angegeben wird, zeigt die Anzeige weiterhin das Bild im Frame Puffer an, auch wenn der entsprechende Frame nicht die aktuelle Position ist. Wenn der Frame Puffer z. b. das Bild aus Frame 7 enthält, zeigt das Gerät weiterhin Frame 7 an, wenn dieses Flag verwendet wird, um das Gerät an eine beliebige andere Position zu überweisen. Mit einem nachfolgenden Hinweis Befehl ohne dieses Flag und ohne das Flag "MCI" wird \_ der aktuelle Frame angezeigt.

</dd> <dt>

<span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>MCI- \_ DGV-Hinweis \_ \_ Ausgabe
</dt> <dd>

Eine Digital Video-Instanz sollte sich auf die Wiedergabe vorbereiten. Wenn der Arbeitsbereich angehalten wird, findet keine Positionierung statt. Wenn der Arbeitsbereich beendet wird, ändert sich die Position möglicherweise zu einem vorherigen Keyframe-Image. Die Anwendung kann dieses Flag weglassen, wenn die aktuelle Präsentations Quelle bereits der Arbeitsbereich ist.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu
</dt> <dd>

Eine Arbeitsbereichs Position ist im **dwto** -Member der durch *lpcue* identifizierten Struktur enthalten. Die den Positions Werten zugewiesenen Einheiten werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [ \_ MCI](mci-set.md) -Befehl festgelegt. Dies entspricht der Suche nach einer Position, mit der Ausnahme, dass das Gerät nach dem Befehl angehalten wird.

</dd> </dl>

Bei **Digitalvideo** -Geräten verweist der *lpcue* -Parameter auf eine [**MCI- \_ DGV \_ \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) -Parameter Struktur.

Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von
</dt> <dd>

Der **dwfrom** -Member der Struktur, auf die von *lpcue* verwiesen wird, enthält die im aktuellen Zeitformat angegebene Startposition.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu
</dt> <dd>

Der **dwto** -Member der Struktur, auf die von *lpcue* verwiesen wird, enthält den im aktuellen Zeitformat angegebenen endspeicherort (Anhalten).

</dd> <dt>

<span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>MCI- \_ VCR-Hinweis \_ \_ Eingabe
</dt> <dd>

Vorbereiten der Aufzeichnung.

</dd> <dt>

<span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>MCI- \_ VCR-Hinweis \_ \_ Ausgabe
</dt> <dd>

Vorbereiten der Wiedergabe. Wenn weder MCI \_ VCR-Hinweis \_ \_ Eingaben noch die MCI- \_ VCR-Hinweis \_ \_ Ausgabe angegeben ist, wird die MCI- \_ VCR-Hinweis \_ \_ Ausgabe angenommen.

</dd> <dt>

<span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>MCI \_ VCR-Hinweis- \_ \_ Preroll
</dt> <dd>

Leiten Sie das Gerät an die aktuelle Position oder an die **dwfrom** -Position abzüglich der vorab Dauer der Vorabversion ab. Dadurch kann sich das Gerät vor dem Wechsel in den Daten Satz-oder Wiedergabemodus vorbereiten.

</dd> <dt>

<span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>MCI- \_ VCR-Hinweis \_ \_ umkehren
</dt> <dd>

Die Richtung des nächsten Wiedergabe-oder Daten Satz Befehls ist umgekehrt.

</dd> </dl>

Wenn Sie die Wiedergabe mit dem MCI-Hinweis \_ Befehl mit dem MCI- \_ VCR-Flag- \_ \_ ausgabeflag verwenden, können Sie die MCI-Verwendung abbrechen, \_ indem Sie den [MCI- \_ Wiedergabe](mci-play.md) Befehl mit MCI \_ von, MCI \_ an oder MCI \_ VCR \_ Play Reverse ausgeben \_ .

Wenn Sie die Aufzeichnung mit dem MCI- \_ Hinweis mit dem MCI \_ VCR-Flag Eingabe Kennzeichen durcharbeiten \_ \_ , können Sie den MCI-Hinweis abbrechen, \_ indem Sie den [MCI- \_ Eintrag](mci-record.md) Befehl mit MCI \_ from, MCI \_ to oder MCI \_ VCR \_ Record \_ Initialize ausgeben.

Bei **VCR** -Geräten verweist der *lpcue* -Parameter auf eine [**MCI- \_ VCR \_ \_**](mci-vcr-cue-parms.md) -Endpunkt-Parameter Struktur.

Die folgenden zusätzlichen Flags werden mit dem **waveaudiogerätetyp** verwendet:

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI- \_ Wave- \_ Eingabe
</dt> <dd>

Ein Waveform-Audioeingabegerät sollte gecutzt werden.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI- \_ Wave- \_ Ausgabe
</dt> <dd>

Ein Waveform-Audioausgabegerät sollte gecutzt werden. Dies ist das Standardflag, wenn kein Flag angegeben wird.

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

 

