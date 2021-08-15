---
description: Der Microsoft Media Foundation MPEG-2-Audioencoder ist eine Media Foundation-Transformation, die Mono- oder Stereoaudio in MPEG-1-Audio (ISO/IEC 11172-3) oder MPEG-2-Audio (ISO/IEC 13818-3) codiert.
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: MPEG-2-Audioencoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 935b6438c79e9bf78a230f707f8930f859c3fa491dab0326208d5cf79b53f474
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240009"
---
# <a name="mpeg-2-audio-encoder"></a>MPEG-2-Audioencoder

Der Microsoft Media Foundation MPEG-2-Audioencoder ist eine [Media Foundation-Transformation,](media-foundation-transforms.md) die Mono- oder Stereoaudio in MPEG-1-Audio (ISO/IEC 11172-3) oder MPEG-2-Audio (ISO/IEC 13818-3) codiert.

Der Encoder unterstützt Layer 1- und Layer 2-Audio. MPEG-Layer 3-Audio (MP3) wird nicht unterstützt. Für MPEG-2 unterstützt der Encoder den Teil mit niedrigen Samplinghäufigkeiten (Low Sampling Frequencies, LSF) von MPEG-2-Audio. Multichannelerweiterungen werden nicht unterstützt. Der MFT gibt einen elementaren MPEG-Stream aus. Es können keine paketisierten elementaren Datenströme, Programmstreams oder Transportstreams generiert werden.

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) des MEPG-2-Audioencoders ist **CLSID \_ CMPEG2AudioEncoderMFT,** definiert in der Headerdatei wmcodecdsp.h.

## <a name="output-types"></a>Ausgabetypen

Der Ausgabetyp muss zuerst vor dem Eingabetyp festgelegt werden. In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Ausgabemedientyp aufgeführt.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>BESCHREIBUNG</th>
<th>Bemerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Haupttyp.</td>
<td>Erforderlich. Muss <strong>MFMediaType_Audio</strong>sein.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Audiountertyp.</td>
<td>Erforderlich. Muss <strong>MFAudioFormat_MPEG</strong>sein. Dieser Untertyp wird sowohl für MPEG-1- als auch MPEG-2-Audio verwendet.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Stichproben pro Sekunde.</td>
<td>Erforderlich. Die folgenden Werte werden sowohl für MPEG-1 als auch für MPEG-2 unterstützt:
<ul>
<li>32000</li>
<li>44100</li>
<li>48000</li>
</ul>
Darüber hinaus werden die folgenden Werte für MPEG-2 LSF unterstützt: <br/>
<ul>
<li>16000</li>
<li>22050</li>
<li>24.000</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Anzahl der Kanäle.</td>
<td>Erforderlich. Muss entweder 1 (Mono) oder 2 (Stereo) sein.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Gibt die Zuweisung von Audiokanälen zu Sprecherpositionen an.</td>
<td>Optional. Wenn diese Einstellung festgelegt ist, muss der Wert für Stereo (frontlinker und rechter Kanal) oder 0x4 für Mono (Front-Center-Kanal) 0x3 werden.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Bitrate des codierten MPEG-Streams in Bytes pro Sekunde.</td>
<td>Optional.<br/> Die SPEZIFIKATIONEN ISO/IEC 11172-3 und ISO/IEC 13818-3 (LSF) definieren mehrere Bitraten, abhängig von der Samplingrate, der Anzahl der Kanäle und der Audioschicht (1 oder 2). <br/> Der Encoder verwendet standardmäßig Layer 2-Audio. Wenn das <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> Attribut nicht festgelegt ist, verwendet der Encoder die folgenden Standardbitraten:<br/>
<ul>
<li>MPEG-1 stereo: 224.000 Bits pro Sekunde (bps) = 28.000 Bytes pro Sekunde.</li>
<li>MPEG-1 mono: 192.000 bps = 24.000 Bytes pro Sekunde.</li>
<li>MPEG-2 LSF, Mono oder Stereo: 160.000 Bps = 20.000 Bytes pro Sekunde.</li>
</ul>
Dieses Attribut kann auf andere Werte festgelegt werden. Wenn der Wert gemäß MPEG-Spezifikationen ungültig ist, lehnt der MFT den Medientyp ab.<br/> Sie können die Bitrate auch mithilfe der <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI-Schnittstelle</strong></a> festlegen. Weitere Informationen finden Sie unter Hinweise.<br/></td>
</tr>
</tbody>
</table>



 

