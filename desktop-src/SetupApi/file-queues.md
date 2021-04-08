---
description: Die Setup Funktionen umfassen Funktionen der Datei Warteschlange.
ms.assetid: 628850ab-eb66-4b60-9298-1a44a7f6a390
title: Datei Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7177e0bb267167ce5b37cf5213ea942c972ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960111"
---
# <a name="file-queues"></a>Datei Warteschlangen

Die Setup Funktionen umfassen Funktionen der Datei Warteschlange. Eine Datei Warteschlange ist eine Liste von Datei Kopier-, Umbenennungs-und Lösch Vorgängen. Diese Vorgänge können in beliebiger Reihenfolge an die Warteschlange gesendet werden. Wenn für die Warteschlange ein Commit ausgeführt wird, werden diese Vorgänge in der Reihenfolge des Vorgangs Typs als Batch verarbeitet.

In den folgenden Abschnitten wird erläutert, was eine Warteschlange ist und wie Sie beim Erstellen einer Setup Anwendung verwendet werden kann. Außerdem wird die Reihenfolge erläutert, in der die in die Warteschlange eingereihten Datei Vorgänge in der Warteschlange verarbeitet werden, und die Benachrichtigungen, die die Warteschlange in jeder Phase an eine Rückruf Routine sendet.

-   [Informationen zu Warteschlangen](about-file-queues.md)
-   [Verwenden von Warteschlangen](using-file-queues.md)
-   [Datei Warteschlangen Verweis](file-queue-reference.md)

 

 



