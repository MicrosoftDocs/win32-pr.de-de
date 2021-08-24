---
title: In-Process-Server
description: In-Process-Server
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccc4c65db19e4ed567a2fe6105fa4d81e9c52cc9165556d9f388d8af181eee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854530"
---
# <a name="in-process-servers"></a>In-Process-Server

Wenn Sie eine OLE-Serveranwendung als In-Process-Server implementieren – eine DLL, die im Prozessbereich der Containeranwendung ausgeführt wird – und nicht als lokaler Server – eine EXE, die in einem eigenen Prozessbereich ausgeführt wird, wird die Kommunikation zwischen Container und Server vereinfacht, da die Kommunikation zwischen den beiden in Form normaler Funktionsaufrufe erfolgen kann. Remoteprozeduraufrufe sind nicht erforderlich, da die beiden Anwendungen im gleichen Prozessbereich ausgeführt werden. Wie Sie erwarten würden, sind die Objekte, die das Marshalling von Parametern verwalten, ebenfalls unnötig, obwohl sie innerhalb der DLL aggregiert werden können, ohne die Kommunikation zwischen Container und Server zu beeinträchtigen.

Wenn eine OLE-Serveranwendung als Prozessserver implementiert wird, ist kein separater Objekthandler erforderlich, da sich der Server selbst im Prozessbereich des Clients befindet. Der Hauptunterschied zwischen einem Prozessserver und einem Objekthandler besteht darin, dass der Server das Objekt in einem ausgeführten Zustand verwalten kann, während der Handler dies nicht kann. Eine Folge dieses Unterschieds ist, dass ein Server eine Benutzeroberfläche zum Bearbeiten des ausgeführten Objekts bereitstellen muss, während ein Handler diese Anforderung an den Server des Objekts delegiert. Beim Erstellen eines In-Process-Servers können Sie für den OLE-Standardhandler aggregieren, sodass er grundlegende Aufgaben wie Anzeige, Speicherung und Benachrichtigungen verarbeiten kann, während Sie nur die Dienste implementieren, die der Handler entweder nicht bereitstellt oder nicht in der von Ihnen benötigten Weise implementiert.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Vorteile](advantages.md)
-   [Nachteile](disadvantages.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zusammengesetzte Dokumente](compound-documents.md)
</dt> </dl>

 

 




