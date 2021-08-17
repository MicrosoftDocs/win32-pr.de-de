---
title: MCI_SETVIDEO Befehl (Mmsystem.h)
description: Der MCI \_ SETVIDEO-Befehl legt Werte fest, die der Videowiedergabe zugeordnet sind. DigitalVideo- und VCR-Geräte erkennen diesen Befehl.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- MCI_SETVIDEO Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SETVIDEO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23206d169ad5e273927ead247c44194660c8d6b201c725e1b4d4ab24fd5e1544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803377"
---
# <a name="mci_setvideo-command"></a>MCI \_ SETVIDEO-Befehl

Der MCI \_ SETVIDEO-Befehl legt Werte fest, die der Videowiedergabe zugeordnet sind. DigitalVideo- und VCR-Geräte erkennen diesen Befehl.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETVIDEO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetVideo
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

**MCI \_ NOTIFY**, **MCI \_ WAIT** oder **MCI \_ TEST**. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*
</dt> <dd>

Zeiger auf eine [**GENERISCHE \_ MCI-PARMS-Struktur. \_**](mci-generic-parms.md) (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp "digitalvideo" verwendet:

<dl> <dt>

<span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI \_ DGV \_ SETVIDEO \_ ALG
</dt> <dd>

Der **lpstrAlgorithm-Member** der von *lpSetVideo* identifizierten Struktur enthält eine Adresse eines Puffers, der den Namen eines Videokomprimierungsalgorithmus enthält. Der Komprimierungsalgorithmus wird von nachfolgenden [MCI \_ RESERVE-](mci-reserve.md) oder [MCI \_ RECORD-Befehlen](mci-record.md) verwendet. Die verfügbaren Algorithmen sind geräteabhängig.

Wenn der angegebene Algorithmus nicht mit dem aktuellen Dateiformat kompatibel ist, wird das Dateiformat in das Standardformat für den Algorithmus geändert.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI \_ DGV \_ SETVIDEO \_ CLOCKTIME
</dt> <dd>

Gibt bei Verwendung mit **MCI \_ DGV \_ SETVIDEO \_ OVER** an, dass die Zeit in Millisekunden angegeben und die absolute Zeit ist. (Dieses Mal ist die Wiedergabe des Arbeitsbereichs nicht schrittweise.)

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>MCI \_ DGV \_ SETVIDEO \_ INPUT
</dt> <dd>

Ändert die **MCI \_ DGV \_ SETVIDEO \_ BRIGHTNESS,** **MCI \_ DGV \_ SETVIDEO \_ COLOR,** **MCI \_ DGV \_ SETVIDEO \_ CONTRAST,** **MCI \_ DGV \_ SETVIDEO \_ GAMMA,** **MCI \_ DGV \_ SETVIDEO \_ SHARPNESS** oder **MCI \_ DGV \_ SETVIDEO \_ TINT,** sodass es sich auf das Eingabesignal auswirkt und ändert, was aufgezeichnet wird. Wenn möglich, ist dies die Standardeinstellung beim Überwachen der Eingabe.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>MCI \_ DGV \_ SETVIDEO \_ ITEM
</dt> <dd>

Eine Videokonstante wird im **dwItem-Member** der durch *lpSetVideo* identifizierten Struktur angegeben. Die Konstante identifiziert den Wert, der festgelegt wird. Sie können die folgenden Konstanten mit diesem Flag angeben:

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>MCI \_ AVI \_ SETVIDEO \_ DRAW \_ PROCEDURE
</dt> <dd>

Eine neue Zeichnungsprozeduradresse wird im **dwValue-Member** der durch *lpSetVideo* identifizierten Struktur angegeben. Sie können eine neue Zeichnungsprozedur nur angeben, wenn sich das Gerät im Leerlauf befindet. Dieses Flag wird nur vom MCIAVI-Treiber für digitale Videos erkannt. Es gibt keine Entsprechung zu diesem Flag in der Zeichenfolgenbefehlsschnittstelle.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI \_ AVI \_ SETVIDEO \_ PALETTE \_ COLOR
</dt> <dd>

Eine neue Palettenfarbe wird in den **dwOver-** und **dwValue-Membern** der durch *lpSetVideo* identifizierten Struktur angegeben. Der **dwOver-Member** gibt den Palettenindex der zu ändernden Farbe an, und der **dwValue-Member** gibt die neue Farbe als RGB-Wert an. Sie müssen auch die **Flags MCI \_ DGV \_ SETVIDEO \_ OVER** und **MCI \_ DGV \_ SETVIDEO \_ VALUE** mit **MCI \_ DGV \_ SETVIDEO \_ ITEM** angeben, wenn Sie diese Konstante verwenden. Dieses Flag wird nur vom MCIAVI-Treiber für digitale Videos erkannt.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI \_ AVI \_ SETVIDEO \_ PALETTE \_ HALFTONE
</dt> <dd>

Gibt an, dass die Halbtonpalette anstelle der Standardpalette verwendet werden soll. Dieses Flag wird nur vom MCIAVI-Treiber für digitale Videos erkannt.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI \_ DGV \_ SETVIDEO \_ BITSPERPEL
</dt> <dd>

Die Anzahl der Bits pro Pixel wird im **dwValue-Member** der durch *lpSetVideo* identifizierten Struktur angegeben. Die Anzahl der Bits pro Pixel wird zum Speichern erfasster oder aufgezeichneter Daten verwendet.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI \_ DGV \_ SETVIDEO \_ BRIGHTNESS
</dt> <dd>

Die Video-Helligkeitsstufe wird als Faktor im **dwValue-Element** der durch *lpSetVideo* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI \_ DGV \_ SETVIDEO \_ COLOR
</dt> <dd>

Die Videofarbsättigungsstufe wird als Faktor im **dwValue-Element** der durch *lpSetVideo* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI \_ DGV \_ SETVIDEO \_ CONTRAST
</dt> <dd>

Die Videokontrastebene wird als Faktor im **dwValue-Element** der durch *lpSetVideo* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>MCI \_ DGV \_ SETVIDEO \_ FRAME \_ RATE
</dt> <dd>

Eine Bildfrequenz wird im **dwValue-Member** der durch *lpSetVideo* identifizierten Struktur angegeben. Die Rate wird in Einheiten von Frames pro Sekunde und 1000 angegeben. Beispielsweise werden 29,97 Frames pro Sekunde als 29970 angegeben.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI \_ DGV \_ SETVIDEO \_ GAMMA
</dt> <dd>

Ein Gammakorrektur-Exponentwert wird im **dwValue-Member** der durch *lpSetVideo* identifizierten Struktur angegeben. Die Gammakorrektur passt die Zuordnung zwischen der in der Präsentationsquelle codierten Intensität und der angezeigten Helligkeit an. Der Wert ist der Exponent multipliziert mit 1000. Beispielsweise gibt 2200 einen Exponenten von 2.2 an. Der Wert 1000 gibt einen Exponenten von 1 an, der keine Gammakorrektur anwendet.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI \_ DGV \_ SETVIDEO \_ KEY \_ COLOR
</dt> <dd>

Eine Schlüsselfarbe wird im **dwValue-Member** der durch *lpSetVideo* identifizierten Struktur angegeben. Die Schlüsselfarbe ist ein RGB-Wert.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI \_ DGV \_ SETVIDEO \_ KEY \_ INDEX
</dt> <dd>

Ein Schlüsselindexwert wird im **dwValue-Member** der durch *lpSetVideo* identifizierten Struktur angegeben. Der Indexparameter ist ein physischer Palettenindex.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI \_ DGV \_ SETVIDEO \_ PALHANDLE
</dt> <dd>

Ein Palettenhandle wird im **dwValue-Member** der durch *lpSetVideo* identifizierten Struktur angegeben. Das Palettenhandle ist im Wort mit niedriger Reihenfolge enthalten. Digitale Videogeräte sollten die mit diesem Befehl übergebene Palette nicht freigeben. Anwendungen sollten es freigeben, nachdem sie das Gerät geschlossen haben. Dieses Flag wird nur von Geräten unterstützt, die Paletten verwenden. Wenn dieses angegebene Palettenhandle 0 (null) ist, wird die Standardpalette verwendet.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI \_ DGV \_ SETVIDEO \_ SHARPNESS
</dt> <dd>

Ein Videoschärfewert wird als Faktor im **dwValue-Element** der durch *lpSetVideo* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>MCI \_ DGV \_ SETVIDEO \_ SOURCE
</dt> <dd>

Eine Konstante, die die Quelle der Videoeingabe angibt, wird im **dwValue-Member** der durch *lpSetVideo* identifizierten Struktur angegeben. Die folgenden Konstanten werden definiert:

-   **MCI \_ DGV \_ SETVIDEO \_ SRC \_ NTSC**: NTSC tv.
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ PAL: PAL tv.
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ RGB: RGB-Video.
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SECAM: SECAM tv.
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SVIDEO: S-Video.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>MCI \_ DGV \_ SETVIDEO \_ STREAM
</dt> <dd>

Ein Videostream wird im **dwValue-Member** der durch *lpSetVideo* identifizierten Struktur angegeben. Der ganzzahlige Wert gibt den vom Arbeitsbereich wiedergegebenen Videostream an. Wenn der Stream nicht angegeben ist und das Dateiformat keinen Standardstream definiert, wird der erste physisch verschachtelte Videostream wiedergegeben.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI \_ DGV \_ \_ SETVIDEO-FARBTON
</dt> <dd>

Ein Videotonwert wird als Faktor im **dwValue-Element** der durch *lpSetVideo* identifizierten Struktur angegeben. In der Regel wird diese Anpassung nach der Farbtonsteuerung vieler Farbsendungen modelliert, wobei 250 als grün, 750 als rot und 0 (oder 1000) als blau definiert sind. Der nominale Wert ist immer 500.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>MCI \_ DGV \_ SETVIDEO \_ OUTPUT
</dt> <dd>

Das **MCI \_ DGV \_ SETVIDEO \_ BRIGHTNESS,** **MCI \_ DGV \_ SETVIDEO \_ COLOR,** **MCI \_ DGV \_ SETVIDEO \_ CONTRAST,** **MCI \_ DGV \_ SETVIDEO \_ GAMMA,** **MCI \_ DGV \_ SETVIDEO \_ SHARPNESS** oder **das MCI \_ DGV \_ SETVIDEO \_ TINT-Flag** werden so geändert, dass es sich nur auf das angezeigte Signal und nicht auf das aufgezeichnete Auswirkt. Wenn möglich, ist dies die Standardeinstellung beim Überwachen einer Datei.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI \_ DGV \_ SETVIDEO \_ OVER
</dt> <dd>

Ein Parameter für die Übergangslänge ist im **dwOver-Member** der durch *lpSetVideo* identifizierten Struktur enthalten. Die Übergangslänge gibt an, wie lange (im aktuellen Zeitformat) die Änderung dauern soll. Wenn dieses Flag nicht verwendet wird, erfolgt die Änderung sofort.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI \_ DGV \_ SETVIDEO \_ QUALITY
</dt> <dd>

Der **lpstrQuality-Member** der von *lpSetVideo* identifizierten Struktur enthält eine Adresse eines Puffers, der die Videoqualität beschreibt. Eine Textzeichenfolge im Puffer gibt die Merkmale des Videokomprimierungsalgorithmus an.

Das **MCI \_ DGV \_ SETVIDEO \_ ALG-Flag** kann verwendet werden, um einen Qualitätsdeskriptor für den angegebenen Algorithmus auszuwählen. Wenn dieses Flag ausgelassen wird, wird der aktuelle Algorithmus verwendet.

Die verfügbaren Algorithmen und Deskriptornamen hängen vom Gerät ab. Jedes Gerät stellt Dokumentation für die verfügbaren Algorithmen und eine Beschreibung der entsprechenden Deskriptornamen bereit. Der [MCI \_ QUALITY-Befehl](mci-quality.md) kann zusätzliche Deskriptornamen definieren. Alle Geräte unterstützen die Deskriptoren "low", "medium" und "high". Der Standardwert ist treiberspezifisch.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>MCI \_ DGV \_ SETVIDEO \_ RECORD
</dt> <dd>

Gibt an, ob die Aufzeichnung Videodaten ein- oder ausschließt. In Kombination mit **MCI \_ SET \_ ON** werden Videodaten aufgezeichnet. In Kombination mit **MCI \_ SET \_ OFF** werden Videodaten ausgeschlossen. Die Standardeinstellung umfasst Videodaten.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI \_ DGV \_ SETVIDEO \_ SRC \_ NUMBER
</dt> <dd>

Eine Zahl für die Videoquelle wird im **dwSourceNumber-Member** der durch *lpSetVideo* identifizierten Struktur angegeben. Wenn mehr als eine Eingabe des von **MCI \_ DGV \_ SETVIDEO \_ VALUE** angegebenen Typs vorhanden ist, wählt der Wert die Eingabe aus. Dieses Flag muss immer mit **MCI \_ DGV \_ SETVIDEO \_ SOURCE** verwendet werden. Wenn **MCI \_ DGV \_ SETVIDEO \_ VALUE** weggelassen wird, gibt die angegebene Quellnummer jedoch die absolute Quelle an, die wie im [MCI \_ LIST-Befehl](mci-list.md) angegeben verwendet werden soll.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI \_ DGV \_ SETVIDEO \_ STILL
</dt> <dd>

Der angegebene Algorithmusname oder Qualitätswert gilt für Standbilder.

Jeder Gerätetreiber muss den Algorithmus "none" unterstützen, d.h. keine Komprimierung. Dies ist die Standardoption. In diesem Fall speichern Digitale Videogeräte Stillbilder als RGB-geräteunabhängige Bitmaps (DIBs).

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>MCI \_ DGV \_ \_ SETVIDEO-WERT
</dt> <dd>

Ein Wert ist im **dwValue-Member** der durch *lpSetVideo* identifizierten Struktur enthalten. Die Bedeutung des Werts wird durch das **MCI \_ DGV \_ SETVIDEO \_ ITEM-Flag** angegeben.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ SET \_ OFF
</dt> <dd>

Deaktiviert die Videoausgabe. Bei Geräten mit digitalem Video wird durch das Deaktivieren von Videos die Pixel im Zielrechteck, das durch den [MCI \_ PUT-Befehl](mci-put.md) (oder dessen Standardeinstellung, der Clientbereich des aktuellen Fensters) definiert wird, auf eine Volltonfarbe festgelegt, hat aber keine Auswirkungen auf den Framepuffer. Sie können das Fenster bei Bedarf mit dem [Befehl MCI \_ WINDOW](mci-window.md) ausblenden. Die Quelle des Videos, unabhängig davon, ob es sich um den Arbeitsbereich oder eine externe Eingabe handelt, speichert möglicherweise weiterhin neue Bilder im Framepuffer, aber sie werden erst angezeigt, wenn das Video aktiviert ist. Anwendungen sollten zwar den MCI \_ SETVIDEO-Befehl verwenden, um diese Funktion zu steuern, digitale Videogeräte müssen dieses Flag jedoch weiterhin unterstützen. Der Standardwert, nachdem ein geöffneter aktiviert wurde.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ SET \_ ON
</dt> <dd>

Aktiviert die Videoausgabe.

</dd> </dl>

Bei Digitalvideogeräten verweist der *lpSetVideo-Parameter* auf eine [**MCI \_ DGV \_ SETVIDEO \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa)

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp "vcr" verwendet:

<dl> <dt>

<span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>MCI \_ VCR \_ SETVIDEO \_ RECORD
</dt> <dd>

Legt die Videoaufzeichnung auf ein oder aus fest. Wird in Verbindung mit einem der folgenden Flags verwendet:

-   **MCI \_ SET \_ ON**. Videoaufzeichnung auf.
-   **MCI \_ SET \_ OFF**. Videoaufzeichnung deaktiviert. Es kann erforderlich sein, zuerst die Assembleraufzeichnung zu deaktivieren (mithilfe des [MCI \_ SET-Befehls](mci-set.md) mit deaktiviertem **MCI \_ VCR SET ASSEMBLE \_ \_ \_ RECORD-Flag),** bevor die Videoaufzeichnung deaktiviert werden kann.

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>MCI \_ TRACK
</dt> <dd>

Der **dwTrack-Member** der von *lpSetVideo* identifizierten Struktur gibt an, welche Spur vom Befehl betroffen ist.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>MCI \_ VCR \_ SETVIDEO \_ SOURCE
</dt> <dd>

Legt die Videoquelle fest und muss mit dem **MCI \_ VCR \_ SETVIDEO \_ TO-Flag** verwendet werden.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MCI \_ VCR \_ SETVIDEO \_ MONITOR
</dt> <dd>

Legt den Videoquellmonitor fest und muss mit dem MCI \_ VCR \_ SETVIDEO \_ TO-Flag verwendet werden.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI \_ VCR \_ SETVIDEO \_ TO
</dt> <dd>

Der **dwTo-Member** der von *lpSetVideo* identifizierten Struktur enthält eine der folgenden Konstanten:

<dl> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ TUNER**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ LINE**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ AUX**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ GENERIC**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ MUTE**</dd> <dd>**AUSGABE DES \_ MCI-VCR-SRC-TYPS \_ \_ \_**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ RGB**</dd> <dd>**MCI \_ VCR \_ SETVIDEO \_ NUMBER**</dd> </dl>

Der **dwNumber-Member** der von *lpSetVideo* identifizierten Struktur enthält die video-Eingabe (des im **dwTo-Member** angegebenen Typs), die verwendet werden soll.

</dd> </dl>

Bei VCR-Geräten zeigt der *lpSetVideo-Parameter* auf eine [**MCI \_ VCR \_ SETVIDEO \_ PARMS-Struktur.**](mci-vcr-setvideo-parms.md)

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

 

