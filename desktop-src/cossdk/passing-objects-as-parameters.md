---
description: Übergeben von Objekten als Parameter
ms.assetid: 174847c8-4545-4f61-ae13-42bdec1405e7
title: Übergeben von Objekten als Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a58e012138bc65cec481f714ac216bb8227fb924
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524043"
---
# <a name="passing-objects-as-parameters"></a>Übergeben von Objekten als Parameter

Der Dienst "com+-Warteschlangen Komponenten" ermöglicht keine Warteschlangen für jede vorhandene COM-Komponente. Es gibt Einschränkungen für die Typen von Methoden, die in die Warteschlange eingereiht werden können. Aufgrund von Messaging Einschränkungen müssen Methoden den folgenden Regeln entsprechen:

-   Sie müssen nur Eingabeparameter enthalten.
-   Sie müssen kein anwendungsspezifisches Ergebnis zurückgeben.

Außerdem gibt es Einschränkungen hinsichtlich der Typen von Eingabe Parametern, die an eine in der Warteschlange eingereihte Komponente weitergegeben werden können. Zur Laufzeit verpackt der Dienst für in der Warteschlange befindliche Komponenten die Argumente auf dem Client und übergibt Sie mithilfe [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85))an die Serverkomponente. Einfache Typen, z. b. ganze Zahlen und boolesche Werte, können problemlos gemarshallt werden – komplexere Typen können ohne Hilfe nicht gemarshallt werden.

Wenn ein Objekt über den Methoden Aufrufder in der Warteschlange befindlichen Komponente als Parameter übergeben wird, übergibt der Client das Objekt an den Recorder. Die Aufzeichnung Marshalls das Objekt in eine Message Queuing Nachricht und übergibt sie an den Listener. Nachdem der Listener die Nachricht übernommen und an den Player weitergeleitet hat, muss der Spieler das Objekt neu installieren, um es an den vom Client angegebenen Methoden Befehl zu verteilen. Basierend auf der Lebensdauer des Clients und des Servers in einer in der Warteschlange befindlichen Umgebung besteht die Auswirkung darauf, dass diese Objekte nach Wert marshallt werden müssen. Da com+ keine Pass-by-Value-Semantik für com-Standardobjekte bereitstellt, benötigen der Recorder und der Player Hilfe von der Komponente, um das Objekt zu Mars Hallen und das Objekt zu entsperren.

Objekt Verweise, die [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) unterstützen, können als Parameter für Methodenaufrufe von in der Warteschlange befindlichen Komponenten verwendet werden. Das Objekt kann keine Annahmen darüber machen, wann es neu installiert wird. Beispielsweise ist der Server möglicherweise nicht verfügbar, oder die Serverkomponente wird erst später am Tag gestartet. Bei Objekten, die **IPersistStream** nicht unterstützen, wird ein Fehler zurückgegeben.

## <a name="visual-basic-persistable-objects"></a>Visual Basic Persistable-Objekte

Microsoft Visual Basic 6 ermöglicht das Erstellen persierbarer Objekte. Diese Objekte unterstützen [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) und können als Parameter an in die Warteschlange eingereihte Komponenten Methodenaufrufe übermittelt werden. Bevor ein Visual Basic Objekt an eine in der Warteschlange eingereihte Komponente weitergeleitet werden kann, muss das persistbare Objekt initialisiert werden. Dies kann auf eine der beiden folgenden Arten erfolgen:

-   Wenn die Anwendung, die das persistbare Objekt erstellt, in Visual Basic geschrieben wird, verarbeitet die Visual Basic-Laufzeit die Objekt Initialisierung automatisch.
-   Wenn die Anwendung, die das Visual Basic permanenten-Objekt erstellt, in einer anderen Sprache als Visual Basic geschrieben wird, z. b. Microsoft Visual C++, muss die Anwendung die Komponente explizit initialisieren, indem die [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) -Schnittstelle des permanenten Objekts abgefragt oder die [**IPersistStreamInit:: InitNew**](/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew)-Methode oder die [**IPersistStream:: Load**](/windows/desktop/api/objidl/nf-objidl-ipersiststream-load) -Methode aufgerufen wird.

## <a name="ado-recordsets-and-ole-db-rowsets"></a>ADO-Recordsets und OLE DB-Rowsets

Durch die Übergabe von ADO- **Recordset** -oder OLE DB-Rowsetobjekten zwischen Komponenten kann eine Komponente die Ergebnisse der von einer anderen Komponente ausgeführten Abfragen verarbeiten. Dies ist hilfreich, wenn Sie eine Anwendung auf mehreren Computern bereitstellen. **Recordset** -und Rowsetobjekte können als Methoden Parameter an Komponenten in der Warteschlange mit den folgenden Einschränkungen übermittelt werden:

-   Server seitige **Recordset** -Objekte können nicht mithilfe von [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)gemarshallt werden. Nur Client seitige Recordsetobjekte können als Parameter an einen in der Warteschlange eingereihten Komponenten Methoden aufgerufen werden. 
-   Wenn Sie direkt mit OLE DB arbeiten, muss das OLE DB-Rowset als Client seitiges Rowset definiert werden.

 

 
