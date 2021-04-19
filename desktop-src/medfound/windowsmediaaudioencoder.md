---
description: 'Der Windows Media Audio Encoder codiert Audiostreams. Der Encoder unterstützt drei Kategorien codierter Ausgabe: Windows Media Audio Standard, Windows Media Audio Professional und Windows Media Audio Lossless.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Windows Media Audio Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361429"
---
# <a name="windows-media-audio-encoder"></a>Windows Media Audio Encoder

Der Windows Media Audio Encoder codiert Audiostreams. Der Encoder unterstützt drei Kategorien codierter Ausgabe: Windows Media Audio Standard, Windows Media Audio Professional und Windows Media Audio Lossless.

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) für den Windows Media Audio Encoder wird durch die Konstante **CLSID \_ cwmaencmediaobject** dargestellt. Sie können eine Instanz des Audioencoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="input-formats"></a>Eingabeformate

Die folgende Tabelle zeigt die audioformattags, die die vom Windows Media Audio Encoder unterstützten Eingabe Kategorien darstellen. Weitere Informationen zum Festlegen der Eingabe-und Ausgabetypen für den Encoder finden Sie unter [Konfigurieren der Audiocodierung](configuringaudioencoding.md).



| Tagkonstante formatieren       | Tagwert formatieren | Audioformat                                          |
|---------------------------|------------------|-------------------------------------------------------|
| PCM im Wave- \_ Format \_         | 0x0001           | PCM-Format                                            |
| "Wave \_ Format \_ IEEE \_ float" | 0x0003           | IEEE-Gleit Komma                                   |
| \_erweiterbares Wave-Format \_  | 0xFFFE           | PCM/IEEE-Format in der **WAVEFORMATEXTENSIBLE** -Struktur |



 

## <a name="output-formats"></a>Ausgabeformate

Die folgende Tabelle zeigt die audioformattags, die die vom Windows Media Audio Encoder unterstützten Ausgabe Kategorien darstellen.



| Tagkonstante formatieren             | Tagwert formatieren | Audioformat                     |
|---------------------------------|------------------|----------------------------------|
| Wave- \_ Format \_ WMAUDIO2          | 0x0161           | Standard Windows Media Audio     |
| Wave- \_ Format \_ WMAUDIO3          | 0x0162           | Windows Media Audio Professional |
| \_ \_ wmaudioverlust im Wave-Format \_ | 0x0163           | Verlust von Windows Media Audio Verlust     |



 

## <a name="interfaces"></a>Schnittstellen

Ein audioendoder-Objekt macht die **imediaobject** -Schnittstelle verfügbar, sodass das Objekt als DirectX Media Object (DMO) verwendet werden kann, und stellt die **imftransform** -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.

Ein Windows Media Audio Encoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird. In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Audioencoder als DMO oder MFT verhält.



| Betriebssystem | Codierungs Verhalten                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Ein Windows Media Audio Encoder verhält sich immer als DMO.                                                                                                                                |
| Windows Vista    | Standardmäßig verhält sich ein Windows Media Audio Encoder als DMO. Wenn Sie eine **imftransform** -Schnittstelle oder eine **IPropertyStore** -Schnittstelle in einem Audioencoder abrufen, verhält sie sich wie eine MFT. |
| Windows 7        | Standardmäßig verhält sich ein Windows Media Audio Encoder als DMO. Wenn Sie eine **imftransform** -Schnittstelle für einen Audioencoder erhalten, verhält sie sich wie eine MFT.                                    |



 

## <a name="encoder-properties"></a>Codierungs Eigenschaften

Der Windows Media Audio Encoder unterstützt die folgenden Eigenschaften.