Wenn die optionalen Attribute nicht festgelegt sind, fügt der Encoder sie dem Medientyp hinzu, nachdem der Typ festgelegt wurde.

## <a name="input-types"></a>Eingabetypen

In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Eingabemedientyp aufgeführt.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>BESCHREIBUNG</th>
<th>Bemerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Haupttyp.</td>
<td>Erforderlich. Muss <strong>MFMediaType_Audio</strong>sein.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Audiountertyp.</td>
<td>Erforderlich. Muss <strong>MFAudioFormat_PCM</strong> oder <strong>MFAudioFormat_Float</strong>sein.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Anzahl von Bits pro Audiobeispiel.</td>
<td>Erforderlich. Der Wert muss 16 sein, wenn der Untertyp <strong>MFAudioFormat_PCM</strong>ist, oder 32, wenn der Untertyp <strong>MFAudioFormat_Float</strong>ist.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Stichproben pro Sekunde.</td>
<td>Erforderlich. Muss mit dem Ausgabetyp übereinstimmen.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Anzahl der Kanäle.</td>
<td>Erforderlich. Muss mit dem Ausgabetyp übereinstimmen.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Blockausrichtung in Bytes.</td>
<td>Erforderlich. Berechnen Sie den Wert wie folgt:
<ul>
<li><strong>MFAudioFormat_PCM:</strong>Anzahl der Kanäle × 2.</li>
<li><strong>MFAudioFormat_Float:</strong>Anzahl der Kanäle × 4.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Bitrate des codierten AC3-Streams in Bytes pro Sekunde.</td>
<td>Erforderlich. Muss der Blockausrichtung × Stichproben pro Sekunde entsprechen.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Gibt die Zuweisung von Audiokanälen zu Sprecherpositionen an.</td>
<td>Optional. Wenn diese Einstellung festgelegt ist, muss der Wert mit dem Ausgabetyp übereinstimmen.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Anzahl der gültigen Bits von Audiodaten in jedem Audiobeispiel.</td>
<td>Optional. Wenn festgelegt, muss der Wert mit dem <a href="mf-mt-audio-bits-per-sample-attribute.md">Wert</a>MF_MT_AUDIO_BITS_PER_SAMPLE.</td>
</tr>
</tbody>
</table>



 

Der Encoder unterstützt keine Abtastratenkonvertierung oder Stereo-/Monokonvertierung. Wenn die optionalen Attribute nicht festgelegt sind, fügt der Encoder sie dem Medientyp hinzu, nachdem der Typ festgelegt wurde.

## <a name="codec-properties"></a>Codec-Eigenschaften

Der Encoder unterstützt die folgenden Eigenschaften über die [**ICodecAPI-Schnittstelle.**](/windows/win32/api/strmif/nn-strmif-icodecapi)



| Eigenschaft                                                                                | BESCHREIBUNG                                                                                      | Standardwert                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)               | Gibt die durchschnittliche codierte Bitrate in Bits pro Sekunde an.                                      | Wie für das [MF \_ MT AUDIO \_ \_ AVG BYTES PER \_ \_ \_ SECOND-Attribut](mf-mt-audio-avg-bytes-per-second-attribute.md) im Ausgabemedientyp beschrieben.                      |
| [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md)                       | Gibt den MPEG-Audiocodierungsmodus an.                                                          | Stereo für 2-Kanal-Audio oder ein Kanal für 1-Kanal-Audio.<br/> Für 2-Kanal-Audio unterstützt der Encoder auch Dualkanal- und Gemeinsame Stereo.<br/> |
| [CODECAPI \_ AVEncMPACopyright](../directshow/avencmpacopyright-property.md)                         | Gibt an, ob das Copyrightbit im MPEG-Audiostream festgelegt werden soll.                             | Kein Copyright.                                                                                                                                                          |
| [CODECAPI \_ AVEncMPAEmphasisType](../directshow/avencmpaemphasistype-property.md)                   | Gibt den Typ des Filters zur De-Hervorhebung an, der beim Decodieren des codierten Streams verwendet werden soll. | Es wurde keine Hervorhebung angegeben.                                                                                                                                                 |
| [AVEncMPAEnableRedundancyProtection](../directshow/avencmpaenableredundancyprotection-property.md) | Gibt an, ob dem Frameheader eine zyklische Redundanzprüfung (CRC) hinzugefügt werden soll.                    | Eine CRC-Prüfsumme wird in den Bitstream geschrieben.                                                                                                                           |
| [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md)                                 | Gibt die MPEG-Audioebene an.                                                                  | Layer 2-Audio.                                                                                                                                                         |
| [CODECAPI \_ AVEncMPAOriginalBitstream](../directshow/avencmpaoriginalbitstream-property.md)         | Gibt an, ob für das ursprüngliche Bit im MPEG-Audiostream festgelegt werden soll.                          | Das "Original"-Bit ist deaktiviert.                                                                                                                                                 |
| [CODECAPI \_ AVEncMPAPrivateUserBit](../directshow/avencmpaprivateuserbit-property.md)               | Gibt an, ob für das private Benutzerbit im MPEG-Audiostream festgelegt werden soll.                      | Privates Benutzerbit ist deaktiviert.                                                                                                                                               |



 

