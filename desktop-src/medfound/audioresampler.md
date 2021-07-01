---
description: Der Audio-Resampler führt eine oder beide der folgenden Aktionen für einen Audiostream aus. Ändern Sie die Samplingrate. Ändern Sie die Anzahl der Kanäle.
ms.assetid: bee755c4-0585-40fb-aa4d-4e964f5144a3
title: Audio Resampler-DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf5e640ffd128a5b9249514284ecef16c5f57e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119414"
---
# <a name="audio-resampler-dsp"></a>Audio-Resampler-DSP

Der Audio-Resampler führt eine oder beide der folgenden Aktionen für einen Audiostream aus.

-   Ändern Sie die Samplingrate.
-   Ändern Sie die Anzahl der Kanäle.

## <a name="clsid"></a>CLSID

CLSID \_ CResamplerMediaObject

## <a name="interfaces"></a>Schnittstellen

-   [**IMediaObject**](/previous-versions/ms785953(v=vs.85))
-   [**ÜBERTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResamplerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops)

## <a name="formats"></a>Formate

PCM oder IEEE-Gleitkomma

Der Medientyp muss ein nicht komprimiertes PCM- oder Gleitkommaaudioformat angeben.

-   Initialisieren Sie für die [**INTERFACESTransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) den Medientyp wie unter [Uncompressed Audio Media Types (Unkomprimierte Audiomedientypen)](uncompressed-audio-media-types.md)beschrieben.
-   Für die [**IMediaObject-Schnittstelle**](/previous-versions/ms785953%28v%3dvs.85%29) muss der Medientyp ein **FORMAT \_ WaveFormatEx-Typ** sein. Weitere Informationen finden Sie unter [**DMO \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type).

## <a name="properties"></a>Eigenschaften

-   [MFPKEY \_ WMRESAMP \_ FILTERQUALITY](mfpkey-wmresamp-filterquality.md)
-   [MFPKEY \_ WMRESAMP \_ CHANNELMTX](mfpkey-wmresamp-channelmtx.md)
-   [MFPKEY \_ WMRESAMP \_ LOWPASS \_ BANDWIDTH](mfpkey-wmresamp-lowpass-bandwidth.md)

## <a name="required-attributes"></a>Erforderliche Attribute.

Für den Resampler müssen die folgenden Attribute festgelegt werden:

-   [MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK](mf-mt-audio-channel-mask-attribute.md)
-   [MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT](mf-mt-audio-block-alignment-attribute.md)

## <a name="custom-channel-mapping"></a>Benutzerdefinierte Kanalzuordnung

Der Audio-Resampler ordnet die Eingabeaudiokanäle den Ausgabeaudiokanälen basierend auf den folgenden Informationen zu:

-   Die Anzahl der Kanäle. Dies wird im [MF MT AUDIO NUM \_ \_ \_ \_ CHANNELS-Attribut](mf-mt-audio-num-channels-attribute.md) des Medientyps oder im **nChannels-Member** der [WAVEFORMATEX-Struktur](mf-mt-audio-prefer-waveformatex-attribute.md) angegeben.
-   Die Kanalmaske, die Kanäle der Sprecherposition zuweist. Die Kanalmaske wird im MF \_ MT \_ AUDIO CHANNEL \_ \_ MASK-Attribut des Medientyps oder im **dwChannelMask-Member** der [**WAVEFORMATEXTENSIBLE-Struktur**](/windows/desktop/api/mmreg/ns-mmreg-waveformatextensible) angegeben.
-   Eine Matrix von Zuordnungsgewichtungen.

Die Matrix enthält eine Reihe von Gewichtungen, sodass jeder Ausgabekanal ein gewichteter Durchschnitt der Eingabekanäle ist.

Sie können eine benutzerdefinierte Matrix für die Kanalzuordnung angeben, indem Sie [**IWMResamplerProps::SetUserChannelMtx**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-setuserchannelmtx) aufrufen oder die [**MFPKEY \_ WMRESAMP \_ CHANNELMTX-Eigenschaft**](mfpkey-wmresamp-channelmtx.md) festlegen. Wenn keine benutzerdefinierte Matrix bereitgestellt wird, verwendet der Audio-Resampler einen Satz von Standardmatrizen.

## <a name="default-channel-mapping"></a>Standardkanalzuordnung

Wenn Sie keine benutzerdefinierte Matrix angeben, verwendet der Audio-Resampler-DSP Standardwerte für die Kanalzuordnung.

In den folgenden Tabellen werden die Kanäle abgekürzt:

-   L: Links
-   R: Rechts
-   C: Center
-   LFE: Low Frequence Effects
-   BL: Zurück links
-   BR: Zurück rechts
-   SL: Umschließen links
-   SR: Umrandung rechts

Die folgende Tabelle zeigt die Standardkoeffizienten für die Zuordnung von 6 Kanälen (maskieren 0x3F) zu 2 Kanälen.



|     | L     | R     | C     | Lfe   | BL    | BR    |
|-----|-------|-------|-------|-------|-------|-------|
| **L**   | 0.314 | 0     | 0.222 | 0.031 | 0,268 | 0.164 |
| **R**   | 0     | 0.314 | 0.222 | 0.031 | 0.164 | 0,268 |



 

