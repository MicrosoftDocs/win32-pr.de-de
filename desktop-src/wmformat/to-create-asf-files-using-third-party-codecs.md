---
title: So erstellen Sie ASF-Dateien mithilfe von Codecs von Drittanbietern
description: So erstellen Sie ASF-Dateien mithilfe von Codecs von Drittanbietern
ms.assetid: 5cd348ca-1f86-429d-92ee-4eab4ced8571
keywords:
- Windows Media-Format-SDK, Erstellen von ASF-Dateien
- Windows Media-Format-SDK, Codecs von Drittanbietern
- Advanced Systems Format (ASF), Erstellen von Dateien
- ASF (Advanced Systems Format), Erstellen von Dateien
- Advanced Systems Format (ASF), Drittanbieter Codecs
- ASF (Advanced Systems Format), Codecs von Drittanbietern
- Drittanbieter Codecs
- Codecs, Drittanbieter
- Codecs, Erstellen von ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6c057f1785ed50e328ac6094ff7dbe078e98fc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314506"
---
# <a name="to-create-asf-files-using-third-party-codecs"></a>So erstellen Sie ASF-Dateien mithilfe von Codecs von Drittanbietern

Sie können das Windows Media Format SDK zum Erstellen von ASF-Dateien verwenden, die digitale Medien enthalten, die mit einem beliebigen von Ihnen gewählten Codec codiert sind. Wenn Sie einen anderen Codec als einen in diesem SDK enthaltenen Codec verwenden, müssen Sie die folgenden Schritte ausführen.

1.  Codieren Sie den Inhalt mit dem gewünschten Codec.
2.  Suchen oder erstellen Sie einen GUID-Wert, um Inhalte zu identifizieren, die mit dem in Schritt 1 verwendeten Codec codiert sind.
3.  Erstellen Sie ein neues Profil, oder ändern Sie ein vorhandenes Profil für die Verwendung mit dem codierten Inhalt.
    -   Erstellen Sie einen Stream für den codierten Inhalt mit dem entsprechenden Haupttyp. Weitere Informationen zu wichtigen Medientypen finden Sie unter [Medientypen](media-types.md). Verwenden Sie die in Schritt 2 identifizierte GUID als Medien Untertyp.
    -   Legen Sie für den Datenstrom die Bitrate und das Puffer Fenster Werte fest, die nicht zu einem Pufferüberlauf führen. Sie sollten diese Werte zum Zeitpunkt der Codierung vom Codec abrufen können. Die SDK-Laufzeitkomponenten überprüfen die Werte für das Bitrate/Puffer Fenster und löschen ggf. Beispiele, um die angegebenen Daten in diese Werte einzufügen. Wenn Sie die Werte falsch festlegen, wird die Datei nicht ordnungsgemäß gestreamt, was zu einer schlechten Wiedergabe führt.
    -   Für Videostreams müssen Sie das **bicompression** -Member der **BITMAPINFOHEADER** -Struktur, die in der [**wmvideoinfoheader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) -Struktur enthalten ist, auf den entsprechenden FourCC-Wert für den Inhalt festlegen. Dieser Wert muss gleich den ersten vier Bytes der Untertyp-GUID sein. Wenn die **bicompression** z. b. makefourcc ('t ', ' E ', 's ') = 0x54455354 ist, beginnt die GUID des unter Typs wie folgt: 54455354-xxxx-xxxx-xxxx-xxxxxxxxxxxx.
4.  Erstellen Sie ein Writer-Objekt, und laden Sie das im vorherigen Schritt erstellte Profil. Weitere Informationen zum Schreiben von Dateien finden Sie unter [Schreiben von ASF-Dateien](writing-asf-files.md).
5.  Durchlaufen Sie die Eingaben der Datei, und weisen Sie Ihnen wie gewohnt Eingabe Eigenschaften zu. Weitere Informationen zu Eingaben finden Sie unter [Arbeiten mit Eingaben](working-with-inputs.md). Legen Sie für den mit einem Drittanbieter-Codec codierten Stream den [**iwminputmedia-**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) Schnittstellen Zeiger auf **null** fest, bevor Sie [**iwmwriter:: BeginWrite**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)aufrufen.
6.  Verwenden Sie das neue Profil, das Sie im vorherigen Schritt erstellt haben, um die Datei zu schreiben. Übergeben Sie die komprimierten Beispiele, indem Sie [**iwmschreiteradvanced:: Write-streamsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) anstelle von [**iwmwriter:: Write tesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)verwenden. Für Videos müssen Sie angeben, welche Stichproben Keyframes sind, indem Sie WM \_ SF- \_ Cleanpoint als *dwFlags* -Parameter übergeben.

