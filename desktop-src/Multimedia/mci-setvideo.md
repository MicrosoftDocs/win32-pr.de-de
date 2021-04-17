---
title: MCI_SETVIDEO Befehl (MMSYSTEM. h)
description: Der MCI \_ setvideo-Befehl legt Werte fest, die mit der Videowiedergabe verknüpft sind. Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- MCI_SETVIDEO Befehl Windows-Multimedia
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
ms.openlocfilehash: 83a20e0cc5466ac9ff28a59543543069fa9acd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476881"
---
# <a name="mci_setvideo-command"></a>Befehl "MCI \_ setvideo"

Der MCI \_ setvideo-Befehl legt Werte fest, die mit der Videowiedergabe verknüpft sind. Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*
</dt> <dd>

Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

**MCI \_ Benachrichtigen**, **MCI- \_ Wartezeit** oder **MCI- \_ Test**. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpsetvideo*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp "Digitalvideo" verwendet:

<dl> <dt>

<span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI \_ DGV \_ setvideo \_ alg
</dt> <dd>

Der **lpstrinalgorithmus** -Member der Struktur, die von *lpsetvideo* identifiziert wird, enthält die Adresse eines Puffers, der den Namen eines Video Komprimierungs Algorithmus enthält. Der Komprimierungs Algorithmus wird von nachfolgenden [MCI- \_ Reserve](mci-reserve.md) -oder [MCI- \_ Daten Satz](mci-record.md) Befehlen verwendet. Die verfügbaren Algorithmen sind Geräte abhängig.

Wenn der angegebene Algorithmus nicht mit dem aktuellen Dateiformat kompatibel ist, wird das Dateiformat in das Standardformat für den Algorithmus geändert.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI \_ DGV \_ setvideo \_ clocktime
</dt> <dd>

Bei Verwendung mit **MCI \_ DGV \_ setvideo \_ over** gibt an, dass die Zeit in Millisekunden angegeben und die absolute Zeit ist. (Diese Zeit ist nicht im Schritt der Wiedergabe des Arbeitsbereichs.)

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>MCI- \_ DGV- \_ setvideo- \_ Eingabe
</dt> <dd>

Ändert die **MCI \_ DGV \_ setvideo- \_ Helligkeit**, **MCI \_ DGV \_ setvideo- \_ Farbe**, **MCI \_ DGV \_ setvideo- \_ Kontrast**, **MCI \_ DGV \_ setvideo \_ Gamma**, **MCI \_ DGV \_ setvideo- \_ Schärfe** oder **MCI \_ DGV \_ setvideo \_ tint** , sodass Sie das Eingabe Signal beeinflussen und ändern, was aufgezeichnet wird. Wenn möglich, ist dies der Standardwert, wenn die Eingabe überwacht wird.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>MCI- \_ DGV- \_ setvideo- \_ Element
</dt> <dd>

Eine Video Konstante wird im **dwitem** -Member der von *lpsetvideo* identifizierten Struktur angegeben. Die Konstante identifiziert den Wert, der festgelegt wird. Sie können die folgenden Konstanten mit diesem Flag angeben:

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>MCI \_ AVI \_ setvideo \_ Draw- \_ Prozedur
</dt> <dd>

Im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur wird eine neue Zeichnungs Prozedur Adresse angegeben. Sie können eine neue Zeichnungs Prozedur nur angeben, wenn sich das Gerät im Leerlauf befindet. Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt. In der Zeichen folgen Befehlsschnittstelle gibt es keine Entsprechung für dieses Flag.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI \_ AVI \_ setvideo \_ - \_ Palettenfarbe
</dt> <dd>

In den Elementen **dwover** und **dwValue** der von *lpsetvideo* identifizierten Struktur wird eine neue Palettenfarbe angegeben. Der Member **dwover** gibt den Palettenindex der zu ändernden Farbe an, und der **dwValue** -Member gibt die neue Farbe als RGB-Wert an. Sie müssen auch die **MCI \_ DGV \_ setvideo \_ over** -und **MCI \_ DGV \_ setvideo- \_ wertflags** mit dem **MCI \_ DGV \_ setvideo- \_ Element** angeben, wenn Sie diese Konstante verwenden. Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI \_ AVI \_ setvideo- \_ Palette \_ halbft1
</dt> <dd>

