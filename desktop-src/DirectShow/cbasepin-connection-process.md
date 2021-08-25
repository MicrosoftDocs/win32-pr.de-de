---
description: CBasePin-Verbindungsprozess
ms.assetid: 4b3a9023-0267-4caa-9d89-88237009df05
title: CBasePin-Verbindungsprozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6134c9094e00ea43c5e4bb9f92c9132287fab3c16f98d56497affc8c1015bd6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916785"
---
# <a name="cbasepin-connection-process"></a>CBasePin-Verbindungsprozess

In diesem Abschnitt wird beschrieben, wie die [**CBasePin-Klasse**](cbasepin.md) den Pinverbindungsprozess implementiert.

Der Filter-Graph-Manager initiiert alle Pinverbindungen. Sie ruft die [**IPin::Verbinden-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) des Ausgabepins auf und gibt den Eingabepin an. Der Ausgabepin schließt die Verbindung ab, indem die [**IPin::ReceiveConnection-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) des Eingabepins aufgerufen wird. Der Eingabepin kann die Verbindung akzeptieren oder ablehnen.

Der Filter-Graph-Manager kann auch einen Medientyp für die Verbindung angeben. Wenn ja, versuchen die Pins, eine Verbindung mit diesem Typ herzustellen. Falls nicht, müssen die Pins den Typ aushandeln. Der Filter-Graph-Manager kann auch einen *partiellen* Medientyp angeben, der den Wert GUID \_ NULL für den Haupttyp, Untertyp oder Formattyp hat. In diesem Fall versuchen die Pins, mit den angegebenen Teilen des Medientyps übereinzugleichen. der Wert GUID \_ NULL fungiert als Platzhalter.

Die [**CBasePin::Verbinden-Methode**](cbasepin-connect.md) beginnt mit der Überprüfung, ob der Pin eine Verbindung akzeptieren kann. Beispielsweise wird überprüft, ob der Stecknadel nicht bereits verbunden ist. Der Rest des Verbindungsprozesses wird an die [**CBasePin::AgreeMediaType-Methode**](cbasepin-agreemediatype.md) delegiert. Alles, was folgt, wird von **AgreeMediaType** ausgeführt.

Wenn der Medientyp vollständig angegeben ist, ruft der Pin die [**CBasePin::AttemptConnection-Methode**](cbasepin-attemptconnection.md) auf, um die Verbindung herzustellen. Andernfalls werden Medientypen in der folgenden Reihenfolge versucht:

1.  Die bevorzugten Typen des Eingabepins.
2.  Die bevorzugten Typen des Ausgabepins.

Sie können diese Reihenfolge umkehren, indem Sie das [**Flag CBasePin::m \_ bTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md) auf **TRUE** festlegen.

In jedem Fall ruft der Pin [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) auf, um die Medientypen aufzuzählen. Diese Methode ruft ein Enumeratorobjekt ab, das an die [**CBasePin::TryMediaTypes-Methode**](cbasepin-trymediatypes.md) übergeben wird. Die **TryMediaTypes-Methode** durchläuft jeden Medientyp und ruft [**AttemptConnection**](cbasepin-attemptconnection.md) für jeden Typ auf.

Innerhalb der [**AttemptConnection-Methode**](cbasepin-attemptconnection.md) ruft der Ausgabepin die folgenden Methoden auf:

-   Sie ruft [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) für sich selbst auf, um zu überprüfen, ob der Eingabepin geeignet ist.
-   Sie ruft [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) für sich selbst auf, um den Medientyp zu überprüfen.
-   Sie ruft [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) auf dem Eingabepin auf. Der Eingabepin verwendet diese Methode, um zu bestimmen, ob die Verbindung akzeptiert werden soll.
-   Sie ruft [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) für sich selbst auf, um die Verbindung abzuschließen.

Beachten Sie Folgendes:

-   [**CheckConnect**](cbasepin-checkconnect.md) ist eine virtuelle Methode. In der Basisklasse überprüft diese Methode, ob die Stecknadelrichtungen kompatibel sind. Ausgabepins müssen eine Verbindung mit Eingabepins herstellen und umgekehrt. Die abgeleitete Pin-Klasse überschreibt diese Methode in der Regel, um andere Überprüfungen durchzuführen. Beispielsweise kann der andere Pin nach einer Schnittstelle abgefragt werden, die für die Verbindung erforderlich ist. Wenn die abgeleitete Klasse **CheckConnect** überschreibt, sollte sie auch die [**CBasePin-Methode**](cbasepin.md) aufrufen.
-   [**CheckMediaType**](cbasepin-checkmediatype.md) ist eine reine virtuelle Methode, die von der abgeleiteten Klasse implementiert werden muss.
-   [**CompleteConnect**](cbasepin-completeconnect.md) ist eine virtuelle Methode, die in der Basisklasse nichts tut. Abgeleitete Klassen können diese Methode überschreiben, um alle zusätzlichen Aufgaben auszuführen, die zum Abschließen der Verbindung erforderlich sind, z. B. die Entscheidung für eine Speicherzuweisung.

Wenn einer dieser Schritte fehlschlägt, ruft der Ausgabepin die [**CBasePin::BreakConnect-Methode**](cbasepin-breakconnect.md) auf, um alle Schritte rückgängig zu machen, die von [**CheckConnect**](cbasepin-checkconnect.md)ausgeführt wurden.

Die [**ReceiveConnection-Methode**](cbasepin-receiveconnection.md) des Eingabepins ruft die [**Methoden CheckConnect,**](cbasepin-checkconnect.md) [**CheckMediaType**](cbasepin-checkmediatype.md)und [**CompleteConnect**](cbasepin-completeconnect.md) des Eingabepins auf. Wenn einer dieser Fehler auftritt, schlägt der Verbindungsversuch ebenfalls fehl.

Das folgende Diagramm zeigt den Verbindungsprozess in [**CBasePin:**](cbasepin.md)

![cbasepin-Verbindungsprozess](images/cbasepin-connect.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



