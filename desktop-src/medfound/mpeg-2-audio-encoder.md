---
description: Der Microsoft Media Foundation MPEG-2-Audioencoder ist eine Media Foundation Transformation, die Mono-oder Stereo-Audiodaten in MPEG-1-Audiodaten (ISO/IEC 11172-3) oder MPEG-2-Audiodaten (ISO/IEC 13818-3) codiert.
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: MPEG-2-Audioencoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863423"
---
# <a name="mpeg-2-audio-encoder"></a>MPEG-2-Audioencoder

Der Microsoft Media Foundation MPEG-2-Audioencoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die Mono-oder Stereo-Audiodaten in MPEG-1-Audiodaten (ISO/IEC 11172-3) oder MPEG-2-Audiodaten (ISO/IEC 13818-3) codiert.

Der Encoder unterstützt Layer 1-und Layer 2-Audiodaten. MPEG-Layer 3-Audiodatei (MP3) wird nicht unterstützt. Für MPEG-2 unterstützt der Encoder den LSF-Teil (Low Sampling Häufigkeits) von MPEG-2-Audiodaten. Die Multichannel-Erweiterungen werden nicht unterstützt. Der MFT gibt einen MPEG-elementaren Stream aus. Es können keine Legenden Datenströme, Programmstreams oder Transportdaten Ströme erstellt werden.

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) des mepg-2-Audioencoders ist **CLSID- \_ CMPEG2AudioEncoderMFT**, die in der Header Datei "wmcodecdsp. h" definiert ist.

## <a name="output-types"></a>Ausgabetypen

Der Ausgabetyp muss zuerst festgelegt werden, vor dem Eingabetyp. In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Ausgabe Medientyp aufgeführt.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
<th>Bemerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Der Haupttyp.</td>
<td>Erforderlich. Muss <strong>MFMediaType_Audio</strong>werden.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Audiountertyp.</td>
<td>Erforderlich. Muss <strong>MFAudioFormat_MPEG</strong>werden. Dieser Untertyp wird sowohl für MPEG-1-als auch für MPEG-2-Audiodaten verwendet.</td>
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
Außerdem werden die folgenden Werte für MPEG-2 LSF unterstützt: <br/>
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
<td>Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</td>
<td>Dies ist optional. Wenn festgelegt, muss der Wert 0x3 für Stereo (Front Left und Right Channels) oder 0x4 für Mono (Front-Center-Kanal) lauten.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Die Bitrate des codierten MPEG-Streams in Bytes pro Sekunde.</td>
<td>Dies ist optional.<br/> Die Spezifikationen ISO/IEC 11172-3 und ISO/IEC 13818-3 (LSF) definieren verschiedene Bitraten, abhängig von der Abtastrate, der Anzahl der Kanäle und der Audioschicht (1 oder 2). <br/> Der Encoder verwendet standardmäßig Layer 2-Audiodaten. Wenn das <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> -Attribut nicht festgelegt ist, verwendet der Encoder die folgenden Standard Bitraten:<br/>
<ul>
<li>MPEG-1 Stereo: 224.000 Bits pro Sekunde (Bit/s) = 28.000 Byte pro Sekunde.</li>
<li>MPEG-1 Mono: 192.000 Bit/s = 24.000 Byte pro Sekunde.</li>
<li>MPEG-2 LSF, Mono oder Stereo: 160.000 Bit/s = 20.000 Byte pro Sekunde.</li>
</ul>
Dieses Attribut kann auf andere Werte festgelegt werden. Wenn der Wert gemäß den MPEG-Spezifikationen ungültig ist, lehnt der MFT den Medientyp ab.<br/> Sie können auch die Bitrate mithilfe der <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>icodecapi</strong></a> -Schnittstelle festlegen. Weitere Informationen finden Sie unter Hinweise.<br/></td>
</tr>
</tbody>
</table>



 

