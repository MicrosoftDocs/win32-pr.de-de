---
title: Lesen von Multichannelaudio
description: Lesen von Multichannelaudio
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows Medienformat-SDK, Lesen von Multichannelaudio
- Advanced Systems Format (ASF), Lesen von Multichannelaudio
- ASF (Advanced Systems Format), Lesen von Multichannelaudio
- Advanced Systems Format (ASF), Multichannel-Audio
- ASF (Advanced Systems Format), Multichannel-Audio
- Codecs, Lesen von Multichannelaudio
- Multichannelaudio, Lesen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ba314c6f2579bb18cd73593a775089c4b04b1c4a8ecd34868af911da29a67a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658530"
---
# <a name="reading-multichannel-audio"></a>Lesen von Multichannelaudio

Der Windows Media Audio 9 Professional Codec kann Mehrkanalaudio (mehr als zwei Kanäle) codieren. Wenn Sie eine Datei mit Multichannelaudio lesen, müssen Sie die Ausgabe ordnungsgemäß konfigurieren. Andernfalls werden die Audiodaten in einer niedrigeren Qualität und in Stereo übermittelt. Um eine Ausgabe für die Multichannelaudioübermittlung festzulegen, müssen Sie zwei Ausgabeeinstellungen festlegen: g \_ wszEnableDiscreteOutput und g \_ wszSpeakerConfig.

Wenn g \_ wszEnableDiscreteOutput auf **TRUE** festgelegt ist, wird der Codec für die Bereitstellung von High-Definition-Audioausgaben festgelegt. High-Definition-Audio wird vom Windows Media Audio 9-Codec mit 24-Bit-Beispielen in Stereo oder mehreren Kanälen codiert. Wenn diese Einstellung **FALSE** ist, wird nur die 16-Bit-Stereoausgabe übermittelt.

Die Anzahl der Lautsprecher auf dem wiedergabenden Computer wird mit g \_ wszSpeakerConfig festgelegt. Diese Einstellung ist ein **DWORD-Wert,** der auf eine der DirectSound-Sprecherkonstanten festgelegt ist, die in der folgenden Tabelle aufgeführt sind. Um diese konstanten Namen für Ihren Compiler aufzulösen, müssen Sie dsound.h einschließen.



| Konstante             | Wert      | Beschreibung                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DSSPEAKER \_ DIRECTOUT | 0x00000000 | Die Audiodaten werden direkt übergeben, ohne für Lautsprecher konfiguriert zu werden. |
| \_DSSPEAKER-SPRECHUNG | 0x00000001 | Der Clientcomputer ist mit 16000000000000000000000                             |
| DSSPEAKER \_ MONO      | 0x00000002 | Der Clientcomputer ist mit einem Lautsprecher ausgestattet.                     |
| DSSPEAKER \_ QUAD      | 0x00000003 | Der Clientcomputer ist mit quadrafonischen Lautsprechern ausgestattet.                  |
| DSSPEAKER \_ STEREO    | 0x00000004 | Der Clientcomputer ist mit Stereo-Lautsprechern ausgestattet.                        |
| DSSPEAKER \_ SURROUND  | 0x00000005 | Der Clientcomputer ist mit vierkanaligen Surround-Sound-Lautsprechern ausgestattet.   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | Der Clientcomputer ist mit fünf Lautsprechern und einem Subwoofer ausgestattet.          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | Der Clientcomputer ist mit sieben Lautsprechern und einem Subwoofer ausgestattet.         |



 

Verwenden Sie [**IWMReaderAdvanced2::SetOutputSetting,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)um diese Einstellungen festzulegen.

Damit die Kanäle diskret und ohne Aufklappung in Stereo ausgegeben werden, müssen Sie den richtigen Medientyp für die Ausgabe festlegen, indem Sie die folgenden Schritte ausführen:

1.  Rufen Sie [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) auf, um die Anzahl der unterstützten Formate für die relevante Audioausgabe abzurufen. Ausgabeformatindizes sind nullbasiert.
2.  Rufen Sie für jedes unterstützte Format [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) auf, um die [**IWMOutputMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) für das Ausgabemedieneigenschaftenobjekt abzurufen.
3.  Rufen Sie [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) auf, um den Medientyp abzurufen.
4.  Wenn der abgerufene Medientyp der gewünschte Multichanneltyp ist, legen Sie ihn fest, indem [**Sie IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops)aufrufen.

Nachdem Sie die diskrete Ausgabe und die Sprecherkonfiguration festgelegt haben, sollten die vom Reader aufzählten Ausgabeformate Mehrkanalformate enthalten, die die [**WAVEFORMATEXTENSIBLE-Struktur**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) verwenden. Wenn Sie die Ausgabeformate aufzählen, bevor Sie die Eigenschaften festlegen, werden nur Formate mit 1 oder 2 Kanälen und maximal 16 Bits pro Kanal eingeschlossen. Wie bei anderen Audioformaten sollten Sie nur die vom Reader aufzählten Formate verwenden. nicht ihre eigene konfigurieren.

> [!Note]  
> Sie können Multichannelaudio nur ausgeben, wenn Ihre Anwendung unter Microsoft Windows XP oder einer neueren Version von Microsoft Windows ausgeführt wird.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> <dt>

[**Ausgabe Einstellungen**](output-settings.md)
</dt> <dt>

[**Arbeiten mit High-Resolution PCM Audio**](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 