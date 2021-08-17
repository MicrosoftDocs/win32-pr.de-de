---
title: Erstellen und Verarbeiten asynchroner Aufrufe
description: COM-Objekte können asynchrone Aufrufe unterstützen.
ms.assetid: bf7f9f8e-66ce-41a4-854c-62dbe840a89e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 173f33ea3a0d4ec59f994eeff259e776efa58ae5b0182ba97f77e1ba99dd0d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130202"
---
# <a name="making-and-processing-asynchronous-calls"></a>Erstellen und Verarbeiten asynchroner Aufrufe

COM-Objekte können asynchrone Aufrufe unterstützen. Wenn ein Client einen asynchronen Aufruf vornimmt, wird die Steuerung sofort an den Client zurückgegeben. Während der Server den Aufruf verarbeitet, kann der Client andere Arbeit erledigen. Wenn der Client nicht mehr ohne die Ergebnisse des Aufrufs fortfahren kann, kann er die Ergebnisse des Aufrufs zu diesem Zeitpunkt abrufen.

Beispielsweise kann eine Anforderung für ein großes oder komplexes Recordset zeitaufwändig sein. Ein Client kann das Recordset durch einen asynchronen Aufruf anfordern und dann andere Arbeit leisten. Wenn das Recordset verfügbar ist, kann es vom Client schnell ohne Blockierung abgerufen werden.

Clients nehmen keine asynchronen Aufrufe direkt auf dem Serverobjekt vor. Stattdessen erhalten sie ein Aufrufobjekt, das eine asynchrone Version einer synchronen Schnittstelle für das Serverobjekt implementiert. Die asynchrone Schnittstelle für das Aufrufobjekt hat den Namen Async *InterfaceName.* Wenn beispielsweise ein Serverobjekt eine synchrone Schnittstelle mit dem Namen IMyInterface implementiert, gibt es ein Aufrufobjekt, das eine asynchrone Schnittstelle mit dem Namen AsyncIMyInterface implementiert.

> [!Note]  
> Asynchrone Unterstützung ist für **IDispatch** oder schnittstellen, die **IDispatch** erben, nicht verfügbar.

 

Serverobjekte, die asynchrone Aufrufe unterstützen, implementieren die [**ICallFactory-Schnittstelle.**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) Diese Schnittstelle macht eine einzelne Methode, [**CreateCall,**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall)verfügbar, die eine Instanz eines angegebenen Aufrufobjekts erstellt. Clients können **ICallFactory** abfragen, um zu bestimmen, ob ein Objekt asynchrone Aufrufe unterstützt.

Für jede Methode auf einer synchronen Schnittstelle implementiert die entsprechende asynchrone Schnittstelle zwei Methoden. Diese Methoden fügen die Präfixe Begin \_ und Finish an den Namen der \_ synchronen Methode an. Wenn beispielsweise eine Schnittstelle mit dem Namen ISimpleStream über eine Read-Methode verfügt, verfügt die AsyncISimpleStream-Schnittstelle über eine Begin \_ Read- und eine Finish \_ Read-Methode. Um einen asynchronen Aufruf zu starten, ruft der Client die \_ Begin-Methode auf.

Wenn Sie ein Serverobjekt implementieren, müssen Sie nicht für jede Schnittstelle, die das Objekt implementiert, ein Aufrufobjekt bereitstellen. Wenn das Serverobjekt die [**ICallFactory-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) implementiert und standardmäßiges Marshalling verwendet, kann ein gemarshallter Client immer ein Proxyaufrufobjekt abrufen, auch wenn auf serverseitiger Seite kein Aufrufobjekt vorhanden ist. Dieser Proxy marshallt die \_ Begin-Methode als synchronen Aufruf, der Server verarbeitet den Aufruf synchron, und der Client kann die out-Parameter abrufen, indem er die \_ Finish-Methode aufruft.

Wenn dagegen ein Client einen gemarshallten synchronen Aufruf für eine Schnittstelle vornimmt, für die auf serverseitiger Seite ein Aufrufobjekt vorhanden ist, verarbeitet der Server den Aufruf immer asynchron. Dieses Verhalten ist für den Client nicht offensichtlich, da der Client die gleichen Out-Parameter und denselben Rückgabewert empfängt, den er von der synchronen Methode erhalten hätte.

In beiden Fällen wird die Interaktion zwischen Client und Server so gemarshallt, als wäre der Aufruf synchron: Die Ausgabe von synchronen und asynchronen Proxys ist nicht zu unterscheiden, ebenso wie die Ausgabe der entsprechenden Stubs. Dieses Verhalten vereinfacht das Programmiermodell sowohl von Clients als auch von Servern erheblich. Wenn ein Serverobjekt [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory)implementiert, muss ein gemarshallter Client nicht versuchen, ein Aufrufobjekt zu erstellen, das möglicherweise nicht verfügbar ist. Für den Client ist immer ein Aufrufobjekt verfügbar.

Wenn sich Client und Server im selben Apartment befinden, verarbeitet das Serverobjekt den Aufruf des Clients. Wenn kein Aufrufobjekt verfügbar ist, muss der Client explizit die synchrone Schnittstelle abrufen und einen synchronen Aufruf vornehmen.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Erstellen eines asynchronen Aufrufs](making-an-asynchronous-call.md)
-   [Abbrechen eines asynchronen Aufrufs](canceling-an-asynchronous-call.md)
-   [Abbrechen von Methodenaufrufen](canceling-method-calls.md)
-   [Aufrufsynchronisierung](call-synchronization.md)

 

 