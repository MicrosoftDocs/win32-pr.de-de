---
title: Lesen von Multichannel-Audiodateien
description: Lesen von Multichannel-Audiodateien
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows Media Format SDK, Lesen von Multichannel-Audiodaten
- Advanced Systems Format (ASF), Lesen von Multichannel-Audiodaten
- ASF (Advanced Systems Format), Lesen von Multichannel-Audiodaten
- Advanced Systems Format (ASF), Multichannel-Audiodatei
- ASF (Advanced Systems Format), Multichannel-Audiodatei
- Codecs, Lesen von Multichannel-Audiodaten
- Multichannel-Audiodaten, lesen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59da950eb4218ad87995ed80e22de4de302f8e42
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729456"
---
# <a name="reading-multichannel-audio"></a>Lesen von Multichannel-Audiodateien

Der Windows Media Audio 9 Professional-Codec kann Multichannel-Audiocodierung (mehr als zwei Kanäle) codieren. Wenn Sie eine Datei mit Multichannel-Audiodaten lesen, müssen Sie die Ausgabe ordnungsgemäß konfigurieren, oder die Audiodaten werden in einer niedrigeren Qualität und in Stereo bereitgestellt. Zum Festlegen einer Ausgabe für die Multichannel-audioübermittlung müssen Sie zwei Ausgabeeinstellungen festlegen: g \_ wszene ablediskreteoutput und g \_ wszspeakerconfig.

Durch Festlegen \_ von g wszene ablediskreteoutput auf **true** wird der Codec so festgelegt, dass eine hochauflösende Audioausgabe bereitstellt wird. High-Definition-Audiodaten werden vom Windows Media Audio 9-Codec mit 24-Bit-Beispielen in Stereo-oder mehreren Kanälen codiert. Wenn diese Einstellung auf " **false**" festgelegt ist, wird nur eine 16-Bit-Stereoausgabe übermittelt.

Die Anzahl der Redner auf dem Spielcomputer wird mit g \_ wszspeakerconfig festgelegt. Diese Einstellung ist ein **DWORD** -Wert, der auf eine der in der folgenden Tabelle aufgeführten DirectSound-Sprecher Konstanten festgelegt ist. Um diese Konstanten Namen für den Compiler aufzulösen, müssen Sie DSound. h einschließen.



| Konstante             | Wert      | BESCHREIBUNG                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| dsspeaker- \_ directout | 0x00000000 | Die Audiodaten werden direkt durchlaufen, ohne für Referenten konfiguriert zu werden. |
| dsspeaker- \_ Telefon | 0x00000001 | Der Client Computer ist mit einem Kopfhörer ausgestattet.                             |
| dsspeaker \_ Mono      | 0x00000002 | Der Client Computer ist mit einem monalen Redner ausgestattet.                     |
| dsspeaker \_ Quad      | 0x00000003 | Der Client Computer ist mit quadratischen sprechenden Referenten ausgestattet.                  |
| dsspeaker- \_ Stereo    | 0x00000004 | Der Client Computer ist mit Stereo Referenten ausgestattet.                        |
| Umschließen von dsspeaker \_  | 0x00000005 | Der Client Computer ist mit vier-Kanal-umschließenden sprechenden ausgestattet.   |
| Dsspeaker \_ 5point1   | 0x00000006 | Der Client Computer ist mit fünf Referenten und einem Subwoofer ausgestattet.          |
| Dsspeaker \_ 7point1   | 0x00000007 | Der Client Computer ist mit sieben Referenten und einem Subwoofer ausgestattet.         |



 

Verwenden Sie [**IWMReaderAdvanced2:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting), um diese Einstellungen festzulegen.

Schließlich müssen Sie den richtigen Medientyp für die Ausgabe festlegen, damit die Kanäle diskret ausgegeben werden, und Sie müssen den richtigen Medientyp für die Ausgabe festlegen, indem Sie die folgenden Schritte ausführen:

1.  Rufen Sie [**iwmreader:: getoutputformatcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) auf, um die Anzahl der unterstützten Formate für die relevante Audioausgabe abzurufen. Ausgabeformat Indizes sind NULL basiert.
2.  Rufen Sie für jedes unterstützte Format [**iwmreader:: getoutputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) auf, um die [**iwmoutputmediaproperties**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) -Schnittstelle für das Eigenschaften Objekt der Ausgabemedien abzurufen.
3.  Rufen Sie [**iwmmedia-Eigenschaften:: getmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) auf, um den Medientyp abzurufen.
4.  Wenn der Typ des abgerufenen Mediums der gewünschte Multichannel-Typ ist, legen Sie ihn durch Aufrufen von [**iwmreader:: SetOutput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops)Eigenschaften fest.

Nachdem Sie die diskrete Ausgabe und die Sprecher Konfiguration festgelegt haben, sollten die vom Reader aufgelisteten Ausgabeformate Multichannel-Formate enthalten, die die [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) -Struktur verwenden. Wenn Sie die Ausgabeformate vor dem Festlegen der Eigenschaften aufzählen, werden nur Formate mit einem oder zwei Kanälen und maximal 16 Bits pro Kanal eingeschlossen. Wie bei anderen Audioformaten sollten Sie nur die Formate verwenden, die vom Reader aufgelistet werden. Konfigurieren Sie keine eigenen.

> [!Note]  
> Sie können Multichannel-Audiodaten nur ausgeben, wenn Ihre Anwendung unter Microsoft Windows XP oder einer neueren Version von Microsoft Windows ausgeführt wird.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> <dt>

[**Ausgabeeinstellungen**](output-settings.md)
</dt> <dt>

[**Arbeiten mit High-Resolution PCM-Audiodatei**](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 