---
description: Der Dolby-Audiodecoder ist ein MFT, das Dolby Digital (AC-3) und Dolby Digital Plus decodiert.
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: Dolby-Audiodecoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f1d8ca21cb3ab86f1fdbeddf03624aaaffb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749264"
---
# <a name="dolby-audio-decoder"></a>Dolby-Audiodecoder

Der Dolby-Audiodecoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) (MFT), mit der die folgenden Streamtypen decodiert werden:

-   Dolby Digital, auch Dolby AC-3 genannt
-   Dolby Digital Plus, auch Enhanced AC-3 (E-AC-3) genannt

> [!IMPORTANT]
> Bei Windows-Versionen vor Windows 8 ist die Microsoft-Implementierung der Dolby Digital-Technologie gemäß den Bedingungen des Dolby Digital Licensing Program, das von Microsoft-Anwendungen verwendet werden soll, eingeschränkt.

 

Weitere Informationen zu diesen Formaten finden Sie im Advanced TV Systems Committee (ATSC) Document *Digital audiocompression Standard (AC-3, E-AC-3) Revision B*.

Der Decoder kann auch einen Dolby Digital Plus-Datenstrom in ein Dolby Digital-Format für die AC-3 S/pidf-Ausgabe konvertieren oder einen Dolby Digital Plus-Datenstrom für die digitale HDMI-Ausgabe formatieren.

## <a name="class-identifier"></a>Klassen Bezeichner

Die Klassen-ID (CLSID) des Dolby-Audiodecoders ist **CLSID \_ cmsddplusdecmft**, die in der Header Datei "wmcodecdsp. h" definiert ist.

## <a name="input-types"></a>Eingabetypen

Der Dolby Audiodecoder unterstützt die folgenden Eingabe Untertypen.



