---
description: Protokollierung und Fehlerberichterstattung
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Protokollierung und Fehlerberichterstattung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdc29d32ae26429f2fe23fe88762fabf82185c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341157"
---
# <a name="logging-and-error-reporting"></a>Protokollierung und Fehlerberichterstattung

## <a name="log-file"></a>Protokolldatei

Comrepl generiert eine Protokolldatei mit Status-und Fehlermeldungen. Diese Datei wird auf dem Computer gespeichert, auf dem Comrepl in% systemdir% \\ com \\ Replication \\ Comrepl. log gestartet wurde.

Diese Protokolldatei wird gelöscht, wenn eine Kopier Phase gestartet wird. Die nachfolgende Installation der Ziele wird an die Datei angehängt.

## <a name="error-handling"></a>Fehlerbehandlung

Fehler werden in der oben beschriebenen Protokolldatei angegeben. Ausführliche Fehlerinformationen finden Sie möglicherweise auch im Ereignisprotokoll auf Quell-oder Ziel Computern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateiverwaltung](file-management.md)
</dt> <dt>

[Replikations Phasen](replication-phases.md)
</dt> <dt>

[Verwenden von Comrepl](using-comrepl.md)
</dt> <dt>

[Was wird repliziert?](what-gets-replicated.md)
</dt> </dl>

 

 