Die folgende Tabelle zeigt die Standardkoeffizienten für die Zuordnung von 6 Kanälen (maskieren 0x60F) zu 2 Kanälen.



|     | L     | R     | C     | Lfe   | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|
| **L**   | 0.320 | 0     | 0.226 | 0.032 | 0.292 | 0.130 |
| **R**   | 0     | 0.320 | 0.226 | 0.032 | 0.130 | 0.292 |



 

Die folgende Tabelle zeigt die Standardkoeffizienten für die Zuordnung von 6 Kanälen (maskieren 0x3F oder 0x60F) zu 1 Kanal.



|     | L     | R     | C     | Lfe   | BL(SL) | BR(SR) |
|-----|-------|-------|-------|-------|--------|--------|
| **C**   | 0.192 | 0.192 | 0.192 | 0.038 | 0.192  | 0.192  |



 

Die folgende Tabelle zeigt die Standardkoeffizienten für die Zuordnung von 8 Kanälen (maskieren 0x63F) zu 2 Kanälen.



|     | L     | R     | C     | Lfe   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| **L**   | 0.222 | 0     | 0.157 | 0.022 | 0,189 | 0.116 | 0.203 | 0.090 |
| **R**   | 0     | 0.222 | 0.157 | 0.022 | 0.116 | 0,189 | 0.090 | 0.203 |



 

Die folgende Tabelle zeigt die Standardkoeffizienten für die Zuordnung von 8 Kanälen (maskieren 0x63F) zu 1 Kanal.



|     | L     | R     | C     | Lfe   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| **C**   | 0.139 | 0.139 | 0.139 | 0.028 | 0.139 | 0.139 | 0.139 | 0.139 |



 

Die folgende Tabelle zeigt die Standardkoeffizienten für die Zuordnung von 8 Kanälen (maskieren 0x63F) zu 6 Kanälen (maskieren 0x3F).



|     | L     | R     | C     | Lfe   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| **L**   | 0.518 | 0     | 0     | 0     | 0     | 0     | 0,189 | 0     |
| **R**   | 0     | 0.518 | 0     | 0     | 0     | 0     | 0     | 0,189 |
| **C**   | 0     | 0     | 0.518 | 0     | 0     | 0     | 0     | 0     |
| **Lfe** | 0     | 0     | 0     | 0.518 | 0     | 0     | 0     | 0     |
| **BL**  | 0     | 0     | 0     | 0     | 0.518 | 0     | 0.482 | 0     |
| **BR**  | 0     | 0     | 0     | 0     | 0     | 0.518 | 0     | 0.482 |



 

Die folgende Tabelle zeigt die Standardkoeffizienten für die Zuordnung von 8 Kanälen (mask 0x63F) zu 6 Kanälen (mask 0x60F).



|     | L     | R     | C     | Lfe   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| **L**   | 0.447 | 0     | 0     | 0     | 0     | 0     | 0     | 0     |
| **R**   | 0     | 0.447 | 0     | 0     | 0     | 0     | 0     | 0     |
| **C**   | 0     | 0     | 0.447 | 0     | 0     | 0     | 0     | 0     |
| **Lfe** | 0     | 0     | 0     | 0.447 | 0     | 0     | 0     | 0     |
| **Sl**  | 0     | 0     | 0     | 0     | 0.429 | 0.124 | 0.447 | 0     |
| **SR**  | 0     | 0     | 0     | 0     | 0.124 | 0.429 | 0     | 0.447 |



 

Um zu verstehen, wie die Tabellen von Koeffizienten interpretiert werden, betrachten Sie die erste Tabelle, die 6 Kanäle 2 zu ordnet. Die erste Zeile der Tabelle (0,314, 0, 0,222, 0,031, 0,268, 0,164) ist ein Gewichtungsvektor, der angibt, wie stark jeder Eingabekanal zum linken Kanal der Ausgabe beiträgt. Die zweite Zeile der Tabelle (0, 0,314, 0,222, 0,031, 0,164, 0,268) ist ein Gewichtungsvektor, der angibt, wie stark jeder Eingabekanal zum richtigen Kanal der Ausgabe beiträgt.

Die folgenden Formeln zeigen, wie die Ausgabekanäle berechnet werden.

``` syntax
L_out = L*0.314 + C*0.222 + LFE*0.031 + BL*0.268 + BR*0.164 
R_out = R*0.314 + C*0.222 + LFE*0.031 + BL*0.164 + BR*0.268
```

> [!Note]  
> Wenn Sie den Audio Resampler-DSP verwenden, um die Anzahl von Kanälen zu erhöhen, werden den hinzugefügten Kanälen Werte von 0 zugewiesen.

 

## <a name="output-quality"></a>Ausgabequalität

Sie können die Ausgabequalität des Audio Resampler-DSP angeben, indem Sie [**IWMResamplerProps::SetHalfFilterLength**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-sethalffilterlength) aufrufen oder die [**MFPKEY \_ WMRESAMP \_ FILTERQUALITY-Eigenschaft**](mfpkey-wmresamp-filterquality.md) festlegen. Wenn Sie die Ausgabequalität nicht angeben, verwendet der Audio Resampler-DSP einen Standardwert von 30.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Resampledmo.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

[Digitale Signalprozessoren](windowsmediadigitalsignalprocessors.md)