Gibt an, dass die "Halbton"-Palette anstelle der Standardpalette verwendet werden soll. Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI \_ DGV \_ setvideo \_ BitsPerPel
</dt> <dd>

Die Anzahl der Bits pro Pixel wird im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben. Die Anzahl der Bits pro Pixel wird zum Speichern erfasster oder aufgezeichneter Daten verwendet.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI \_ DGV \_ setvideo- \_ Helligkeit
</dt> <dd>

Die videohelligkeits Ebene wird als Faktor im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI- \_ DGV- \_ setvideo- \_ Farbe
</dt> <dd>

Die Farb Sättigungs Ebene der Farbe wird als Faktor für den **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI- \_ DGV- \_ setvideo- \_ Kontrast
</dt> <dd>

Die Video Kontrast Ebene wird als Faktor für den **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>MCI \_ DGV \_ setvideo- \_ Frame \_ Rate
</dt> <dd>

Im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur wird eine Frame Rate angegeben. Die Rate wird in den Rahmen Einheiten pro Sekunde 1000 angegeben. Beispielsweise werden 29,97 Frames pro Sekunde als 29970 angegeben.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI \_ DGV \_ setvideo \_ Gamma
</dt> <dd>

Ein Gammakorrektur-Exponent-Wert wird im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben. Gamma Korrektur passt die Zuordnung zwischen der in der Präsentations Quelle codierten Intensität und der angezeigten Helligkeit an. Der Wert ist der Exponent multipliziert mit 1000. 2200 gibt beispielsweise einen Exponenten von 2,2 an. Der Wert 1000 gibt einen Exponenten von 1 an, der keine Gammakorrektur anwendet.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI- \_ DGV- \_ setvideo- \_ Schlüssel \_ Farbe
</dt> <dd>

Im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur wird eine Schlüsselfarbe angegeben. Die Schlüsselfarbe ist ein RGB-Wert.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI- \_ DGV- \_ setvideo- \_ Schlüssel \_ Index
</dt> <dd>

Ein Schlüssel Indexwert wird im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben. Der Index-Parameter ist ein physischer Palettenindex.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI \_ DGV \_ setvideo \_ palhandle
</dt> <dd>

Ein Palettenhandle wird im **dwValue** -Member der von *lpsetvideo* identifizierten-Struktur angegeben. Das Palettenhandle ist im nieder wertigen Wort enthalten. Digitale Videogeräte dürfen die mit diesem Befehl bestandene Palette nicht freigeben. Anwendungen sollten Sie nach dem Schließen des Geräts freigeben. Dieses Flag wird nur von Geräten unterstützt, die Paletten verwenden. Wenn das angegebene Palettenhandle 0 (null) ist, wird die Standardpalette verwendet.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI \_ DGV \_ setvideo- \_ Schärfe
</dt> <dd>

Ein Video-Schärfe Wert wird als Faktor im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>MCI- \_ DGV- \_ setvideo- \_ Quelle
</dt> <dd>

Eine Konstante, die die Quelle der Videoeingabe angibt, wird im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben. Die folgenden Konstanten sind definiert:

-   **MCI \_ DGV \_ setvideo \_ src \_ NTSC**: NTSC-TV.
-   MCI \_ DGV \_ setvideo \_ src \_ PAL: PAL TV.
-   MCI \_ DGV \_ setvideo \_ src \_ RGB: RGB-Video.
-   MCI \_ DGV \_ setvideo \_ src \_ SECAM: SECAM-Fernsehen.
-   MCI \_ DGV \_ setvideo \_ src \_ SVideo: S-Video.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>MCI- \_ DGV- \_ setvideo- \_ Stream
</dt> <dd>

Ein Videostream wird im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben. Der ganzzahlige Wert gibt den Videostream an, der im Arbeitsbereich wiedergegeben wird. Wenn der Stream nicht angegeben wird und das Dateiformat keinen Standardstream definiert, wird der erste physisch verschachtelte Videostream wiedergegeben.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI \_ DGV \_ setvideo \_ tint
</dt> <dd>

Ein Video-Tönungs-Wert wird als Faktor im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben. Diese Anpassung wird in der Regel nach dem Tönungs-Steuerelement von vielen Farb Fernseh Sätzen modelliert, wobei 250 als grün, 750 als rot definiert und 0 (oder 1000) als Blau definiert ist. Der nominale Wert ist immer 500.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>MCI- \_ DGV- \_ setvideo- \_ Ausgabe
</dt> <dd>

