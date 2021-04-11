---
title: In-Process Server
description: In-Process Server
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4886932b9669aa2d3cdd49979324f9ccc6e03d44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206719"
---
# <a name="in-process-servers"></a>In-Process Server

Wenn Sie eine OLE-Serveranwendung als in-Process-Server implementieren – eine DLL, die im Prozessbereich der Containeranwendung ausgeführt wird – anstelle eines lokalen Servers – eine exe-Datei, die in einem eigenen Prozessbereich ausgeführt wird – die Kommunikation zwischen Container und Server wird vereinfacht, da die Kommunikation zwischen den beiden die Form normaler Funktionsaufrufe annehmen kann. Remote Prozedur Aufrufe sind nicht erforderlich, da die beiden Anwendungen im gleichen Prozessbereich ausgeführt werden. Erwartungsgemäß sind die Objekte, die das Marshalling von Parametern verwalten, ebenfalls unnötig, obwohl Sie möglicherweise innerhalb der dll aggregiert werden, ohne die Kommunikation zwischen Container und Server zu beeinträchtigen.

Wenn eine OLE-Serveranwendung als Prozess interner Server implementiert wird, ist ein separater Objekt Handler nicht erforderlich, da sich der Server selbst im Prozessbereich des Clients befindet. Der Hauptunterschied zwischen einem in-Process-Server und einem Objekt Handler besteht darin, dass der Server das Objekt im Zustand "wird ausgeführt" verwalten kann, während der Handler dies nicht zulässt. Eine Folge dieses Unterschieds besteht darin, dass ein Server eine Benutzeroberfläche für die Bearbeitung des laufenden Objekts bereitstellen muss, während ein Handler diese Anforderung an den Server des Objekts delegiert. Beim Erstellen eines in-Process-Servers können Sie den OLE-Standard Handler aggregieren, sodass grundlegende Aufgaben wie Anzeige, Speicherung und Benachrichtigungen behandelt werden können, während Sie nur die Dienste implementieren, die der Handler entweder nicht bereitstellt oder nicht auf die gewünschte Weise implementiert.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Vorteile](advantages.md)
-   [Nachteile](disadvantages.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbund Dokumente](compound-documents.md)
</dt> </dl>

 

 




