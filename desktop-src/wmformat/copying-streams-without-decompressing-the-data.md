---
title: Kopieren von Streams ohne Dekomprimieren der Daten
description: Kopieren von Streams ohne Dekomprimieren der Daten
ms.assetid: c268ce44-a09d-4304-bc39-8b6657da2bdb
keywords:
- Windows Medienformat-SDK, Kopieren von Datenströmen
- Advanced Systems Format (ASF), Kopieren von Datenströmen
- ASF (Advanced Systems Format), Kopieren von Datenströmen
- Streams,Kopieren ohne Dekomprimieren von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2387861c25ad565298fb2731300f6da8ccc00c26c5f7c82c36fede1bb7f62f9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931560"
---
# <a name="copying-streams-without-decompressing-the-data"></a>Kopieren von Streams ohne Dekomprimieren der Daten

Die einfachste und gängigste Methode zum Kopieren eines Streams aus einer Datei in eine andere besteht im Abrufen der Beispiele im komprimierten Zustand und anschließenden Schreiben in die neue Datei, ohne sie zu dekomprimieren und erneut zu dekomprimieren. Beispiele, die aus einer Datei in ihrem komprimierten Zustand erhalten werden, werden als Streambeispiele bezeichnet, da sie von ihrer Darstellung im Stream nicht geändert werden. Es wird empfohlen, Datenströme immer mithilfe von Streambeispielen zu kopieren, da das Dekomprimieren und Erneute Dekomprimieren digitaler Mediendaten die Qualität beeinträchtigt. Wenn Sie einen Stream aus dekomprimierten Daten kopieren müssen, finden Sie weitere Informationen unter Kopieren Streams [mit dekomprimierten Beispielen.](copying-streams-using-decompressed-samples.md)

Es ist möglich, zwei oder mehr Datenströme mithilfe komprimierter Stichproben in einem einzelnen Stream zu verketten, jedoch nur, wenn die Bitraten identisch sind. Der Prozess ist im Wesentlichen mit den unten beschriebenen Schritten identisch, mit der Ausnahme, dass Sie mehrere Originaldateien lesen müssen, um alle benötigten Inhalte zu erhalten. Sie können jedoch nur komprimierte Stichproben aus mehreren Dateien in einen einzelnen Stream schreiben, wenn die **WM \_ MEDIA \_ TYPE-Strukturen** (einschließlich aller **pbFormat-Strukturmitglieder)** aller komprimierten Datenströme identisch sind. Um Daten aus mehreren Streams zu kombinieren, die nicht das gleiche Format haben, müssen Sie den Inhalt dekomprimieren und in den Zielstream erneut dekomprimieren. Darüber hinaus müssen Sie beim Kombinieren von Daten aus zwei oder mehr Streams in einem einzelnen Stream die Pufferfensterwerte für alle Streams hinzufügen, um das Pufferfenster für den neuen Stream zu erhalten. Dies liegt daran, dass es unmöglich ist zu bestimmen, wie viel des Puffers am Ende eines Streams und am Anfang eines anderen Datenstroms aufgenommen wird.

Sie können Streambeispiele mit dem asynchronen Reader [**mithilfe von IWMReaderAdvanced::SetReceiveStreamSamples abrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) Streambeispiele werden [**an IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample)und nicht an [**IWMReaderCallback::OnSample übermittelt.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) Wenn Sie eine Datei lesen und einige komprimierte und dekomprimierte Streams abrufen, müssen Sie beide Rückrufmethoden implementieren.

Der synchrone Reader bietet mehr Flexibilität beim Abrufen von Beispielen. Sie können mitHILFE von [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples)frei zwischen komprimierten und dekomprimierten Beispielen während der Wiedergabe wechseln.

Führen Sie die folgenden Schritte aus, um einen gesamten Stream aus einer ASF-Datei in eine neue ASF-Datei zu kopieren. Diese Schritte verwenden den synchronen Reader, da es viel einfacher ist, für diese Art von Vorgang zu verwenden.

