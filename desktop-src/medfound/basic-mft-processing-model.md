---
description: In diesem Thema wird beschrieben, wie ein Client eine Media Foundation Transformation (MFT) verwendet, um Daten zu verarbeiten. Der Client ist alles, was Methoden auf dem MFT direkt aufruft. Dies kann die Anwendung oder die Media Foundation Pipeline sein.
ms.assetid: be977d75-999e-4e57-9672-00a89246a2c1
title: Einfaches MFT-Verarbeitungsmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca54df6d9765aaf54456c3d9dc4461a82a93d41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041569"
---
# <a name="basic-mft-processing-model"></a>Einfaches MFT-Verarbeitungsmodell

In diesem Thema wird beschrieben, wie ein Client eine Media Foundation Transformation (MFT) verwendet, um Daten zu verarbeiten. Der *Client* ist alles, was Methoden auf dem MFT direkt aufruft. Dies kann die Anwendung oder die Media Foundation Pipeline sein.

Lesen Sie dieses Thema, wenn Sie Folgendes tun:

-   Schreiben einer Anwendung, die direkte Aufrufe an eine oder mehrere MFTs durchführt.
-   Schreiben eines benutzerdefinierten MFT-Vorgangs, um das erwartete Verhalten einer MFT zu verstehen.

In diesem Thema wird ein *synchrones* Verarbeitungsmodell beschrieben. In diesem Modell blockieren alle Datenverarbeitungsmethoden, bis Sie beendet werden. MFTs können auch ein *asynchrones* Modell unterstützen, das im Thema [asynchrone MFTs](asynchronous-mfts.md)beschrieben wird.

