---
description: In diesem Thema wird beschrieben, wie eine benutzerdefinierte Medienquelle in Microsoft Media Foundation implementiert wird.
ms.assetid: 82db6f32-ad94-4563-b8bd-8a5072c5b221
title: Schreiben einer benutzerdefinierten Medienquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8769fa16d4dcbfd3438b66f9a9e78c34274735a5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353627"
---
# <a name="writing-a-custom-media-source"></a>Schreiben einer benutzerdefinierten Medienquelle

In diesem Thema wird beschrieben, wie eine benutzerdefinierte Medienquelle in Microsoft Media Foundation implementiert wird. Sie enthält die folgenden Abschnitte:

-   [Erstellen des Präsentations Deskriptors](#creating-the-presentation-descriptor)
-   [Starten der Medienquelle](#starting-the-media-source)
    -   [Diejenigen](#seeking)
-   [Anhalten der Medienquelle](#pausing-the-media-source)
-   [Quelldaten werden erzeugt.](#generating-source-data)
    -   [Beispiel Anforderungen](#sample-requests)
    -   [Zuordnen von Beispielen](#allocating-samples)
    -   [Lücken im Stream](#gaps-in-the-stream)
-   [Die Medienquelle wird heruntergefahren.](#shutting-down-the-media-source)
-   [Live Quellen](#live-sources)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-the-presentation-descriptor"></a>Erstellen des Präsentations Deskriptors

Die [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) -Methode gibt eine Kopie des Präsentations Deskriptors der Quelle zurück. Um den Präsentations Deskriptor zu erstellen, müssen Sie die Anzahl der Streams im Quell Inhalt und die möglichen Formate jedes Streams kennen. Erstellen Sie für jeden Stream einen Datenstrom Deskriptor wie folgt:

1.  Erstellen Sie ein Array von Medientypen. Jeder Medientyp im Array stellt ein mögliches Format für den Stream dar. Weitere Informationen zum Erstellen von Medientypen finden Sie unter [Medientypen](media-types.md).
2.  Rufen Sie [**mfkreatestreamdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) auf, um den Datenstrom Deskriptor zu erstellen. Übergeben Sie das Array von Medientypen. Die-Funktion gibt einen [**IMF streamdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) -Zeiger zurück.
3.  Aufrufen von [**imfstreamdescriptor:: getmediatyphandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) zum Abrufen des Medientyp Handlers für den Datenstrom Deskriptor.
4.  Aufrufen von [**imfmediatyphandler:: setcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) zum Festlegen des standardmäßigen streamformats. Verwenden Sie einen der Medientypen, die Sie in Schritt 1 erstellt haben. Im Allgemeinen sollten Sie das Format mit der höchsten Qualität verwenden.
5.  Legen Sie optional Attribute für den Datenstrom Deskriptor fest. Eine Liste der Attribute, die für streamdeskriptoren gelten, finden Sie unter [streamdeskriptorattribute](stream-descriptor-attributes.md).

Erstellen Sie nun den Präsentations Deskriptor:

1.  Aufrufen von [**mfkreatepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) und übergeben des Arrays der streamdeskriptoren. Die-Funktion gibt einen [**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Zeiger zurück.
2.  Wählen Sie die standardstreamauswahl aus, indem Sie [**imfpresentationdescriptor:: selectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) aufrufen, um einen oder mehrere Streams auszuwählen. In der Standardkonfiguration muss mindestens ein Stream ausgewählt werden.
3.  Legen Sie optional Attribute für den Präsentations Deskriptor fest. Eine Liste der Attribute, die für streamdeskriptoren gelten, finden Sie unter [Präsentations deskriptorattribute](presentation-descriptor-attributes.md).

Sie sollten den Präsentations Deskriptor einmal erstellen, entweder beim Start oder nachdem die Quelle genug Quelldaten analysiert hat, um den Inhalt zu ermitteln. Die Methode " [**kreatepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) " sollte eine Kopie des Präsentations Deskriptors zurückgeben. Rufen Sie zum Erstellen der Kopie [**imfpresentationdescriptor:: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone)auf. Durch das Zurückgeben einer Kopie wird verhindert, dass der Client den Status des ursprünglichen Präsentations Deskriptors ändert, z. b. die Attribute oder die Datenstrom Auswahl. Beachten Sie jedoch, dass der **Klon** eine flache Kopie erstellt, sodass der Client die zugrunde liegenden streamdeskriptoren potenziell ändern kann.

## <a name="starting-the-media-source"></a>Starten der Medienquelle

Die [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode startet die Medienquelle oder sucht an einer neuen Position. Ein Aufruf von **Start** bewirkt eine *Suche* , wenn der vorherige Zustand entweder angehalten oder ausgeführt wurde und eine neue Startzeit angegeben wird. Andernfalls verursacht die **Start** -Methode einen *Start* Vorgang. Wenn der **Start** Vorgang abgeschlossen ist, senden Sie die folgenden Ereignisse.

1.  Senden Sie ein [menewstream](menewstream.md) -Ereignis für jeden neuen Stream – d. h. jeden Datenstrom, der zuvor deaktiviert wurde und nun ausgewählt ist. Bei den Ereignisdaten handelt es sich um einen Zeiger auf den Stream.
2.  Senden Sie ein [meupdatedstream](meupdatedstream.md) -Ereignis für jeden Datenstrom, der zuvor ausgewählt wurde und noch ausgewählt ist. Bei den Ereignisdaten handelt es sich um einen Zeiger auf den Stream. (Senden Sie kein Ereignis für nicht ausgewählte Streams.)
3.  Wenn die Quelle sucht, senden Sie ein [mesourceseeked](mesourceseeked.md) -Ereignis. Andernfalls wird ein [mesourcestarted](mesourcestarted.md) -Ereignis gesendet. Bei den Ereignisdaten handelt es sich um die Startzeit, die in der [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode angegeben wurde. Legen Sie für das mesourcestarted-Ereignis, wenn die Startzeit VT \_ leer ist, das [**\_ \_ \_ tatsächliche \_ Start**](mf-event-source-actual-start-attribute.md) -Attribut der MF-Ereignis Quelle für das Ereignis fest. Der Attribut Wert ist die tatsächliche Startzeit.
4.  Senden Sie für jeden Stream, wenn die Quelle sucht, ein [mestreamseeked](mestreamseeked.md) -Ereignis. Andernfalls senden Sie ein [mestreamstarted](mestreamstarted.md) -Ereignis. Die Ereignisdaten sind die Startzeit. (Die Medienquelle kann ein Ereignis im Stream durch Aufrufen der [**imfmediaeventgenerator:: queueevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent) -Methode des Streams in die Warteschlange stellen.)

Wenn ein Datenstrom deaktiviert wird, fahren Sie den Datenstrom herunter. Der Stream sollte an diesem Punkt keine weiteren Ereignisse in die Warteschlange stellen.

Das Zeitformat für die [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) Methode wird im *pguidtimeformat* -Parameter angegeben. Das Standardzeit Format (angegeben durch **GUID \_ null**) ist 100-Nanosecond-Einheiten. Eine Medienquelle muss dieses Zeitformat unterstützen.

### <a name="seeking"></a>Diejenigen

Bei der Suche wird die angeforderte Anfangsposition möglicherweise nicht auf eine exakte Stichproben Grenze zurückgegriffen. Außerdem kann die Startposition für komprimierten Inhalt zwischen Keyframes liegen. Ein Datenstrom sollte Beispiele aus dem frühesten Punkt liefern, der erforderlich ist, um ein unkomprimiertes Beispiel an der angeforderten Startposition zu liefern. Für Video bedeutet das, dass Sie mit dem vorherigen Keyframe beginnen. Die Pipeline ist dafür verantwortlich, die zusätzlichen Frames aus dem Decoder abzulegen, sodass die Wiedergabe zum angeforderten Zeitpunkt beginnt.

Die in den Quell Ereignissen angegebene Startzeit ([mesourcestarted](mesourcestarted.md), [mesourceseeked](mesourceseeked.md), [mestreamstarted](mestreamstarted.md)und [mestreamseeked](mestreamseeked.md)) ist die angeforderte Startzeit (der Wert, der in der [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) Methode angegeben ist), unabhängig von der tatsächlichen Startposition.

Nehmen wir beispielsweise an, dass die ersten Frames eines Videodaten Stroms die folgenden Eigenschaften aufweisen:



| Beispiel     | 1       | 2       | 3        | 4        |
|------------|---------|---------|----------|----------|
| Time       | 33 MS | 66 MS | 100 MS | 133 MS |
| Keyframe? | Ja     | Nein      | Nein       | Ja      |



 

Wenn die [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode mit einem Wert von 100 Millisekunden aufgerufen wird, muss die Quelle Videos aus dem Frame 1, dem ersten Keyframe vor diesem Zeitpunkt, ausgeben. Das Start Ereignis gibt weiterhin 100 Millisekunden in den Ereignisdaten an.

## <a name="pausing-the-media-source"></a>Anhalten der Medienquelle

Die [**imfmediasource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) -Methode hält die Medienquelle an.

Während die Quelle angehalten ist, kann ein Stream neue Beispiele erstellen und diese in einer Warteschlange speichern, aber der Stream liefert die Beispiele nicht. Hier sind einige Ausnahmen zu dieser Regel:

-   Live Quellen sollten Daten bei angehaltenen Daten löschen.
-   Wenn die Quelle Daten aus einem Netzwerk abruft, wird der Server möglicherweise angehalten.

Wenn der Client [**IMF Mediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) aufruft, während die Quelle angehalten ist, wird die Anforderung auch in die Warteschlange eingereiht, bis die Quelle erneut gestartet wird. Anforderungen dürfen nicht gelöscht werden.

Das Anhalten ist nur im Zustand "gestartet" zulässig. Andernfalls sollte die [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) einen **\_ \_ ungültigen \_ Status \_ Übergang von MF E** zurückgeben.

## <a name="generating-source-data"></a>Quelldaten werden erzeugt.

Media Foundation verwendet ein *Pull-Modell*, d. h., dass Streams als Reaktion auf Anforderungen von der Pipeline Stichproben generieren und bereitstellt. Ein Datenstrom kann Beispiele liefern, wenn die Medienquelle ausgeführt wird und der Stream ausgewählt ist. Ein Datenstrom liefert nur Daten, wenn der Client ein neues Beispiel anfordert.

### <a name="sample-requests"></a>Beispielanforderungen

Der Client fordert ein neues Beispiel durch Aufrufen von [**imfmediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)an. Dies ist die Abfolge der Vorgänge:

1.  Der Client ruft [**IMF Mediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)auf. Das-Argument ist ein Zeiger auf ein optionales *Tokenobjekt* , das der Client zum Nachverfolgen der Anforderung verwendet. Der Client implementiert das Token. Token müssen die **IUnknown** -Schnittstelle verfügbar machen. Der Client kann auch einen NULL-Zeiger anstelle eines Tokens übergeben.
2.  Wenn der Client ein Token bereitgestellt hat, ruft der Medienstrom die **adressf** für das Token auf und platziert das Token in einer First-in-First-Out-Warteschlange. Die-Methode gibt zurück, und die restlichen Schritte werden asynchron ausgeführt.

3.  Wenn weitere Daten verfügbar sind, erstellt der Mediendaten Strom ein neues Beispiel. (Dieser Schritt wird im nächsten Abschnitt ausführlicher beschrieben.)
4.  Der Mediendaten Strom Ruft das erste Token aus der Warteschlange ab.
5.  Wenn das Token nicht **null** ist, legt der Medienstrom das [**MF SampleExtension- \_ tokenattribut**](mfsampleextension-token-attribute.md) für das Medien Beispiel fest. Der Wert des-Attributs ist ein Zeiger auf das Token.
6.  Der Mediendaten Strom sendet ein [memediasample](memediasample.md) -Ereignis. Die Ereignisdaten sind ein Zeiger auf die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle des Beispiels.
7.  Wenn der Client ein Token bereitgestellt hat, ruft der Medienstrom die **Freigabe** für das Tokenobjekt auf.

Wenn der Mediendaten Strom die [**requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Anforderung des Clients nicht erfüllen kann, ruft er das Token aus der Warteschlange ab und ruft die **Freigabe** für das Token auf, sendet jedoch kein [memediasample](memediasample.md) -Ereignis.

Der Client kann das Token verwenden, um den Status der Anforderung zu überprüfen. Wenn der Client das [memediasample](memediasample.md) -Ereignis empfängt, kann er das Token aus dem Beispiel erhalten und mit der ursprünglichen Anforderung vergleichen. Der Client kann auch das Token verwenden, um zu ermitteln, ob die Medienquelle die Anforderung gelöscht hat. Wenn der Verweis Zähler des Tokens auf Null fällt und der Mediendaten Strom kein memediasample-Ereignis sendet, bedeutet dies, dass die Anforderung gelöscht wurde.

In den folgenden Schritten wird davon ausgegangen, dass die [**requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode als asynchroner Vorgang implementiert ist. Wenn die Methode synchron ist, müssen Sie das Anforderungs Token nicht in eine Warteschlange einfügen. Wenn das Erstellen von Daten eine beträchtliche Zeitspanne benötigt, wird jedoch ein asynchroner Ansatz empfohlen – beispielsweise, wenn die Quelle Daten aus einem Bytestream liest.

Der Stream ist für das Puffern von Daten verantwortlich, die zwischen Aufrufen von [**requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)akkumuliert werden.

Wenn der Mediendaten Strom das Ende des Streams erreicht, sendet er ein [meendof Stream](meendofstream.md) -Ereignis nach dem letzten Beispiel. Nachdem jeder Stream beendet wurde, sendet die Medienquelle ein [meendof Presentation](meendofpresentation.md) -Ereignis. Nachdem ein Mediendaten Strom das meendof Stream-Ereignis gesendet hat, gibt die [**requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode das **\_ \_ Ende \_ des Daten \_ Stroms von MF E** zurück, bis die Quelle neu gestartet wird.

### <a name="allocating-samples"></a>Zuordnen von Beispielen

Wenn der Stream zum Ausfüllen einer ausstehenden Beispiel Anforderung bereit ist, wird ein neues Beispiel erstellt, dem ein oder mehrere Medien Puffer hinzugefügt werden. Weitere Informationen zum Erstellen von Medien Puffern finden Sie unter [Medien Puffer](media-buffers.md).

Der Stream muss den Zeitstempel und die Dauer, sofern bekannt, festlegen. Der Zeitstempel ist relativ zur Quelle. In den meisten Fällen entspricht der Anfang des Inhalts einem Zeitstempel von NULL. Wenn die Quelle beispielsweise aus einer Mediendatei liest, hat der Start der Datei den Zeitstempel NULL.

Der Zeitstempel im Beispiel entspricht nicht notwendigerweise der Präsentationszeit. Die Medien Sitzung wird aus der Quell Zeit in die Präsentationszeit übersetzt. Bei komprimierten Daten sollte der Stream Daten generieren, beginnend mit dem nächsten Keyframe vor der Startzeit. Dadurch kann der Decoder den Frame übermitteln, der zum angeforderten Startzeitpunkt angezeigt wird. (Andernfalls muss der Decoder bis zum folgenden Keyframe warten.)

Wenn die Wiedergabe Rate schneller oder langsamer als 1,0 ist, passt die Pipeline die Rate der Präsentations Uhr an. Die Quelle passt die Zeitstempel für Stichproben nicht an.

Die Quelle kann zusätzliche Informationen über das Beispiel festlegen, indem Attribute festgelegt werden. Eine Liste der Beispiel Attribute finden Sie unter [Beispiel Attribute](sample-attributes.md).

### <a name="gaps-in-the-stream"></a>Lücken im Stream

Wenn ein Datenstrom eine Lücke mit signifikanter Länge aufweist, wird empfohlen, dass der Stream ein [mestreamtick](mestreamtick.md) -Ereignis sendet. Dieses Ereignis benachrichtigt den Client, dass ein Beispiel fehlt. Bei den Ereignisdaten handelt es sich um den Zeitstempel des fehlenden Beispiels in 100-Nanosecond-Einheiten (**VT \_ I8**). Dieses Ereignis kann dazu führt, dass Downstreamkomponenten auf nicht eingehende Beispiele warten. Der Stream kann beliebig viele mestreamtick-Ereignisse senden, um die Lücke im Stream zu überspannen.

## <a name="shutting-down-the-media-source"></a>Die Medienquelle wird heruntergefahren.

Wenn der Client mithilfe der Medienquelle ausgeführt wird, wird [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)aufgerufen. Innerhalb dieser Methode sollte die Medienquelle alle Zirkel Verweis Zählungen unterbrechen. In der Regel gibt es zirkuläre Verweise zwischen der Medienquelle und den Mediendaten strömen.

Wenn Sie [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)mithilfe der Ereignis Warteschlange implementieren, müssen Sie [**imfmediaeventqueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) für die Ereignis Warteschlange abrufen. Diese Methode beendet die Ereignis Warteschlange und signalisiert jedem Aufrufer, der zurzeit auf ein Ereignis wartet.

Nach dem Herunterfahren geben alle Methoden der Quelle **das \_ \_ Herunterfahren von MF E** zurück, mit Ausnahme von **IUnknown** -Methoden.

## <a name="live-sources"></a>Live Quellen

Ab Windows 7 werden von Media Foundation automatisch Audiogeräte und Video Erfassungsgeräte unterstützt. Für das Video muss das Gerät in der Kategorie Video Erfassung einen "Kernel Streaming"-Mini Treiber ("") bereitstellen. Media Foundation verwendet den PNP-Pfad zum Aufzählen des Geräts. Für Audiodaten verwendet Media Foundation die Windows-Multimedia-Geräte-API (mmdevice), um audioendpunktgeräte aufzuzählen. Wenn das Gerät diese Kriterien erfüllt, muss keine benutzerdefinierte Medienquelle implementiert werden.

Möglicherweise möchten Sie jedoch eine benutzerdefinierte Medienquelle für einen anderen Gerätetyp oder eine andere Live Datenquelle implementieren. Es gibt nur wenige Unterschiede zwischen einer Live Quelle und anderen Medienquellen:

-   Geben Sie in der [**imfmediasource:: getcharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics) -Methode das Flag " **mfmediasource \_ is \_ Live** " zurück.
-   Das erste Beispiel sollte einen Zeitstempel von NULL aufweisen.
-   Ereignisse und streamingzustände werden wie Medienquellen behandelt, mit Ausnahme des angehaltenen Zustands.
-   Bei angehaltenen Warteschlangen nicht in die Warteschlange. Löschen Sie alle Daten, die während der Unterbrechung generiert werden.
-   Live Quellen unterstützen in der Regel nicht das suchen, umkehren von spielen oder Raten Kontrolle.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienquellen](media-sources.md)
</dt> <dt>

[Tutorial: Schreiben einer benutzerdefinierten Medienquelle](tutorial--writing-a-custom-media-source.md)
</dt> </dl>

 

 