Die **MCI \_ DGV \_ setvideo- \_ Helligkeit**, **MCI \_ DGV \_ setvideo \_ Color**, **MCI \_ DGV \_ setvideo- \_ Kontrast**, **MCI \_ DGV \_ setvideo \_ Gamma**, **MCI \_ DGV \_ setvideo- \_ Schärfe** oder das **MCI \_ DGV \_ setvideo \_ tint** -Flag wird so geändert, dass nur das angezeigte Signal und nicht was aufgezeichnet wird. Wenn möglich, ist dies die Standardeinstellung beim Überwachen einer Datei.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI \_ DGV \_ setvideo \_ over
</dt> <dd>

Ein Parameter für die Übergangs Länge ist im Member **dwover** der von *lpsetvideo* identifizierten Struktur enthalten. Die Übergangs Länge gibt an, wie lange (im aktuellen Zeitformat) benötigt wird, um eine Änderung vorzunehmen. Wenn dieses Flag nicht verwendet wird, erfolgt die Änderung sofort.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI \_ DGV \_ setvideo- \_ Qualität
</dt> <dd>

Der **lpstrauquality** -Member der Struktur, die von *lpsetvideo* identifiziert wird, enthält die Adresse eines Puffers, der die Videoqualität beschreibt. Eine Text Zeichenfolge im Puffer gibt die Merkmale des Video Komprimierungs Algorithmus an.

Das **MCI \_ DGV \_ setvideo \_ ALG** -Flag kann verwendet werden, um einen Qualitäts Deskriptor für den angegebenen Algorithmus auszuwählen. Wenn dieses Flag weggelassen wird, wird der aktuelle Algorithmus verwendet.

Welche Algorithmen und Deskriptornamen verfügbar sind, hängt vom Gerät ab. Jedes Gerät bietet eine Dokumentation für die verfügbaren Algorithmen und eine Beschreibung der anwendbaren Deskriptornamen. Mit dem [MCI- \_ Qualitäts](mci-quality.md) Befehl können zusätzliche Deskriptornamen definiert werden. Alle Geräte unterstützen die Deskriptoren "Low", "Medium" und "High". Der Standardwert ist Treiber spezifisch.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>MCI- \_ DGV- \_ setvideo- \_ Datensatz
</dt> <dd>

Gibt an, ob Videodaten von der Aufzeichnung eingeschlossen oder ausgeschlossen werden. In Kombination mit **MCI, das \_ \_ auf festgelegt** ist, werden Videodaten aufgezeichnet. In Kombination mit der Deaktivierung **\_ \_ von MCI** werden Videodaten ausgeschlossen. Der Standardwert enthält Videodaten.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI \_ DGV \_ setvideo- \_ src- \_ Nummer
</dt> <dd>

Eine Zahl für die Videoquelle wird im **dwsourcenumber** -Member der von *lpsetvideo* identifizierten Struktur angegeben. Wenn es mehr als eine Eingabe des Typs gibt, der durch den **MCI \_ DGV \_ setvideo- \_ Wert** angegeben wird, wählt der Wert die Eingabe aus. Dieses Flag muss immer mit der **MCI- \_ DGV- \_ setvideo- \_ Quelle** verwendet werden. Wenn der **MCI \_ DGV- \_ setvideo- \_ Wert** weggelassen wird, gibt die angegebene Quellnummer jedoch die absolute zu verwendende Quelle an, wie im [MCI- \_ Listen](mci-list.md) Befehl angegeben.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI- \_ DGV- \_ setvideo \_ weiterhin
</dt> <dd>

Der angegebene Algorithmusname oder Qualitäts Wert gilt für weiterhin Bilder.

Jeder Gerätetreiber muss den Algorithmus "None" unterstützen, was bedeutet, dass keine Komprimierung erforderlich ist. Dies ist die Standardoption. In diesem Fall speichern Digital Videogeräte weiterhin Images als RGB-geräteunabhängige Bitmaps (Disb).

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>MCI- \_ DGV- \_ setvideo- \_ Wert
</dt> <dd>

Im **dwValue** -Member der durch *lpsetvideo* identifizierten Struktur ist ein Wert enthalten. Die Bedeutung des Werts wird durch das **MCI- \_ DGV- \_ setvideo \_** -elementflag angegeben.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI- \_ festgelegt \_
</dt> <dd>

