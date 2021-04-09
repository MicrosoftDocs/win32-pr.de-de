---
description: Comrepl ist ein Hilfsprogramm, mit dem der com+-Katalog von einem bestimmten Quellcomputer auf einem oder mehreren Ziel Computern repliziert wird.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: Das Hilfsprogramm zur Comrepl-Replikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08ecd77a679b6fc150e7a91fc0214eb829792dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958531"
---
# <a name="the-comrepl-replication-utility"></a>Das Hilfsprogramm zur Comrepl-Replikation

Comrepl ist ein Hilfsprogramm, mit dem der com+-Katalog von einem bestimmten Quellcomputer auf einem oder mehreren Ziel Computern repliziert wird. Stellen Sie sich den Quellcomputer vor, der eine "Master Konfiguration" darstellt. Mit Comrepl wird diese Master Konfiguration repliziert, um einen Satz identisch konfigurierter Computer beizubehalten.

Die Replikations Einheit ist die gesamte com+-Konfiguration auf dem Master Computer. Alle com+-Anwendungen auf dem Master werden auf den Ziel Computern repliziert. Alles oder nichts. Außerdem werden alle com+-Anwendungen, die zuvor auf den Ziel Computern installiert wurden, mit Ausnahme der vorinstallierten com+-Anwendungen, im Rahmen des Replikations Prozesses gelöscht.

Comrepl repliziert nur com+-Konfigurationsdaten. Dies schließt com+-Anwendungen und com+-spezifische Computereinstellungen ein. Microsoft Internetinformationsdienste (IIS) verfügt über ein ähnliches Dienstprogramm (Iissync), das Comrepl zum Replizieren von IIS-und com+-Konfigurationen verwendet.

Ausführliche Informationen zum Starten und Verwenden von Comrepl finden Sie in den folgenden Themen in diesem Abschnitt:

-   [Verwenden von Comrepl](using-comrepl.md)
-   [Was wird repliziert?](what-gets-replicated.md)
-   [Replikations Phasen](replication-phases.md)
-   [Dateiverwaltung](file-management.md)
-   [Protokollierung und Fehlerberichterstattung](logging-and-error-reporting.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Installationspakete für COM+-Anwendungen werden erstellt.](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Anwendungs Proxys](deploying-application-proxies.md)
</dt> <dt>

[Der com+-Katalog](the-com--catalog.md)
</dt> </dl>

 

 



