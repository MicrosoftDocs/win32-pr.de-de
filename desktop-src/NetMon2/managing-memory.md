---
description: Wenn ein Experte während der Laufzeit einen Fehler verursacht, wird der zugewiesene Arbeitsspeicher von Netzwerkmonitor freigegeben, wenn Sie Netzwerkmonitor Funktionen für die Speicherverwaltung verwenden.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Verwalten des Arbeitsspeichers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e2a6cca89a095c03c5c0cad25642b87d2c252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959021"
---
# <a name="managing-memory"></a>Verwalten des Arbeitsspeichers

Wenn ein Experte während der Laufzeit einen Fehler verursacht, wird der zugewiesene Arbeitsspeicher von Netzwerkmonitor freigegeben, wenn Sie Netzwerkmonitor Funktionen für die Speicherverwaltung verwenden. Wenn Sie jedoch einen Experten schreiben, ist es möglicherweise erforderlich, Systemressourcen und Datenstruktur Informationen abzurufen. Der Netzwerkmonitor Protokoll-COALESCE-Experte erhält z. b. ein Datei Handle zum Erstellen einer neuen Erfassung. Jeder Experte muss eine eigene **try/catch-** Behandlung erstellen, damit der Experte Ressourcen freigeben kann, die er erworben hat.

Wenn Arbeitsspeicher zugewiesen ist, verwenden Sie die folgenden vorhandenen Speicherfunktionen:

-   [**"Expertenlocmemory"**](expertallocmemory.md)
-   [**Expertrebelegcmemory**](expertreallocmemory.md)

 

 



