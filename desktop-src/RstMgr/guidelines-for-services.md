---
title: Richtlinien für Dienste
description: Dienste sollten diese Richtlinien einhalten, um sicherzustellen, dass der Neustart-Manager Dienste herunterfahren und neu starten kann, wenn dies zum Installieren von Updates erforderlich ist. Anwendungen können die Richtlinien verwenden, die unter Richtlinien für Anwendungen beschrieben sind.
ms.assetid: 69a98f82-71bb-4780-8a3f-294cc5629900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6198da0d4f6f7887aaf37c858d98f3eb48e72c0d7722a1b5785a1cb280c96fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010138"
---
# <a name="guidelines-for-services"></a>Richtlinien für Dienste

Dienste sollten diese Richtlinien einhalten, um sicherzustellen, dass der Neustart-Manager Dienste herunterfahren und neu starten kann, wenn dies zum Installieren von Updates erforderlich ist. Anwendungen können die Richtlinien verwenden, die unter [Richtlinien für Anwendungen](guidelines-for-applications.md)beschrieben sind.

-   Dienste sollten mit dem [Dienststeuerungs-Manager](/windows/desktop/Services/service-control-manager) heruntergefahren und neu gestartet werden können, ohne dass ein Systemneustart erforderlich ist. Ausnahmen von dieser Richtlinie sind kritische Systemprozesse, die im Kontext von lsass.exe oder services.exe ausgeführt werden.
-   Neustart-Manager berücksichtigt Dienstabhängigkeiten. Wenn ein Dienst heruntergefahren und neu gestartet wird, werden seine abhängigen Dienste heruntergefahren und neu gestartet.
-   Dienste sollten das Wiederherstellungsintervall und den Zurücksetzungszeitraum im [Dienststeuerungs-Manager (Service Control Manager, SCM)](/windows/desktop/Services/service-control-manager)angeben. Das Wiederherstellungsintervall ist die Zeit in Sekunden nach dem letzten Fehler, den der SCM wartet, bevor die Wiederherstellungsaktion erfolgt. Der Zurücksetzungszeitraum ist die Zeit in Sekunden nach dem letzten Fehler, den der Dienststeuerungs-Manager wartet, bevor die Fehleranzahl auf 0 zurückgesetzt wird. Dienste können die [**ChangeServiceConfig2-Funktion**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a) verwenden, um die Konfigurationseinstellungen zu ändern.

    [Kritische Dienste](critical-system-services.md) sollten die folgenden Wiederherstellungseinstellungen verwenden, um anzugeben, dass der Dienst eine Minute nach dem ersten Neustart des Diensts neu gestartet wird, zwei Minuten nach dem zweiten Fehler neu gestartet wird und dass der Computer eine Minute nach dem dritten Fehler neu gestartet wird. Die Fehleranzahl wird nach 300 Sekunden auf 0 zurückgesetzt.

    <dl> Wiederherstellungsaktionen: Restart/60000/Restart/120000/Reboot/60000 & Reset =300  
    </dl>

    [Kritische Dienste](critical-system-services.md) sollten vor nicht kritischen Diensten gestartet werden. Dienste, die keine kritischen Dienste sind, sollten die folgenden Wiederherstellungseinstellungen verwenden, um anzugeben, dass der Dienst zwei Minuten nach dem ersten Fehler beim Neustart des Diensts neu gestartet wird. Der Dienst wird nach dem zweiten Fehler nicht neu gestartet, und ein Administrator muss in diesem Fall eingreifen. Die Fehleranzahl wird nach 900 Sekunden auf 0 zurückgesetzt.

    <dl> Wiederherstellungsaktionen: Restart/120000/Restart/300000/None/0 & Reset = 900  
    </dl>

 

 