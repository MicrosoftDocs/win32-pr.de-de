---
title: So erstellen Sie ASF-Dateien mitHilfe von Codecs von Drittanbietern
description: So erstellen Sie ASF-Dateien mitHilfe von Codecs von Drittanbietern
ms.assetid: 5cd348ca-1f86-429d-92ee-4eab4ced8571
keywords:
- Windows Medienformat-SDK, Erstellen von ASF-Dateien
- Windows Medienformat-SDK, Codecs von Drittanbietern
- Advanced Systems Format (ASF), Erstellen von Dateien
- ASF (Advanced Systems Format), Erstellen von Dateien
- Advanced Systems Format (ASF), Codecs von Drittanbietern
- ASF (Advanced Systems Format), Codecs von Drittanbietern
- Drittanbietercodecs
- Codecs, Drittanbieter
- Codecs, Erstellen von ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1eeeb891037581a550d8c15c2f2b4cefa14f81f20d0d55623d382d0e933e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197079"
---
# <a name="to-create-asf-files-using-third-party-codecs"></a>So erstellen Sie ASF-Dateien mitHilfe von Codecs von Drittanbietern

Sie können das Windows Media Format SDK verwenden, um ASF-Dateien zu erstellen, die digitale Medien enthalten, die mit einem beliebigen Codec codiert sind. Wenn Sie einen anderen Codec als den in diesem SDK enthaltenen verwenden, müssen Sie die folgenden Schritte ausführen.

1.  Codieren Sie den Inhalt mit dem gewünschten Codec.
2.  Suchen oder erstellen Sie einen GUID-Wert, um Inhalt zu identifizieren, der mit dem in Schritt 1 verwendeten Codec codiert ist.
3.  Erstellen Sie ein neues Profil, oder ändern Sie ein vorhandenes Profil für die Verwendung mit dem codierten Inhalt.
    -   Erstellen Sie einen Stream für den codierten Inhalt mit dem entsprechenden Haupttyp. Weitere Informationen zu den wichtigsten Medientypen finden Sie unter [Medientypen.](media-types.md) Verwenden Sie die in Schritt 2 identifizierte GUID als Medienuntertyp.
    -   Legen Sie die Bitrate und das Pufferfenster für den Stream auf Werte fest, die nicht zu einem Pufferüberlauf führen. Sie sollten in der Lage sein, diese Werte zum Zeitpunkt der Codierung vom Codec abzurufen. Die SDK-Laufzeitkomponenten überprüfen die Bitraten-/Pufferfensterwerte und löschen ggf. Stichproben, damit die angegebenen Daten in diese Werte passen. Wenn Sie die Werte falsch festlegen, wird die Datei nicht ordnungsgemäß gestreamt, was zu einer schlechten Wiedergabe führt.
    -   Für Videostreams müssen Sie den **biCompression-Member** der **BITMAPINFOHEADER-Struktur** in der [**WMVIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) auf den entsprechenden FOURCC-Wert für den Inhalt festlegen. Dieser Wert muss gleich den ersten vier Bytes der Untertyp-GUID sein. Wenn **biCompression** beispielsweise MAKEFOURCC('T','E','S','T')=0x54455354 ist, beginnt der Untertyp GUID wie folgt: 54455354-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXXXX.
4.  Erstellen Sie ein Writer-Objekt, und laden Sie das im vorherigen Schritt erstellte Profil. Weitere Informationen zum Schreiben von Dateien finden Sie unter [Schreiben von ASF-Dateien.](writing-asf-files.md)
5.  Durchlaufen Sie die Eingaben der Datei in einer Schleife, und weisen Sie ihnen wie gewohnt Eingabeeigenschaften zu. Weitere Informationen zu Eingaben finden Sie unter [Arbeiten mit Eingaben.](working-with-inputs.md) Legen Sie für den mit einem Drittanbietercodec codierten Stream den [**IWMInputMediaProps-Schnittstellenzeiger**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) auf **NULL** fest, bevor [**Sie IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)aufrufen.
6.  Verwenden Sie das im vorherigen Schritt erstellte neue Profil, um die Datei zu schreiben. Übergeben Sie die komprimierten Beispiele mithilfe von [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) anstelle von [**IWMWriter::WriteSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) Für Videos müssen Sie angeben, welche Beispiele Keyframes sind, indem Sie WM \_ SF \_ CLEANPOINT als *dwFlags-Parameter* übergeben.

