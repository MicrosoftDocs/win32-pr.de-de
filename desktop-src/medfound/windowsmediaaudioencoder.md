---
description: 'Der Windows Media Audio Encoder codiert Audiostreams. Der Encoder unterstützt drei Kategorien von codierter Ausgabe: Windows Media Audio Standard, Windows Media Audio Professional und Windows Media Audio Lossless.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Windows Medienaudioencoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba1a94ff5867282049521e3ac13ae28f949a7fc3ccd1855962fb9abb2217d3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117688184"
---
# <a name="windows-media-audio-encoder"></a>Windows Medienaudioencoder

Der Windows Media Audio Encoder codiert Audiostreams. Der Encoder unterstützt drei Kategorien von codierter Ausgabe: Windows Media Audio Standard, Windows Media Audio Professional und Windows Media Audio Lossless.

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) für den Windows Media Audio Encoder wird durch die konstante **CLSID \_ CWMAEncMediaObject** dargestellt. Sie können eine Instanz des Audioencoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="input-formats"></a>Eingabeformate

In der folgenden Tabelle sind die Audioformattags aufgeführt, die die vom Windows Media Audio-Encoder unterstützten Eingabekategorien darstellen. Informationen zum Festlegen der Eingabe- und Ausgabetypen für den Encoder finden Sie unter [Konfigurieren der Audiocodierung.](configuringaudioencoding.md)



| Formattagkonstante       | Tagwert formatieren | Audioformat                                          |
|---------------------------|------------------|-------------------------------------------------------|
| WAVE \_ FORMAT \_ PCM         | 0x0001           | PCM-Format                                            |
| WELLENFORMAT \_ \_ IEEE \_ FLOAT | 0x0003           | IEEE-Gleitkomma                                   |
| ERWEITERBARES \_ WAVEFORMAT \_  | 0xFFFE           | PCM-/IEEE-Format in **WAVEFORMATEXTENSIBLE-Struktur** |



 

## <a name="output-formats"></a>Ausgabeformate

Die folgende Tabelle zeigt die Audioformattags, die die ausgabekategorien darstellen, die vom Windows Media Audio Encoder unterstützt werden.



| Formattagkonstante             | Tagwert formatieren | Audioformat                     |
|---------------------------------|------------------|----------------------------------|
| WAVE \_ FORMAT \_ WMAUDIO2          | 0x0161           | Windows Medienaudiostandard     |
| WAVE \_ FORMAT \_ WMAUDIO3          | 0x0162           | Windows Medienaudio Professional |
| WAVEFORMAT \_ \_ WMAUDIO \_ LOSSLESS | 0x0163           | Windows Medienaudio verlustfrei     |



 

## <a name="interfaces"></a>Schnittstellen

Ein Audioobjekt macht die **IMediaObject-Schnittstelle** verfügbar, sodass das Objekt als DirectX Media Object (DMO) verwendet werden kann, und macht die **INTERFACESTransform-Schnittstelle** verfügbar, sodass das Objekt als Media Foundation Transform (MFT) verwendet werden kann.

Ein Windows Media Audio-Encoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird. Die folgende Tabelle zeigt die Bedingungen, unter denen sich ein Audioencoder als DMO oder MFT verhält.



| Betriebssystem | Encoderverhalten                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Ein Windows Media Audio-Encoder verhält sich immer als DMO.                                                                                                                                |
| Windows Vista    | Standardmäßig verhält sich ein Windows Media Audio-Encoder als DMO. Wenn Sie eine **OPCTransform-Schnittstelle** oder eine **IPropertyStore-Schnittstelle** auf einem Audioencoder erhalten, verhält sie sich wie ein MFT. |
| Windows 7        | Standardmäßig verhält sich ein Windows Media Audio-Encoder als DMO. Wenn Sie eine **ENCODERTransform-Schnittstelle** auf einem Audioencoder erhalten, verhält sich diese wie ein MFT.                                    |



 

## <a name="encoder-properties"></a>Encodereigenschaften

Der Windows Media Audio-Encoder unterstützt die folgenden Eigenschaften.