| Subtype                                 | BESCHREIBUNG                                                                                                                                                 | Header       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **Mediasubtype \_ Dolby \_ AC3**            | Dolby Digital-Audiodatei.                                                                                                                                        | mfapi. h      |
| **mediasubtype \_ DVM**                   | Dolby Digital-Audiodatei; siehe [**audiountertypen**](../directshow/audio-subtypes.md). Dieser Untertyp kann austauschbar mit **mediasubtype \_ Dolby \_ AC3** verwendet werden.<br/> | wmcodecdsp. h |
| **MF Audioformat \_ Dolby \_ Digital \_ Plus** | Dolby Digital Plus-Audiodatei.                                                                                                                                   | mfapi. h      |



 

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
<td>Erforderlich. Weitere Informationen finden Sie in der vorherigen Tabelle.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Abtastrate in Samplings pro Sekunde.</td>
<td>Dies ist optional. Gültige Werte sind: 48000, 44100, 32000, 24000, 22050 und 16000. Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert 48000. <br/>
<blockquote>
[!Note]<br />
Dolby AC-3-Streams sind auf die drei höchsten Sätze in dieser Liste beschränkt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Anzahl der Kanäle, einschließlich des LFE-Kanals (Low Frequency), falls vorhanden.</td>
<td>Dies ist optional. Gültige Werte liegen im Bereich von 1 (Mono) bis 8 (7,1 Channel-Konfiguration). Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert 2 (Stereo).</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</td>
<td>Dies ist optional. Wenn angegeben, muss der Wert mit der Anzahl der Audiokanäle konsistent sein. Wenn das-Attribut nicht festgelegt ist, verwendet der Decoder eine Standard Kanalmaske, basierend auf der Anzahl der Kanäle.</td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle sind die unterstützten Dolby Channel-Konfigurationen aufgeführt.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Kanal Konfiguration</th>
<th>Anzahl von Kanälen</th>
<th>Kanalmasken</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1/0 (Mono)</td>
<td>1</td>
<td>0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</td>
</tr>
<tr class="even">
<td>2/0 (Stereo) oder 1 + 1 (Dual Mono)</td>
<td>2</td>
<td>0x3 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>)</td>
</tr>
<tr class="odd">
<td>3/0</td>
<td>3</td>
<td>0x7 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</td>
</tr>
<tr class="even">
<td>2/1</td>
<td>3</td>
<td>0x103 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</td>
</tr>
<tr class="odd">
<td>3/1</td>
<td>4</td>
<td>0x107 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</td>
</tr>
<tr class="even">
<td>2/2</td>
<td>4</td>
<td>0x33 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)<br/> oder<br/> 0x603 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>) <br/></td>
</tr>
<tr class="odd">
<td>3/2</td>
<td>5</td>
<td>0x37 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)<br/> oder<br/> 0x607 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>) <br/></td>
</tr>
<tr class="even">
<td>3/2 + LFE</td>
<td>6</td>
<td>0x3f (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)<br/> oder<br/> 0x60f (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)<br/></td>
</tr>
<tr class="odd">
<td>3/2/2 + LFE
<blockquote>
[!Note]<br />
Nur Dolby Digital Plus.
</blockquote>
<br/> <br/></td>
<td>8</td>
<td>0x63f (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</td>
</tr>
</tbody>
</table>



 

Außerdem können die Kanal Konfigurationen 1/0, 2/0, 3/0, 2/1, 3/1 und 2/2 ebenfalls mit einem LFE-Kanal angezeigt werden.

## <a name="output-types"></a>Ausgabetypen

Der Dolby-Audiodecoder unterstützt die folgenden Ausgabe Untertypen.



| Subtype                                                   | BESCHREIBUNG                                                                                                                               | Header    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **MF Audioformat \_ Dolby \_ AC3 \_ SPDIF**                      | Dolby AC-3-audioformatierung für die digitale S/PDIF-Ausgabe.                                                                                     | mfapi. h   |
| **Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ Digital \_ Plus** | Dolby Digital Plus-Audiodatei für die digitale Codec-Ausgabe formatiert.                                                                               | ksmedia. h |
| **MF Audioformat ( \_ float)**                                  | IEEE 32-Bit-PCM für Gleit Komma-PCM<br/> **Windows 10**: Stereo, 5,1, 7,1<br/> **Vorherige Versionen**: Stereo, 5,1<br/> | mfapi. h   |
| **MF Audioformat \_ PCM**                                    | 16-Bit-PCM-Audiodaten<br/> **Windows 10**: Stereo, 5,1, 7,1<br/> **Vorherige Versionen**: Stereo, 5,1<br/>                     | mfapi. h   |



 

In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Ausgabe Medientyp aufgeführt.



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
<td>Erforderlich. Weitere Informationen finden Sie in der vorherigen Tabelle.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Abtastrate in Samplings pro Sekunde.</td>
<td>Erforderlich. Gültige Werte sind: 48000, 44100, 32000, 24000, 22050 und 16000. Die Ausgabe Stichproben Rate muss mit der Eingabe Stichproben Rate identisch sein. Der Decoder kann die Samplingrate des Streams nicht ändern.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Anzahl der Kanäle, einschließlich des LFE-Kanals (Low Frequency), falls vorhanden.</td>
<td>Erforderlich für die PCM-Ausgabe. <br/> Bei digitaler Ausgabe nicht erforderlich. <br/> Wenn der Eingabetyp Mono, Stereo oder Dual-Mono (alle ohne LFE-Kanal) ist, ist der einzige gültige Wert 2 für die Stereoausgabe. Andernfalls kann der Wert wie folgt lauten: <br/>
<ul>
<li>2 für Stereo Downmix</li>
<li>6 für 5,1-Kanal Konfigurationen</li>
<li>8 für 7,1-Kanal Konfigurationen</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</td>
<td>Erforderlich für die PCM-Ausgabe, wenn die Anzahl der Kanäle größer als 2 ist. Der Wert muss wie folgt lauten:<br/>
<ul>
<li>0x3 für Stereoausgabe</li>
<li>0x3f für 5,1-Kanal Ausgabe</li>
<li>0x63f für 7,1-Kanal Ausgabe</li>
</ul>
Bei digitaler Ausgabe nicht erforderlich. <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Anzahl von Bits pro audiostich Probe.</td>
<td>Erforderlich für die PCM-Ausgabe. Der Wert muss 32 für <strong>MFAudioFormat_Float</strong>und 16 für <strong>MFAudioFormat_PCM</strong>sein.<br/> Bei digitaler Ausgabe nicht erforderlich.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Anzahl gültiger Bits von Audiodaten in jedem Audiobeispiel.</td>
<td>Optional für die PCM-Ausgabe. Wenn dieser Wert festgelegt ist, muss der Wert mit <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>identisch sein.<br/> Für die digitalen Ausgabe Untertypen nicht erforderlich.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Block Ausrichtung (in Bytes).</td>
<td>Optional für die PCM-Ausgabe. Bei digitaler Ausgabe nicht erforderlich.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Die durchschnittliche Anzahl von Bytes pro Sekunde.</td>
<td>Optional für die PCM-Ausgabe. Bei digitaler Ausgabe nicht erforderlich.</td>
</tr>
</tbody>
</table>



 

## <a name="transform-attributes"></a>Transformations Attribute

Der Dolby-Audiodecoder implementiert die [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode. Die Anwendung kann diese Methode verwenden, um die folgenden Attribute zu erhalten oder festzulegen.



| Attribut                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codecapi \_ avdecaudiodualmono](../directshow/avdecaudiodualmono-property.md)                        | Gibt an, ob ein Dolby-Audiostream mit zwei Kanälen als Stereo-oder Dual-Mono-codiert wird. Bevor der erste Dolby-Frame decodiert wird, ist **eavdecaudiodualmono \_ nicht angegeben**. Nachdem das Decodieren begonnen hat, spiegelt der Wert den letzten Dolby-Frame wider.<br/> Schreibgeschützt. <br/> |
| [Codecapi \_ avdecaudiodualmonorepromode](../directshow/avdecaudiodualmonorepromode-property.md)      | Gibt an, wie der Decoder Dual-Mono-Audiodaten wiederherstellt. Der Standardwert ist **eavdecaudiodualmonorepromode \_ left \_ Mono**. Diese Eigenschaft kann von der Anwendung jederzeit festgelegt werden.<br/> Lese-/Schreibzugriff.<br/>                                                                            |
| [Codecapi \_ avdeccommonmeanbitrate](../directshow/avdeccommonmeanbitrate.md)                         | Gibt für Dolby Digital (AC-3)-Streams die Bitrate des Eingabedaten Stroms in Bits pro Sekunde an. Für Dolby Digital Plus (E-AC3) ist der Wert immer 0 (null).<br/> Schreibgeschützt.<br/>                                                                                              |
| [Codecapi \_ avdecdddynamicrangescalehigh](../directshow/avdecdddynamicrangescalehigh-property.md)    | Der auf hoher Ebene ausgeschnittene, wenn der Decoder das dynamische Bereichs Steuerelement ausführt.<br/> Lese-/Schreibzugriff.<br/>                                                                                                                                                                                    |
| [Codecapi \_ avdecdddynamicrangescalelow](../directshow/avdecdddynamicrangescalelow-property.md)      | Die Verstärkung auf niedriger Ebene, wenn der Decoder das dynamische Bereichs Steuerelement ausführt.<br/> Lese-/Schreibzugriff.<br/>                                                                                                                                                                                   |
| [Codecapi \_ avdecddoperationalmode](../directshow/avdecddoperationalmode-property.md)                | Der Komprimierungs Steuerelement Modus.<br/> Lese-/Schreibzugriff.<br/>                                                                                                                                                                                                                          |
| [Codecapi \_ avdecddstereodownmixmode](codecapi-avdecddstereodownmixmode.md)              | Der Typ der Stereo downmischung. Diese Eigenschaft ist gültig, wenn es sich bei der Eingabe um einen Multichannel-Stream handelt und die Ausgabe ein Stereodaten Strom ist<br/> Lese-/Schreibzugriff.<br/>                                                                                                                           |
| [MFT- \_ Unterstützung für \_ dynamisches \_ Format \_ ändern](mft-support-dynamic-format-change-attribute.md) | Dieses Attribut gibt **false** zurück, um anzugeben, dass der Decoder vor dem Festlegen eines neuen Eingabetyps entladen werden muss.<br/> Lese-/Schreibzugriff.<br/>                                                                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Der Decoder akzeptiert nur unformatierte Dolby Streams, wie von A/52b definiert. Nutzlasten, wie z. b. "packetisiert Elementary Streams" (PES) werden nicht unterstützt. Für Dolby Digital Plus decodiert der Decoder bis zu 5,1 Kanäle. Unter Windows 10 werden 7,1-kanalstreams ohne Downmix decodiert. Bei früheren Betriebssystemversionen, wenn der Stream 7,1-Kanäle ist, wird nur die 5,1-kanaldownmischung decodiert. Wenn der Stream Dolby Digital Plus mit mehr als einem unabhängigen untergeordneten Stream ist, wird nur der unabhängige unter Datenstrom 0 decodiert. Der Decoder überspringt andere unabhängige unter Ströme. Außerdem überspringt der Decoder alle abhängigen unter Ströme. Der Decoder unterstützt das Entschlüsseln und Decodieren von Streams, die durch Digital Rights Management-Technologie (DRM) geschützt sind.

Wenn der Eingabe Medientyp über eine andere Kanal Konfiguration als Mono, Stereo oder Dual-Mono (ohne LFE-Kanal) verfügt, stellt der Decoder zwei Optionen für die Ausgabekanal Konfigurationen bereit:

-   8-Kanal-Ausgabe (7,1-Kanal Konfiguration)
-   6-Kanal-Ausgabe (5,1-Kanal Konfiguration)
-   Stereo-Downmix

Wenn Stereo Downmix ausgewählt ist, kann der Typ von Downmix auf der MFT mithilfe der [codecapi \_ avdecddstereodownmixmode](codecapi-avdecddstereodownmixmode.md) -Eigenschaft festgelegt werden.

Wenn der Ausgabetyp **MF Audioformat \_ Dolby \_ AC3 \_ SPDIF** ist, enthält jeder Ausgabepuffer 6.144 bytes. Der Puffer beginnt mit einem 8-Byte-S/PDIF-Header, gefolgt von einem komprimierten AC-3-Frame, gefolgt von 0 (null) bis 6.144 bytes.

Wenn der Ausgabetyp **ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ Digital \_ plus** ist, enthält jeder Ausgabepuffer 24.576 Bytes. Der Puffer beginnt mit einem 8-Byte-S/PDIF-Header, gefolgt von 1 – 6 komprimierten Dolby Digital Plus-Frames, die 1.536 PCM-Stichproben entsprechen, gefolgt von einer NULL-Auffüll Funktion auf 24.576 Bytes. Bei der HDMI-Ausgabe wird nur der unabhängige unter Datenstrom 0 gepackt.

Der Decoder-MFT ist mit dem Flag " **MFT \_ Enum \_ Flag \_ fieldofuse**" registriert, das angibt, dass die MFT von der Anwendung vor der Verwendung entsperrt werden muss. Weitere Informationen finden Sie unter [Einschränkungen](field-of-use-restrictions.md)für das Feld "Verwendung".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                  |
| DLL<br/>                      | <dl> <dt>Msauddecmft.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
