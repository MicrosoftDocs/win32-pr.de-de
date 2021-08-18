---
description: Informationen zu MFTs
ms.assetid: ca9cef70-b897-4fd5-9a13-8bf1c2b84b00
title: Informationen zu MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04bfc09cbd17e5f0810f46eb6e42b230010348e89040b3cd407e98ee069c8f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035710"
---
# <a name="about-mfts"></a>Informationen zu MFTs

Media Foundation Transformationen (MFTs) stellen ein generisches Modell für die Verarbeitung von Mediendaten bereit. MFTs werden für Decoder, Encoder und digitale Signalprozessoren (DSPs) verwendet. Kurz gesagt: Alles, was sich in der Medienpipeline zwischen der Medienquelle und der Mediensenke befindet, ist ein MFT.

Bei den meisten Anwendungen werden die Details der MFT-Datenverarbeitung durch höhere Ebenen der Media Foundation-Architektur ausgeblendet. Viele Media Foundation Anwendungen führen nie einen direkten Aufruf an einen MFT aus. Es ist jedoch sicherlich möglich, einen MFT direkt in Ihrer Anwendung zu hosten.

MFTs sind eine Weiterentwicklung des Transformationsmodells, das erstmals mit DirectX Media Objects (DMOs) eingeführt wurde. Tatsächlich ist es relativ einfach, eine Transformation zu erstellen, die beide Modelle unterstützt. Im Vergleich zu DMOs sind die erforderlichen Verhaltensweisen von MFTs eindeutiger angegeben, wodurch es einfacher ist, eine korrekte Implementierung zu schreiben. Darüber hinaus können MFTs die hardwarebeschleunigte Videoverarbeitung unterstützen.

Dieses Thema bietet eine kurze Übersicht über das MFT-Verarbeitungsmodell, wobei der Schwerpunkt auf dem Gesamtentwurf und nicht auf bestimmten Methodenaufrufen liegt. Eine ausführlichere, schrittweise Beschreibung finden Sie unter [Grundlegendes MFT-Verarbeitungsmodell.](basic-mft-processing-model.md)

## <a name="streams"></a>Datenströme

Ein MFT verfügt über Eingabe- und Ausgabestreams. Eingabestreams empfangen Daten, und Ausgabestreams erzeugen Daten. Beispielsweise verfügt ein Decoder über einen Eingabestream, der die codierten Daten empfängt, und einen Ausgabestream, der die decodierten Daten erzeugt.

Die Streams in einem MFT werden nicht als unterschiedliche COM-Objekte dargestellt. Stattdessen verfügt jeder Stream über einen bestimmten Streambezeichner, und die Methoden in der [**INTERFACESTransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) nehmen Streambezeichner als Eingabeparameter an.

Einige MFTs verfügen über eine feste Anzahl von Datenströmen. Decoder und Encoder verfügen beispielsweise normalerweise über genau eine Eingabe und eine Ausgabe. Andere MFTs verfügen über eine dynamische Anzahl von Datenströmen. Wenn ein MFT dynamische Datenströme unterstützt, kann der Client neue Eingabestreams hinzufügen. Der Client kann keine Ausgabestreams hinzufügen, aber der MFT kann während der Verarbeitung Ausgabestreams hinzufügen oder entfernen. Beispielsweise ermöglichen Multiplexer dem Client in der Regel das Hinzufügen von Eingabestreams und eine Ausgabe für den Multiplexstream. Demultiplexer sind umgekehrt, mit einer Eingabe, aber einer dynamischen Anzahl von Ausgabestreams, abhängig vom Inhalt des Eingabestreams. Die folgende Abbildung zeigt den Unterschied zwischen multiplexer und demultiplexer.

![Diagramm mit einem Encoder/Decoder (1 Eingabe, 1 Ausgabe), einem Multiplexer (2 Eingaben, 1 Ausgabe) und einem Demultiplexer (1 Eingabe, 2 Ausgaben)](images/f2b95bd5-f862-4d66-9d75-550a90f6cc97.gif)

## <a name="media-types"></a>Medientypen

Wenn ein MFT zum ersten Mal erstellt wird, hat keiner der Streams ein festgelegtes Format. Bevor der MFT Daten verarbeiten kann, muss der Client die Formate für die Streams festlegen. Bei einem Decoder ist das Eingabeformat beispielsweise das Komprimierungsformat, das in der ursprünglichen Quelldatei verwendet wird, und das Ausgabeformat ist ein unkomprimiertes Format, z. B. PCM-Audio oder RGB-Video. Die Streamformate werden mithilfe von [Medientypen](media-types.md)beschrieben.

