---
description: Informationen zu MFTs
ms.assetid: ca9cef70-b897-4fd5-9a13-8bf1c2b84b00
title: Informationen zu MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09adce4bc93c110cf98e4fd8ed427ffcd009c3c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862755"
---
# <a name="about-mfts"></a>Informationen zu MFTs

Media Foundation Transformationen (MFTs) stellen ein generisches Modell zum Verarbeiten von Mediendaten bereit. MFTs werden für Decoders, Encoder und digitale Signalprozessoren (DSPs) verwendet. Kurz gesagt: alles, was sich in der Medien Pipeline zwischen der Medienquelle und der Medien Senke befindet, ist eine MFT.

Bei den meisten Anwendungen werden die Details der MFT-Datenverarbeitung durch höhere Ebenen der Media Foundation Architektur ausgeblendet. Viele Media Foundation Anwendungen führen niemals einen direkten Rückruf an eine MFT aus. Es ist jedoch sicherlich möglich, eine MFT direkt in Ihrer Anwendung zu hosten.

MFTs sind eine Weiterentwicklung des Transformations Modells, das zuerst mit DirectX Media Objects (DMOs) eingeführt wurde. Tatsächlich ist es relativ einfach, eine Transformation zu erstellen, die beide Modelle unterstützt. Im Vergleich zu DMOS werden die erforderlichen Verhalten von MFTs eindeutiger festgelegt, sodass es einfacher ist, eine korrekte Implementierung zu schreiben. Darüber hinaus kann MFTs die hardwarebeschleunigte Videoverarbeitung unterstützen.

Dieses Thema enthält eine kurze Übersicht über das MFT-Verarbeitungsmodell, das sich auf den Gesamtentwurf und nicht auf bestimmte Methodenaufrufe konzentriert. Eine ausführlichere Schritt-für-Schritt-Beschreibung finden Sie unter [Grundlegendes MFT-Verarbeitungsmodell](basic-mft-processing-model.md).

## <a name="streams"></a>Datenströme

Ein MFT verfügt über Eingabestreams und Ausgabedaten Ströme. Eingabestreams empfangen Daten, und Ausgabedaten Ströme liefern Daten. Ein Decoder verfügt z. b. über einen Eingabestream, der die codierten Daten empfängt, und einen Ausgabestream, der die decodierten Daten erzeugt.

