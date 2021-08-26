---
description: Übergeben von Objekten als Parameter
ms.assetid: 174847c8-4545-4f61-ae13-42bdec1405e7
title: Übergeben von Objekten als Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47669d3e3e5af572b6dfd50dcbbefacf5c008971f276408fa87b37ccbed9a1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070380"
---
# <a name="passing-objects-as-parameters"></a>Übergeben von Objekten als Parameter

Der COM+-Komponentendienst in der Warteschlange aktiviert nicht das Warteschlangening für jede vorhandene COM-Komponente. Es gibt Einschränkungen hinsichtlich der Methodentypen, die in die Warteschlange eingereiht werden können. Aufgrund von Messagingeinschränkungen müssen Methoden die folgenden Regeln einhalten:

-   Sie dürfen nur Eingabeparameter enthalten.
-   Sie dürfen kein anwendungsspezifisches Ergebnis zurückgeben.

Darüber hinaus gibt es Einschränkungen hinsichtlich der Typen von Eingabeparametern, die an eine Komponente in der Warteschlange übergeben werden können. Zur Laufzeit packt der Komponentendienst in der Warteschlange die Argumente auf dem Client und übergibt sie mithilfe von [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85))an die Serverkomponente. Einfache Typen, z. B. ganze Zahlen und Boolesche Werte, können problemlos gemarshallt werden– komplexere Typen können nicht ohne Hilfe gemarshallt werden.

Wenn ein Objekt über den Methodenaufruf einer Komponente in der Warteschlange als Parameter übergeben wird, übergibt der Client das Objekt an den Recorder. Die Aufzeichnung marshallt das -Objekt in eine Message Queuing Nachricht und übergibt es an den Listener. Nachdem der Listener die Nachricht aufgenommen und an den Player übergeben hat, muss der Player das Objekt neu initialisiert haben, um es an den vom Client angegebenen Methodenaufruf zu senden. Basierend auf der Lebensdauer des Clients und Servers in einer Umgebung in der Warteschlange müssen diese Objekte als Wert gemarshallt werden können. Da COM+ keine Pass-by-Value-Semantik für COM-Standardobjekte bereitstellt, benötigen die Aufzeichnung und der Player Hilfe von der Komponente, um das Objekt zu marshallen und zu entfernen.

Objektverweise, die [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) unterstützen, können als Parameter für Methodenaufrufe auf Komponenten in der Warteschlange verwendet werden. Das Objekt kann keine Annahmen darüber treffen, wann es erneut instanziiert wird. Beispielsweise ist der Server möglicherweise nicht verfügbar, oder die Serverkomponente wird möglicherweise erst später am Tag gestartet. Objekte, die **IPersistStream** nicht unterstützen, geben einen Fehler zurück.

## <a name="visual-basic-persistable-objects"></a>Visual Basic Persistente Objekte

Microsoft Visual Basic 6 ermöglicht das Erstellen von persistenten Objekten. Diese Objekte unterstützen [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) und können als Parameter an Aufrufe von Komponentenmethoden in der Warteschlange übergeben werden. Bevor ein Visual Basic-Objekt an eine Komponente in der Warteschlange übergeben werden kann, muss das persistente Objekt initialisiert werden. Dies kann auf eine der folgenden beiden Arten erfolgen:

-   Wenn die Anwendung, die das persistente Objekt erstellt, in Visual Basic geschrieben wird, verarbeitet die Visual Basic Runtime die Objektinitialisierung automatisch.
-   Wenn die Anwendung, die das Visual Basic persistente Objekt erstellt, in einer anderen Sprache als Visual Basic geschrieben wird, z. B. Microsoft Visual C++, muss die Anwendung die Komponente explizit initialisieren, indem sie entweder die [**IPersistStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) des persistenten Objekts abfragt oder die [**IPersistStreamInit::InitNew**](/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew)-Methode oder die [**IPersistStream::Load-Methode**](/windows/desktop/api/objidl/nf-objidl-ipersiststream-load) aufruft.

## <a name="ado-recordsets-and-ole-db-rowsets"></a>ADO-Recordsets und OLE DB Rowsets

Das Übergeben von **ADO-Recordset-** oder OLE DB Rowsetobjekten zwischen Komponenten ermöglicht einer Komponente die Verarbeitung der Ergebnisse von Abfragen, die von einer anderen Komponente ausgeführt werden. Dies ist hilfreich, wenn Sie eine Anwendung auf mehreren Computern bereitstellen. **Recordset-** und Rowsetobjekte können mit den folgenden Einschränkungen als Methodenparameter an Komponenten in der Warteschlange übergeben werden:

-   Serverseitige **Recordsetobjekte** können nicht mit [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)gemarshallt werden. Nur clientseitige **Recordsetobjekte** können als Parameter an einen Methodenaufruf einer Komponente in der Warteschlange übergeben werden.
-   Wenn Sie direkt mit OLE DB arbeiten, muss das OLE DB Rowset als clientseitiges Rowset definiert werden.

 

 
