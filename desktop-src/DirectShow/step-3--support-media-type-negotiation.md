---
description: 'Schritt 3:'
ms.assetid: b2b5dafc-d38d-4ec3-a390-55229495b4f9
title: 'Schritt 3: Unterstützung der Medientyp Aushandlung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3ff8539d0d7de2c9b7300ddb90ad86ca471710
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869508"
---
# <a name="step-3-support-media-type-negotiation"></a>Schritt 3: Unterstützung der Medientyp Aushandlung

Dies ist Schritt 3 des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).

Wenn zwei Pins eine Verbindung herstellen, müssen Sie einem Medientyp für die Verbindung zustimmen. Der Medientyp beschreibt das Format der Daten. Ohne den Medientyp stellt ein Filter möglicherweise eine Art von Daten bereit, sodass er nur von einem anderen Filter als etwas anderes behandelt werden kann.

Der grundlegende Mechanismus für das Aushandeln von Medientypen ist die [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) -Methode. Die Ausgabe-PIN ruft diese Methode für die Eingabe-PIN mit einem vorgeschlagenen Medientyp auf. Die Eingabe-PIN akzeptiert die Verbindung oder lehnt sie ab. Wenn die Verbindung abgelehnt wird, kann die Ausgabe-PIN einen anderen Medientyp ausprobieren. Wenn keine geeigneten Typen gefunden werden, tritt bei der Verbindung ein Fehler auf. Optional kann die Eingabe-PIN über die [**IPin:: enummediatypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) -Methode eine Liste der von ihr bevorzugten Typen ankündigen. Die Ausgabepin kann diese Liste verwenden, wenn Sie Medientypen vorschlägt, obwohl dies nicht erforderlich ist.

Die **ctransformfilter** -Klasse implementiert wie folgt ein allgemeines Framework für diesen Prozess:

-   Die eingabepin weist keine bevorzugten Medientypen auf. Er basiert ausschließlich auf dem Upstream-Filter, um den Medientyp vorzuschlagen. Für Videodaten ist dies sinnvoll, da der Medientyp die Bildgröße und die Framerate enthält. Normalerweise müssen diese Informationen von einem Upstream-Quell Filter oder Parserfilter bereitgestellt werden. Im Fall von Audiodaten ist der Satz möglicher Formate kleiner, sodass es für die Eingabe-PIN möglicherweise sinnvoll ist, einige bevorzugte Typen anzubieten. Überschreiben Sie in diesem Fall [**cbasepin:: getmediatype**](cbasepin-getmediatype.md) in der Eingabe-PIN.
-   Wenn der upstreamfilter einen Medientyp vorschlägt, ruft die Eingabe-PIN die [**ctransformfilter:: checkinputtype**](ctransformfilter-checkinputtype.md) -Methode auf, die den Typ akzeptiert oder ablehnt.
-   Die Ausgabe-PIN wird nur dann verbunden, wenn die Eingabe-PIN zuerst verbunden ist. Dieses Verhalten ist für Transformations Filter typisch. In den meisten Fällen muss der Filter den Eingabetyp bestimmen, bevor der Ausgabetyp festgelegt werden kann.
-   Wenn die Ausgabe-PIN eine Verbindung herstellt, enthält Sie eine Liste der Medientypen, die Sie dem downstreamfilter vorschlägt. Sie ruft die [**ctransformfilter:: getmediatype**](ctransformfilter-getmediatype.md) -Methode auf, um diese Liste zu generieren. Mit der Ausgabe-PIN werden auch alle Medientypen ausprobiert, die vom downstreamfilter vorgeschlagen werden.
-   Um zu überprüfen, ob ein bestimmter Ausgabetyp mit dem Eingabetyp kompatibel ist, ruft die Ausgabe-PIN die [**ctransformfilter:: checktransform**](ctransformfilter-checktransform.md) -Methode auf.

Die drei oben aufgeführten **ctransformfilter** -Methoden sind reine virtuelle Methoden, sodass Sie von ihrer abgeleiteten Klasse implementiert werden müssen. Keine dieser Methoden gehört zu einer COM-Schnittstelle. Sie sind einfach Teil der Implementierung, die von den Basisklassen bereitgestellt wird.

In den folgenden Abschnitten werden die einzelnen Methoden ausführlicher beschrieben:

-   [Schritt 3a. Implementieren der checkinputtype-Methode](step-3a--implement-the-checkinputtype-method.md)
-   [Schritt 3B. Implementieren der getmediatype-Methode](step-3b--implement-the-getmediatype-method.md)
-   [Schritt 3C: Implementieren der checktransform-Methode](step-3c--implement-the-checktransform-method.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen der Verbindung von Filtern](how-filters-connect.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



