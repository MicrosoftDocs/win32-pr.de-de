---
title: Objekthandler
description: Objekthandler
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85221456d637e0d9e982aad253c06d34618018a3648a31a7bd21e8c1465fa84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992320"
---
# <a name="object-handlers"></a>Objekthandler

Wenn eine OLE-Serveranwendung ein lokaler Server ist, d. h., sie wird in einem eigenen Prozessbereich ausgeführt, muss die Kommunikation zwischen Container und Server über Prozessgrenzen hinweg erfolgen. Da dieser Prozess teuer ist, verwendet OLE ein Ersatzobjekt, das in den Prozessbereich des Containers geladen wird, um im Auftrag einer lokalen Serveranwendung zu agieren. Dieses Ersatzobjekt, das als *Objekthandler* bezeichnet wird, wartet Containeranforderungen, die die Aufmerksamkeit der Serveranwendung nicht erfordern, z. B. Zeichnungsanforderungen. Wenn ein Container etwas anfordet, das der Objekthandler nicht bereitstellen kann, kommuniziert der Handler mit der Serveranwendung über den out-of-process-Kommunikationsmechanismus von COM.

Ein Objekthandler ist für eine Objektklasse eindeutig. Wenn Sie eine Instanz eines Handlers für eine Klasse erstellen, können Sie sie nicht für eine andere Klasse verwenden. Bei Verwendung für ein zusammengesetztes Dokument implementiert der Objekthandler die containerseitigen Datenstrukturen, wenn remote auf Objekte einer bestimmten Klasse zugegriffen wird.

OLE stellt einen Standardobjekthandler bereit, den lokale Serveranwendungen verwenden können. Für Anwendungen, die spezielle Verhaltensweisen erfordern, können Entwickler einen benutzerdefinierten Handler implementieren, der entweder den Standardhandler ersetzt oder ihn verwendet, um bestimmte Standardverhalten bereitzustellen.

Ein Objekthandler ist eine DLL, die mehrere interagierende Komponenten enthält. Zu diesen Komponenten gehören Remotingelemente zum Verwalten der Kommunikation zwischen dem Handler und seiner Serveranwendung, ein Cache zum Speichern der Daten eines Objekts sowie Informationen dazu, wie diese Daten formatiert und angezeigt werden sollen, sowie ein steuernde Objekt, das die Aktivitäten der anderen Komponenten der DLL koordiniert. Wenn ein Objekt ein Link ist, enthält die DLL außerdem eine Verknüpfungskomponente oder ein *verknüpftes Objekt,* das den Namen und speicherort der Linkquelle nachverfolgt.

Der *Cache* enthält Daten und Präsentationsinformationen, die ausreichen, damit der Handler ein geladenes, aber nicht ausgeführtes Objekt in seinem Container anzeigen kann. OLE stellt eine Implementierung des Caches bereit, der vom Standardobjekthandler von OLE und dem Linkobjekt verwendet wird. Der Cache speichert Daten in Formaten, die vom Objekthandler benötigt werden, um Container draw-Anforderungen zu erfüllen. Wenn sich die Daten eines Objekts ändern, sendet das Objekt eine Benachrichtigung an den Cache, damit ein Update erfolgen kann. Weitere Informationen zum Cache finden Sie unter [View Caching](view-caching.md).

Weitere Informationen finden Sie in den folgenden Themen:

-   [Standardhandler und benutzerdefinierte Handler](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zusammengesetzte Dokumente](compound-documents.md)
</dt> </dl>

 

 




