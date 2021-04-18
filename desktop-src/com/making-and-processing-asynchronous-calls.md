---
title: Erstellen und Verarbeiten von asynchronen Aufrufen
description: COM-Objekte können asynchronen Aufruf von unterstützen.
ms.assetid: bf7f9f8e-66ce-41a4-854c-62dbe840a89e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059f55cc64a70f130e7fb654426803edbe8b7209
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341562"
---
# <a name="making-and-processing-asynchronous-calls"></a>Erstellen und Verarbeiten von asynchronen Aufrufen

COM-Objekte können asynchronen Aufruf von unterstützen. Wenn ein Client einen asynchronen Rückruf ausführt, wird die Steuerung sofort an den Client zurückgegeben. Während der Server den-Befehl verarbeitet, kann der-Client andere Aufgaben ausführen. Wenn der Client nicht mehr ohne die Ergebnisse des Aufrufes aufgerufen werden kann, kann er die Ergebnisse des Aufrufes zu diesem Zeitpunkt abrufen.

Beispielsweise kann eine Anforderung eines großen oder komplexen Recordsets zeitaufwändig sein. Ein Client kann das Recordset durch einen asynchronen-Rückruf anfordern und dann andere Aufgaben ausführen. Wenn das Recordset verfügbar ist, kann der Client es ohne Blockierung schnell abrufen.

Clients führen keine asynchronen Aufrufe direkt für das Server Objekt aus. Stattdessen erhalten Sie ein Callcenter, das eine asynchrone Version einer synchronen Schnittstelle auf dem Server Objekt implementiert. Die asynchrone Schnittstelle des callobjekts hat den Namen "Async *interfakename*". Wenn ein Server Objekt z. b. eine synchrone Schnittstelle namens IMyInterface implementiert, gibt es ein-Rückruf Objekt, das eine asynchrone Schnittstelle mit dem Namen asyncimyinterface implementiert.

> [!Note]  
> Die asynchrone Unterstützung ist für **IDispatch** oder für Schnittstellen, die **IDispatch** erben, nicht verfügbar.

 

Server Objekte, die asynchrone Aufrufe unterstützen, implementieren die [**icallfactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) -Schnittstelle. Diese Schnittstelle macht eine einzelne Methode (" [**anatecall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall)") verfügbar, mit der eine Instanz eines angegebenen Anruf Objekts erstellt wird. Clients können **icallfactory** Abfragen, um zu bestimmen, ob ein-Objekt asynchrone Aufrufe unterstützt.

Für jede Methode in einer synchronen Schnittstelle implementiert die zugehörige asynchrone Schnittstelle zwei Methoden. Diese Methoden fügen die Präfixe "BEGIN" \_ und "Finish" \_ an den Namen der synchronen Methode an. Wenn eine Schnittstelle mit dem Namen isimplestream z. b. über eine Read-Methode verfügt, verfügt die asyncisimplestream-Schnittstelle über die Read \_ -Methode Begin und Finish Read \_ . Zum Starten eines asynchronen Aufrufs ruft der Client die BEGIN- \_ Methode auf.

Wenn Sie ein Server Objekt implementieren, müssen Sie kein-Objekt für jede Schnittstelle bereitstellen, die das Objekt implementiert. Wenn das Server Objekt die [**icallfactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) -Schnittstelle implementiert und Standard-Marshalling verwendet, kann ein gemarshallter Client immer ein Proxy Aufruf Objekt abrufen, auch wenn kein Aufruf Objekt auf der Serverseite vorhanden ist. Dieser Proxy marshallt die BEGIN- \_ Methode als synchronen Aufruf, der Server verarbeitet den Aufruf synchron, und der Client kann die Out-Parameter abrufen, indem er die Finish- \_ Methode aufruft.

Wenn ein Client dagegen einen gemarshallten synchronen Aufrufvorgang an eine Schnittstelle sendet, für die ein Rückruf Objekt auf der Serverseite vorhanden ist, verarbeitet der Server den-Rückruf immer asynchron. Dieses Verhalten ist für den Client nicht offensichtlich, da der Client dieselben out-Parameter und denselben Rückgabewert erhält, den er von der synchronen Methode erhalten hätte.

In beiden Fällen wird die Interaktion zwischen Client und Server gemarshallt, als ob der-Befehl synchron wäre: die Ausgabe von synchronen und asynchronen Proxys ist nicht unter scheidbar, ebenso wie die Ausgabe der entsprechenden Stubdateien. Dieses Verhalten vereinfacht das Programmiermodell sowohl von Clients als auch von Servern erheblich. Wenn ein Server Objekt [**icallfactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory)implementiert, muss ein gemarshallter Client nicht versuchen, ein Aufruf Objekt zu erstellen, das möglicherweise nicht verfügbar ist – für den Client ist ein Aufruf Objekt immer verfügbar.

Wenn sich Client und Server im selben Apartment befinden, verarbeitet das Server Objekt den vom Client vorgerichteten Rückruf. Wenn kein calltobjekt verfügbar ist, muss der Client explizit die synchrone-Schnittstelle abrufen und einen synchronen-Befehl ausführen.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Ausführen eines asynchronen Aufrufes](making-an-asynchronous-call.md)
-   [Abbrechen eines asynchronen Aufrufes](canceling-an-asynchronous-call.md)
-   [Abbrechen von Methoden aufrufen](canceling-method-calls.md)
-   [Rückruf Synchronisierung](call-synchronization.md)

 

 