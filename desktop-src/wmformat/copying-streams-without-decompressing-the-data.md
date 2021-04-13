---
title: Kopieren von Streams, ohne die Daten zu entkomprimieren
description: Kopieren von Streams, ohne die Daten zu entkomprimieren
ms.assetid: c268ce44-a09d-4304-bc39-8b6657da2bdb
keywords:
- Windows Media-Format-SDK, Kopieren von Streams
- Advanced Systems Format (ASF), Kopieren von Streams
- ASF (Advanced Systems Format), Kopieren von Streams
- Streams, Kopieren ohne das Komprimieren von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 831b85ad431a6c4d3f4255c281d22ca17004674f
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104390041"
---
# <a name="copying-streams-without-decompressing-the-data"></a>Kopieren von Streams, ohne die Daten zu entkomprimieren

Der einfachste und gängigste Weg, einen Stream aus einer Datei in einen anderen zu kopieren, besteht darin, die Stichproben im komprimierten Zustand abzurufen und Sie dann in die neue Datei zu schreiben, ohne Sie zu dekomprimieren und erneut zu komprimieren. Beispiele aus einer Datei im komprimierten Zustand werden als streambeispiele bezeichnet, da Sie aus ihrer Darstellung im Stream nicht geändert werden. Es wird empfohlen, streambeispiele immer zum Kopieren von Datenströmen zu verwenden, da die Qualität durch Dekomprimieren und erneutes komprimieren digitaler Mediendaten beeinträchtigt wird. Wenn Sie einen Stream aus dekomprimierten Daten kopieren müssen, finden Sie weitere Informationen unter Kopieren von Daten [strömen mit dekomprimierten Beispielen](copying-streams-using-decompressed-samples.md).

Es ist möglich, zwei oder mehr Streams mit komprimierten Beispielen zu einem einzigen Stream zu verketten, aber nur, wenn die Bitraten identisch sind. Der Prozess ist im Wesentlichen mit den unten beschriebenen Schritten identisch, mit dem Unterschied, dass Sie mehrere Originaldateien lesen müssen, um den gesamten benötigten Inhalt zu erhalten. Sie können jedoch nur komprimierte Beispiele aus mehreren Dateien in einen einzigen Stream schreiben, wenn die **WM- \_ \_ Medientyp** Strukturen (einschließlich aller **pbformat** -Strukturmember) aller komprimierten Streams identisch sind. Zum Kombinieren von Daten aus mehreren Datenströmen, die nicht das gleiche Format aufweisen, müssen Sie den Inhalt dekomprimieren und erneut in den Zielstream komprimieren. Außerdem müssen Sie beim Kombinieren von Daten aus mindestens zwei Datenströmen in einem einzigen Stream die Puffer Fenster Werte für alle Streams zusammenfügen, um das Puffer Fenster für den neuen Stream zu erhalten. Dies liegt daran, dass es nicht möglich ist, zu bestimmen, wie viel Puffer am Ende eines Streams und am Anfang eines anderen Datenstroms benötigt wird.

Sie können streambeispiele mit dem asynchronen Reader mithilfe von [**iwmreaderadvanced:: setreceivestreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples)abrufen. Streambeispiele werden an [**iwmreadercallbackadvanced:: onstreamsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample)und nicht an [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample)übermittelt. Wenn Sie eine Datei lesen und einige komprimierte Datenströme und dekomprimierte Datenströme abrufen, müssen Sie beide Rückruf Methoden implementieren.

Der synchrone Reader bietet mehr Flexibilität beim Abrufen von Beispielen. Sie können bei der Wiedergabe mithilfe von [**iwmsynkreader:: abtreadstreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples)kostenlos zwischen komprimierten und nicht komprimierten Beispielen wechseln.

Führen Sie die folgenden Schritte aus, um einen vollständigen Stream aus einer ASF-Datei in eine neue ASF-Datei zu kopieren. In diesen Schritten wird der synchrone Reader verwendet, da dieser Vorgang für diese Art von Vorgang wesentlich einfacher ist.