Wenn die optionalen Attribute nicht festgelegt sind, fügt der Encoder Sie dem Medientyp hinzu, nachdem der Typ festgelegt wurde.

## <a name="input-types"></a>Eingabetypen

In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Eingabe Medientyp aufgeführt.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
<th>Bemerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Der Haupttyp.</td>
<td>Erforderlich. Muss <strong>MFMediaType_Audio</strong>werden.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Audiountertyp.</td>
<td>Erforderlich. Muss <strong>MFAudioFormat_PCM</strong> oder <strong>MFAudioFormat_Float</strong>sein.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Anzahl von Bits pro audiostich Probe.</td>
<td>Erforderlich. Der Wert muss 16 sein, wenn der Untertyp <strong>MFAudioFormat_PCM</strong>ist, oder 32, wenn der Untertyp <strong>MFAudioFormat_Float</strong>ist.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Stichproben pro Sekunde.</td>
<td>Erforderlich. Muss mit dem Ausgabetyp identisch sein.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Anzahl der Kanäle.</td>
<td>Erforderlich. Muss mit dem Ausgabetyp identisch sein.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Block Ausrichtung (in Bytes).</td>
<td>Erforderlich. Berechnen Sie den Wert wie folgt:
<ul>
<li><strong>MFAudioFormat_PCM</strong>: Anzahl der Kanäle × 2.</li>
<li><strong>MFAudioFormat_Float</strong>: Anzahl der Kanäle × 4.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Die Bitrate des codierten AC3-Streams in Bytes pro Sekunde.</td>
<td>Erforderlich. Muss die Block Ausrichtung × Samples pro Sekunde gleich sein.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</td>
<td>Dies ist optional. Wenn festgelegt, muss der Wert mit dem Ausgabetyp identisch sein.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Anzahl gültiger Bits von Audiodaten in jedem Audiobeispiel.</td>
<td>Dies ist optional. Wenn dieser Wert festgelegt ist, muss der Wert mit <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>identisch sein.</td>
</tr>
</tbody>
</table>



 

Der Encoder unterstützt keine Stichproben Raten Konvertierung oder Stereo/Mono-Konvertierung. Wenn die optionalen Attribute nicht festgelegt sind, fügt der Encoder Sie dem Medientyp hinzu, nachdem der Typ festgelegt wurde.

## <a name="codec-properties"></a>Codec-Eigenschaften

Der Encoder unterstützt die folgenden Eigenschaften über die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle.



| Eigenschaft                                                                                | BESCHREIBUNG                                                                                      | Standardwert                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codecapi \_ avenccommonmeanbitrate](../directshow/avenccommonmeanbitrate-property.md)               | Gibt die durchschnittliche codierte Bitrate in Bits pro Sekunde an.                                      | Wie für das Attribut [MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) im Ausgabe Medientyp beschrieben.                      |
| [Codecapi \_ avencmpacodingmode](../directshow/avencmpacodingmode-property.md)                       | Gibt den MPEG-audiocodierungs Modus an.                                                          | Stereo für 2-Kanal-Audiodaten oder einzelner Kanal für 1-Kanal-Audiodaten.<br/> Für zweistufige Audiodaten unterstützt der Encoder auch Dual Kanäle und Joint Stereo.<br/> |
| [Codecapi \_ avencmpacopyright](../directshow/avencmpacopyright-property.md)                         | Gibt an, ob das Copyright-Bit im MPEG-Audiostream festgelegt wird.                             | Kein Copyright.                                                                                                                                                          |
| [Codecapi \_ avencmpbetonung sType](../directshow/avencmpaemphasistype-property.md)                   | Gibt den Typ des deduplizierungsfilters an, der verwendet werden soll, wenn der codierte Stream decodiert wird. | Es wurde kein Schwerpunkt angegeben.                                                                                                                                                 |
| [Avencmpenableredundancyprotection](../directshow/avencmpaenableredundancyprotection-property.md) | Gibt an, ob dem Frame Header eine zyklische Redundanz Überprüfung (CRC) hinzugefügt werden soll.                    | Eine CRC-Prüfsumme wird in den Bitstream geschrieben.                                                                                                                           |
| [Codecapi \_ avencmpalayer](../directshow/avencmpalayer-property.md)                                 | Gibt die MPEG-Audioschicht an.                                                                  | Layer 2-Audiodatei.                                                                                                                                                         |
| [Codecapi \_ avencmporiginalbitstream](../directshow/avencmpaoriginalbitstream-property.md)         | Gibt an, ob für das ursprüngliche Bit im MPEG-Audiostream festgelegt werden soll.                          | "Ursprüngliches" Bit ist deaktiviert.                                                                                                                                                 |
| [Codecapi \_ avencmpaprivateuserbit](../directshow/avencmpaprivateuserbit-property.md)               | Gibt an, ob für das private Benutzer Bit im MPEG-Audiostream festgelegt werden soll.                      | Privates Benutzer Bit ist deaktiviert.                                                                                                                                               |



 

