---
description: Eine Datei Warteschlange ist eine Liste von Datei Vorgängen, die gleichzeitig verarbeitet werden. Die Datei Vorgänge in der Warteschlange sind möglicherweise Kopier-, Umbenennungs-oder Löschvorgänge. Die Datei Warteschlange organisiert Datei Vorgänge nach Typ, das Kopieren, umbenennen und Löschen von unter Warteschlangen.
ms.assetid: 9ad42c37-1d6b-4f1b-8173-629e2d3678f2
title: Informationen zu Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af441a1195bad5116306ca93cfbe658be5b3efc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348762"
---
# <a name="about-file-queues"></a>Informationen zu Warteschlangen

Eine Datei Warteschlange ist eine Liste von Datei Vorgängen, die gleichzeitig verarbeitet werden. Die Datei Vorgänge in der Warteschlange sind möglicherweise Kopier-, Umbenennungs-oder Löschvorgänge. Die Datei Warteschlange organisiert Datei Vorgänge nach Typ, das Kopieren, umbenennen und Löschen von unter Warteschlangen.

Diese Vorgänge können in beliebiger Reihenfolge an die Warteschlange gesendet werden, und der in die Warteschlange eingereihte Prozess muss nicht zusammenhängend sein. Wenn für die Warteschlange ein Commit ausgeführt wird, führt die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion Datei Vorgänge in der Reihenfolge des Vorgangs Typs aus.

Normalerweise werden alle für eine gesamte Installation erforderlichen Datei Vorgänge in die Warteschlange eingereiht und dann in einem einzelnen Batch verarbeitet, wenn ein Commit für die Warteschlange ausgeführt wird.

Der Vorteil, dass Datei Vorgänge in der Warteschlange über die Installation von Dateien in einer INF-Datei durchgeführt werden, besteht darin, den Installationsvorgang zu optimieren. Anstatt für jeden zu installierenden Abschnitt Informationen vom Benutzer abrufen zu müssen, können Sie beim Aufbau der Warteschlange Installationsinformationen vom Benutzer abrufen, damit alle Dateien installiert werden. Dadurch wird der Benutzer zur Verfolgung anderer Aktivitäten freigegeben, während die zeitintensiven Kopiervorgänge von der [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion verarbeitet werden.

Ein weiterer Vorteil von Datei Warteschlangen besteht darin, dass Sie den Fortschritt der Installation als Ganzes verfolgen können. Bei der Installation von "section-by-Section" aus einer INF-Datei können Status Indikatoren wie z. b. Status anzeigen nur den aktuellen INF-Abschnitt nachverfolgen. Wenn der nächste Abschnitt installiert ist, beginnt die Statusanzeige. Bei einer Warteschlange ist die Gesamtanzahl der Dateien, die während der gesamten Installation verarbeitet werden müssen, bekannt, bevor ein Commit für die Warteschlange ausgeführt wird. auf diese Weise kann eine Statusanzeige generiert werden, um die gesamte Installation zu verfolgen.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Reihenfolge der Warteschlangen Verpflichtung](order-of-queue-commitment.md)
-   [Warteschlangen Benachrichtigungen](queue-notifications.md)

 

 



