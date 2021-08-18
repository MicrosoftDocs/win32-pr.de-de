---
description: In diesem Thema wird beschrieben, wie ein Client eine Media Foundation Transform (MFT) zum Verarbeiten von Daten verwendet. Der Client ist alles, was Methoden direkt auf dem MFT aufruft. Dies kann die Anwendung oder die Media Foundation sein.
ms.assetid: be977d75-999e-4e57-9672-00a89246a2c1
title: Grundlegendes MFT-Verarbeitungsmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a1edb0c5144c6e3a3e1825e637cd5d19049699ad60bbf764629c9ade7cd3aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035452"
---
# <a name="basic-mft-processing-model"></a>Grundlegendes MFT-Verarbeitungsmodell

In diesem Thema wird beschrieben, wie ein Client eine Media Foundation Transform (MFT) zum Verarbeiten von Daten verwendet. Der *Client* ist alles, was Methoden direkt auf dem MFT aufruft. Dies kann die Anwendung oder die Media Foundation sein.

Lesen Sie dieses Thema, wenn Sie:

-   Schreiben einer Anwendung, die direkte Aufrufe an eine oder mehrere MFTs macht.
-   Schreiben eines benutzerdefinierten MFT und Verstehen des erwarteten Verhaltens eines MFT.

In diesem Thema wird ein *synchrones Verarbeitungsmodell* beschrieben. In diesem Modell werden alle Datenverarbeitungsmethoden blockiert, bis sie abgeschlossen sind. MFTs können auch ein *asynchrones Modell* unterstützen, das im Thema Asynchrone [MFTs beschrieben wird.](asynchronous-mfts.md)

