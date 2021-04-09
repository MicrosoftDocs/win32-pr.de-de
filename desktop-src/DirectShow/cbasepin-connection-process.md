---
description: Cbasepin-Verbindungsprozess
ms.assetid: 4b3a9023-0267-4caa-9d89-88237009df05
title: Cbasepin-Verbindungsprozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1441b0daba58857e00da0139d3312fb277287fc2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957891"
---
# <a name="cbasepin-connection-process"></a>Cbasepin-Verbindungsprozess

In diesem Abschnitt wird beschrieben, wie die [**cbasepin**](cbasepin.md) -Klasse den PIN-Verbindungsprozess implementiert.

Der Filter Graph-Manager initiiert alle Pin-Verbindungen. Sie ruft die [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) -Methode der Ausgabe-PIN auf, wobei die Eingabe-PIN angegeben wird. Die Ausgabe-PIN schließt die Verbindung ab, indem die [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) -Methode der Eingabe-PIN aufgerufen wird. Die Eingabe-PIN kann die Verbindung akzeptieren oder ablehnen.

Der Filter Graph-Manager kann auch einen Medientyp für die Verbindung angeben. Wenn dies der Fall ist, versuchen die Pins, eine Verbindung mit diesem Typ herzustellen. Andernfalls müssen die Pins den Typ aushandeln. Der Filter Graph-Manager kann auch einen *partiellen* Medientyp angeben, der den Wert GUID \_ NULL für den Haupttyp, den Untertyp oder den Formattyp aufweist. In diesem Fall versuchen die Pins, die jeweiligen Teile des Medientyps abzugleichen. der Wert GUID \_ Null fungiert als Platzhalter.

Die [**cbasepin:: Connect**](cbasepin-connect.md) -Methode wird gestartet, indem überprüft wird, ob die PIN eine Verbindung annehmen kann. Beispielsweise wird überprüft, ob die PIN bereits verbunden ist. Der Rest des Verbindungsprozesses wird an die [**cbasepin:: agreemediatype**](cbasepin-agreemediatype.md) -Methode delegiert. Alles, was folgt, wird von **agreemediatype** ausgeführt.

Wenn der Medientyp vollständig angegeben ist, ruft die PIN die [**cbasepin::**](cbasepin-attemptconnection.md) der Connection-Methode auf, um die Verbindung herzustellen. Andernfalls werden Medientypen in der folgenden Reihenfolge ausprobiert:

1.  Die bevorzugten Typen der Eingabe-PIN.
2.  Die bevorzugten Typen der Ausgabepin.

Sie können diese Reihenfolge umkehren, indem Sie das [**cbasepin:: m \_ btrymytypesfirst**](cbasepin-m-btrymytypesfirst.md) -Flag auf " **true**" festlegen.

In jedem Fall ruft die PIN [**IPin:: enummediatypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) auf, um die Medientypen aufzuzählen. Diese Methode ruft ein Enumeratorobjekt ab, das an die [**cbasepin:: trymediatypes**](cbasepin-trymediatypes.md) -Methode übergeben wird. Die **trymediatypes** -Methode durchläuft jeden Medientyp und ruft "Try- [**Connection**](cbasepin-attemptconnection.md) " für jeden Typ auf.

In der [**Methode "**](cbasepin-attemptconnection.md) Methode" wird die Ausgabe-PIN die folgenden Methoden aufrufen:

-   [**Cbasepin:: checkConnect**](cbasepin-checkconnect.md) wird für sich selbst aufgerufen, um zu überprüfen, ob die Eingabe-PIN geeignet ist.
-   [**Cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) wird auf sich selbst aufgerufen, um den Medientyp zu validieren.
-   Er ruft [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) für die Eingabe-PIN auf. Die Eingabe-PIN verwendet diese Methode, um zu bestimmen, ob die Verbindung akzeptiert werden soll.
-   [**Cbasepin:: completeconnect**](cbasepin-completeconnect.md) wird für sich selbst aufgerufen, um die Verbindung fertigzustellen.

Beachten Sie Folgendes:

-   [**CheckConnect**](cbasepin-checkconnect.md) ist eine virtuelle Methode. In der Basisklasse überprüft diese Methode, ob die PIN-Anweisungen kompatibel sind. Ausgabe Pins müssen mit Eingabe-Pins verbunden werden und umgekehrt. Die abgeleitete Pin-Klasse überschreibt diese Methode in der Regel, um andere Überprüfungen auszuführen. Beispielsweise kann die andere PIN nach einer Schnittstelle abgefragt werden, die für die Verbindung erforderlich ist. Wenn die abgeleitete Klasse **checkConnect** überschreibt, sollte Sie auch die [**cbasepin**](cbasepin.md) -Methode aufzurufen.
-   [**Checkmediatype**](cbasepin-checkmediatype.md) ist eine rein virtuelle Methode, die von der abgeleiteten Klasse implementiert werden muss.
-   [**Completeconnect**](cbasepin-completeconnect.md) ist eine virtuelle Methode, die in der Basisklasse nichts bewirkt. Abgeleitete Klassen können diese Methode überschreiben, um zusätzliche Aufgaben auszuführen, die zum Abschluss der Verbindung erforderlich sind, z. b. die Entscheidung für eine Speicherzuweisung.

Wenn einer dieser Schritte fehlschlägt, ruft die Ausgabepin die [**cbasepin:: breakconnect**](cbasepin-breakconnect.md) -Methode auf, um die von [**checkConnect**](cbasepin-checkconnect.md)ausgeführten Schritte rückgängig zu machen.

Die [**receiveconnection**](cbasepin-receiveconnection.md) -Methode der Eingabe-PIN Ruft die Methoden [**checkConnect**](cbasepin-checkconnect.md), [**checkmediatype**](cbasepin-checkmediatype.md)und [**completeconnect**](cbasepin-completeconnect.md) der Eingabe-PIN auf. Wenn einer dieser Fehler ausfällt, tritt beim Verbindungsversuch ebenfalls ein Fehler auf.

Das folgende Diagramm zeigt den Verbindungsprozess in [**cbasepin**](cbasepin.md):

![cbasepin-Verbindungsprozess](images/cbasepin-connect.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cbasepin**](cbasepin.md)
</dt> </dl>

 

 