Um einen Zeiger auf die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle abzurufen, nennen Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf der MFT.

Die MFT implementiert die folgenden [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Methoden:

-   [**Getparameterrange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**Ismodifizierbar**](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

Alle anderen [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Methoden geben **E \_ notimpl** zurück.

## <a name="remarks"></a>Bemerkungen

Jeder MPEG-audioframe enthält entweder 384 (Layer 1)-oder 1152 (Layer 2)-Audiobeispiele pro Kanal. Jeder Eingabepuffer für den Encoder kann jedoch eine beliebige Anzahl von PCM-Stichproben enthalten. Die Größe jedes Eingabe Puffers muss ein Vielfaches der Block Ausrichtung sein. Der Encoder speichert Eingabe Beispiele zwischen, bis er für einen MPEG-audioframe ausreichend ist.

Jeder Ausgabepuffer enthält einen unformatierten MPEG-Frame. Die Größe jedes Ausgabepuffers hängt von der Bitrate und der Stichprobenrate ab.

### <a name="configuring-the-encoder"></a>Konfigurieren des Encoders

Um die Standardeinstellungen für den Encoder zu ändern, führen Sie die folgenden Schritte aus:

1.  Erstellen Sie eine Instanz des MFT-Encoders.
2.  Aufrufen von [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , um die Liste der bevorzugten Ausgabetypen zu erhalten. Der Encoder listet alle Stichproben Raten für Mono und Stereo auf. Wählen Sie basierend auf der Samplingrate und der Anzahl der Kanäle einen der folgenden Medientypen aus. Das Attribut " [MF \_ MT \_ audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) " gibt die Standard Bitrate in Byte pro Sekunde an.
3.  Optional: Sie können die standardbitrate überschreiben, indem Sie für den Ausgabe Medientyp einen neuen Wert für " [MF \_ MT \_ -audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) " festlegen. Gültige Bitraten sind abhängig von der Abtastrate, der Anzahl der Kanäle und der Audioschicht.
    > [!Note]  
    > An dieser Stelle im Konfigurationsprozess verwendet der Encoder standardmäßig Layer 2-Audiodaten und akzeptiert nur Layer 2-Bitraten. In einem späteren Schritt können Sie den Encoder auf Schicht 1 umstellen (siehe Schritt 7). Überlassen Sie in diesem Fall die Standard Bitrate für jetzt. Sie können Sie in Schritt 8 wieder ändern.

     

4.  Aufrufen von [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) zum Festlegen des Ausgabemedien Typs. Wenn Sie einen eigenen Wert für " [MF \_ MT \_ -audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) " festlegen und der MFT den Ausgabe Medientyp ablehnt, liegt dies wahrscheinlich daran, dass Sie eine ungültige Bitrate angegeben haben.
5.  Aufrufen von [**imftransform:: getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) zum Aufzählen des Eingabemedien Typs. Da die Stichprobenrate und die Anzahl der Kanäle mit dem Ausgabetyp identisch sein müssen, werden nur zwei Optionen aufgelistet: 32-Bit-Gleit Komma-PCM-Eingabe und 32-Bit-ganzzahlige PCM-Eingabe. Wählen Sie eine der folgenden aus.
6.  Greifen Sie auf [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) zu, um den Eingabe Medientyp festzulegen.
7.  Optional: Legen Sie zum Codieren von Layer-1-Audiodaten die [codecapi-Eigenschaft " \_ avencmpalayer](../directshow/avencmpalayer-property.md) " auf **eavencmpalayer \_ 1** fest.
8.  Optional: um die Bitrate zu ändern, legen Sie die [codecapi-Eigenschaft " \_ avenccommonmeanbitrate](../directshow/avenccommonmeanbitrate-property.md) " fest. Die Bitrate muss eine der gültigen Bitraten sein, die in den LSF-Spezifikationen MPEG-1 oder MPEG-2 aufgeführt sind. Alternativ können Sie [**icodecapi:: getParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) aufrufen, um eine Liste gültiger Bitraten basierend auf den aktuellen Einstellungen abzurufen.
9.  Optional: mit der 2-Kanal-Audiodatei können Sie die [codecapi-Eigenschaft " \_ avencmpacodingmode](../directshow/avencmpacodingmode-property.md) " festlegen, um den Codierungs Modus in den dualen Kanal oder den gemeinsamen Stereo zu ändern. Sie können [**icodecapi:: getparameterrange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) aufrufen, um die gültigen Optionen zu erhalten. (Für eine audioaudioschnittstelle ist die einzige Option Mono.)
10. Optional: Legen Sie alle anderen zuvor aufgeführten [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Eigenschaften fest.

Es ist wichtig, die Reihenfolge dieser Schritte zu befolgen. Legen Sie insbesondere den Ausgabe Medientyp vor dem Ändern von [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Eigenschaften fest. Außerdem müssen Sie die **icodecapi** -Eigenschaften festlegen, bevor das erste Eingabe Beispiel vom MFT empfangen wird. Nachdem die MFT Eingaben empfangen hat, sind die Codec-Eigenschaften schreibgeschützt, und [**icodecapi:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) gibt den Wert **S \_ false** zurück.

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

### <a name="example-media-types"></a>Beispiel Medientypen

Im folgenden finden Sie ein Beispiel für die Medientypen, die zum Codieren von ganzzahligen 16-Bit-PCM, 48-kHz-Stereo Audiodaten mit der Standard Bitrate benötigt werden.

Ausgabe Medientyp:

| Attribut                                                                           | Wert                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [Haupt-Typ des MF- \_ MT \_ \_](mf-mt-major-type-attribute.md)                               | **MF MediaType \_ -Audiodatei**  |
| [MF- \_ MT- \_ Untertyp](mf-mt-subtype-attribute.md)                                      | **MF Audioformat \_ MPEG** |
| [MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde](mf-mt-audio-samples-per-second-attribute.md) | 48000                   |
| [MF \_ \_ -MT- \_ audionum- \_ Kanäle](mf-mt-audio-num-channels-attribute.md)              | 2                       |



 

Eingabe Medientyp:

| Attribut                                                                                | Wert                  |
|------------------------------------------------------------------------------------------|------------------------|
| [Haupt-Typ des MF- \_ MT \_ \_](mf-mt-major-type-attribute.md)                                    | **MF MediaType \_ -Audiodatei** |
| [MF- \_ MT- \_ Untertyp](mf-mt-subtype-attribute.md)                                           | **MF Audioformat \_ PCM** |
| [MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [MF \_ \_ -MT- \_ audionum- \_ Kanäle](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                 |
| DLL<br/>                      | <dl> <dt>Msmpeg2enc.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