1.  Erstellen Sie ein synchrones Reader-Objekt, indem Sie die [**wmcreatesyncreader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) -Funktion aufrufen.
2.  Öffnen Sie eine Datei im Reader mit einem Befehl zum Aufrufen von [**iwmsynkreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).
3.  Abrufen eines Zeigers auf die [**iwmprofile**](iwmprofile.md) -Schnittstelle des synchronen Reader-Objekts durch Aufrufen von **iwmsyncreader:: QueryInterface**.
4.  Rufen Sie die Eigenschaften des gewünschten Streams durch Aufrufen von [**iwmprofile:: getstreambynumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)ab. Dadurch wird ein Zeiger auf die [**iwmstreamconfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) -Schnittstelle des Datenstrom-Konfigurations Objekts für den gewünschten Stream abgerufen.
5.  Eine Kopie der WM- [**\_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur für den Stream erhalten. Erstellen Sie zwei Aufrufe an [**iwmmedia-Eigenschaften:: getmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype): das erste-Element, um die Größe der Struktur zu erhalten, die zweite, um die Struktur selbst zu erhalten.
6.  Erstellen Sie ein Profil-Manager-Objekt, indem Sie die [**wmcreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion aufrufen.
7.  Rufen Sie [**iwmprofilemanager:: kreateemptyprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) auf, um ein neues Profil zu erstellen (oder öffnen Sie ein vorhandenes Profil, dem Sie den Stream hinzufügen möchten). Nennen Sie [**iwmprofile:: addstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) für das neue Profil, um den Stream aus der vorhandenen Datei hinzuzufügen. Verwenden Sie beim Hinzufügen des Streams den in Schritt 4 erhaltenen **iwmstreamconfig** -Zeiger.
8.  Erstellen Sie ein Writer-Objekt, indem Sie die [**wmkreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) -Funktion aufrufen. Legen Sie das neu erstellte Profil als aktives Profil im Writer fest, indem Sie [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile)aufrufen. Erstellen Sie eine Datei für die Ausgabe, indem Sie [**iwmwriter:: setoutputfilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename)aufrufen.
9.  **Geben Sie für jede** Eingabe, die dem Stream bzw [**. den Daten**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) strömen zugeordnet ist, den Sie kopieren, den Befehl [**iwmwriter::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops)"". Dadurch wird dem Writer-Objekt mitgeteilt, dass es nicht erforderlich ist, die Daten zu überprüfen, die Sie weiterleiten. Sie müssen diesen Aufruf vor dem Aufrufen von **beginwriting** ausführen (Schritt 14), andernfalls ist ein Lese Objekt möglicherweise nicht in der Lage, den Inhalt zu decodieren.
10. Legen Sie den synchronen Reader für die Bereitstellung von komprimierten streambeispielen für den ausgewählten Stream fest, indem Sie [**iwmsyncreader:: setreadstreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) aufrufen, wobei der *fcompressed* -Parameter auf true festgelegt
11. Abrufen von Codec-Informationen für jeden Stream, der kopiert wird, und Hinzufügen der Codec-Informationen zum Header vor dem Schreiben. Rufen Sie zum Abrufen der Codec-Informationen [**IWMHeaderInfo2:: getcodecinfocount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) und [**IWMHeaderInfo2:: getcodecinfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) auf, um die Codecs aufzulisten, die der Datei im Reader zugeordnet sind. Wählen Sie die Codec-Informationen aus, die der Datenstrom Konfiguration entsprechen. Legen Sie dann die Codec-Informationen im Writer durch Aufrufen von [**IWMHeaderInfo3:: addcodecinfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo)fest, und übergeben Sie dabei die Informationen, die vom Reader abgerufen werden.
12. Abrufen eines Zeigers auf die [**iwmschreibadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced) -Schnittstelle durch Aufrufen von **iwmwriter:: QueryInterface**.
13. Legen Sie den Writer auf den Schreibmodus fest, indem Sie [**iwmwriter:: BeginWrite**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)aufrufen.
14. Führen Sie wiederholte Aufrufe von [**iwmsynkreader:: getnextsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample)aus, und geben Sie dabei die gewünschte streamnummer an. Wenn Beispiele empfangen werden, übergeben Sie Sie an den Writer mit Aufrufen von [**iwmschreiteradvanced:: Beschreib testreamsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample). Bei Videostreams sollten Sie die Flags (sofern vorhanden) überprüfen, die der Writer bei jedem Aufrufen von **getnextsample** festgelegt hat. Wenn der WM- \_ SF- \_ Cleanpoint festgelegt ist, müssen Sie ihn auch für den Aufrufen von " **Write-streamsample**" festlegen.
15. Wenn der Lesevorgang beendet ist, nennen Sie [**iwmwriter:: EndWrite**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting). Der Stream sollte übertragen werden.

> [!Note]  
> Bildstreams können mithilfe von streambeispielen nicht aus einer Datei in eine andere kopiert werden. Wenn Sie bildstreamdaten kopieren möchten, rufen Sie die Beispiele unkomprimiert ab, und verarbeiten Sie Sie wie gewohnt über den Writer.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Kopieren von Daten aus einer Datei in eine andere**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Kopieren von Streams mithilfe von nicht komprimierten Beispielen**](copying-streams-using-decompressed-samples.md)
</dt> </dl>

 

 