Um den mit einem Codec eines Drittanbieters codierten Stream zu verarbeiten und zu dekomprimieren, müssen Sie komprimierte Streambeispiele lesen. Ihre Leseanwendung muss auch die Beispieldekomprimierung für den Stream verarbeiten.

## <a name="putting-mpeg-2-streams-into-asf"></a>Integrieren von MPEG-2-Streams in ASF

> [!Note]  
> Dieses Thema gilt für Anwendungen, die das Windows Media Format SDK verwenden, um MPEG-2 (oder andere Komprimierungsformate, die B Frames verwenden) in den ASF-Dateicontainer zu integrieren.

 

Das Writer-Objekt erfordert, dass alle Eingabebeispiele Zeitstempel aufweisen, und es wird davon ausgegangen, dass jedes Eingabebeispiel eine Präsentationszeit nach der vorherigen Zeit hat. Obwohl praktisch alle unkomprimierten Videodatenströme und sogar einige komprimierte Videostreams diese Bedingungen erfüllen, entsprechen MPEG-2-Streams nicht. In MPEG-2 werden nicht alle Stichproben mit einem Zeitstempel versehen, und wenn B-Frames vorhanden sind, ist die Reihenfolge der Stichprobendecodierung nicht mit der Renderingreihenfolge identisch. Wenn das Writer-Objekt auf Fehlordnungsbeispiele trifft, ordnet es sie in der "richtigen" Reihenfolge neu an. Um MPEG-2-Streams nativ (nicht decodiert) in einem ASF-Container zu speichern, müssen Sie daher die folgenden Schritte ausführen:

Beim Schreiben der Datei:

1.  Fügen Sie jedem Eingabebeispiel eine Dateneinheitserweiterung mit fester Größe (DUE) hinzu, die eine Struktur enthält, die die tatsächlichen MPEG-Zeitstempelwerte start-time und stop-time für das Beispiel enthält. Verwenden Sie -1 für diese Werte, wenn das Beispiel über keinen Zeitstempel verfügt.
2.  Geben Sie dem Writerobjekt "Dummy"-Eingabezeitstempel, die sich immer erhöhen, sodass die Beispiele in genau der reihenfolge geschrieben werden, in der sie empfangen werden. Die Dummyzeitstempel sollten ungefähr den tatsächlichen Präsentationszeiten entsprechen, wie im Zeitverlauf gemittelt. Die Dummyzeitstempel bilden die Suchzeitachse. Wenn sie also relativ zu den Echtzeitstempeln abweichen, führen Suchvorgänge für die Datei zu unerwarteten Ergebnissen. Eine begrenzte Jittermenge zwischen den Samplingzeiten wirkt sich jedoch nicht schwerwiegend auf Suchvorgänge aus.

Beim Lesen der Datei:

-   Untersuchen Sie für jedes aus der Datei gelesene Beispiel due. Wenn sie eine Startzeit enthält, die größer oder gleich 0 (null) ist, kopieren Sie diesen Wert in den Zeitstempel für das Ausgabebeispiel, bevor er an den Decoder übermittelt wird. Legen Sie alle anderen Zeitstempel für die Ausgabebeispiele auf **NULL** fest. In DirectShow erfolgt dies durch Aufrufen von **IMediaSample::SetTime**(**NULL**,**NULL**).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Puffern von Inhalten**](buffering-content.md)
</dt> <dt>

[**IWMWriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**IWMWriterErweiterte Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**So übermitteln Sie komprimierte Beispiele mit dem asynchronen Reader**](to-deliver-compressed-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**So rufen Sie Streambeispiele mit dem synchronen Reader ab**](to-retrieve-stream-samples-with-the-synchronous-reader.md)
</dt> <dt>

[**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




