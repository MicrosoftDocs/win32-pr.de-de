---
title: Objekt Handler
description: Objekt Handler
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7294ddd48d2acaa010ad15c0e2497fd33c7f071
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855644"
---
# <a name="object-handlers"></a>Objekt Handler

Wenn eine OLE-Serveranwendung ein lokaler Server ist, was bedeutet, dass Sie in einem eigenen Prozessbereich ausgeführt wird, muss die Kommunikation zwischen Container und Server über Prozess Grenzen hinweg erfolgen. Da dieser Prozess teuer ist, verwendet OLE ein Ersatzobjekt, das in den Prozessbereich des Containers geladen wird, um im Auftrag einer lokalen Serveranwendung zu agieren. Dieses Ersatzobjekt, das als *Objekt Handler* bezeichnet wird, verarbeitet Container Anforderungen, die keine Aufmerksamkeit der Serveranwendung erfordern, wie z. b. das Zeichnen von Anforderungen. Wenn ein Container etwas anfordert, das der Objekt Handler nicht bereitstellen kann, kommuniziert der Handler mit der Serveranwendung mithilfe des Out-of-Process-Kommunikationsmechanismus von com.

Ein Objekt Handler ist für eine Objektklasse eindeutig. Wenn Sie eine Instanz eines Handlers für eine Klasse erstellen, können Sie Sie nicht für eine andere Klasse verwenden. Bei Verwendung für ein zusammengesetztes Dokument implementiert der Objekt Handler die Container seitigen Datenstrukturen, wenn auf Objekte einer bestimmten Klasse Remote zugegriffen wird.

OLE stellt einen Standard Objekt Handler bereit, der von lokalen Server Anwendungen verwendet werden kann. Für Anwendungen, die ein spezielles Verhalten erfordern, können Entwickler einen benutzerdefinierten Handler implementieren, der entweder den Standard Handler ersetzt oder ihn verwendet, um bestimmte Standardverhalten bereitzustellen.

Ein Objekt Handler ist eine DLL, die mehrere interagierende Komponenten enthält. Diese Komponenten umfassen Remoting-Komponenten zum Verwalten der Kommunikation zwischen dem Handler und seiner Serveranwendung, einem Cache zum Speichern der Daten eines Objekts sowie Informationen dazu, wie diese Daten formatiert und angezeigt werden sollen, sowie ein Steuerungsobjekt, das die Aktivitäten der anderen Komponenten der dll koordiniert. Wenn ein Objekt ein Link ist, enthält die dll außerdem eine Verknüpfungs Komponente oder ein *verknüpftes Objekt*, das den Namen und den Speicherort der Link Quelle nachverfolgt.

Der *Cache* enthält Daten und Präsentationsinformationen, die für den Handler ausreichen, um ein geladenes, aber nicht ausgelaufetes Objekt in seinem Container anzuzeigen. OLE stellt eine Implementierung des Caches bereit, der von OLE-Standard Objekt Handler und dem Link-Objekt verwendet wird. Der Cache speichert Daten in Formaten, die vom Objekt Handler benötigt werden, um Container Zeichnungs Anforderungen zu erfüllen. Wenn sich die Daten eines Objekts ändern, sendet das Objekt eine Benachrichtigung an den Cache, damit ein Update erfolgen kann. Weitere Informationen zum Cache finden Sie unter [View Caching (anzeigen](view-caching.md)der Zwischenspeicherung).

Weitere Informationen finden Sie in den folgenden Themen:

-   [Der Standard Handler und benutzerdefinierte Handler](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbund Dokumente](compound-documents.md)
</dt> </dl>

 

 