Die Streams in einer MFT werden nicht als eindeutige com-Objekte dargestellt. Stattdessen hat jeder Stream einen bestimmten Datenstrom Bezeichner, und die Methoden in der [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle übernehmen Datenstrom-IDs als Eingabeparameter.

Einige MFTs verfügen über eine bestimmte Anzahl von Streams. Decoder und Encoder haben beispielsweise normalerweise genau eine Eingabe und eine Ausgabe. Andere MFTs verfügen über eine dynamische Anzahl von Streams. Wenn eine MFT dynamische Streams unterstützt, kann der Client neue Eingabedaten Ströme hinzufügen. Der Client kann keine Ausgabedaten Ströme hinzufügen, aber der MFT kann während der Verarbeitung Ausgabedaten Ströme hinzufügen oder entfernen. Multiplexers (gestatten z. b. normalerweise dem Client das Hinzufügen von Eingabedaten strömen und eine Ausgabe für den Multiplex-Stream. Demultiplexers sind umgekehrt, mit einer Eingabe, aber mit einer dynamischen Anzahl von Ausgabestreams, abhängig vom Inhalt des Eingabestreams. Die folgende Abbildung zeigt den Unterschied zwischen Multiplexer und Demultiplexer.

![Diagramm mit einem Encoder/Decoder (1 Eingabe, 1 Ausgabe), einem Multiplexer (2 Eingaben, 1 Ausgabe) und einem Demultiplexer (1 Eingabe, 2 Ausgaben)](images/f2b95bd5-f862-4d66-9d75-550a90f6cc97.gif)

## <a name="media-types"></a>Medientypen

Wenn eine MFT erstmalig erstellt wird, hat keines der Streams ein festgelegtes Format. Bevor die MFT Daten verarbeiten kann, muss der Client die Formate für die Streams festlegen. Bei einem Decoder ist das Eingabeformat beispielsweise das in der ursprünglichen Quelldatei verwendete Komprimierungs Format, und das Ausgabeformat ist ein unkomprimiertes Format, z. b. PCM-Audiodaten oder RGB-Video. Die Datenstrom Formate werden mithilfe von [Medientypen](media-types.md)beschrieben.

Abhängig vom internen Status der MFT kann eine Liste möglicher Medientypen für jeden Stream bereitgestellt werden. Sie können diese Liste als Hinweis verwenden, wenn Sie die Medientypen festlegen. Wenn Sie den Medientyp für einen Stream festlegen, kann die Liste der möglichen Typen für einen anderen Stream geändert werden. Ein Decoder kann z. b. normalerweise keine Ausgabetypen bereitstellen, bis der Client den Eingabetyp festlegt. Der Eingabetyp enthält die Informationen, die der Decoder benötigt, um eine Liste möglicher Ausgabetypen zurückzugeben.

Um den Medientyp für einen Stream festzulegen, müssen Sie [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) oder [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen. Um die Liste der möglichen Medientypen für einen Stream abzurufen, nennen Sie [**imftransform:: getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) oder [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).

## <a name="processing-data"></a>Verarbeiten von Daten

Nachdem der Client die Medientypen in den Streams festgelegt hat, kann der MFT Daten verarbeiten. Um dies zu erreichen, wechselt der Client zwischen dem Bereitstellen von Eingabedaten zum MFT und dem erhalten von Ausgabedaten aus dem MFT:

-   Um Eingabedaten an die MFT zu übergeben, nennen Sie [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).
-   Rufen Sie zum Abrufen von Ausgabedaten aus dem MFT [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)auf.

Die [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) -Methode nimmt einen Zeiger auf ein vom Client zugewiesenes Medien Beispiel an. Das Medien Beispiel enthält einen oder mehrere Puffer, und jeder Puffer enthält Eingabedaten für die zu verarbeitende MFT.

Die [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode unterstützt zwei verschiedene Zuordnungs Modelle: entweder ordnet der MFT die Ausgabepuffer zu, oder der Client ordnet die Ausgabepuffer zu. Einige MFTs unterstützen beide Zuordnungs Modelle, aber es ist nicht erforderlich, dass eine MFT beide unterstützt. Beispielsweise kann es erforderlich sein, dass eine MFT den Client die Ausgabepuffer zuweist. Die [**imftransform:: getoutputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) -Methode gibt Informationen über einen Ausgabestream zurück, einschließlich des vom MFT unterstützten Zuordnungs Modells.

MFTs sind so konzipiert, dass so wenig Daten wie möglich gepuffert werden, um die Latenz in der Pipeline zu minimieren. Daher kann die MFT zu jedem beliebigen Zeitpunkt eine der folgenden Bedingungen signalisieren:

-   Der MFT erfordert mehr Eingabedaten. In diesem Zustand kann die MFT keine Ausgabe ausgeben, bis der Client mindestens einmal [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) aufruft.
-   Der MFT akzeptiert keine weiteren Eingaben, bis der Client [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) mindestens einmal aufruft.

Nehmen Sie beispielsweise an, dass Sie einen Video-Decoder zum Decodieren eines Videodaten Stroms verwenden, der eine Mischung aus Keyframes und Delta Frames enthält. Anfänglich erfordert die MFT eine Eingabe, bevor alle Frames decodiert werden können. Der Client ruft [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) auf, um den ersten Frame zu übermitteln. Angenommen, der erste Frame ist ein Delta Rahmen (im folgenden Diagramm als "P" für den vorhergesagten Frame dargestellt). Der Decoder hält in diesem Frame, aber er kann erst dann eine Ausgabe ausgeben, wenn der nächste Keyframe abgerufen wird.

![Diagramm mit dem MFT, das Eingaben benötigt und auf einen vorhergesagten Frame zeigt](images/f5a88ac6-24da-40e5-b356-649aa6f811c3.gif)

Der Client ruft weiterhin [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) auf und erreicht schließlich den nächsten Keyframe (im nächsten Diagramm als ' I ' für den Intra-Coded Frame angezeigt). Der Decoder verfügt nun über genügend Rahmen, um die Decodierung zu starten. An diesem Punkt wird die Eingabe nicht mehr akzeptiert, und der Client muss [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) zum Abrufen der decodierten Frames abrufen.

![Diagramm, das einen MFT anzeigt, der keine Eingaben annimmt und auf einen intercodierten Frame und drei vorhergesagte Frames zeigt](images/ae014a1a-9d03-4cfa-a04d-4a63bdc83f73.gif)

Der einfachste Ansatz für den Client besteht darin, einfach Aufrufe von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) und [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)zu wechseln. Ein anspruchsvollerer Algorithmus wird im Thema [Grundlegendes MFT-Verarbeitungsmodell](basic-mft-processing-model.md)beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 