Um einen Zeiger auf die [**ICodecAPI-Schnittstelle zu**](/windows/win32/api/strmif/nn-strmif-icodecapi) erhalten, rufen [**Sie QueryInterface auf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) dem MFT auf.

MFT implementiert die folgenden [**ICodecAPI-Methoden:**](/windows/win32/api/strmif/nn-strmif-icodecapi)

-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**IsModifiable**](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [**Issupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

Alle anderen [**ICodecAPI-Methoden**](/windows/win32/api/strmif/nn-strmif-icodecapi) geben **E \_ NOTIMPL zurück.**

## <a name="remarks"></a>Hinweise

Jeder MPEG-Audioframe enthält entweder 384 (Schicht 1) oder 1152 (Schicht 2) Audiobeispiele pro Kanal. Jeder Eingabepuffer für den Encoder kann jedoch eine beliebige Anzahl von PCM-Stichproben enthalten. Die Größe jedes Eingabepuffers muss ein Vielfaches der Blockausrichtung sein. Der Encoder speichert Eingabebeispiele zwischen, bis er genügend für einen MPEG-Audioframe hat.

Jeder Ausgabepuffer enthält einen unformatten MPEG-Frame. Die Größe der einzelnen Ausgabepuffer hängt von der Bitrate und der Abtastrate ab.

### <a name="configuring-the-encoder"></a>Konfigurieren des Encoders

Führen Sie die folgenden Schritte aus, um die Standardeinstellungen für den Encoder zu ändern:

1.  Erstellen Sie eine Instanz des Encoder-MFT.
2.  Rufen [**Sie DEN TYP 1::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf, um die Liste der bevorzugten Ausgabetypen zu erhalten. Der Encoder aufzählt alle Abtastraten für Mono und Stereo. Wählen Sie basierend auf der Abtastrate und der Anzahl der Kanäle einen dieser Medientypen aus. Das [MF \_ MT AUDIO \_ \_ AVG BYTES PER \_ \_ \_ SECOND-Attribut](mf-mt-audio-avg-bytes-per-second-attribute.md) gibt die Standardbitrate in Bytes pro Sekunde an.
3.  Optional: Sie können die Standardbitrate überschreiben, indem Sie einen neuen Wert für [MF \_ MT AUDIO \_ \_ AVG BYTES PER \_ \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) für den Ausgabemedientyp festlegen. Gültige Bitraten hängen von der Abtastrate, der Anzahl der Kanäle und der Audioebene ab.
    > [!Note]  
    > An diesem Punkt des Konfigurationsprozesses verwendet der Encoder standardmäßig Layer 2-Audio und akzeptiert nur Layer-2-Bitraten. Sie können den Encoder in einem späteren Schritt auf Ebene 1 umschalten (siehe Schritt 7). Belasse in diesem Fall vorerst die Standardbitrate. Sie können ihn in Schritt 8 erneut ändern.

     

4.  Rufen [**Sie ZUM Festlegen des Ausgabemedientyps DEN WERTTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) auf. Wenn Sie einen eigenen Wert für [MF \_ MT AUDIO \_ \_ AVG BYTES PER \_ \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) festlegen und der MFT den Ausgabemedientyp zurückweisen, liegt dies wahrscheinlich daran, dass Sie eine ungültige Bitrate angegeben haben.
5.  Rufen [**Sie DEN TYP DER EINGABETRANSFORM::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) auf, um den Eingabemedientyp aufzählen. Da die Abtastrate und die Anzahl der Kanäle mit dem Ausgabetyp identisch sein müssen, werden nur zwei Optionen aufzählt: 32-Bit-PCM-Eingabe mit Gleitkomma und PCM-Eingabe mit 16-Bit-Ganzzahl. Wählen Sie eine dieser Beiden aus.
6.  Rufen [**Sie ZUM Festlegen des Eingabemedientyps DEN WERTTRANSFORM::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) auf.
7.  Optional: Legen Sie zum Codieren von Layer 1-Audio die [ \_ CODECAPI-Eigenschaft AVEncMPALayer](../directshow/avencmpalayer-property.md) auf **eAVEncMPALayer \_ 1 fest.**
8.  Optional: Legen Sie zum Ändern der Bitrate die [ \_ CODECAPI-Eigenschaft AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) fest. Die Bitrate muss eine der gültigen Bitraten sein, die in den MPEG-1- oder MPEG-2-LSF-Spezifikationen aufgeführt sind. Alternativ können Sie [**ICodecAPI::GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) aufrufen, um basierend auf den aktuellen Einstellungen eine Liste gültiger Bitraten zu erhalten.
9.  Optional: Mit 2-Kanal-Audio können Sie die [ \_ CODECAPI-Eigenschaft AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) festlegen, um den Codierungsmodus in Dual-Channel- oder Joint Stereo-Modus zu ändern. Sie können [**ICodecAPI::GetParameterRange aufrufen,**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) um die gültigen Optionen zu erhalten. (Für 1-Kanal-Audio ist mono die einzige Option.)
10. Optional: Legen Sie eine der anderen zuvor aufgeführten [**ICodecAPI-Eigenschaften**](/windows/win32/api/strmif/nn-strmif-icodecapi) fest.

Es ist wichtig, die Reihenfolge dieser Schritte zu befolgen. Legen Sie insbesondere den Ausgabemedientyp fest, bevor Sie [**ICodecAPI-Eigenschaften**](/windows/win32/api/strmif/nn-strmif-icodecapi) ändern. Außerdem müssen Sie **ICodecAPI-Eigenschaften** festlegen, bevor MFT das erste Eingabebeispiel empfängt. Nachdem MFT Eingaben empfangen hat, sind die Codeceigenschaften schreibgeschützt, und [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) gibt den Wert **S FALSE \_ zurück.**

### <a name="supported-bit-rates"></a>Unterstützte Bitraten

Der Encoder unterstützt die folgenden Bitraten.



MPEG-1

MPEG-2

Ebene 1

Layer 2-

Ebene 1

Layer 2-

32

32\*

32

8

64

48\*

38

16

96

56\*

56

24

128

64

64

32

160

80\*

80

40

192

96

96

48

224

112

112

56

256

128

128

64

288

160

144

80

320

192

160

96

352

224\*\*

176

112

384

256\*\*

192

128

416

230\*\*

224

144

448

384\*\*

256

160



 

<dl> \* Nur Mono  
\*\* Nur Stereo  
</dl>

### <a name="example-media-types"></a>Beispielmedientypen

Hier sehen Sie ein Beispiel für die Medientypen, die zum Codieren von 16-Bit-Ganzzahl-PCM-Stereoaudio mit 48 kHz mit der Standardbitrate erforderlich sind.

Ausgabemedientyp:

| attribute                                                                           | Wert                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [MF \_ \_ MT-HAUPTTYP \_](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ Audio**  |
| [MF \_ \_ MT-UNTERTYP](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ MPEG** |
| [MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE](mf-mt-audio-samples-per-second-attribute.md) | 48000                   |
| [MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS](mf-mt-audio-num-channels-attribute.md)              | 2                       |



 

Eingabemedientyp:

| attribute                                                                                | Wert                  |
|------------------------------------------------------------------------------------------|------------------------|
| [MF \_ \_ MT-HAUPTTYP \_](mf-mt-major-type-attribute.md)                                    | **MFMediaType \_ Audio** |
| [MF \_ \_ MT-UNTERTYP](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [MF \_ \_ MT-AUDIOBITS \_ \_ PRO \_ BEISPIEL](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                 |
| DLL<br/>                      | <dl> <dt>Msmpeg2enc.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