-   [Grundlegendes Verarbeitungsmodell](#basic-processing-model)
    -   [Erstellen der MFT](#create-the-mft)
    -   [Stream-IDs erhalten](#get-stream-identifiers)
    -   [Medientypen festlegen](#set-media-types)
    -   [Puffer Anforderungen erhalten](#get-buffer-requirements)
    -   [Verarbeiten von Daten](#process-data)
-   [Erweiterungen für das Basismodell](#extensions-to-the-basic-model)
-   [IMF2DBuffer](#imf2dbuffer)
-   [Leeren eines MFT](#flushing-an-mft)
-   [Entleeren eines MFT](#draining-an-mft)
-   [Beispiel Attribute](#sample-attributes)
-   [Unterbrechungen](#discontinuities)
-   [Dynamische Format Änderungen](#dynamic-format-changes)
-   [Streamereignisse](#stream-events)
-   [Zugehörige Themen](#related-topics)

## <a name="basic-processing-model"></a>Grundlegendes Verarbeitungsmodell

### <a name="create-the-mft"></a>Erstellen der MFT

Es gibt mehrere Möglichkeiten, eine MFT zu erstellen:

-   Ruft die [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion auf.
-   Ruft die [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion auf.
-   Wenn Sie die CLSID der MFT bereits kennen, können Sie einfach **cokreateinstance** aufrufen.

Einige MFTs können andere Optionen bereitstellen, z. b. eine spezialisierte Erstellungs Funktion.

### <a name="get-stream-identifiers"></a>Stream-IDs erhalten

Ein MFT verfügt über einen oder mehrere Daten *Ströme*. Eingabedaten Ströme empfangen Eingabedaten, und Ausgabedaten Ströme generieren Ausgabedaten. Streams werden nicht als unterschiedliche Objekte dargestellt. Stattdessen übernehmen verschiedene MFT-Methoden Datenstrom-IDs als Parameter.

Einige MFTs ermöglichen dem Client das Hinzufügen oder Entfernen von Eingabedaten strömen. Beim Streaming kann ein MFT Ausgabedaten Ströme hinzufügen oder entfernen. (Der Client kann keine Ausgabedaten Ströme hinzufügen oder entfernen.)

1.  (Optional) Wenn Sie [**imftransform:: getstreamlimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits) aufrufen, erhalten Sie die minimale und maximale Anzahl von Datenströmen, die von der MFT unterstützt werden können. Wenn der Minimalwert und der Höchstwert identisch sind, verfügt die MFT über eine Fixed Anzahl von Streams.
2.  Aufrufen von [**imftransform:: getstreamcount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) , um die anfängliche Anzahl von Streams zu erhalten.
3.  Aufrufen von [**imftransform:: getstreamids**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) zum Abrufen der Datenstrom Bezeichner. Wenn diese Methode E \_ notimpl zurückgibt, bedeutet dies, dass die MFT über eine Fixed Anzahl von Streams verfügt und die Datenstrom Bezeichner aufeinander folgen, beginnend bei Null.
4.  (Optional) Wenn die MFT nicht über eine festgelegte Anzahl von Streams verfügt, müssen Sie [**imftransform:: addinputstreams**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-addinputstreams) zum Hinzufügen von weiteren Eingabedaten Strömen oder [**imftransform::D eleteinputstream**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-deleteinputstream) zum Entfernen von Eingabedaten strömen aufruft. (Sie können keine Ausgabedaten Ströme hinzufügen oder entfernen.)

### <a name="set-media-types"></a>Medientypen festlegen

Bevor Daten vom MFT verarbeitet werden können, muss der Client für jeden Stream der MFT einen Medientypen festlegen. Eine MFT erfordert möglicherweise, dass der Client die Eingabetypen festlegt, bevor die Ausgabetypen festgelegt werden, oder erfordert möglicherweise die umgekehrte Reihenfolge (zuerst Ausgabetypen). Einige MFTs haben keine Voraussetzung für die Reihenfolge.

Eine MFT kann eine Liste der bevorzugten Medientypen für einen Stream bereitstellen. Außerdem können MFTs die allgemeinen Formate angeben, die Sie unterstützen, indem diese Informationen der Registrierung hinzugefügt werden.

Gehen Sie folgendermaßen vor, um die Medientypen festzulegen:

1.  (Optional) Aufrufen Sie für jeden Eingabestream [**imftransform:: getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) , um die Liste der bevorzugten Typen für diesen Stream abzurufen.
    -   Wenn diese Methode den von \_ MF \_ E \_ transformierentyp \_ nicht \_ festgelegt zurückgibt, müssen Sie zuerst die Ausgabetypen festlegen; fahren Sie mit Schritt 3 fort.
    -   Wenn die Methode E \_ notimpl zurückgibt, verfügt die MFT nicht über eine Liste der bevorzugten Eingabetypen; fahren Sie mit Schritt 2 fort.
2.  Für jeden Eingabestream wird [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) aufgerufen, um den Eingabetyp festzulegen. Sie können einen Medientyp aus Schritt 1 oder einen Typ verwenden, der Ihre Eingabedaten beschreibt. Wenn ein Stream einen \_ nicht festgelegten MF-E- \_ \_ Transformationstyp zurückgibt \_ \_ , springen Sie zu Schritt 3.
3.  (Optional) Für jeden Ausgabestream müssen Sie [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) aufrufen, um eine Liste der bevorzugten Typen für diesen Stream abzurufen.
    -   Wenn diese Methode den MF- \_ E- \_ \_ Transformationstyp \_ nicht festgelegt zurückgibt \_ , müssen Sie zuerst die Eingabetypen festlegen, sondern zu Schritt 1 zurückkehren.
    -   Wenn ein Datenstrom E \_ notimpl zurückgibt, verfügt die MFT nicht über eine Liste der bevorzugten Ausgabetypen; fahren Sie mit Schritt 4 fort.
4.  Für jeden Ausgabestream müssen Sie [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) aufrufen, um den Ausgabetyp festzulegen. Sie können einen Medientyp aus Schritt 3 oder einen Typ verwenden, der das erforderliche Ausgabeformat beschreibt.
5.  Wenn Eingabedaten Ströme keinen Medientyp aufweisen, gehen Sie zurück zu Schritt 1.

### <a name="get-buffer-requirements"></a>Puffer Anforderungen erhalten

Nachdem der Client die Medientypen festgelegt hat, sollte er die Puffer Anforderungen für jeden Stream erhalten:

-   Aufrufen Sie für jeden Eingabestream [**imftransform:: getinputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo).
-   Aufrufen Sie für jeden Ausgabestream [**imftransform:: getoutputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).

### <a name="process-data"></a>Daten verarbeiten

Eine MFT ist als zuverlässiger Zustands Automat konzipiert. Es werden keine Aufrufe an den Client zurück gemacht.

1.  " [**Imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) " mit der Meldung "Meldung zum [**Starten von MFT- \_ Nachricht \_ Benachrichtigen \_ \_**](mft-message-notify-begin-streaming.md) ". Mit dieser Meldung wird die MFT aufgefordert, alle Ressourcen zuzuordnen, die während des Streamings benötigt werden.
2.  Aufrufen von [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) in mindestens einem Eingabedaten Strom, um eine Eingabe Stichprobe für die MFT bereitzustellen.
3.  (Optional) Rufen Sie [**imftransform:: getoutputstatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus) auf, um abzufragen, ob der MFT eine Ausgabe Stichprobe generieren kann. Wenn die Methode S OK zurückgibt \_ , überprüfen Sie den *pdwflags* -Parameter. Wenn *pdwflags* den **MFT- \_ Ausgabe \_ Status \_ Sample \_ Ready** -Flag enthält, fahren Sie mit Schritt 4 fort. Wenn *pdwflags* gleich NULL ist, wechseln Sie zurück zu Schritt 2. Wenn die Methode E \_ notimpl zurückgibt, fahren Sie mit Schritt 4 fort.
4.  [**Imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) zum Abrufen von Ausgabedaten.
    -   Wenn die Methode " **MF E Transform" zurückgibt, \_ benötigen Sie \_ \_ \_ mehr \_ Eingaben**. Dies bedeutet, dass der MFT mehr Eingabedaten erfordert. wechseln Sie zurück zu Schritt 2.
    -   Wenn die Methode die **Änderung von MF \_ E \_ Transform \_ Stream \_** zurückgibt, bedeutet dies, dass sich die Anzahl der Ausgabestreams geändert hat oder sich das Ausgabeformat geändert hat. Möglicherweise muss der Client neue Datenstrom Bezeichner Abfragen oder neue Medientypen festlegen. Weitere Informationen finden Sie in der Dokumentation zu [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
5.  Wenn noch Eingabedaten verarbeitet werden müssen, fahren Sie mit Schritt 2 fort. Wenn die MFT alle verfügbaren Eingabedaten verbraucht hat, fahren Sie mit Schritt 6 fort.
6.  Wenden Sie [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der Nachricht Nachrichten [**\_ \_ \_ Ende der \_ \_ Nachricht benachrichtigen an**](mft-message-notify-end-of-stream.md) .
7.  Wenden Sie [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der [**MFT- \_ Nachrichten \_ Befehls \_**](mft-message-command-drain.md) Ausgleichs Meldung an.
8.  Wenden Sie [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) an, um die verbleibende Ausgabe abzurufen. Wiederholen Sie diesen Schritt, bis die Methode " **MF \_ E \_ Transform" \_ \_ mehr \_ Eingaben benötigt**. Dieser Rückgabewert gibt an, dass die gesamte Ausgabe aus dem MFT entladen wurde. (Behandeln Sie dies nicht als Fehlerbedingung.)

Die hier beschriebene Sequenz speichert so wenig Daten wie möglich in der MFT. Nach jedem Aufrufen von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)versucht der Client, die Ausgabe abzurufen. Möglicherweise sind mehrere Eingabe Beispiele erforderlich, um ein Ausgabe Beispiel zu erzeugen, oder eine einzelne Eingabe Stichprobe generiert möglicherweise mehrere Ausgabe Beispiele. Das optimale Verhalten für den Client besteht darin, Ausgabe Beispiele aus dem MFT abzurufen, bis die MFT mehr Eingaben erfordert.

Die MFT sollte jedoch in der Lage sein, eine andere Reihenfolge von Methoden aufrufen durch den Client zu verarbeiten. Beispielsweise kann der Client einfach zwischen den Aufrufen von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) und [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)wechseln. Der MFT sollte die Menge der eingegebenen Eingaben einschränken, indem er von **ProcessInput** eine Ausgabe von **MF \_ E \_ notannimmt** , wenn eine Ausgabe erzeugt wird.

Die hier beschriebene Reihenfolge der Methodenaufrufe ist nicht die einzige gültige Abfolge von Ereignissen. Bei den Schritten 3 und 4 wird z. b. davon ausgegangen, dass der Client mit den Eingabetypen beginnt und dann die Ausgabetypen ausprobiert. Der Client kann diese Reihenfolge ebenfalls umkehren und mit den Ausgabetypen beginnen. Wenn für die MFT in beiden Fällen die umgekehrte Reihenfolge erforderlich ist, sollte der Fehlercode MF \_ E \_ \_ \_ nicht \_ festgelegt werden.

Der Client kann während des Streamings jederzeit Informationsmethoden, z. b. [**getinputcurrenttype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype) und [**getoutputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo), aufrufen. Der Client kann auch versuchen, die Medientypen jederzeit zu ändern. Der MFT sollte einen Fehlercode zurückgeben, wenn dies kein gültiger Vorgang ist. Kurz gesagt, die MFTs sollten nur sehr wenig von der Reihenfolge der Vorgänge ausgehen, außer den in den Aufrufen selbst dokumentierten.

Das folgende Diagramm zeigt ein Flussdiagramm der in diesem Thema beschriebenen Prozeduren.

![Flussdiagramm, das aus Get Stream-bezeichlern durch Schleifen führt, die Eingabetypen festlegen, Eingaben erhalten und die Ausgabe verarbeiten.](images/mft-processing.gif)

## <a name="extensions-to-the-basic-model"></a>Erweiterungen für das Basismodell

Optional kann ein MFT einige Erweiterungen für das grundlegende Streamingmodell unterstützen.

-   Träge gelesene Datenströme. Wenn die [**imftransform:: getoutputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) -Methode den **MFT \_ - \_ \_ Ausgabestream Lazy \_ Read** -Flag für einen Ausgabestream zurückgibt, muss der Client keine Daten aus diesem Ausgabestream sammeln. Der MFT akzeptiert weiterhin Eingaben, und die MFT verwirft die Ausgabedaten aus diesem Stream zu einem bestimmten Zeitpunkt. Wenn alle Ausgabedaten Ströme über dieses Flag verfügen, wird die Eingabe von der MFT niemals akzeptiert. Ein Beispiel hierfür ist eine Visualisierungs Transformation, bei der der Client die Ausgabe nur dann abruft, wenn er über freie CPU-Zyklen zum Zeichnen der Visualisierung verfügt.
-   Ververwerfbare Streams. Wenn die [**getoutputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) -Methode das Flag zum **verwerfen des MFT- \_ Ausgabestreams \_ \_** für einen Ausgabestream zurückgibt, kann der Client den MFT zum Verwerfen der Ausgabe anfordern, aber die MFT verwirft keine Ausgabe, sofern Sie nicht angefordert wurde. Wenn der MFT den maximalen Eingabepuffer erreicht, muss der Client entweder einige Ausgabedaten sammeln oder den MFT anfordern, um die Ausgabe zu verwerfen.
-   Optionale Streams. Wenn die [**getoutputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) -Methode das **optionale Flag des MFT- \_ Ausgabestreams \_ \_** für einen Ausgabestream zurückgibt oder die [**imftransform:: getinputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo) -Methode das optionale Flag des **MFT- \_ Eingabedaten \_ Stroms \_** für einen Eingabestream zurückgibt, ist dieser Stream optional. Der Client muss keinen Medientyp für den Stream festlegen. Wenn der Client den Typ nicht festgelegt, wird der Stream deaktiviert. Ein deaktivierter Ausgabedatenstrom erzeugt keine Beispiele, und der Client stellt keinen Puffer für den Datenstrom bereit, wenn [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)aufgerufen wird. Ein deaktivierter Eingabedaten Strom akzeptiert keine Eingabedaten. Ein MFT kann alle seine Eingabe-und Ausgabedaten Ströme als optional markieren. Es wird jedoch erwartet, dass mindestens eine Eingabe und eine Ausgabe ausgewählt werden müssen, damit der MFT funktioniert.
-   Asynchrone Verarbeitung. Das asynchrone Verarbeitungsmodell wurde in Windows 7 eingeführt. Dies wird im Thema [asynchrone MFTs](asynchronous-mfts.md)beschrieben.

## <a name="imf2dbuffer"></a>IMF2DBuffer

Wenn eine MFT unkomprimierte Videodaten verarbeitet, sollte Sie die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle verwenden, um die Beispiel Puffer zu bearbeiten. Um diese Schnittstelle zu erhalten, Fragen Sie die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle in einem beliebigen Eingabe-oder Ausgabepuffer ab. Wenn diese Schnittstelle nicht verwendet wird, wenn Sie verfügbar ist, kann dies zu zusätzlichen Puffer Kopien führen. Um diese Schnittstelle ordnungsgemäß zu verwenden, sollte die Transformation den Puffer nicht mithilfe der **imfmediabuffer** -Schnittstelle sperren, wenn **IMF2DBuffer** verfügbar ist.

Weitere Informationen zum Verarbeiten von Videodaten finden Sie unter [nicht komprimierte Video Puffer](uncompressed-video-buffers.md).

## <a name="flushing-an-mft"></a>Leeren eines MFT

Das *leeren eines* MFT bewirkt, dass der MFT alle Eingabedaten verworfen hat. Dies kann zu einer Unterbrechung im Ausgabestream führen. Ein Client würde in der Regel eine MFT leeren, bevor er einen neuen Punkt im Eingabestream sucht oder zu einem neuen Eingabestream wechselt, wenn der Client keinen Datenverlust berücksichtigt.

Um einen MFT zu leeren, wenden Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der [**MFT- \_ Nachrichten \_ Befehls \_**](mft-message-command-flush.md) Leerungs Meldung an.

## <a name="draining-an-mft"></a>Entleeren eines MFT

Das *entleeren* eines MFT bewirkt, dass der MFT so viele Ausgaben erzeugt, wie er von den bereits gesendeten Eingabedaten möglich ist. Wenn die MFT kein vollständiges Ausgabe Beispiel aus der verfügbaren Eingabe erzeugt, werden die Eingabedaten gelöscht. Ein Client würde in der Regel eine MFT beim Erreichen des Endes des Quelldaten Stroms oder unmittelbar vor einer Formatänderung im Quellstream entleeren. Gehen Sie folgendermaßen vor, um ein MFT zu entfernen:

1.  Wenden Sie [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der [**MFT- \_ Nachrichten \_ Befehls \_**](mft-message-command-drain.md) Ausgleichs Meldung an. Diese Meldung benachrichtigt die MFT, dass Sie so viele Ausgabedaten wie möglich aus den bereits gesendeten Eingabedaten bereitstellt.
2.  Ruft [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf, um Ausgabedaten zu erhalten, bis die Methode die MF E-Transformation zurückgibt, **\_ \_ \_ benötigt \_ mehr \_ Eingaben**.

Während der MFT-Vorgang wird die Eingabe nicht mehr akzeptiert.

## <a name="sample-attributes"></a>Beispiel Attribute

Die Eingabe Beispiele können Attribute enthalten, die in die entsprechenden Ausgabe Beispiele kopiert werden müssen.

-   Wenn die MFT **Variant \_ true** für die [**\_ \_ unterstützte Eigenschaft mfpkey exattribute**](mfpkey-exattribute-supported-property.md) zurückgibt, muss die MFT die Attribute kopieren.
-   Wenn die [**\_ \_ unterstützte mfpkey exattribute**](mfpkey-exattribute-supported-property.md) -Eigenschaft entweder **Variant \_ false** ist oder nicht festgelegt ist, muss der Client die Attribute kopieren.

Für eine MFT mit einer Eingabe und einer Ausgabe können Sie die folgende allgemeine Regel verwenden:

-   Wenn jedes Eingabe Beispiel genau ein Ausgabe Beispiel erzeugt, können Sie den Client die Attribute kopieren lassen. Lassen Sie die [**\_ \_ unterstützte Eigenschaft "mfpkey exattribute**](mfpkey-exattribute-supported-property.md) " nicht festgelegt.
-   Wenn keine 1:1-Entsprechung zwischen Eingabe Beispielen und Ausgabe Beispielen vorhanden ist, muss der MFT die richtigen Attribute für Ausgabe Beispiele ermitteln. Legen Sie die Eigenschaft [**mfpkey \_ exattribute \_ unterstützt**](mfpkey-exattribute-supported-property.md) auf **Variant \_ true** fest.

## <a name="discontinuities"></a>Unterbrechungen

Eine Diskontinuität ist eine Unterbrechung in einem Audiostream oder Videostream. Diskontinuitäten können durch gelöschte Pakete in einer Netzwerkverbindung, beschädigte Datei Daten, einen Wechsel von einem Quelldaten Strom zu einem anderen oder eine Vielzahl anderer Ursachen verursacht werden. Diskontinuitäten werden signalisiert, indem das " [**MF SampleExtension \_ discontinuity**](mfsampleextension-discontinuity-attribute.md) "-Attribut im ersten Beispiel nach der Diskontinuität festgelegt wird. Es ist nicht möglich, eine Diskontinuität in der Mitte eines Beispiels zu signalisieren. Daher sollten alle diskontinuierlichen Daten in separaten Beispielen gesendet werden.

Einige Transformationen, insbesondere solche, die nicht komprimierte Daten verarbeiten, z. b. Audio-und Video Effekte, sollten Diskontinuitäten ignorieren, wenn Sie Eingabedaten verarbeiten. Diese MFTs sind in der Regel so konzipiert, dass kontinuierliche Daten verarbeitet werden, und sollten alle Daten, die Sie als kontinuierlich empfangen, auch nach einer Diskontinuität behandeln.

Wenn eine MFT eine Diskontinuität der Eingabedaten ignoriert, sollte Sie trotzdem das Diskontinuität-Flag für das Ausgabe Beispiel festlegen, wenn die Ausgabe Stichprobe denselben Zeitstempel wie das Eingabe Beispiel aufweist. Wenn die Ausgabe Stichprobe jedoch einen anderen Zeitstempel aufweist, sollte der MFT die Diskontinuität nicht weitergeben. (Dies wäre z. b. bei einigen audioresamplern der Fall.) Eine Diskontinuität an der falschen Stelle im Stream ist schlechter als keine Diskontinuität.

Die meisten Decoder können Diskontinuitäten nicht ignorieren, da eine Diskontinuität sich auf die Interpretation des nächsten Beispiels auswirkt. Alle Codierungstechnologien, die eine Frame übergreifende Komprimierung verwenden (z. b. MPEG-2), fallen in diese Kategorie. Einige Codierungs Schemas verwenden nur die interne Komprimierung, wie z. b. DV und MJPEG. Diese Decoder können Diskontinuitäten gefahrlos ignorieren.

Transformationen, die auf Diskontinuitäten reagieren, sollten in der Regel so viele Daten wie möglich vor der Diskontinuität ausgeben und den Rest verwerfen. Das Eingabe Beispiel mit dem Diskontinuität-Flag sollte so verarbeitet werden, als wäre es das erste Beispiel im Stream. (Dieses Verhalten entspricht dem, was für die [**MFT \_ - \_ Nachrichten \_ Befehls**](mft-message-command-drain.md) Ausgleichs Meldung angegeben wird.) Die genauen Details hängen jedoch vom Medienformat ab.

Wenn ein Decoder keine Diskontinuität mindern kann, sollte das Flag für die Diskontinuität in die Ausgabedaten kopiert werden. Demultiplexer und andere MFTs, die vollständig mit komprimierten Daten arbeiten, müssen alle Diskontinuitäten in Ihre Ausgabedaten Ströme kopieren. Andernfalls können die Downstreamkomponenten die komprimierten Daten möglicherweise nicht ordnungsgemäß decodieren. Im Allgemeinen ist es fast immer korrekt, Diskontinuitäten nachgelagert zu übergeben, es sei denn, der MFT enthält expliziten Code zum Glätten von Diskontinuitäten.

## <a name="dynamic-format-changes"></a>Dynamische Format Änderungen

Formate können während des Streamings geändert werden. Beispielsweise kann sich das Seitenverhältnis in der Mitte eines Videodaten Stroms ändern.

Ausführliche Informationen dazu, wie streamänderungen von einem MFT behandelt werden, finden Sie unter [Handling Stream Changes](handling-stream-changes.md).

## <a name="stream-events"></a>Streamereignisse

Um ein Ereignis an einen MFT zu senden, wird [**imftransform::P rocesabvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)aufgerufen. Wenn die Methode das **" \_ MF \_ S \_ Transform \_ Not \_ propagieren \_**"-Ereignis zurückgibt, gibt die MFT das Ereignis für einen nachfolgenden Aufruf von [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)an den Aufrufer zurück. Wenn die Methode einen anderen **HRESULT** -Wert zurückgibt, wird das Ereignis vom MFT nicht an den Client in **ProcessOutput** zurückgegeben. In diesem Fall ist der Client für die Weitergabe des Ereignisses an die nächste Komponente in der Pipeline zuständig, falls zutreffend. Weitere Informationen finden Sie unter [**IMF Transform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 