-   [Grundlegendes Verarbeitungsmodell](#basic-processing-model)
    -   [Erstellen des MFT](#create-the-mft)
    -   [Get Stream Identifiers](#get-stream-identifiers)
    -   [Festlegen von Medientypen](#set-media-types)
    -   [Get Buffer Requirements](#get-buffer-requirements)
    -   [Verarbeiten von Daten](#process-data)
-   [Erweiterungen des Basismodells](#extensions-to-the-basic-model)
-   [2DBuffer](#imf2dbuffer)
-   [Leeren eines MFT](#flushing-an-mft)
-   [Leeren eines MFT](#draining-an-mft)
-   [Beispielattribute](#sample-attributes)
-   [Unterbrechungen](#discontinuities)
-   [Dynamische Formatänderungen](#dynamic-format-changes)
-   [Streamen von Ereignissen](#stream-events)
-   [Zugehörige Themen](#related-topics)

## <a name="basic-processing-model"></a>Grundlegendes Verarbeitungsmodell

### <a name="create-the-mft"></a>Erstellen des MFT

Es gibt mehrere Möglichkeiten zum Erstellen eines MFT:

-   Rufen Sie die [**MFTEnum-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) auf.
-   Rufen Sie die [**MFTEnumEx-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) auf.
-   Wenn Sie die CLSID des MFT bereits kennen, rufen Sie einfach **CoCreateInstance auf.**

Einige MFTs bieten möglicherweise andere Optionen, z. B. eine spezialisierte Erstellungsfunktion.

### <a name="get-stream-identifiers"></a>Get Stream Identifiers

Ein MFT verfügt über einen oder mehrere *Streams.* Eingabestreams empfangen Eingabedaten, und Ausgabestreams generieren Ausgabedaten. Streams werden nicht als unterschiedliche Objekte dargestellt. Stattdessen verwenden verschiedene MFT-Methoden Streambezeichner als Parameter.

Einige MFTs ermöglichen es dem Client, Eingabestreams hinzuzufügen oder zu entfernen. Während des Streamings kann ein MFT Ausgabestreams hinzufügen oder entfernen. (Der Client kann keine Ausgabestreams hinzufügen oder entfernen.)

1.  (Optional.) Rufen [**Sie DEN AUFRUF VON VERGRÖßERTransform::GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits) auf, um die minimale und maximale Anzahl von Streams zu erhalten, die MFT unterstützen kann. Wenn das Minimum und der Höchstwert identisch sind, verfügt MFT über eine feste Anzahl von Streams.
2.  Rufen Sie ZUM Abruf der anfänglichen Anzahl [**von Datenströmen DEN CALLTransform::GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) auf.
3.  Rufen [**Sie DIEBTRANSFORM::GetStreamIDs auf,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) um die Streambezeichner zu erhalten. Wenn diese Methode E NOTIMPL zurückgibt, bedeutet dies, dass MFT über eine feste Anzahl von Datenströmen verfügt und die Streambezeichner aufeinanderfolgende ab \_ 0 (null) sind.
4.  (Optional.) Wenn MFT nicht über eine feste Anzahl von Datenströmen verfügt, rufen Sie ZUM Hinzufügen von zusätzlichen [**Eingabestreams DEN AUFRUF VON DURCHGEFORMTRANSFORM::AddInputStreams**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-addinputstreams) oder ZUM Entfernen von Eingabestreams [**AUF: ELETRANSFORM::D eleteInputStream.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-deleteinputstream) (Ausgabestreams können nicht hinzugefügt oder entfernt werden.)

### <a name="set-media-types"></a>Festlegen von Medientypen

Bevor ein MFT Daten verarbeiten kann, muss der Client einen Medientypen für jeden der Streams des MFT festlegen. Ein MFT erfordert möglicherweise, dass der Client die Eingabetypen vor dem Festlegen der Ausgabetypen oder die umgekehrte Reihenfolge (Ausgabetypen zuerst) festlegen muss. Für einige MFTs ist die Bestellung nicht erforderlich.

Ein MFT kann eine Liste der bevorzugten Medientypen für einen Stream bereitstellen. Darüber hinaus können MFTs die allgemeinen Formate angeben, die sie unterstützen, indem sie diese Informationen zur Registrierung hinzufügen.

Gehen Sie wie folgt vor, um die Medientypen zu festlegen:

1.  (Optional.) Rufen Sie für jeden Eingabestream [**DEN TYPTRANSFORM::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) auf, um die Liste der bevorzugten Typen für diesen Stream zu erhalten.
    -   Wenn diese Methode MF E TRANSFORM TYPE NOT SET zurückgibt, müssen Sie zuerst die Ausgabetypen festlegen. Fahren Sie \_ \_ mit Schritt \_ \_ \_ 3 fort.
    -   Wenn die Methode E NOTIMPL zurückgibt, verfügt MFT nicht über eine Liste bevorzugter Eingabetypen. Fahren Sie \_ mit Schritt 2 fort.
2.  Rufen Sie für jeden Eingabestream [**DEN EINGABETRANSFORM::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) auf, um den Eingabetyp fest zu legen. Sie können einen Medientyp aus Schritt 1 oder einen Typ verwenden, der Ihre Eingabedaten beschreibt. Wenn ein Stream MF \_ E TRANSFORM TYPE NOT SET \_ \_ \_ \_ zurückgibt, fahren Sie mit Schritt 3 fort.
3.  (Optional.) Rufen Sie für jeden Ausgabestream [**DEN TYPTRANSFORM::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf, um eine Liste der bevorzugten Typen für diesen Stream zu erhalten.
    -   Wenn diese Methode MF E TRANSFORM TYPE NOT SET zurückgibt, müssen Sie zuerst die Eingabetypen festlegen. Wechseln Sie \_ \_ zurück zu Schritt \_ \_ \_ 1.
    -   Wenn ein Stream E NOTIMPL zurückgibt, verfügt MFT nicht über eine Liste bevorzugter Ausgabetypen. Fahren Sie \_ mit Schritt 4 fort.
4.  Rufen Sie für jeden Ausgabestream [**DEN OUTPUTTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) auf, um den Ausgabetyp zu festlegen. Sie können einen Medientyp aus Schritt 3 oder einen Typ verwenden, der das erforderliche Ausgabeformat beschreibt.
5.  Wenn Eingabestreams keinen Medientyp haben, fahren Sie mit Schritt 1 fort.

### <a name="get-buffer-requirements"></a>Get Buffer Requirements

Nachdem der Client die Medientypen festgelegt hat, sollte er die Pufferanforderungen für jeden Stream erhalten:

-   Rufen Sie für jeden Eingabedatenstrom [**DEN TEXT 2016 AUF: 150022222222222222211122222222222222**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   Rufen Sie für jeden Ausgabestream [**den Aufruf VON 5000022222222222272222222277222222222222222**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)

### <a name="process-data"></a>Daten verarbeiten

Ein MFT ist als zuverlässiger Zustandsautomat konzipiert. Es werden keine Aufrufe an den Client ausgeführt.

1.  Rufen Sie MIT DER MFT MESSAGE NOTIFY [**\_ \_ \_ BEGIN \_**](mft-message-notify-begin-streaming.md) [**STREAMING:P Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) auf. Diese Meldung fordert den MFT auf, während des Streamings alle benötigten Ressourcen zu reservieren.
2.  Rufen [**Sie DIE EINGABETRANSFORM::P rocessInput für**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) mindestens einen Eingabestream auf, um ein Eingabebeispiel an MFT zu liefern.
3.  (Optional.) Rufen [**Sie DEN BEFEHLSTRANSFORM::GetOutputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus) auf, um zu fragen, ob MFT ein Ausgabebeispiel generieren kann. Wenn die Methode S \_ OK zurückgibt, überprüfen Sie den *pdwFlags-Parameter.* Wenn *pdwFlags das* **Flag MFT OUTPUT STATUS SAMPLE \_ \_ \_ \_ READY** enthält, fahren Sie mit Schritt 4 fort. Wenn *pdwFlags 0* (null) ist, fahren Sie mit Schritt 2 fort. Wenn die Methode E \_ NOTIMPL zurückgibt, fahren Sie mit Schritt 4 fort.
4.  Rufen [**Sie ZUM Erhalten von Ausgabedaten DEN CALLTRANSFORM::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf.
    -   Wenn die Methode **MF \_ E TRANSFORM NEED MORE \_ \_ \_ \_ INPUT** zurückgibt, bedeutet dies, dass MFT mehr Eingabedaten erfordert. Fahren Sie zurück zu Schritt 2.
    -   Wenn die Methode **MF \_ E TRANSFORM STREAM \_ \_ \_ CHANGE** zurückgibt, bedeutet dies, dass sich die Anzahl der Ausgabestreams geändert hat oder das Ausgabeformat geändert wurde. Der Client muss möglicherweise neue Streambezeichner abfragen oder neue Medientypen festlegen. Weitere Informationen finden Sie in der Dokumentation zu [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
5.  Wenn noch Eingabedaten zu verarbeiten sind, fahren Sie mit Schritt 2 fort. Wenn MFT alle verfügbaren Eingabedaten verbraucht hat, fahren Sie mit Schritt 6 fort.
6.  Rufen [**Sie ProcessMessage mit**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) der [**MFT MESSAGE NOTIFY END OF \_ \_ \_ \_ \_ STREAM-Nachricht**](mft-message-notify-end-of-stream.md) auf.
7.  Rufen [**Sie ProcessMessage mit**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) der [**MFT MESSAGE COMMAND \_ \_ \_ DRAIN-Nachricht**](mft-message-command-drain.md) auf.
8.  Rufen [**Sie ProcessOutput auf,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) um die verbleibende Ausgabe zu erhalten. Wiederholen Sie diesen Schritt, bis die Methode **MF \_ E TRANSFORM NEED MORE INPUT \_ \_ \_ \_ zurückgibt.** Dieser Rückgabewert signalisiert, dass die ganze Ausgabe aus dem MFT-Wert entleert wurde. (Behandeln Sie dies nicht als Fehlerbedingung.)

Die hier beschriebene Sequenz speichert so wenig Daten wie möglich im MFT. Nach jedem Aufruf [**von ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)versucht der Client, die Ausgabe zu erhalten. Möglicherweise sind mehrere Eingabebeispiele erforderlich, um ein Ausgabebeispiel zu erzeugen, oder ein einzelnes Eingabebeispiel generiert möglicherweise mehrere Ausgabebeispiele. Das optimale Verhalten für den Client besteht im Pullen von Ausgabebeispielen aus dem MFT, bis MFT mehr Eingaben erfordert.

MFT sollte jedoch in der Lage sein, eine andere Reihenfolge von Methodenaufrufen durch den Client zu verarbeiten. Beispielsweise kann der Client einfach zwischen Aufrufen von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) und [**ProcessOutput wechseln.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) Der MFT sollte die Menge an Eingaben einschränken, die er erhält, indem **er MF \_ E \_ NOTACCEPTING** von **ProcessInput** zurücksendet, wenn eine Ausgabe erzeugt werden muss.

Die hier beschriebene Reihenfolge der Methodenaufrufe ist nicht die einzige gültige Sequenz von Ereignissen. In den Schritten 3 und 4 wird beispielsweise davon ausgegangen, dass der Client mit den Eingabetypen beginnt und dann die Ausgabetypen versucht. Der Client kann diese Reihenfolge auch umkehren und mit den Ausgabetypen beginnen. Wenn der MFT in beiden Fällen die umgekehrte Reihenfolge erfordert, sollte er den Fehlercode MF \_ E TRANSFORM TYPE NOT SET \_ \_ \_ \_ zurückgeben.

Der Client kann während des Streamings jederzeit Informationsmethoden wie [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype) und [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)aufrufen. Der Client kann auch jederzeit versuchen, die Medientypen zu ändern. MFT sollte einen Fehlercode zurückgeben, wenn dies kein gültiger Vorgang ist. Kurz gesagt: MFTs sollten nur sehr wenig von der Reihenfolge der Vorgänge ausgehen, die nicht in den Aufrufen selbst dokumentiert ist.

Das folgende Diagramm zeigt ein Flussdiagramm der in diesem Thema beschriebenen Verfahren.

![Flussdiagramm, das vom Erhalten von Datenstrombezeichnern durch Schleifen führt, die Eingabetypen festlegen, Eingaben erhalten und Ausgaben verarbeiten](images/mft-processing.gif)

## <a name="extensions-to-the-basic-model"></a>Erweiterungen des Basismodells

Optional kann ein MFT einige Erweiterungen des grundlegenden Streamingmodells unterstützen.

-   Datenströme mit verzögerter Leseung. Wenn [**die METHODE VERFORMTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) das **MFT \_ OUTPUT STREAM \_ \_ LAZY \_ READ-Flag** für einen Ausgabestream zurückgibt, muss der Client keine Daten aus diesem Ausgabestream sammeln. Der MFT akzeptiert weiterhin Eingaben, und zu einem bestimmten Zeitpunkt verwirft MFT die Ausgabedaten aus diesem Stream. Wenn alle Ausgabestreams über dieses Flag verfügen, kann MFT keine Eingaben akzeptieren. Ein Beispiel hierfür ist eine Visualisierungstransformation, bei der der Client die Ausgabe nur erhält, wenn er über freie CPU-Zyklen verfügt, um die Visualisierung zu zeichnen.
-   Verwerfende Datenströme. Wenn die [**GetOutputStreamInfo-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) das **MFT \_ OUTPUT STREAM \_ \_ DISCARDABLE-Flag** für einen Ausgabestream zurückgibt, kann der Client vom MFT anfordern, die Ausgabe zu verwerfen, aber der MFT verwirft keine Ausgabe, sofern dies nicht angefordert wird. Wenn MFT den maximalen Eingabepuffer erreicht, muss der Client entweder ausgabedaten sammeln oder den MFT bitten, die Ausgabe zu verwerfen.
-   Optionale Streams. Wenn die [**GetOutputStreamInfo-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) das **OPTIONALe MFT \_ OUTPUT \_ \_ STREAM-Flag** für einen Ausgabestream zurückgibt oder die [**METHODE VERFORM::GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo) das **optionale MFT \_ INPUT \_ \_ STREAM-Flag** für einen Eingabestream zurückgibt, ist dieser Stream optional. Der Client muss keinen Medientyp für den Stream festlegen. Wenn der Client den Typ nicht festgelegt, wird die Auswahl des Streams aufgehoben. Ein deaktivierter Ausgabestream erzeugt keine Stichproben, und der Client stellt beim Aufrufen von [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)keinen Puffer für den Stream zur Verfügung. Ein deaktivierter Eingabestream akzeptiert keine Eingabedaten. Ein MFT kann alle eingabe- und ausgabestreams als optional markieren. Es wird jedoch erwartet, dass mindestens eine Eingabe und eine Ausgabe ausgewählt werden müssen, damit MFT funktioniert.
-   Asynchrone Verarbeitung. Das asynchrone Verarbeitungsmodell wurde in Windows 7 eingeführt. Dies wird im Thema [Asynchrone MFTs beschrieben.](asynchronous-mfts.md)

## <a name="imf2dbuffer"></a>2DBuffer

Wenn ein MFT nicht komprimierte Videodaten verarbeitet, sollte er die [**BEF2DBuffer-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) verwenden, um die Beispielpuffer zu bearbeiten. Um diese Schnittstelle zu erhalten, fragen Sie die [**BENUTZEROBERFLÄCHEMediaBuffer-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) für einen beliebigen Eingabe- oder Ausgabepuffer ab. Wenn diese Schnittstelle nicht verwendet wird, wenn sie verfügbar ist, kann dies zu zusätzlichen Pufferkopien führen. Um diese Schnittstelle ordnungsgemäß zu verwenden, sollte die Transformation den Puffer nicht mithilfe der **NSMMediaBuffer-Schnittstelle** sperren, wenn **DER2DBuffer** verfügbar ist.

Weitere Informationen zur Verarbeitung von Videodaten finden Sie unter [Unkomprimierte Videopuffer.](uncompressed-video-buffers.md)

## <a name="flushing-an-mft"></a>Leeren eines MFT

*Das Leeren* eines MFT bewirkt, dass MFT alle Eingabedaten verwirft. Dies kann zu einer Unterbrechung im Ausgabestream führen. Ein Client würde in der Regel einen MFT leeren, bevor er zu einem neuen Punkt im Eingabestream sucht oder zu einem neuen Eingabestream wechselt, wenn es dem Client nicht darum geht, Daten zu verlieren.

Um eine MFT zu leeren, rufen Sie [**MITTTTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der [**Meldung MFT \_ MESSAGE COMMAND \_ \_ FLUSH**](mft-message-command-flush.md) auf.

## <a name="draining-an-mft"></a>Leeren eines MFT

*Das Leeren* eines MFT führt dazu, dass MFT so viele Ausgaben wie möglich aus den bereits gesendeten Eingabedaten erzeugt. Wenn MFT kein vollständiges Ausgabebeispiel aus der verfügbaren Eingabe erzeugen kann, werden Eingabedaten entfernt. Ein Client würde einen MFT in der Regel leeren, wenn er das Ende des Quellstreams erreicht hat, oder unmittelbar vor einer Formatänderung im Quellstream. Gehen Sie wie folgt vor, um eine MFT zu leeren:

1.  Rufen [**Sie ProcessMessage mit**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) der [**MFT MESSAGE COMMAND \_ \_ \_ DRAIN-Nachricht**](mft-message-command-drain.md) auf. Diese Meldung benachrichtigt den MFT, dass er so viele Ausgabedaten wie möglich aus den bereits gesendeten Eingabedaten liefern sollte.
2.  Rufen [**Sie ProcessOutput auf,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) um Ausgabedaten zu erhalten, bis die **Methode MF E TRANSFORM NEED \_ MORE INPUT \_ \_ \_ \_ zurückgibt.**

Während der MFT-Entleerung wird keine weitere Eingabe akzeptiert.

## <a name="sample-attributes"></a>Beispielattribute

Die Eingabebeispiele können Attribute haben, die in die entsprechenden Ausgabebeispiele kopiert werden müssen.

-   Wenn der MFT **VARIANT \_ TRUE für** die [**MFPKEY \_ EXATTRIBUTE \_ SUPPORTED-Eigenschaft**](mfpkey-exattribute-supported-property.md) zurückgibt, muss MFT die Attribute kopieren.
-   Wenn die [**MFPKEY \_ EXATTRIBUTE \_ SUPPORTED-Eigenschaft**](mfpkey-exattribute-supported-property.md) entweder **VARIANT \_ FALSE** ist oder nicht festgelegt ist, muss der Client die Attribute kopieren.

Für ein MFT mit einer Eingabe und einer Ausgabe können Sie die folgende allgemeine Regel verwenden:

-   Wenn jedes Eingabebeispiel genau ein Ausgabebeispiel erzeugt, können Sie den Client die Attribute kopieren lassen. Lassen Sie [**die MFPKEY \_ EXATTRIBUTE \_ SUPPORTED-Eigenschaft**](mfpkey-exattribute-supported-property.md) nicht festgelegt.
-   Wenn keine 1:1-Entsprechung zwischen Eingabe- und Ausgabebeispielen besteht, muss MFT die richtigen Attribute für Ausgabebeispiele bestimmen. Legen Sie die [**MFPKEY \_ EXATTRIBUTE \_ SUPPORTED-Eigenschaft**](mfpkey-exattribute-supported-property.md) auf **VARIANT TRUE \_ fest.**

## <a name="discontinuities"></a>Unterbrechungen

Eine Diskontinuität ist eine Unterbrechung in einem Audio- oder Videostream. Diskontinuitäten können durch verworfene Pakete in einer Netzwerkverbindung, beschädigte Dateidaten, einen Wechsel von einem Quellstream zu einem anderen oder eine Vielzahl anderer Ursachen verursacht werden. Diskontinuitäten werden signalisiert, indem das [**MFSampleExtension \_ Discontinuity-Attribut**](mfsampleextension-discontinuity-attribute.md) in der ersten Stichprobe nach der Diskontinuität eingestellt wird. Es ist nicht möglich, eine Diskontinuität in der Mitte eines Beispiels zu signalisieren. Daher sollten alle diskontinuierlich gespeicherten Daten in separaten Stichproben gesendet werden.

Einige Transformationen, insbesondere solche, die nicht komprimierte Daten verarbeiten, z. B. Audio- und Videoeffekte, sollten Diskontinuitäten bei der Verarbeitung von Eingabedaten ignorieren. Diese MFTs sind im Allgemeinen für die Verarbeitung kontinuierlicher Daten konzipiert und sollten alle empfangenen Daten auch nach einer Unterbrechung als kontinuierlich behandeln.

Wenn ein MFT eine Diskontinuität für Eingabedaten ignoriert, sollte es weiterhin das Diskontinuitätsflag für das Ausgabebeispiel festlegen, wenn das Ausgabebeispiel denselben Zeitstempel wie das Eingabebeispiel auf hat. Wenn das Ausgabebeispiel jedoch über einen anderen Zeitstempel verfügt, sollte MFT die Diskontinuität nicht weiter geben. (Dies wäre beispielsweise bei einigen Audio-Resampler der Fall.) Eine Diskontinuität an der falschen Stelle im Stream ist schlechter als keine Diskontinuität.

Die meisten Decoder können Diskontinuitäten nicht ignorieren, da eine Diskontinuität die Interpretation der nächsten Stichprobe beeinflusst. Jede Codierungstechnologie, die frameübergreifende Komprimierung verwendet, z. B. MPEG-2, fällt in diese Kategorie. Einige Codierungsschemas verwenden nur frameinterne Komprimierung, z. B. DV und MJPEG. Diese Decoder können Diskontinuitäten problemlos ignorieren.

Transformationen, die auf Diskontinuitäten reagieren, sollten in der Regel so viele Daten wie möglich vor der Diskontinuität ausgegeben und den Rest verwerfen. Das Eingabebeispiel mit dem Diskontinuitätsflag sollte so verarbeitet werden, als wäre es das erste Beispiel im Stream. (Dieses Verhalten entspricht dem, was für die [**Meldung MFT \_ MESSAGE COMMAND \_ DRAIN \_ angegeben**](mft-message-command-drain.md) ist.) Die genauen Details hängen jedoch vom Medienformat ab.

Wenn ein Decoder keine Abmilderung einer Diskontinuität tut, sollte er das Diskontinuitätsflag in die Ausgabedaten kopieren. Demultiplexer und andere MFTs, die vollständig mit komprimierten Daten arbeiten, müssen alle Diskontinuitäten in ihre Ausgabestreams kopieren. Andernfalls können die komprimierten Daten von den Downstreamkomponenten möglicherweise nicht ordnungsgemäß decodiert werden. Im Allgemeinen ist es fast immer richtig, Diskontinuitäten nachgelagert zu übergeben, es sei denn, MFT enthält expliziten Code, um Diskontinuitäten zu glätten.

## <a name="dynamic-format-changes"></a>Dynamische Formatänderungen

Formate können sich während des Streamings ändern. Beispielsweise kann sich das Seitenverhältnis in der Mitte eines Videostreams ändern.

Weitere Informationen dazu, wie Streamänderungen von einem MFT verarbeitet werden, finden Sie unter [Behandeln von Streamänderungen.](handling-stream-changes.md)

## <a name="stream-events"></a>Streamen von Ereignissen

Um ein Ereignis an eine MFT zu senden, rufen [**Sie DIETRANSFORM::P rocessEvent auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) Wenn die Methode **MF \_ S TRANSFORM DO NOT \_ \_ \_ \_ PROPAGATE \_ EVENT** zurückgibt, gibt MFT das Ereignis bei einem nachfolgenden Aufruf von [**ProcessOutput an den Aufrufer zurück.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) Wenn die Methode einen anderen **HRESULT-Wert** zurückgibt, gibt MFT das Ereignis nicht an den Client in **ProcessOutput zurück.** In diesem Fall ist der Client für die Nachverteilung des Ereignisses an die nächste Komponente in der Pipeline (falls zutreffend) verantwortlich. Weitere Informationen finden Sie unter [**ROCTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 