<table>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></td>
<td>Gibt an, ob der Encoder eine durchschnittlich steuerbare VBR-Codierung verwendet.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Gibt das Pufferfenster eines eingeschränkten VBR-Streams (Variable Bit-Rate) mit spitzen Bitraten in Millisekunden an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></td>
<td>Gibt an, ob der Encoder beim Ausführen der VBR-Codierung mit zwei Durchläufen die Datenkonsistenz über Durchläufe hinweg überprüfen soll. <br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></td>
<td>Gibt an, ob der Encoder durch eine maximale Decoderlatenzanforderung eingeschränkt ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></td>
<td>Gibt an, ob die Komplexität des Codierungsalgorithmus eingeschränkt ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></td>
<td>Gibt an, ob der Encoder durch eine maximale Latenzanforderung eingeschränkt ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Gibt an, ob vom Encoder aufzählte Modi auf dieJenigen beschränkt sind, die eine Qualitätsanforderungen erfüllen.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Gibt das Komplexitätsprofil des codierten Inhalts an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, Verlustlos.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Gibt die gewünschte Qualitätsstufe für die VBR-Codierung an.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></td>
<td>Gibt an, ob der Encoder Rauschuntersetzung verwendet.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></td>
<td>Gibt an, ob der Encoder PCM-Bereichsbegrenzung verwendet.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></td>
<td>Gibt die maximale codierte Bandbreite an, die durch Bandschneiden im Encoder zulässig ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></td>
<td>Gibt die minimale codierte Bandbreite an, die durch Bandschneiden im Encoder zulässig ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></td>
<td>Gibt die Qualität an, mit der die codierte Mindestbandbreite zulässig ist. <br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></td>
<td>Gibt die Qualität an, mit der die maximale codierte Bandbreite zulässig ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></td>
<td>Gibt an, ob der Encoder eine Bandschneidung ausführt.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></td>
<td>Gibt an, ob der Encoder den Stil der Maskenberechnung verwendet, der von Version 7 des Windows Media Audio Encoders ausgeführt wird.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></td>
<td>Gibt an, ob der Encoder die Stereobildverarbeitung ausführt. <br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></td>
<td>Gibt das Pufferfenster in Millisekunden für einen Encoder an, der für die Verwendung der durchschnittlich steuerbaren VBR-Codierung konfiguriert ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></td>
<td>Gibt die durchschnittliche Bitrate in Bits pro Sekunde für einen Encoder an, der für die Verwendung der durchschnittlich steuerbaren VBR-Codierung konfiguriert ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></td>
<td>Gibt die Komplexität des Codierungsalgorithmus an.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Gibt das Ende eines Codierungspasses an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></td>
<td>Gibt an, ob der Kernencoder das &quot; Plus-Feature &quot; verwendet.<br/> <dl> Windows Vista und höher.<br />
Professional.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></td>
<td>Gibt die maximale Latenz für den Decoder in Millisekunden an.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></td>
<td>Gibt die maximale Latenz für den Encoder in Millisekunden an.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Gibt die VBR-Qualitätsstufe des zuletzt aufzählten Ausgabetyps an.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Gibt die maximale Anzahl von Durchläufen an, die vom Encoder unterstützt werden.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, Verlustlos.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Gibt die Anzahl der Durchläufe an, die der Encoder zum Codieren des Inhalts verwendet.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></td>
<td>Gibt an, ob der Encoder durch eine Spitzenbitrate eingeschränkt ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></td>
<td>Gibt die bevorzugte Anzahl von Stichproben pro Frame an.<br/> <dl> Windows Vista und höher.<br />
Professional.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></td>
<td>Gibt an, ob der Encoder eine bevorzugte Framegröße verwenden soll.<br/> <dl> Windows Vista und höher.<br />
Professional.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Gibt die Spitzenbitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-VBR-Codierung (Variable-Bit-Rate) verwendet wird. <br/> <dl> Windows XP und höher.<br />
Standard, Professional.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></td>
<td>Gibt das durchschnittliche Pufferfenster eines codierten Streams in Millisekunden an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, Verlustlos.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></td>
<td>Gibt das maximale Pufferfenster eines codierten Streams in Millisekunden an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, Verlustlos.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></td>
<td>Gibt die durchschnittliche Bitrate eines codierten Streams in Bits pro Sekunde an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, Verlustlos.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></td>
<td>Gibt die maximale Bitrate eines codierten Streams in Bits pro Sekunde an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, Verlustlos.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Gibt an, ob der Encoder die VBR-Codierung verwendet.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></td>
<td>Diese Eigenschaft wird derzeit nicht vom Windows Media Audio-Codec verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Gibt die durchschnittliche Lautstärke des Audioinhalts an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, Verlustlos.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Gibt die höchste Volumeebene an, die in Audioinhalten auftritt.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, Verlustlos.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></td>
<td>Gibt die durchschnittlichen Bytes pro Sekunde für VBR-codierte Audiodaten an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, Verlustlos.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></td>
<td>Gibt an, ob der Encoder ein WMA-Paket pro Frame erzeugen soll.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></td>
<td>Gibt an, ob der Encoder Dynamische Bereichssteuerungsparameter generieren soll.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, Verlustlos.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></td>
<td>Gibt die <strong>WAVEFORMATEX-Struktur</strong> an, die den Audioeingabeinhalt beschreibt.<br/> <dl> Windows XP und höher.<br />
Standard, Professional.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></td>
<td>Gibt an, ob der Encoder die S/PDIF-Codierung in Echtzeit aktivieren soll.<br/> <dl> Windows Vista und höher.<br />
Professional.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmoe.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codecimplementierung](codecimplementation.md)
</dt> </dl>

 

 




