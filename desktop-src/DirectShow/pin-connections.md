---
description: PIN-Verbindungen
ms.assetid: 1406ade4-77d8-49a7-8f36-cc49ff007a26
title: PIN-Verbindungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b509abddf4a915b65dfd322f76b4afb132a7f835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392506"
---
# <a name="pin-connections"></a>PIN-Verbindungen

Filter verbinden sich über die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle an Ihren Pins. Ausgabe Pins stellen eine Verbindung mit Eingabe-Pins her. Jede Pin-Verbindung weist einen Medientyp auf, der von der [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur beschrieben wird.

Eine Anwendung verbindet Filter durch Aufrufen von Methoden für den Filter Graph-Manager, nie durch Aufrufen von Methoden für die Filter oder Pins selbst. Die Anwendung kann direkt angeben, welche Filter zum Verbinden verwendet werden sollen, indem Sie die [**ifiltergraph:: connectdirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) -Methode oder die [**igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) -Methode aufrufen. Sie können Filter auch indirekt verbinden, indem Sie eine Graph-Erstellungs Methode wie z. b. [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)verwenden.

Damit die Verbindung erfolgreich hergestellt werden kann, müssen sich beide Filter im Filter Diagramm befinden. Die Anwendung kann dem Diagramm einen Filter hinzufügen, indem Sie die [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) -Methode aufrufen. Der Filter Graph-Manager kann dem Diagramm ebenfalls Filter hinzufügen. Wenn ein Filter hinzugefügt wird, ruft der Filter Graph-Manager die [**ibasefilter:: joinfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) -Methode des Filters auf, um den Filter zu benachrichtigen.

Die allgemeine Übersicht über den Verbindungsprozess lautet wie folgt:

1.  Der Filter Graph-Manager ruft [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) in der Ausgabe-PIN auf und übergibt einen Zeiger auf die Eingabe-PIN.
2.  Wenn die Ausgabe-PIN die Verbindung akzeptiert, ruft Sie [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) für die Eingabe-PIN auf.
3.  Wenn die Eingabe-PIN auch die Verbindung akzeptiert, ist der Verbindungsversuch erfolgreich, und die Pins sind verbunden.

Einige Pins können getrennt und wieder verbunden werden, während der Filter aktiv ist. Diese Art der erneuten Verbindung wird als *dynamische* erneute Verbindung bezeichnet. Weitere Informationen finden Sie unter [Dynamic Graph Building](dynamic-graph-building.md). Die meisten Filter unterstützen jedoch keine dynamische erneute Verbindung.

Filter sind normalerweise in der nachgelagerten Reihenfolge verbunden – das heißt, die Eingabe Pins des Filters sind vor den Ausgabe Pins verbunden. Ein Filter sollte immer diese Verbindungs Reihenfolge unterstützen. Einige Filter unterstützen auch Verbindungen in umgekehrter Reihenfolge – zuerst Ausgabe Pins, gefolgt von Eingabe Pins. Beispielsweise kann es möglich sein, die Ausgabe-PIN eines MUX-Filters mit dem Datei Schreiber Filter zu verbinden, bevor die Eingabe Pins des MUX-Filters verbunden werden.

Wenn die **Connect** -oder **receiveconnection** -Methode einer PIN aufgerufen wird, muss die PIN überprüfen, ob die Verbindung unterstützt werden kann. Die Details hängen vom jeweiligen Filter ab. Die häufigsten Aufgaben umfassen Folgendes:

-   Überprüfen Sie, ob der Medientyp akzeptabel ist.
-   Aushandeln einer Zuweisung
-   Fragen Sie die andere PIN nach erforderlichen Schnittstellen ab.

 

 



