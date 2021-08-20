---
description: 'Weitere Informationen zu: Funktionsweise der Windows Imaging-Komponente'
ms.assetid: c233e25b-bec6-4e67-8fbf-2bf9b70c7522
title: Funktionsweise der Windows Imaging-Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a63fe341bbb16afe78b159caa5c50c13fdb2cb8ee7a92f4c482dd03f8d9b8a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965109"
---
# <a name="how-the-windows-imaging-component-works"></a>Funktionsweise der Windows Imaging-Komponente

Dieses Thema enthält folgende Abschnitte:

-   [Ermittlung und Vermittlung](#discovery-and-arbitration)
-   [Decodierung](#decoding)
-   [Codieren](#encoding)
-   [Die Lebensdauer eines Codecs](#the-lifetime-of-a-codec)
-   [WIC-fähiger Codec](#how-to-wic-enabled-a-codec)
-   [Multithread-Apartmentunterstützung in WIC](#multi-threaded-apartment-support-in-wic)
-   [Zugehörige Themen](#related-topics)

## <a name="discovery-and-arbitration"></a>Ermittlung und Vermittlung

Bevor ein Bild decodiert werden kann, muss ein geeigneter Codec gefunden werden, der dieses Bildformat decodieren kann. Da die unterstützten Bildformate in den meisten Systemen hart codiert sind, ist kein Ermittlungsprozess erforderlich. Da die WIC-Plattform (Windows Imaging Component) erweiterbar ist, muss das Format eines Bilds identifiziert und mit einem geeigneten Codec übereinstimmen können.

Um die Laufzeitermittlung zu unterstützen, muss jedes Bildformat über ein Identifikationsmuster verfügen, das verwendet werden kann, um den geeigneten Decoder für dieses Format zu identifizieren. (Es wird dringend empfohlen, für neue Dateiformate eine GUID für das Identifizierensmuster zu verwenden, da sie garantiert eindeutig ist.) Das identifizierende Muster muss in jede Bilddatei eingebettet werden, die diesem Bildformat entspricht. Jeder Decoder verfügt über einen Registrierungseintrag, der das identifizierende Muster oder die Muster der Bildformate angibt, die decodiert werden können. Wenn eine Anwendung ein Image öffnen muss, fordert sie einen Decoder von WIC an. WIC sucht die verfügbaren Decoder in der Registrierung und überprüft jeden Registrierungseintrag auf ein identifizierendes Muster, das dem in der Imagedatei eingebetteten Muster entspricht. Weitere Informationen zu Decoderregistrierungseinträgen finden Sie unter [Encoderspezifische Registrierungseinträge.](-wic-decoderregentries.md)

Wenn WIC einen einzelnen Decoder findet, der dem Identifizierensmuster im Bild entspricht, erstellt er eine Instanz des Decoders und übergibt die Bilddatei an ihn. Wenn WIC mehrere Übereinstimmungen findet, ruft sie eine Methode namens [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) für jeden übereinstimmenden Decoder auf, um zwischen ihnen zu suchen und die beste Übereinstimmung zu finden. Weitere Informationen finden Sie im Abschnitt [QueryCapabilities](-wic-imp-iwicbitmapdecoder.md) im [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

## <a name="decoding"></a>Decodierung

Nachdem der entsprechende Decoder ausgewählt und instanziiert wurde, spricht die Anwendung direkt mit dem Decoder. Der Decoder hat mehrere Aufgaben, die er über verschiedene Schnittstellen implementiert. Diese Dienste können wie folgt klassifiziert werden:

-   Dienste auf Containerebene
-   Dienste auf Frameebene
-   Metadatenenumerationsdienste
-   Transformationen des nativen Decoders
-   Statusbenachrichtigungen und Abbruchunterstützung
-   Rohdatenverarbeitungsdienste

Dienste auf Containerebene umfassen das Abrufen der Miniaturansicht der obersten Ebene (sofern unterstützt), die Vorschau, Farbkontexte, die Palette (falls zutreffend) und das Containerformat sowie den Zugriff auf die einzelnen Bildrahmen im Container. (Einige Container enthalten nur einen einzelnen Frame, während andere, z. B. Tagged Image File Format (TIFF), mehrere Frames enthalten können.) Dieser Satz von Diensten umfasst auch das Bereitstellen von Informationen über den Decoder selbst und seine Funktionen in Bezug auf eine bestimmte Bilddatei.

Einzelne Frames verfügen über eigene Miniaturansichten und können auch über eigene Farbkontexte, Paletten und andere Eigenschaften verfügen, die auf Frameebene verfügbar gemacht werden. Der wichtigste Vorgang, der auf Frameebene ausgeführt wird, ist jedoch die eigentliche Decodierung der Bildbits für diesen Frame.

WIC stellt Metadatenleser für die gängigsten Metadatenformate (IFD, EXIF, IPTC, XMP, APP0, APP1 und andere Formate) bereit und unterstützt auch die Erweiterbarkeit für Metadatenformate von Drittanbietern. Dadurch wird der Codec für die Analyse von Metadaten freigegeben. Der Codec ist jedoch für das Aufzählen der Metadatenblöcke und das Anfordern eines Metadatenreaders für jeden Block verantwortlich. WIC führt die Ermittlung für Metadatenhandler auf die gleiche Weise wie für Codecs aus, basierend auf einem Muster im Blockheader, das einem Muster im Registrierungseintrag des Metadatenhandlers entspricht. Weitere Informationen finden Sie unter [Encoderspezifische Registrierungseinträge.](-wic-decoderregentries.md)

Decoder sind nicht erforderlich, um Transformationsvorgänge nativ zu unterstützen, aber dies ermöglicht erhebliche Leistungsoptimierungen, die eine bessere Endbenutzererfahrung bieten. Beispielsweise kann eine Anwendung eine Pipeline verschiedener Transformationen (Skalierung, Zuschnitt, Drehung und Pixelformatkonvertierung) erstellen, die für ein Bild ausgeführt werden, bevor das Bild gerendert wird. Weitere Informationen zu Transformationspipelines finden Sie unter [IWICBitmapSource.](-wic-imp-iwicbitmapsource.md) Nach dem Erstellen einer Transformationspipeline fordert die Anwendung die endgültige Transformation in der Pipeline an, um die Bitmap zu erzeugen, die sich aus der Anwendung aller Transformationen auf die Bildquelle ergibt. Wenn der Decoder selbst Transformationsvorgänge ausführen kann, fragt WIC an diesem Punkt, welche der angeforderten Transformationen er ausführen kann. Alle angeforderten Transformationen, die der Decoder nicht ausführen kann, werden von WIC für das decodierte Bild ausgeführt, bevor es an den Aufrufer zurückgegeben wird. Diese optimierte Transformationspipeline bietet eine bessere Leistung als jede Transformation sequenziell im Arbeitsspeicher, insbesondere dann, wenn während des Decodierungsprozesses einige oder alle Transformationen durchgeführt werden können.

Statusbenachrichtigungen und Abbruchunterstützung ermöglichen einer Anwendung, Statusbenachrichtigungen für lange Vorgänge anzufordern, und ermöglichen es der Anwendung, dem Benutzer die Möglichkeit zu geben, einen Vorgang abzubrechen, der zu lange dauert. Dies ist wichtig, denn wenn ein Benutzer einen Vorgang nicht abbrechen kann, kann er das Gefühl haben, dass der Prozess hängen geblieben ist, und versuchen, ihn abzubrechen, indem er die Anwendung schließt.

Diese Schnittstellen werden im Abschnitt [Implementieren eines WIC-Enabled Decoders](-wic-implementingwicdecoder.md)ausführlich beschrieben.

Zu den Rohdatenverarbeitungsdiensten gehören das Anpassen von Kameraeinstellungen wie Belichtung, Kontrast und Schärfe oder das Ändern des Farbraums vor der Verarbeitung der rohen Bits.

## <a name="encoding"></a>Codierung

Wie Decoder haben Encoder die Verantwortung, die sie über Schnittstellen implementieren. Die Von Encodern bereitgestellten Dienste ergänzen die von Decodern bereitgestellten Dienste, mit dem Unterschied, dass sie Bilddaten schreiben, anstatt sie zu lesen. Encoder stellen auch Dienste in den folgenden Kategorien bereit:

-   Dienste auf Containerebene
-   Dienste auf Frameebene
-   Metadatenenumeration und Updatedienste
-   Unterstützung für Statusbenachrichtigungen und Abbruch

Dienste auf Containerebene für einen Encoder umfassen das Festlegen der Miniaturansicht der obersten Ebene (sofern unterstützt), die Vorschau und die Palette (falls zutreffend) sowie das Durchlaufen der einzelnen Bildrahmen, damit sie in den Container serialisiert werden können.

Dienste auf Frameebene für einen Encoder spiegeln die Dienste für den Decoder wider, mit dem Unterschied, dass sie die Bilddaten, Miniaturansichten und alle zugehörigen Paletten oder andere Komponenten ausschreiben, anstatt sie zu lesen.

Metadatenenumerationsdienste für einen Encoder umfassen außerdem das Durchlaufen der zu schreibenden Metadatenblöcke und das Aufrufen der entsprechenden Metadatenwriter zum Serialisieren der Metadaten auf den Datenträger.

Diese Schnittstellen werden im Abschnitt [Implementieren eines WIC-Enabled Encoders](-wic-implementingwicencoder.md)ausführlich beschrieben.

## <a name="the-lifetime-of-a-codec"></a>Die Lebensdauer eines Codecs

Ein WIC-Codec wird instanziiert, um ein einzelnes Bild zu verarbeiten, und hat in der Regel eine kurze Lebensdauer. Sie wird erstellt, wenn ein Image geladen wird, und wird freigegeben, wenn das Image geschlossen wird. Eine Anwendung kann eine große Anzahl von Codecs gleichzeitig mit überlappender Lebensdauer verwenden (denken Sie daran, durch ein Verzeichnis mit Hunderten von Bildern zu scrollen), und mehrere Anwendungen können dies gleichzeitig tun.

Obwohl einige Codecs über eine Lebensdauer verfügen, die auf die Lebensdauer des Prozesses, in dem sie sich befindet, beumfang, ist dies bei WIC-Codecs nicht der Fall. Die Windows Vista Fotogalerie, Windows Explorer und Bildanzeige sowie zahlreiche andere Anwendungen basieren auf WIC und verwenden Ihren Codec, um Bilder und Miniaturansichten anzuzeigen. Wenn die Lebensdauer ihres Codecs auf die Lebensdauer des Prozesses befristet ist, bleibt der Codec jedes Mal, wenn ein Bild oder eine Miniaturansicht im Windows Vista-Explorer angezeigt wird, zum Decodieren des Bilds im Arbeitsspeicher, bis der Benutzer den Computer das nächste Mal neu gestartet hat. Wenn Ihr Codec nie entladen wird, werden seine Ressourcen tatsächlich "kompensiert", da sie von keiner anderen Komponente im System verwendet werden können.

## <a name="how-to-wic-enabled-a-codec"></a>WIC-fähiger Codec

1.  Implementieren Sie eine Decoderklasse auf Containerebene und eine Decoderklasse auf Frameebene, die die erforderlichen WIC-Schnittstellen zum Decodieren von Bildern und Durchlaufen von Metadatenblöcken verfügbar macht. Dadurch können alle WIC-basierten Anwendungen auf die gleiche Weise mit Ihrem Codec interagieren wie mit Standardbildformaten.
2.  Implementieren Sie eine Encoderklasse auf Containerebene und eine Encoderklasse auf Frameebene, die die erforderlichen WIC-Schnittstellen zum Codieren von Bildern und Serialisieren von Metadatenblöcken in eine Bilddatei verfügbar macht.
3.  Wenn Ihr Containerformat nicht auf einem TIFF- oder JPEG-Container basiert, müssen Sie möglicherweise Metadatenhandler für die gängigen Metadatenformate (EXIF, XMP) schreiben. Wenn Sie jedoch ein TIFF- oder JPEG-basiertes Containerformat verwenden, ist dies nicht erforderlich, da Sie an die vom System bereitgestellten Metadatenhandler delegieren können.
4.  Einbetten eines eindeutigen Identifizierungsmusters (wir empfehlen eine GUID) in alle Ihre Bilddateien. Dadurch kann ihr Bildformat während der Ermittlung mit Ihrem Codec abgegleichen werden. Wenn Sie einen WIC-Wrapper für ein vorhandenes Bildformat schreiben, müssen Sie ein Bitmuster finden, das der Encoder immer in seine Bilddateien schreibt, die für dieses Bildformat eindeutig sind, und dieses als identifizierendes Muster verwenden.)
5.  Registrieren Sie Ihren Codec zur Installationszeit. Dadurch kann Ihr Codec zur Laufzeit ermittelt werden, indem das identifizierende Muster in der Registrierung mit dem in der Imagedatei eingebetteten Muster übereinstimmt.
6.  Ab Windows 7 erfordert WIC, dass Codecs vom COM-Apartmenttyp "Beide" sind. Dies bedeutet, dass Sie die entsprechende Sperrung durchführen müssen, um apartmentübergreifende Aufrufer und Aufrufer in Multithreadszenarien zu behandeln. Weitere Informationen finden Sie im nächsten Abschnitt zur Multithread-Apartmentunterstützung.
7.  Unterstützung für 64-Bit-Plattformen: Für Windows 7 erfordert WIC, dass WIC-Codecs von Drittanbietern sowohl als native 32-Bit- als auch als 64-Bit-Binärdateien bereitgestellt werden. Darüber hinaus muss das 32-Bit-Formular auf 64-Bit-Systemen installiert und ausgeführt werden, und das Installationsprogramm des Drittanbieters Windows 7-Codecs muss sowohl die 32-Bit- als auch die 64-Bit-Binärdateien auf 64-Bit-Systemen installieren.

## <a name="multi-threaded-apartment-support-in-wic"></a>Multithread-Apartmentunterstützung in WIC

Objekte in einem Multithread-Apartment (MTA) können von einer beliebigen Anzahl von Threads innerhalb des MTA gleichzeitig aufgerufen werden. Dies ermöglicht eine bessere Leistung auf Systemen mit mehreren Kernen und bestimmten Serverszenarien. Darüber hinaus können WIC-Codecs in einem MTA andere Objekte im MTA aufrufen, ohne dass die Marshallingkosten für das Aufrufen zwischen Threads in verschiedenen STA-Apartments entstehen. In Windows 7 wurden alle integrierten WIC-Codecs aktualisiert, um MTAs zu unterstützen, einschließlich JPEG, TIFF, PNG, GIF, ICO und BMP. Es wird dringend empfohlen, Codecs von Drittanbietern zur Unterstützung von MTAs zu schreiben. Codecs von Drittanbietern, die MTAs nicht unterstützen, verursachen aufgrund des Marshallings erhebliche Leistungskosten in Multithreadanwendungen. Für die Aktivierung der MTA-Unterstützung muss eine ordnungsgemäße Synchronisierung im Drittanbietercodec implementiert werden. Die genaue Implementierung dieser Synchronisierungstechniken würde den Rahmen dieses Whitepapers sprengen. Weitere Informationen zum Synchronisieren von COM-Objekten finden Sie unter [Grundlegendes zu und Verwenden von COM-Threadingmodellen.](/previous-versions/ms809971(v=msdn.10))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Einführung (Schreiben eines WIC-Enabled CODEC)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Implementieren eines WIC-Enabled Decoders](-wic-implementingwicdecoder.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> </dl>

 

 



