---
description: Der Windows Media Audio-Decoder decodiert Audiostreams, die vom Windows Media Audio Encoder codiert wurden.
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: Windows Media Audio Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359279"
---
# <a name="windows-media-audio-decoder"></a>Windows Media Audio Decoder

Der Windows Media Audio-Decoder decodiert Audiostreams, die vom [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md)codiert wurden. Der Encoder und der Decoder unterstützen drei Kategorien codierter Audiodaten: Windows Media Audio Standard, Windows Media Audio Professional und Windows Media Audio Lossless.

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) für den Windows Media Audio Decoder wird durch die Konstante **CLSID \_ cwmadecmediaobject** dargestellt. Sie können eine Instanz des Audiodecoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="input-formats"></a>Eingabeformate

Die folgende Tabelle zeigt die audioformattags, die die vom Windows Media Audio Decoder unterstützten Eingabe Kategorien darstellen. Informationen zum Festlegen der Eingabe-und Ausgabetypen für den Decoder finden Sie unter [Konfigurieren der Audiodecodierung](configuringaudiodecoding.md).



| Tagkonstante formatieren             | Tagwert formatieren | Audioformat                     |
|---------------------------------|------------------|----------------------------------|
| Wave- \_ Format \_ WMAUDIO2          | 0x0161           | Standard Windows Media Audio     |
| Wave- \_ Format \_ WMAUDIO3          | 0x0162           | Windows Media Audio Professional |
| \_ \_ wmaudioverlust im Wave-Format \_ | 0x0163           | Verlust von Windows Media Audio Verlust     |



 

## <a name="output-formats"></a>Ausgabeformate

Die folgende Tabelle zeigt die audioformattags, die die vom **Windows Media Audio Decoder** unterstützten Ausgabetypen darstellen. Informationen zum Festlegen der Eingabe-und Ausgabetypen für den Decoder finden Sie unter [Konfigurieren der Audiocodierung](configuringaudioencoding.md).



| Tagkonstante formatieren       | Tagwert formatieren | Audioformat                                          |
|---------------------------|------------------|-------------------------------------------------------|
| PCM im Wave- \_ Format \_         | 0x0001           | PCM-Format                                            |
| "Wave \_ Format \_ IEEE \_ float" | 0x0003           | IEEE-Gleit Komma                                   |
| \_erweiterbares Wave-Format \_  | 0xFFFE           | PCM/IEEE-Format in der **WAVEFORMATEXTENSIBLE** -Struktur |



 

## <a name="interfaces"></a>Schnittstellen

Ein Audiodecoder-Objekt macht die **imediaobject** -Schnittstelle verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und stellt die **imftransform** -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.

Ein Windows Media Audio Decoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird. In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Audiodecoder als DMO oder MFT verhält.



| Betriebssystem | Decoderverhalten                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Ein Windows Media Audio Decoder verhält sich immer als DMO.                                                                                                                                |
| Windows Vista    | Standardmäßig verhält sich ein Windows Media Audio Decoder als DMO. Wenn Sie eine **imftransform** -Schnittstelle oder eine **IPropertyStore** -Schnittstelle in einem Audiodecoder abrufen, verhält sie sich wie eine MFT. |
| Windows 7        | Standardmäßig verhält sich ein Windows Media Audio Decoder als DMO. Wenn Sie eine **imftransform** -Schnittstelle für einen Audiodecoder erhalten, verhält sie sich wie eine MFT.                                    |



 

## <a name="properties"></a>Eigenschaften

Der Windows Media Audio-Decoder unterstützt die folgenden Eigenschaften.



<table>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></td>
<td>Gibt die maximale Anzahl zusätzlicher PCM-Beispiele an, die möglicherweise am Ende der Decodierung einer Datei zurückgegeben werden.<br/> <dl> Windows Vista und höher.<br />
Standard, Professional, verlustfrei.<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></td>
<td>Gibt den dynamischen Bereichs Steuerungs Modus an, den der Audiodecoder verwendet.<br/> <dl> Windows XP und höher.<br />
Standard, Professional, verlustfrei.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></td>
<td>Gibt die vom Autor bereitgestellten Fold-Koeffizienten für das Decodieren von Multichannel-Audiodaten für weniger Kanäle an, als der codierte Stream enthält. <br/> <dl> Windows XP und höher.<br />
Professionell<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></td>
<td>Gibt an, ob der Audiodecoder eine hochauflösende Ausgabe bereitstellt.<br/> <dl> Windows XP und höher.<br />
Professional, verlustfrei.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></td>
<td>Gibt an, ob der Audiodecoder Lt-Rt-Fold ausführen soll.<br/> <dl> Windows Vista und höher.<br />
Professional.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></td>
<td>Gibt die Sprecher Konfiguration auf dem Client Computer an.<br/> <dl> Windows XP und höher.<br />
Professional.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Gibt die durchschnittliche Volumeebene von Audioinhalten an.<br/> <dl> Windows XP und höher.<br />
Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></td>
<td>Gibt die gewünschte durchschnittliche Volumeebene der Ausgabe Audioinhalte an.<br/> <dl> Windows XP und höher.<br />
Professional, verlustfrei.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Gibt die höchste volumenbene an, die im Audioinhalt auftritt.<br/> <dl> Windows XP und höher.<br />
Professional, verlustfrei.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></td>
<td>Gibt die gewünschte maximale Volumeebene der Ausgabe Audioinhalte an.<br/> <dl> Windows XP und höher.<br />
Professional, verlustfrei.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmod.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codec-Implementierung](codecimplementation.md)
</dt> </dl>

 

 




