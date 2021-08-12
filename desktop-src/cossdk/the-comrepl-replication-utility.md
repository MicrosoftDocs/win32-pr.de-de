---
description: COMREPL ist ein Hilfsprogramm, das den COM+-Katalog von einem bestimmten Quellcomputer auf einen oder mehrere Zielcomputer repliziert.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: Das COMREPL-Replikationshilfsprogramm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446cfc0e627463e8c142ccab624c3773123034c2becebc402a6069f74d30ccd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305295"
---
# <a name="the-comrepl-replication-utility"></a>Das COMREPL-Replikationshilfsprogramm

COMREPL ist ein Hilfsprogramm, das den COM+-Katalog von einem bestimmten Quellcomputer auf einen oder mehrere Zielcomputer repliziert. Stellen Sie sich den Quellcomputer vor, der eine "Masterkonfiguration" darstellt. COMREPL wird verwendet, um diese Masterkonfiguration zu replizieren, um eine Gruppe identisch konfigurierter Computer zu verwalten.

Die Replikationseinheit ist die gesamte COM+-Konfiguration auf dem Mastercomputer. Alle COM+-Anwendungen auf dem Master werden auf die Zielcomputer repliziert. es ist alles oder nichts. Darüber hinaus werden alle COM+-Anwendungen, die zuvor auf den Zielcomputern installiert wurden, mit Ausnahme der vorinstallierten COM+-Anwendungen im Rahmen des Replikationsprozesses gelöscht.

COMREPL repliziert nur COM+-Konfigurationsdaten. Dies schließt COM+-Anwendungen und COM+-spezifische Computereinstellungen ein. Microsoft-Internetinformationsdienste (IIS) verfügt über ein ähnliches Hilfsprogramm (IISSync), das COMREPL zum Replizieren von IIS- und COM+-Konfigurationen verwendet.

Ausführliche Informationen zum Starten und Verwenden von COMREPL finden Sie in den folgenden Themen in diesem Abschnitt:

-   [Verwenden von COMREPL](using-comrepl.md)
-   [Was wird repliziert?](what-gets-replicated.md)
-   [Replikationsphasen](replication-phases.md)
-   [Dateiverwaltung](file-management.md)
-   [Protokollierung und Fehlerberichterstattung](logging-and-error-reporting.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Installationspaketen für COM+-Anwendungen](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Bereitstellen von Anwendungsproxys](deploying-application-proxies.md)
</dt> <dt>

[Der COM+-Katalog](the-com--catalog.md)
</dt> </dl>

 

 



