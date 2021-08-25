---
title: MCI_CUE Befehl (Mmsystem.h)
description: Der MCI \_ CUE-Befehl gibt ein Gerät an, sodass die Wiedergabe oder Aufzeichnung mit minimaler Verzögerung beginnt. Digital-Video-, VCR- und Waveform-Audio-Geräte erkennen diesen Befehl.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- MCI_CUE Befehl Windows Multimedia
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
ms.openlocfilehash: 432c3fcd89a4841840559e44400716834df260b533d2cf40daa9da5e6a8fb6f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784600"
---
# <a name="mci_cue-command"></a>MCI \_ CUE-Befehl

Der MCI \_ CUE-Befehl gibt ein Gerät an, sodass die Wiedergabe oder Aufzeichnung mit minimaler Verzögerung beginnt. Digital-Video-, VCR- und Waveform-Audio-Geräte erkennen diesen Befehl.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsmeldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder, für Digital Video- und VCR-Geräte, MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*
</dt> <dd>

Zeiger auf eine [**GENERISCHE \_ MCI-PARMS-Struktur. \_**](mci-generic-parms.md) (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden zusätzlichen Flags werden mit dem **Gerätetyp digitalvideo** verwendet:

<dl> <dt>

<span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>MCI \_ DGV \_ CUE \_ INPUT
</dt> <dd>

Eine Digitale-Video-Instanz sollte sich auf die Aufzeichnung vorbereiten. Wenn die Anwendung nicht über reservierten Speicherplatz verfügt, reserviert das Gerät den Speicherplatz mithilfe seiner Standardparameter. Die Anwendung kann dieses Flag weglassen, wenn die aktuelle Präsentationsquelle bereits die externe Eingabe ist. (Dieses Flag hat keine Auswirkungen auf die Auswahl der Präsentationsquelle.)

</dd> <dt>

<span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI \_ DGV \_ CUE \_ NOSHOW
</dt> <dd>

Eine Digital-Video-Instanz sollte sich auf die Wiedergabe des mit dem Befehl angegebenen Frames vorbereiten, ohne ihn anzuzeigen. Wenn dieses Flag angegeben wird, zeigt die Anzeige weiterhin das Bild im Framepuffer an, obwohl der entsprechende Frame nicht die aktuelle Position ist. Wenn der Framepuffer beispielsweise das Bild aus Frame 7 enthält, zeigt das Gerät weiterhin Frame 7 an, wenn dieses Flag verwendet wird, um das Gerät an eine andere Position zu bringen. Ein nachfolgender Cue-Befehl ohne dieses Flag und ohne das MCI \_ TO-Flag zeigt den aktuellen Frame an.

</dd> <dt>

<span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>MCI \_ DGV \_ CUE \_ OUTPUT
</dt> <dd>

Eine Digitale-Video-Instanz sollte sich auf die Wiedergabe vorbereiten. Wenn der Arbeitsbereich angehalten wird, erfolgt keine Positionierung. Wenn der Arbeitsbereich beendet wird, ändert sich die Position möglicherweise in ein vorheriges Keyframebild. Die Anwendung kann dieses Flag weglassen, wenn die aktuelle Präsentationsquelle bereits der Arbeitsbereich ist.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Eine Arbeitsbereichsposition ist im **dwTo-Member** der durch *lpCue identifizierten* Struktur enthalten. Die Einheiten, die Positionswerten zugewiesen sind, werden mithilfe des MCI \_ SET \_ TIME \_ FORMAT-Flags des [MCI \_ SET-Befehls](mci-set.md) angegeben. Dies entspricht dem Suchen nach einer Position, mit dem Unterschied, dass das Gerät nach dem Befehl angehalten wird.

</dd> </dl>

Bei **Digitalvideogeräten** verweist der *lpCue-Parameter* auf eine [**MCI \_ DGV \_ CUE \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms)

Die folgenden zusätzlichen Flags werden mit dem **Vcr-Gerätetyp** verwendet:

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Der **dwFrom-Member** der -Struktur, auf die *von lpCue* gezeigt wird, enthält die Startposition, die im aktuellen Zeitformat angegeben ist.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Der **dwTo-Member** der -Struktur, auf die *lpCue* zeigt, enthält die endende (anhaltende) Position, die im aktuellen Zeitformat angegeben ist.

</dd> <dt>

<span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>MCI \_ VCR \_ CUE \_ INPUT
</dt> <dd>

Bereiten Sie die Aufzeichnung vor.

</dd> <dt>

<span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>MCI \_ VCR \_ CUE \_ OUTPUT
</dt> <dd>

Bereiten Sie sich auf die Wiedergabe vor. Wenn weder MCI \_ VCR \_ CUE \_ INPUT noch MCI \_ VCR \_ CUE OUTPUT angegeben \_ ist, wird MCI \_ VCR \_ CUE OUTPUT \_ angenommen.

</dd> <dt>

<span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>MCI \_ VCR \_ CUE \_ PREROLL
</dt> <dd>

Cue the device to the current position, or the dwFrom position, minus the preroll duration. (Cue the device to the current position, or the **dwFrom** position, minus the preroll duration. Dadurch kann sich das Gerät vorbereiten, bevor es in den Aufzeichnungs- oder Wiedergabemodus wechselt.

</dd> <dt>

<span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>MCI \_ VCR \_ CUE \_ REVERSE
</dt> <dd>

Die Richtung des nächsten Wiedergabe- oder Aufzeichnungsbefehls ist umgekehrt.

</dd> </dl>

Beim Cueing für die Wiedergabe mit dem MCI \_ CUE-Befehl mit dem MCI \_ VCR \_ CUE \_ OUTPUT-Flag können Sie MCI CUE abbrechen, indem Sie \_ den [MCI \_ PLAY-Befehl](mci-play.md) mit MCI \_ FROM, MCI \_ TO oder MCI \_ VCR PLAY REVERSE \_ \_ ausgeben.

Beim Cueing für die Aufzeichnung mit MCI \_ CUE mit dem MCI \_ VCR \_ CUE \_ INPUT-Flag können Sie MCI CUE abbrechen, indem Sie \_ den [MCI \_ RECORD-Befehl](mci-record.md) mit MCI \_ FROM, MCI \_ TO oder MCI \_ VCR RECORD \_ \_ INITIALIZE ausgeben.

Bei **Vcr-Geräten** zeigt der *lpCue-Parameter* auf eine [**MCI \_ VCR \_ CUE \_ PARMS-Struktur.**](mci-vcr-cue-parms.md)

Die folgenden zusätzlichen Flags werden mit dem **Gerätetyp waveaudio** verwendet:

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ INPUT
</dt> <dd>

Ein Waveform-Audio-Eingabegerät sollte angekuppelt werden.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ \_ WAVE-AUSGABE
</dt> <dd>

Ein Waveform-Audio-Ausgabegerät sollte angekuppelt werden. Dies ist das Standardflag, wenn kein Flag angegeben ist.

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

 

