---
description: Weitere Informationen zur Funktionsweise der Windows-Abbild Erstellungs Komponente
ms.assetid: c233e25b-bec6-4e67-8fbf-2bf9b70c7522
title: Funktionsweise der Windows-Abbild Erstellungs Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc9fe31ae4346f2c2d1f0b273e78ed10a0ec7e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757836"
---
# <a name="how-the-windows-imaging-component-works"></a>Funktionsweise der Windows-Abbild Erstellungs Komponente

Dieses Thema enthält folgende Abschnitte:

-   [Ermittlung und Schiedsgerichtsbarkeit](#discovery-and-arbitration)
-   [Decodierung](#decoding)
-   [Codieren](#encoding)
-   [Die Lebensdauer eines Codecs.](#the-lifetime-of-a-codec)
-   [Gewusst wie: WIC-aktivierter Codec](#how-to-wic-enabled-a-codec)
-   [Multithread-Apartment Unterstützung in WIC](#multi-threaded-apartment-support-in-wic)
-   [Zugehörige Themen](#related-topics)

## <a name="discovery-and-arbitration"></a>Ermittlung und Schiedsgerichtsbarkeit

Bevor ein Bild decodiert werden kann, muss ein entsprechender Codec gefunden werden, der das Bildformat decodieren kann. In den meisten Systemen ist kein Ermittlungs Vorgang erforderlich, da die unterstützten Bildformate hart codiert sind. Da die WIC-Plattform (Windows Imaging Component) erweiterbar ist, müssen Sie in der Lage sein, das Format eines Bilds zu identifizieren und mit einem passenden Codec abzugleichen.

Zur Unterstützung der Lauf Zeit Ermittlung muss jedes Bildformat ein Identifizierungs Muster aufweisen, mit dem der entsprechende Decoder für dieses Format identifiziert werden kann. (Es wird dringend empfohlen, dass Sie für neue Dateiformate eine GUID für das identifizierende Muster verwenden, da es garantiert eindeutig ist.) Das Identifizierungs Muster muss in jede Bilddatei eingebettet werden, die diesem Bildformat entspricht. Jeder Decoder verfügt über einen Registrierungs Eintrag, der das identifizierende Muster oder Muster der Bildformate angibt, die es decodieren kann. Wenn eine Anwendung ein Image öffnen muss, fordert Sie einen Decoder von WIC an. WIC sucht in der Registrierung nach den verfügbaren Decodern und überprüft jeden Registrierungs Eintrag auf ein identifizierendes Muster, das mit dem in der Bilddatei eingebetteten Muster übereinstimmt. Weitere Informationen zu Decoder-Registrierungs Einträgen finden Sie unter [encoderspezifische Registrierungseinträge](-wic-decoderregentries.md) .

Wenn WIC einen einzelnen Decoder findet, der mit dem identifizierenden Muster im Image übereinstimmt, erstellt er eine Instanz des Decoders und übergibt die Bilddatei an ihn. Wenn WIC mehr als eine Übereinstimmung findet, wird für jeden übereinstimmenden Decoder eine Methode namens [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) aufgerufen, um Sie zu untersuchen und die beste Übereinstimmung zu finden. Weitere Informationen finden Sie im Abschnitt [queryfunktionen](-wic-imp-iwicbitmapdecoder.md) des [implementierenden iwicbitmapdecoders](-wic-imp-iwicbitmapdecoder.md).

## <a name="decoding"></a>Decodierung

Nachdem der entsprechende Decoder ausgewählt und instanziiert wurde, spricht die Anwendung direkt mit dem Decoder. Der Decoder hat mehrere Aufgaben, die er über verschiedene Schnittstellen implementiert. Diese Dienste können wie folgt klassifiziert werden:

-   Dienste auf Container Ebene
-   Dienste auf Frame-Ebene
-   Metadatenenumerationsdienste
-   Native Decoder-Transformationen
-   Fortschritts Benachrichtigungen und Abbruch Unterstützung
-   Rohverarbeitungs Dienste

Dienste auf Container-Ebene umfassen das Abrufen der Miniaturansicht der obersten Ebene (falls unterstützt), der Vorschau, der Farb Kontexte, der Palette (falls zutreffend) und des Container Formats sowie das Bereitstellen des Zugriffs auf die einzelnen Bildframes innerhalb des Containers. (Einige Container enthalten nur einen einzelnen Frame, während andere, z. b. Tagged Image File Format (TIFF), mehrere Frames enthalten können.) Diese Dienste umfassen auch die Bereitstellung von Informationen zum Decoder und dessen Funktionen in Bezug auf eine bestimmte Bilddatei.

Einzelne Frames verfügen über eigene Miniaturansichten und können auch über eigene Farb Kontexte, Paletten und andere Eigenschaften verfügen, die auf Frame-Ebene verfügbar gemacht werden. Der wichtigste Vorgang, der auf der Frame-Ebene ausgeführt wird, ist jedoch die tatsächliche Decodierung der Bildbits für diesen Frame.

WIC stellt metadatenreader für die gängigsten Metadatenformate (IFD, EXIF, IPTC, XMP, APP0, App1 und andere Formate) bereit und unterstützt außerdem die Erweiterbarkeit für Metadatenformate von Drittanbietern. Dadurch wird der Codec der Verantwortung für das Durchsuchen von Metadaten freigegeben. Der Codec ist jedoch für das Auflisten der Metadatenblöcke und das Anfordern eines metadatenreaders für jeden Block verantwortlich. WIC führt die Ermittlung für Metadatenhandler auf die gleiche Weise durch wie bei Codecs, basierend auf einem Muster im Block Header, das mit einem Muster im Registrierungs Eintrag des metadatenhandlers übereinstimmt. Weitere Informationen finden Sie in den [Codierungs spezifischen Registrierungs Einträgen](-wic-decoderregentries.md) .

Decoders sind nicht für die systemeigene Unterstützung von Transformations Vorgängen erforderlich. Dadurch werden jedoch erhebliche Leistungsoptimierungen ermöglicht, die eine bessere Endbenutzer Leistung ermöglichen. Beispielsweise kann eine Anwendung eine Pipeline verschiedener Transformationen (Skalierung, Zuschneiden, Drehung und Pixel Formatkonvertierung) erstellen, die vor dem Rendern des Bilds für ein Bild durchgeführt werden soll. Weitere Informationen zu Transformations Pipelines finden Sie unter [IWICBitmapSource](-wic-imp-iwicbitmapsource.md). Nachdem eine Transformations Pipeline erstellt wurde, fordert die Anwendung die endgültige Transformation in der Pipeline an, um die Bitmap zu erzeugen, die sich aus der Anwendung aller Transformationen auf die Bildquelle ergibt. Wenn der Decoder an dieser Stelle in der Lage ist, Transformations Vorgänge auszuführen, fragt WIC, welche der angeforderten Transformationen er ausführen kann. Alle angeforderten Transformationen, die der Decoder nicht ausführen kann, werden von WIC für das decodierte Bild ausgeführt, bevor es an den Aufrufer zurückgegeben wird. Diese optimierte Transformations Pipeline bietet eine bessere Leistung als die sequenzielle Ausführung jeder Transformation im Speicher, insbesondere dann, wenn einige oder alle Transformationen während des Decodierungs Vorgangs durchgeführt werden können.

Status Benachrichtigungen und Abbruch Unterstützung ermöglichen es einer Anwendung, Status Benachrichtigungen für lange Vorgänge anzufordern. Außerdem kann die Anwendung den Benutzern die Möglichkeit geben, einen Vorgang abzubrechen, der zu lange dauert. Dies ist wichtig, denn wenn ein Benutzer einen Vorgang nicht abbrechen kann, hat er möglicherweise den Meinung, dass der Prozess nicht reagiert hat, und versucht, ihn abzubrechen, indem er die Anwendung schließt.

Diese Schnittstellen werden im Abschnitt über die [Implementierung eines WIC-Enabled Decoders](-wic-implementingwicdecoder.md)ausführlich beschrieben.

Die rohverarbeitungs Dienste umfassen das Anpassen von Kameraeinstellungen wie z. b. das verfügbar machen, den Kontrast und das Schärfen oder das Ändern des Farb Raums vor der Verarbeitung der rohbits.

## <a name="encoding"></a>Codierung

Wie Decoders haben Encoder Verantwortlichkeiten, die Sie über Schnittstellen implementieren. Die von Encodern bereitgestellten Dienste ergänzen die Dienste, die von Decodern bereitgestellt werden, mit dem Unterschied, dass Sie Bilddaten schreiben, anstatt Sie zu lesen. Encoder stellen auch Dienste in den folgenden Kategorien bereit:

-   Dienste auf Container Ebene
-   Dienste auf Frame-Ebene
-   Metadatenenumeration und Aktualisierungs Dienste
-   Fortschritts Benachrichtigung und Abbruch Unterstützung

Dienste auf Container-Ebene für einen Encoder beinhalten das Festlegen der Miniaturansicht der obersten Ebene (falls unterstützt), der Vorschau und der Palette (falls zutreffend) und durchlaufen der einzelnen Bildframes, damit Sie in den Container serialisiert werden können.

Dienste auf Frame-Ebene für einen Encoder spiegeln die Werte für den Decoder wider, mit dem Unterschied, dass Sie die Bilddaten, die Miniaturansicht und eine beliebige zugeordnete Palette oder andere Komponente schreiben, anstatt Sie zu lesen.

Außerdem umfassen metadatenenumerationsdienste für einen Encoder das Durchlaufen der zu schreibenden Metadatenblöcke und das Aufrufen der entsprechenden metadatenwriter, um die Metadaten auf den Datenträger zu serialisieren.

Diese Schnittstellen werden im Abschnitt über die [Implementierung eines WIC-Enabled Encoders](-wic-implementingwicencoder.md)ausführlich beschrieben.

## <a name="the-lifetime-of-a-codec"></a>Die Lebensdauer eines Codecs.

Ein WIC-Codec wird instanziiert, um ein einzelnes Bild zu verarbeiten, und weist normalerweise eine kurze Lebensdauer auf. Sie wird erstellt, wenn ein Bild geladen wird, und wird freigegeben, wenn das Bild geschlossen wird. Eine Anwendung verwendet möglicherweise eine große Anzahl von Codecs gleichzeitig mit überlappenden Lebens dauern (Scrollen Sie durch ein Verzeichnis mit Hunderten von Bildern), und mehrere Anwendungen können dies gleichzeitig durchführen.

Obwohl einige Codecs eine Lebensdauer aufweisen, die auf die Lebensdauer des Prozesses beschränkt ist, in dem Sie leben, ist dies bei WIC-Codecs nicht der Fall. Die Windows Vista-Fotogalerie, Windows-Explorer und die Photo Viewer sowie zahlreiche andere Anwendungen basieren auf WIC und verwenden ihren Codec zum Anzeigen von Bildern und Miniaturansichten. Wenn die Lebensdauer Ihres Codecs auf die Lebensdauer des Prozesses festgelegt wurde, wird jedes Mal, wenn ein Bild oder eine Miniaturansicht in Windows Vista Explorer angezeigt wurde, der Codec, der zum Decodieren dieses Images instanziiert wurde, im Arbeitsspeicher verbleiben, bis der Benutzer das nächste Mal seinen Computer neu gestartet hat. Wenn Ihr Codec nie entladen wird, sind seine Ressourcen tatsächlich "kompromittiert", da Sie nicht von einer anderen Komponente im System verwendet werden können.

## <a name="how-to-wic-enabled-a-codec"></a>Gewusst wie: WIC-aktivierter Codec

1.  Implementieren Sie eine Decoder-Klasse auf Container-Ebene und eine Decoder-Klasse auf Frame-Ebene, die die erforderlichen WIC-Schnittstellen zum Decodieren von Bildern und durchlaufen von metadatenblöcken verfügbar macht. Dies ermöglicht allen WIC-basierten Anwendungen die Interaktion mit Ihrem Codec auf dieselbe Weise, wie Sie mit Standardbild Formaten interagieren.
2.  Implementieren Sie eine Encoder-Klasse auf Container Ebene und eine Encoder-Klasse auf Frame-Ebene, die die erforderlichen WIC-Schnittstellen für die Codierung von Bildern und das Serialisieren von metadatenblöcken in eine Bilddatei verfügbar macht
3.  Wenn Ihr Containerformat nicht auf einem TIFF-oder JPEG-Container basiert, müssen Sie möglicherweise Metadatenhandler für die allgemeinen Metadatenformate (EXIF, XMP) schreiben. Wenn Sie jedoch ein TIFF-oder JPEG-basiertes Containerformat verwenden, ist dies nicht erforderlich, da Sie an die vom System bereitgestellten Metadatenhandler delegieren können.
4.  Betten Sie ein eindeutiges Identifikationsmuster (Wir empfehlen eine GUID) in alle Ihre Bilddateien ein. Dadurch kann Ihr Bildformat während der Ermittlung mit Ihrem Codec abgeglichen werden. Wenn Sie einen WIC-Wrapper für ein vorhandenes Bildformat schreiben, müssen Sie ein Muster von Bits suchen, das der Encoder immer in seine Bilddateien schreibt, die für dieses Bildformat eindeutig sind, und dieses als identifizierendes Muster verwenden.)
5.  Registrieren Sie Ihren Codec beim Installations Zeitpunkt. Dadurch kann der Codec zur Laufzeit ermittelt werden, indem das identifizierende Muster in der Registrierung mit dem in die Bilddatei eingebetteten Muster übereinstimmt.
6.  Ab Windows 7 erfordert WIC, dass Codecs den com-Apartment-Typ "beide" aufweisen. Dies bedeutet, dass Sie die entsprechende Sperre durchführen müssen, um Apartment übergreifende Aufrufer und Aufrufer in Szenarios mit mehreren Threads zu verarbeiten. Weitere Informationen finden Sie im nächsten Abschnitt der Multithread-Apartment Unterstützung.
7.  Unterstützung für 64-Bit-Plattformen: für Windows 7 erfordert WIC, dass WIC-Codecs von Drittanbietern sowohl als native 32-Bit-als auch als 64-Bit-Binärdateien geliefert werden. Außerdem muss das 32-Bit-Formular auf 64-Bit-Systemen installiert und ausgeführt werden, und der Drittanbieter Windows 7 Codec-Installer muss sowohl die 32-Bit-als auch die 64-Bit-Binärdatei auf einem 64-Bit-System installieren.

## <a name="multi-threaded-apartment-support-in-wic"></a>Multithread-Apartment Unterstützung in WIC

Objekte innerhalb eines Multithread-Apartment (MTA) können gleichzeitig durch eine beliebige Anzahl von Threads im MTA aufgerufen werden. Dies ermöglicht eine bessere Leistung für Multikernsysteme und bestimmte Server Szenarien. Darüber hinaus können WIC-Codecs in einem MTA andere Objekte im MTA aufrufen, ohne die Marshallingkosten im Zusammenhang mit dem Aufruf zwischen Threads in verschiedenen STA-Apartments zu haben. In Windows 7 wurden alle in-Box-WIC-Codecs aktualisiert, um MTAs zu unterstützen, einschließlich JPEG, TIFF, PNG, GIF, ICO und BMP. Es wird dringend empfohlen, dass Drittanbieter-Codecs für die Unterstützung von MTAs geschrieben werden. Codecs von Drittanbietern, die MTAs nicht unterstützen, verursachen aufgrund von Marshalling erhebliche Leistungskosten in Multithreadanwendungen. Zum Aktivieren der MTA-Unterstützung muss die ordnungsgemäße Synchronisierung im Codec von Drittanbietern implementiert werden. Die genaue Implementierung dieser Synchronisierungs Verfahren geht über den Rahmen dieses Artikels hinaus. Weitere Informationen zum Synchronisieren von COM-Objekten finden [Sie unter verstehen und Verwenden von COM-Threading Modellen](/previous-versions/ms809971(v=msdn.10)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Einführung (Schreiben eines WIC-Enabled Codecs)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Implementieren eines WIC-Enabled Decoders](-wic-implementingwicdecoder.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> </dl>

 

 