Um den mit einem Drittanbieter-Codec codierten Stream zu verarbeiten und zu dekomprimieren, müssen Sie komprimierte streambeispiele lesen. Die Leseanwendung muss auch die Beispiel Dekomprimierung für den Stream verarbeiten.

## <a name="putting-mpeg-2-streams-into-asf"></a>Einfügen von MPEG-2-Streams in ASF

> [!Note]  
> Dieses Thema gilt für Anwendungen, die das Windows Media-Format-SDK verwenden, um MPEG-2 (oder andere Komprimierungs Formate, die B-Frames verwenden) in den ASF-Datei Container einzufügen.

 

Das Writer-Objekt erfordert, dass alle Eingabe Beispiele Zeitstempel enthalten, und es wird davon ausgegangen, dass jedes Eingabe Beispiel eine Präsentationszeit aufweist, die später als das vorangegangene vorhanden ist. Obwohl praktisch alle nicht komprimierten Videos und sogar einige komprimierte Videostreams diese Bedingungen erfüllen, ist dies in MPEG-2-Streams nicht der Fall. In MPEG-2 sind nicht alle Beispiele mit Zeitstempel versehen, und wenn B-Frames vorhanden sind, ist die Decodierung der Decodierung nicht mit der Rendering-Reihenfolge identisch. Wenn das Writer-Objekt nicht ordnungsgemäß formatierte Stichproben findet, ordnet es diese in der Reihenfolge "richtig" an. Daher müssen Sie zum Speichern von MPEG-2-Streams (nicht decodiert) in einem ASF-Container die folgenden Schritte ausführen:

Beim Schreiben der Datei:

1.  Fügen Sie jedem Eingabe Beispiel, das eine Struktur mit den tatsächlichen Start-und Endzeit Werten für den MPEG-Zeitstempel für das Beispiel enthält, eine Dateneinheiten Erweiterung mit fester Größe (Due) hinzu. Verwenden Sie-1 für diese Werte, wenn das Beispiel keinen Zeitstempel aufweist.
2.  Geben Sie dem Writer-Objekt "Dummy"-Eingabe Zeitstempel, die immer zunehmen, sodass die Beispiele in genau derselben Reihenfolge in die Datei geschrieben werden, in der Sie empfangen werden. Die Dummy-Zeitstempel sollten ungefähr der tatsächlichen Präsentationszeit entsprechen, wie im Laufe der Zeit. Die Dummy-Zeitstempel bilden die gesuchte Zeitachse. Wenn Sie also relativ zu den echt Zeitstempeln abweichen, führen Suchvorgänge in der Datei zu unerwarteten Ergebnissen. Eine begrenzte Menge an Jitter zwischen den Stichproben Zeiten wirkt sich jedoch nicht ernsthaft auf Suchvorgänge aus.

Beim Lesen der Datei:

-   Überprüfen Sie für jedes aus der Datei gelesene Beispiel den fälligen. Wenn Sie eine Startzeit enthält, die größer oder gleich 0 (null) ist, kopieren Sie diesen Wert in den Zeitstempel für das Ausgabe Beispiel, bevor dieser an den Decoder übermittelt wird. Legen Sie alle anderen Zeitstempel der Ausgabe Beispiele auf **null** fest. In DirectShow erfolgt dies durch Aufrufen von **imediasample:: setTime**(**null**,**null**).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Pufferung von Inhalten**](buffering-content.md)
</dt> <dt>

[**Iwmwriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Iwmschreiteradvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**So liefern Sie komprimierte Beispiele mit dem asynchronen Reader**](to-deliver-compressed-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**So rufen Sie streambeispiele mit dem synchronen Reader ab**](to-retrieve-stream-samples-with-the-synchronous-reader.md)
</dt> <dt>

[**Wmvideoinfoheader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




