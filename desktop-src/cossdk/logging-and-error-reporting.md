---
description: Protokollierung und Fehlerberichterstattung
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Protokollierung und Fehlerberichterstattung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d974b4043b4365839aec6a4fae392ae1d84900e8b8347949147b8df13326bd1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990760"
---
# <a name="logging-and-error-reporting"></a>Protokollierung und Fehlerberichterstattung

## <a name="log-file"></a>Protokolldatei

COMREPL generiert eine Protokolldatei mit Status- und Fehlermeldungen. Diese Datei wird auf dem Computer gespeichert, auf dem COMREPL in %systemdir% \\ com \\ replication \\ ComRepl.log gestartet wurde.

Diese Protokolldatei wird beim Starten einer Kopierphase nicht mehr angezeigt. Die nachfolgende Installation auf Zielen wird an die Datei angefügt.

## <a name="error-handling"></a>Fehlerbehandlung

Fehler sind in der oben beschriebenen Protokolldatei angegeben. Ausführliche Fehlerinformationen finden Sie auch im Ereignisprotokoll auf Quell- oder Zielcomputern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateiverwaltung](file-management.md)
</dt> <dt>

[Replikationsphasen](replication-phases.md)
</dt> <dt>

[Verwenden von COMREPL](using-comrepl.md)
</dt> <dt>

[Was wird repliziert?](what-gets-replicated.md)
</dt> </dl>

 

 