Je nach internem Zustand des MFT kann eine Liste der möglichen Medientypen für jeden Stream angezeigt werden. Sie können diese Liste als Hinweis verwenden, wenn Sie die Medientypen festlegen. Wenn Sie den Medientyp für einen Stream festlegen, kann die Liste der möglichen Typen für einen anderen Stream geändert werden. Beispielsweise kann ein Decoder in der Regel keine Ausgabetypen bereitstellen, bis der Client den Eingabetyp festlegt. Der Eingabetyp enthält die Informationen, die der Decoder benötigt, um eine Liste möglicher Ausgabetypen zurückzugeben.

Um den Medientyp für einen Stream festzulegen, rufen Sie [**DIE NSDTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) oder [**DENTRANSTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)auf. Um die Liste der möglichen Medientypen für einen Stream abzurufen, rufen [**Sie ÜBERTRANSFORM::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) oder [**ÜBERTRANSTRANSFORM::GetOutputAvailableType auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)

## <a name="processing-data"></a>Verarbeiten von Daten

Nachdem der Client die Medientypen für die Streams festgelegt hat, kann der MFT Daten verarbeiten. Um dies zu ermöglichen, wechselt der Client zwischen der Bereitstellung von Eingabedaten für den MFT und dem Abrufen von Ausgabedaten aus dem MFT:

-   Um dem MFT Eingabedaten zu geben, rufen Sie [**ÜBERTRANSFORM::P rocessInput auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   Um Ausgabedaten aus dem MFT zu pullen, rufen Sie [**ÜBERTRANSFORM::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)auf.

Die [**ProcessInput-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) verwendet einen Zeiger auf ein vom Client zugeordnetes Medienbeispiel. Das Medienbeispiel enthält mindestens einen Puffer, und jeder Puffer enthält Eingabedaten, die der MFT verarbeiten kann.

Die [**ProcessOutput-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) unterstützt zwei verschiedene Zuordnungsmodelle: Entweder ordnet der MFT die Ausgabepuffer zu, oder der Client ordnet die Ausgabepuffer zu. Einige MFTs unterstützen beide Zuordnungsmodelle, aber es ist nicht erforderlich, dass ein MFT beide unterstützt. Beispielsweise kann ein MFT erfordern, dass der Client die Ausgabepuffer zuordnet. Die [**METHODE DERTRANSFORM::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) gibt Informationen zu einem Ausgabestream zurück, einschließlich des vom MFT unterstützten Zuordnungsmodells.

MFTs sind so konzipiert, dass so wenig Daten wie möglich gepuffert werden, um die Latenz in der Pipeline zu minimieren. Daher kann der MFT jederzeit eine der folgenden Bedingungen signalisieren:

-   Der MFT erfordert mehr Eingabedaten. In diesem Zustand kann der MFT erst dann eine Ausgabe erzeugen, wenn der Client [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) mindestens einmal aufruft.
-   Der MFT akzeptiert keine weiteren Eingaben, bis der Client [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) mindestens einmal aufruft.

Angenommen, Sie verwenden einen Videodecoder, um einen Videostream zu decodieren, der eine Mischung aus Keyframes und Deltaframes enthält. Zunächst erfordert der MFT einige Eingaben, bevor frames decodiert werden können. Der Client ruft [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) auf, um den ersten Frame zu übermitteln. Angenommen, der erste Frame ist ein Deltarahmen (im folgenden Diagramm als "P" für vorhergesagten Frame dargestellt). Der Decoder hält an diesem Frame fest, kann aber erst dann eine Ausgabe erzeugen, wenn er den nächsten Keyframe erhält.

![Diagramm, das den Diebstahl zeigt, der Eingaben erfordert, die auf einen vorhergesagten Frame zeigen](images/f5a88ac6-24da-40e5-b356-649aa6f811c3.gif)

Der Client ruft weiterhin [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) auf und erreicht schließlich den nächsten Keyframe (im nächsten Diagramm als "I" für den intra-codierten Frame dargestellt). Der Decoder verfügt nun über genügend Frames, um mit der Decodierung zu beginnen. An diesem Punkt wird die Eingabe nicht mehr akzeptiert, und der Client muss [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) aufrufen, um die decodierten Frames abzurufen.

![Diagramm, das einen Mft zeigt, der keine Eingabe akzeptiert und auf einen intra-codierten Frame und drei vorhergesagte Frames zeigt](images/ae014a1a-9d03-4cfa-a04d-4a63bdc83f73.gif)

Der einfachste Ansatz für den Client besteht darin, einfach alternative Aufrufe von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) und [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)zu verwenden. Ein komplexerer Algorithmus wird im Thema [Grundlegendes MFT-Verarbeitungsmodell](basic-mft-processing-model.md)beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 



