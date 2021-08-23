---
title: So transcodieren Sie Inhalte mit intelligenter Rekomprimierung
description: So transcodieren Sie Inhalte mit intelligenter Rekomprimierung
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Windows Medienformat-SDK, Transcodieren von Inhalt
- Windows Medienformat-SDK, intelligente Rekomprimierung
- Windows Medienformat-SDK, Neukomprimierung
- Windows Medienformat-SDK, Windows Medienaudiocodecs
- Advanced Systems Format (ASF), Transcodinginhalt
- ASF (Advanced Systems Format), Transcoding von Inhalt
- Advanced Systems Format (ASF), intelligente Rekomprimierung
- ASF (Advanced Systems Format), intelligente Rekomprimierung
- Advanced Systems Format (ASF), Recompression
- ASF (Advanced Systems Format), Recompression
- Advanced Systems Format (ASF), Windows Medienaudiocodecs
- ASF (Advanced Systems Format), Windows Medienaudiocodecs
- Transcodieren von Inhalt
- Intelligente Rekomprimierung
- Rekomprimierung
- Windows Codecs für Medienaudio, Transcodieren von Inhalten
- Codecs,Windows Medienaudiocodecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1cf363e196feca81ef9757f006b211758c2ff7fbdd1f50b5136992b394f8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699091"
---
# <a name="to-transcode-content-with-smart-recompression"></a>So transcodieren Sie Inhalte mit intelligenter Rekomprimierung

Sie können Inhalte mithilfe des Windows Media Format SDK von einer Bitrate in eine andere transcodieren. Normalerweise umfasst dies einfach das Decodieren des Inhalts und die Codierung wieder in die gewünschte Bitrate. Der Windows Media Audio 9-Codec unterstützt die intelligente Rekomprimierung, die eine Transcodierung ermöglicht, die eine bessere Qualität als normal erreicht.

Für die intelligente Rekomprimierung muss der ursprüngliche Audiodatenstrom mit dem Windows Medienaudiocodec codiert werden. Alle Versionen des Codecs werden unterstützt, die spezialisierten Audiocodecs (Windows Media Audio 9 Professional und Windows Media Audio 9 Voice) jedoch nicht. Wenn die ursprüngliche Audiodatei mit dem Windows Media Audio 9 Lossless-Codec codiert wurde, ist keine intelligente Rekomprimierung notwendig, da in der ursprünglichen Codierung keine Informationen verloren gegangen sind.

Führen Sie die folgenden Schritte aus, um die intelligente Rekomprimierung zu verwenden.

1.  Richten Sie ein Readerobjekt mit der Quelldatei zum Lesen ein. Weitere Informationen finden Sie unter [Lesen von ASF-Dateien.](reading-asf-files.md)
2.  Richten Sie ein Writerobjekt ein, das zum Transcodieren der Datei verwendet werden soll. Legen Sie den Dateinamen für die neue Datei fest. Wählen Sie ein Profil aus, das für die neue Datei verwendet werden soll. Legen Sie das ausgewählte Profil im Writerobjekt fest. Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien.](writing-asf-files.md)
3.  Rufen Sie einen Zeiger auf die [**IWMProfile-Schnittstelle**](iwmprofile.md) des Readerobjekts ab, indem **Sie IWMReader::QueryInterface aufrufen.**
4.  Rufen Sie [**die IWMStreamConfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) für den zu transcodierten Audiodatenstrom ab, indem Sie [**IWMProfile::GetStream aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)
5.  Rufen Sie [**die IWMMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) für das Streamkonfigurationsobjekt ab, indem **Sie IWMStreamConfig::QueryInterface aufrufen.**
6.  Rufen Sie die [**WM \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) für den Stream ab, indem Sie zwei Aufrufe von [**IWMMediaProps::GetMediaType tätigen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) Rufen Sie die Größe der -Struktur beim ersten Aufruf ab, und ordnen Sie Arbeitsspeicher zu, damit ein Puffer beim zweiten Aufruf übergeben wird.
7.  Rufen Sie einen Zeiger auf die [**IWMInputMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) für die Eingabe im Writer ab, indem [**Sie IWMWriter::GetInputProps aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)
8.  Rufen Sie [**die IWMPropertyVault-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) für das Eingabemedieneigenschaftenobjekt ab, indem **Sie IWMInputMediaProps::QueryInterface aufrufen.**
9.  Verwenden Sie [**die IWMPropertyVault::SetProperty-Methode,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) um die g \_ wszOriginalWaveFormat-Eigenschaft festlegen. Verwenden Sie die IN Schritt 6 erhaltene **WAVEFORMATEX-Struktur** als Wert der -Eigenschaft.
10. Schließen Sie Änderungen an den Eingabemedieneigenschaften ein, indem [**Sie IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) aufrufen und einen Zeiger auf **die IWMInputMediaProps-Schnittstelle** übergeben.
11. Beginnen Sie mit dem Lesen von Beispielen aus der originalen Datei, und übergeben Sie sie mit Aufrufen von [**IWMWriter::WriteSample an den Writer.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Weiterführende Themen**](advanced-topics.md)
</dt> <dt>

[**IWMInputMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[**IWMMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**IWMProfile-Schnittstelle**](iwmprofile.md)
</dt> <dt>

[**IWMPropertyVault-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[**IWMStreamConfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