Deaktiviert die Videoausgabe. Bei digitalen Videogeräten werden bei der Deaktivierung von Videos die Pixel im Ziel Rechteck, das durch den [MCI \_ Put](mci-put.md) -Befehl (oder der Standardwert, den Client Bereich des aktuellen Fensters) definiert ist, auf eine voll Tonfarbe festgelegt, aber Sie hat keine Auswirkung auf den Frame Puffer. Wenn gewünscht, können Sie das Fenster mit dem [MCI- \_ Fenster](mci-window.md) Befehl ausblenden. Die Quelle des Videos, unabhängig davon, ob es sich um den Arbeitsbereich oder eine externe Eingabe handelt, speichert möglicherweise weiterhin neue Images im Frame Puffer, aber Sie werden erst angezeigt, wenn das Video aktiviert ist. Wenngleich Anwendungen den MCI \_ setvideo-Befehl verwenden sollten, um diese Funktion zu steuern, müssen digitale Videogeräte dieses Flag weiterhin unterstützen. Der Standardwert, nachdem ein geöffnet ist.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ festgelegt \_ auf
</dt> <dd>

Aktiviert die Videoausgabe.

</dd> </dl>

Für Digital Video-Geräte zeigt der *lpsetvideo* -Parameter auf eine [**MCI \_ DGV- \_ setvideo \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) -Parameter Struktur.

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp "VCR" verwendet:

<dl> <dt>

<span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>MCI \_ VCR- \_ setvideo- \_ Datensatz
</dt> <dd>

Legt die Videoaufzeichnung auf ein oder aus fest. Wird in Verbindung mit einem der folgenden Flags verwendet:

-   **MCI \_ Legen Sie \_ auf fest**. Video Aufzeichnung in.
-   **MCI \_ Legen Sie \_ aus fest**. Video Aufzeichnung aus. Möglicherweise ist es erforderlich, zuerst die Assemblierung zu deaktivieren (mit dem Befehl [MCI \_ set](mci-set.md) , wobei das Flag **MCI \_ VCR Set assemblierungsdatensatz \_ \_ \_** auf OFF festgelegt ist), bevor die Videoaufzeichnung ausgeschaltet werden kann.

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>MCI- \_ Track
</dt> <dd>

Der **dwtrack** -Member der durch *lpsetvideo* identifizierten Struktur gibt an, welcher Titel vom Befehl betroffen ist.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>MCI \_ VCR- \_ setvideo- \_ Quelle
</dt> <dd>

Legt die Videoquelle fest und muss mit dem **MCI \_ VCR \_ setvideo zum Markieren \_ von** verwendet werden.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MCI \_ VCR- \_ setvideo- \_ Monitor
</dt> <dd>

Legt den Video Quell Monitor fest und muss mit dem MCI \_ VCR \_ setvideo \_ zum Markieren von verwendet werden.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI \_ VCR \_ setvideo \_ für
</dt> <dd>

Der **dwto** -Member der von *lpsetvideo* identifizierten Struktur enthält eine der folgenden Konstanten:

<dl> <dd>**MCI \_ VCR- \_ src- \_ \_ typtuner**</dd> <dd>**MCI \_ VCR- \_ src- \_ \_ typzeile**</dd> <dd>**MCI \_ VCR \_ src \_ Type \_ aux**</dd> <dd>**MCI \_ VCR- \_ src- \_ Typ \_ generisch**</dd> <dd>**MCI \_ VCR- \_ src- \_ Typ \_ stumm schalten**</dd> <dd>**Ausgabe des MCI- \_ VCR- \_ src- \_ Typs \_**</dd> <dd>**MCI \_ VCR- \_ src- \_ Typ \_ RGB**</dd> <dd>**MCI \_ VCR- \_ setvideo- \_ Nummer**</dd> </dl>

Der **dwnumber** -Member der-Struktur, die von *lpsetvideo* identifiziert wird, enthält die Videoeingabe (vom Typ, der im **dwto** -Member angegeben ist), der verwendet werden soll.

</dd> </dl>

Bei VCR-Geräten verweist der *lpsetvideo* -Parameter auf eine [**MCI \_ VCR- \_ setvideo \_**](mci-vcr-setvideo-parms.md) -Parameter Struktur.

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

 

