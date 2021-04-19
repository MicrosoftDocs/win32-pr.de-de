---
description: Der audioresampler führt eine oder beide der folgenden Aktionen für einen Audiostream aus. Ändern Sie die Abtastrate. Ändern Sie die Anzahl der Kanäle.
ms.assetid: bee755c4-0585-40fb-aa4d-4e964f5144a3
title: Audio Resampler-DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb173fa4f8d964bec1102c4cfeefa4bf83f1ffe
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106367288"
---
# <a name="audio-resampler-dsp"></a>Audioresampler-DSP

Der audioresampler führt eine oder beide der folgenden Aktionen für einen Audiostream aus.

-   Ändern Sie die Abtastrate.
-   Ändern Sie die Anzahl der Kanäle.

## <a name="clsid"></a>CLSID

CLSID " \_ samsamplermediaobject"

## <a name="interfaces"></a>Schnittstellen

-   [**Imediaobject**](/previous-versions/ms785953(v=vs.85))
-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**Iwmresamplerproperties**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops)

## <a name="formats"></a>Formate

PCM-oder IEEE-Gleit Komma

Der Medientyp muss ein unkomprimiertes PCM oder Gleit Komma-Audioformat angeben.

-   Initialisieren Sie für die [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle den Medientyp, wie in [unkomprimierten Audiodateitypen](uncompressed-audio-media-types.md)beschrieben.
-   Bei der [**imediaobject**](/previous-versions/ms785953%28v%3dvs.85%29) -Schnittstelle muss der Medientyp ein **Format \_ WaveFormatEx** -Typ sein. Weitere Informationen finden Sie unter [**DMO \_ - \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type).

## <a name="properties"></a>Eigenschaften

-   [mfpkey \_ wmresamp \_ filterquality](mfpkey-wmresamp-filterquality.md)
-   [mfpkey \_ wmresamp \_ channelmtx](mfpkey-wmresamp-channelmtx.md)
-   [mfpkey \_ wmresamp \_ Lowpass- \_ Bandbreite](mfpkey-wmresamp-lowpass-bandwidth.md)

## <a name="required-attributes"></a>Erforderliche Attribute.

Der Resampler erfordert, dass die folgenden Attribute festgelegt werden:

-   [MF \_ \_ -MT \_ - \_ audiokanalmaske](mf-mt-audio-channel-mask-attribute.md)
-   [MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung](mf-mt-audio-block-alignment-attribute.md)

## <a name="custom-channel-mapping"></a>Benutzerdefinierte Kanal Zuordnung

Der audioresampler ordnet die eingabeaudiokanäle den audioweitergabekanälen zu, basierend auf den folgenden Informationen:

-   Die Anzahl der Kanäle. Dies wird im Attribut " [MF \_ MT \_ \_ audionum \_ Channels](mf-mt-audio-num-channels-attribute.md) " des Medientyps oder im **nchannels** -Member der [WaveFormatEx](mf-mt-audio-prefer-waveformatex-attribute.md) -Struktur angegeben.
-   Die Kanalmaske, die Kanäle der Redner Position zuweist. Die Kanalmaske wird im MF \_ MT \_ - \_ Audiokanal \_ Mask-Attribut des Medientyps oder im **dwchannelmask** -Member der [**WAVEFORMATEXTENSIBLE**](/windows/desktop/api/mmreg/ns-mmreg-waveformatextensible) -Struktur angegeben.
-   Eine Matrix von Mapping-Gewichtungen.

Die Matrix enthält eine Reihe von Gewichtungen, sodass jeder Ausgabekanal ein gewichteter Durchschnitt der Eingabe Kanäle ist.

Sie können eine benutzerdefinierte Matrix für die Kanal Zuordnung angeben, indem Sie [**iwmresamplerproperties:: setuserchannelmtx**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-setuserchannelmtx) aufrufen, oder indem Sie die Eigenschaft " [**mfpkey \_ wmresamp \_ channelmtx**](mfpkey-wmresamp-channelmtx.md) " festlegen. Wenn keine benutzerdefinierte Matrix bereitgestellt wird, verwendet der audioresampler eine Reihe von Standard Matrizen.

## <a name="default-channel-mapping"></a>Standard Kanal Zuordnung

Wenn Sie keine benutzerdefinierte Matrix angeben, verwendet der audioresampler-DSP Standardwerte für die Kanal Zuordnung.

In den folgenden Tabellen werden die Kanäle abgekürzt:

-   L: Links
-   R: rechts
-   C: zentrieren
-   LFE: geringe frequenzeffekte
-   BL: zurück Links
-   BR: zurück rechts
-   SL: umgeben Links
-   SR: rechts umschließen

In der folgenden Tabelle sind die Standard Koeffizienten für die Zuordnung von 6 Kanälen (Maske 0x3f) und 2 Kanälen aufgeführt.



|     | L     | R     | C     | LFE   | BL    | BR    |
|-----|-------|-------|-------|-------|-------|-------|
| L   | 0.314 | 0     | 0.222 | 0,031 | 0,268 | 0,164 |
| R   | 0     | 0.314 | 0.222 | 0,031 | 0,164 | 0,268 |



 

In der folgenden Tabelle sind die Standard Koeffizienten für die Zuordnung von 6 Kanälen (Maske 0x60f) und 2 Kanälen aufgeführt.



|     | L     | R     | C     | LFE   | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|
| L   | 0,320 | 0     | 0,226 | 0,032 | 0,292 | 0,130 |
| R   | 0     | 0,320 | 0,226 | 0,032 | 0,130 | 0,292 |



 

In der folgenden Tabelle sind die Standard Koeffizienten für die Zuordnung von 6-Kanälen (Maske 0x3f oder 0x60f) zu einem Kanal aufgeführt.



|     | L     | R     | C     | LFE   | BL (SL) | BR (SR) |
|-----|-------|-------|-------|-------|--------|--------|
| C   | 0,192 | 0,192 | 0,192 | 0,038 | 0,192  | 0,192  |



 

In der folgenden Tabelle sind die Standard Koeffizienten für die Zuordnung von 8 Kanälen (Maske 0x63f) und 2 Kanälen aufgeführt.



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0.222 | 0     | 0,157 | 0,022 | 0,189 | 0,116 | 0,203 | 0,090 |
| R   | 0     | 0.222 | 0,157 | 0,022 | 0,116 | 0,189 | 0,090 | 0,203 |



 

Die folgende Tabelle zeigt die Standard Koeffizienten für die Zuordnung von 8 Kanälen (Maske 0x63f) zu einem Kanal.



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| C   | 0,139 | 0,139 | 0,139 | 0,028 | 0,139 | 0,139 | 0,139 | 0,139 |



 

In der folgenden Tabelle sind die Standard Koeffizienten für die Zuordnung von 8 Kanälen (Maske 0x63f) und 6 Kanälen (Maske 0x3f) aufgeführt.



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,518 | 0     | 0     | 0     | 0     | 0     | 0,189 | 0     |
| R   | 0     | 0,518 | 0     | 0     | 0     | 0     | 0     | 0,189 |
| C   | 0     | 0     | 0,518 | 0     | 0     | 0     | 0     | 0     |
| LFE | 0     | 0     | 0     | 0,518 | 0     | 0     | 0     | 0     |
| BL  | 0     | 0     | 0     | 0     | 0,518 | 0     | 0,482 | 0     |
| BR  | 0     | 0     | 0     | 0     | 0     | 0,518 | 0     | 0,482 |



 

In der folgenden Tabelle sind die Standard Koeffizienten für die Zuordnung von 8 Kanälen (Maske 0x63f) und 6 Kanälen (Maske 0x60f) aufgeführt.



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,447 | 0     | 0     | 0     | 0     | 0     | 0     | 0     |
| R   | 0     | 0,447 | 0     | 0     | 0     | 0     | 0     | 0     |
| C   | 0     | 0     | 0,447 | 0     | 0     | 0     | 0     | 0     |
| LFE | 0     | 0     | 0     | 0,447 | 0     | 0     | 0     | 0     |
| SL  | 0     | 0     | 0     | 0     | 0,429 | 0,124 | 0,447 | 0     |
| SR  | 0     | 0     | 0     | 0     | 0,124 | 0,429 | 0     | 0,447 |



 

Um zu verstehen, wie die Tabellen von Koeffizienten interpretiert werden, sehen Sie sich die erste Tabelle an, die sechs Kanäle zu 2 zuordnet. Die erste Zeile der Tabelle (0,314, 0, 0,222, 0,031, 0,268, 0,164) ist ein Vektor von Gewichtungen, der angibt, wie stark jeder Eingabe Kanal zum linken Kanal der Ausgabe beiträgt. Die zweite Zeile der Tabelle (0, 0,314, 0,222, 0,031, 0,164, 0,268) ist ein Vektor von Gewichtungen, der angibt, wie stark jeder Eingabe Kanal zum rechten Kanal der Ausgabe beiträgt.

Die folgenden Formeln veranschaulichen, wie die Ausgabekanäle berechnet werden.

``` syntax
L_out = L*0.314 + C*0.222 + LFE*0.031 + BL*0.268 + BR*0.164 
R_out = R*0.314 + C*0.222 + LFE*0.031 + BL*0.164 + BR*0.268
```

> [!Note]  
> Wenn Sie das audioresampler-DSP verwenden, um die Anzahl der Kanäle zu erhöhen, werden den hinzugefügten Kanälen Werte von 0 zugewiesen.

 

## <a name="output-quality"></a>Ausgabequalität

Sie können die Ausgabequalität des-audioresampler-DSP angeben, indem Sie [**iwmresamplerproperties:: setthalffilterlength**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-sethalffilterlength) aufrufen, oder indem Sie die Eigenschaft " [**\_ \_ filterquality" für mfpkey**](mfpkey-wmresamp-filterquality.md) festlegen. Wenn Sie die Ausgabequalität nicht angeben, verwendet der audioresampler-DSP einen Standardwert von 30.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Resampledmo.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

[Digitale Signal Prozessoren](windowsmediadigitalsignalprocessors.md)
