---
description: Wenn ein Experte während der Laufzeit fehlschlägt und Sie Netzwerkmonitor Funktionen für die Speicherverwaltung verwenden, gibt Netzwerkmonitor zugewiesenen Arbeitsspeicher frei.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Verwalten des Arbeitsspeichers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4cc5b38f5525b7c0d19e115c83ed9f770c72215c6b64825a089ec389bfc09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555880"
---
# <a name="managing-memory"></a>Verwalten des Arbeitsspeichers

Wenn ein Experte während der Laufzeit fehlschlägt und Sie Netzwerkmonitor Funktionen für die Speicherverwaltung verwenden, gibt Netzwerkmonitor zugewiesenen Arbeitsspeicher frei. Wenn Sie jedoch einen Experten schreiben, kann es erforderlich sein, Systemressourcen und Datenstrukturinformationen zu erhalten. Beispielsweise erhält der Netzwerkmonitor Protocol Coalesce Expert ein Dateihandle, um eine neue Erfassung zu erstellen. Jeder Experte muss eine eigene **Try/Catch-Behandlung** erstellen, damit der Experte die erworbenen Ressourcen freigeben kann.

Wenn Arbeitsspeicher belegt wird, verwenden Sie die folgenden vorhandenen Arbeitsspeicherfunktionen:

-   [**ExpertAllocMemory**](expertallocmemory.md)
-   [**ExpertReallocMemory**](expertreallocmemory.md)

 

 