1.  Erstellen Sie ein synchrones Readerobjekt, indem Sie die [**WMCreateSyncReader-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) aufrufen.
2.  Öffnen Sie eine Datei im Reader mit einem Aufruf von [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).
3.  Rufen Sie einen Zeiger auf die [**IWMProfile-Schnittstelle**](iwmprofile.md) des synchronen Readerobjekts ab, indem **Sie IWMSyncReader::QueryInterface aufrufen.**
4.  Rufen Sie die Eigenschaften des gewünschten Streams ab, indem Sie [**IWMProfile::GetStreamByNumber aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) Dadurch wird ein Zeiger auf die [**IWMStreamConfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) des Streamkonfigurationsobjekts für den Stream abgerufen, den Sie wünschen.
5.  Hier erhalten Sie eine Kopie der [**WM \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) für den Stream. Führen Sie zwei Aufrufe von [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)aus: der erste aufruft die Größe der Struktur, den zweiten, um die Struktur selbst zu erhalten.
6.  Erstellen Sie ein Profil-Manager-Objekt, indem Sie die [**WMCreateProfileManager-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) aufrufen.
7.  Rufen [**Sie IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) auf, um ein neues Profil zu erstellen (oder öffnen Sie ein vorhandenes Profil, dem Sie den Stream hinzufügen möchten). Rufen [**Sie IWMProfile::AddStream für**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) das neue Profil auf, um den Stream aus der vorhandenen Datei hinzuzufügen. Verwenden Sie beim Hinzufügen des Streams den IN Schritt 4 erhaltenen **IWMStreamConfig-Zeiger.**
8.  Erstellen Sie ein Writerobjekt mit einem Aufruf der [**WMCreateWriter-Funktion.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) Legen Sie das neu erstellte Profil als aktives Profil im Writer fest, indem [**Sie IWMWriter::SetProfile aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) Erstellen Sie eine Datei für die Ausgabe, indem [**Sie IWMWriter::SetOutputFilename aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename)
9.  Rufen Sie für jede Eingabe, die dem Stream oder den Streams zugeordnet ist, die Sie kopieren, [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops)auf, und übergeben Sie **NULL** für die [**IWMInputMediaProps-Schnittstelle.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) Dadurch wird das Writer-Objekt darüber informiert, dass es die übergebenen Daten nicht überprüfen muss. Sie müssen diesen Aufruf vor dem Aufrufen von **BeginWriting** (Schritt 14) erstellen. Andernfalls kann ein Leseobjekt den Inhalt möglicherweise nicht decodieren.
10. Legen Sie den synchronen Reader fest, um komprimierte Streambeispiele für den ausgewählten Stream zu liefern, indem [**Sie IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) aufrufen, während *der Parameter fCompressed* auf True festgelegt ist.
11. Abrufen von Codecinformationen für jeden kopierten Stream und Hinzufügen der Codecinformationen zum Header vor dem Schreiben. Um die Codecinformationen zu erhalten, rufen Sie [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) und [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) auf, um die Codecs zu aufzählen, die der Datei im Reader zugeordnet sind. Wählen Sie die Codecinformationen aus, die der Streamkonfiguration entspricht. Legen Sie dann die Codecinformationen im Writer fest, indem [**Sie IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo)aufrufen und die vom Reader erhaltenen Informationen übergeben.
12. Rufen Sie einen Zeiger auf die [**IWMWriterAdvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced) ab, indem **Sie IWMWriter::QueryInterface aufrufen.**
13. Legen Sie den Writer auf den Schreibmodus fest, indem [**Sie IWMWriter::BeginWriting aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)
14. Führen Sie wiederholte [**Aufrufe an IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample)aus, und geben Sie dabei die gewünschte Streamnummer an. Wenn Beispiele empfangen werden, übergeben Sie sie mit Aufrufen von [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample)an den Writer. Für Videostreams sollten Sie die Flags (sofern diese vom Writer bei jedem Aufruf von **GetNextSample festgelegt** werden) überprüfen. Wenn WM SF CLEANPOINT festgelegt ist, müssen Sie es auch bei Ihrem Aufruf von \_ \_ **WriteStreamSample festlegen.**
15. Wenn das Lesen abgeschlossen ist, rufen Sie [**IWMWriter::EndWriting auf.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) Der Stream sollte übertragen werden.

> [!Note]  
> Bildstreams können nicht mithilfe von Streambeispielen aus einer Datei in eine andere kopiert werden. Um Bilddatenstromdaten zu kopieren, rufen Sie die Beispiele unkomprimiert ab und verarbeiten sie dann wie gewohnt über den Writer.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Kopieren von Daten aus einer Datei in eine andere**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Kopieren von Streams mit dekomprimierten Beispielen**](copying-streams-using-decompressed-samples.md)
</dt> </dl>

 

 




