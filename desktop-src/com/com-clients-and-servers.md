---
title: COM-Clients und-Server
description: Ein wichtiger Aspekt von com ist die Interaktion von Clients und Servern.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7c3e29e4a4a3e2fcefe1c3473350d3423a8c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710968"
---
# <a name="com-clients-and-servers"></a>COM-Clients und-Server

Ein wichtiger Aspekt von com ist die Interaktion von Clients und Servern. Bei einem *com-Client* handelt es sich um einen beliebigen Code oder ein Objekt, das einen Zeiger auf einen com-Server erhält Ein *com-Server* ist ein beliebiges Objekt, das Dienste für Clients bereitstellt. Diese Dienste sind in Form von COM-Schnittstellen Implementierungen, die von jedem Client aufgerufen werden können, der einen Zeiger auf eine der Schnittstellen des Server Objekts erhalten kann.

Es gibt zwei Haupttypen von Servern: *in-Process* und *out-of-Process*. Prozess interne Server werden in einer dynamischen verknüpften Bibliothek (dll) implementiert, und prozessübergreifende Server werden in einer ausführbaren Datei (exe) implementiert. Out-of-Process-Server können sich entweder auf dem lokalen Computer oder auf einem Remote Computer befinden. Außerdem bietet com einen Mechanismus, mit dem ein Prozess interner Server (eine DLL) in einem Ersatz-exe-Prozess ausgeführt werden kann, um den Vorteil zu erhalten, dass der Prozess auf einem Remote Computer ausgeführt werden kann. Weitere Informationen finden Sie unter [dll-Surrogates](dll-surrogates.md).

Das COM-Programmiermodell und die Konstrukte wurden nun erweitert, sodass COM-Clients und-Server über das Netzwerk hinweg zusammenarbeiten können, nicht nur innerhalb eines bestimmten Computers. Dadurch können vorhandene Anwendungen mit neuen Anwendungen und untereinander in Netzwerken mit ordnungsgemäßer Verwaltung interagieren, und neue Anwendungen können so geschrieben werden, dass Sie die Netzwerk Features nutzen können.

COM-Client Anwendungen müssen nicht wissen, wie Server Objekte verpackt werden, unabhängig davon, ob Sie als Prozess interne Objekte (in DLLs) oder als lokale oder Remote Objekte (in exe) verpackt sind. Mithilfe von verteiltem com können Objekte als Dienst Anwendungen verpackt werden, und com wird mit den umfassenden Verwaltungs-und System Integrationsfunktionen von Windows synchronisiert.

> [!Note]  
> In dieser Dokumentation wird das Akronym com im Gegensatz zu DCOM verwendet. Dies liegt daran, dass DCOM nicht getrennt ist, sondern nur com mit einem längeren Netzwerk. In Fällen, in denen beschrieben wird, was speziell ein Remote Vorgang ist, wird der Begriff *verteilte com* verwendet.

 

COM ist so konzipiert, dass es möglich ist, die Unterstützung für Standort Transparenz hinzuzufügen, die sich über ein Netzwerk erstreckt. Dadurch können Anwendungen, die für einzelne Computer geschrieben werden, in einem Netzwerk ausgeführt werden, und es werden Features bereitgestellt, die diese Funktionen erweitern und die in einem Netzwerk erforderliche Sicherheit erhöhen. (Weitere Informationen finden Sie unter [Sicherheit in com](security-in-com.md).)

COM gibt einen Mechanismus an, mit dem der Klassen Code von vielen verschiedenen Anwendungen verwendet werden kann.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Einen Zeiger auf ein Objekt zu erhalten](getting-a-pointer-to-an-object.md)
-   [Erstellen eines Objekts über ein Klassenobjekt](creating-an-object-through-a-class-object.md)
-   [Zuständigkeiten von com-Servern](com-server-responsibilities.md)
-   [Persistentes Objektstatus](persistent-object-state.md)
-   [Bereitstellen von Klassen Informationen](providing-class-information.md)
-   [Kommunikation zwischen Objekten](inter-object-communication.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückruf Synchronisierung](call-synchronization.md)
</dt> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 