<table>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></td>
<td>Gibt an, ob der Encoder eine Average-steuerbare VBR-Codierung verwendet.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der Spitzen Bitrate in Millisekunden an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></td>
<td>Gibt an, ob der Encoder bei der Durchführung einer zweistufigen VBR-Codierung eine übergreifende Datenkonsistenz überprüfen soll. <br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></td>
<td>Gibt an, ob der Encoder durch eine maximale Anzahl von decoderlatenzanforderungen eingeschränkt wird.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></td>
<td>Gibt an, ob die Komplexität des Codierungs Algorithmus eingeschränkt ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></td>
<td>Gibt an, ob der Encoder durch eine maximale Latenz Anforderung eingeschränkt wird.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Gibt an, ob vom Encoder aufgelistete Modi auf diejenigen beschränkt sind, die eine Qualitätsanforderung erfüllen.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Gibt das Komplexitäts Profil des codierten Inhalts an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, verlustfrei.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Gibt die gewünschte Qualitätsstufe für die VBR-Codierung an.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></td>
<td>Gibt an, ob der Encoder die Rausch Ersetzung verwendet.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></td>
<td>Gibt an, ob der Encoder PCM-Bereichs Beschränkung verwendet.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></td>
<td>Gibt die maximale codierte Bandbreite an, die für die bandtrunzierung im Encoder zulässig ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></td>
<td>Gibt die minimale codierte Bandbreite an, die für die Band abkürzen im Encoder zulässig ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></td>
<td>Gibt die Qualität an, mit der die minimale codierte Bandbreite zulässig ist. <br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></td>
<td>Gibt die Qualität an, mit der die maximale codierte Bandbreite zulässig ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></td>
<td>Gibt an, ob der Encoder die bandtrunzierung ausführt.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></td>
<td>Gibt an, ob der Encoder den Stil der Masken Berechnung verwendet, der von Version 7 des Windows Media Audio Encoders ausgeführt wird.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></td>
<td>Gibt an, ob der Encoder die Stereobild Verarbeitung ausführt. <br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></td>
<td>Gibt das Puffer Fenster (in Millisekunden) für einen Encoder an, der für die Verwendung der durchschnittlich kontrollierbaren VBR-Codierung konfiguriert ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></td>
<td>Gibt die durchschnittliche Bitrate in Bits pro Sekunde für einen Encoder an, der für die Verwendung der durchschnittlich kontrollierbaren VBR-Codierung konfiguriert ist.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></td>
<td>Gibt die Komplexität des Codierungs Algorithmus an.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Gibt das Ende eines Codierungs Durchlaufs an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></td>
<td>Gibt an, ob der kerncodierer das &quot; Plus- &quot; Feature verwendet.<br/> <dl> Windows Vista und höher.<br />
Professional.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></td>
<td>Gibt die maximale Latenzzeit für den Decoder in Millisekunden an.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></td>
<td>Gibt die maximale Latenzzeit für den Encoder in Millisekunden an.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Gibt die VBR-Qualitätsstufe des zuletzt aufgezählten Ausgabe Typs an.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Gibt die maximale Anzahl von durch den Encoder unterstützten Durchläufen an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, verlustfrei.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Gibt die Anzahl von Durchläufen an, die der Encoder zum Codieren des Inhalts verwendet.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></td>
<td>Gibt an, ob der Encoder durch eine Spitzen Bitrate eingeschränkt wird.<br/> <dl> Windows Vista und höher.<br />
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
<td>Gibt an, ob der Encoder eine bevorzugte Frame Größe verwenden soll.<br/> <dl> Windows Vista und höher.<br />
Professional.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Gibt die Spitzen Bitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-VBR-Codierung (Variable Bitrate) verwendet wird. <br/> <dl> Windows XP und höher.<br />
Standard, Professional.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></td>
<td>Gibt das durchschnittliche Puffer Fenster (in Millisekunden) eines codierten Streams an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, verlustfrei.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></td>
<td>Gibt das maximale Puffer Fenster (in Millisekunden) eines codierten Streams an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, verlustfrei.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></td>
<td>Gibt die durchschnittliche Bitrate eines codierten Streams in Bits pro Sekunde an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, verlustfrei.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></td>
<td>Gibt die maximale Bitrate eines codierten Streams in Bits pro Sekunde an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, verlustfrei.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Gibt an, ob der Encoder die VBR-Codierung verwendet.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></td>
<td>Diese Eigenschaft wird derzeit nicht vom Windows Media Audio Codec verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Gibt die durchschnittliche Volumeebene von Audioinhalten an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, verlustfrei.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Gibt die höchste volumenbene an, die im Audioinhalt auftritt.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, verlustfrei.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></td>
<td>Gibt die durchschnittlichen Bytes pro Sekunde für VBR-codierte Audiodaten an.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, verlustfrei.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></td>
<td>Gibt an, ob der Encoder 1 WMA-Paket pro Frame liefern soll.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></td>
<td>Gibt an, ob der Encoder dynamische Bereichs Steuerungsparameter generieren soll.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></td>
<td>Gibt die <strong>WaveFormatEx</strong> -Struktur an, die den audioinhaltstyp beschreibt.<br/> <dl> Windows XP und höher.<br />
Standard, Professional.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></td>
<td>Gibt an, ob der Encoder die S/PDIF-Echtzeitcodierung aktivieren soll.<br/> <dl> Windows Vista und höher.<br />
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
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmoe.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codec-Implementierung](codecimplementation.md)
</dt> </dl>

 

 




