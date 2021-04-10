---
title: Richtlinien für Dienste
description: Dienste sollten diese Richtlinien einhalten, um sicherzustellen, dass der Neustart-Manager Dienste bei Bedarf Herunterfahren und neu starten kann, um Updates zu installieren. Anwendungen können die Richtlinien verwenden, die unter Richtlinien für Anwendungen beschrieben werden.
ms.assetid: 69a98f82-71bb-4780-8a3f-294cc5629900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51374c0a4c6fc561b8259aadf15e3d5487e12483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039331"
---
# <a name="guidelines-for-services"></a>Richtlinien für Dienste

Dienste sollten diese Richtlinien einhalten, um sicherzustellen, dass der Neustart-Manager Dienste bei Bedarf Herunterfahren und neu starten kann, um Updates zu installieren. Anwendungen können die Richtlinien verwenden, die unter [Richtlinien für Anwendungen](guidelines-for-applications.md)beschrieben werden.

-   Dienste sollten mit dem [Dienststeuerungs-Manager](/windows/desktop/Services/service-control-manager) heruntergefahren und neu gestartet werden können, ohne dass ein Systemneustart erforderlich ist. Die Ausnahmen zu dieser Richtlinie sind wichtige System Prozesse, die im Kontext von lsass.exe oder services.exe ausgeführt werden.
-   Der Neustart-Manager berücksichtigt Dienst Abhängigkeiten. Wenn ein Dienst heruntergefahren und neu gestartet wird, werden die abhängigen Dienste heruntergefahren und neu gestartet.
-   Dienste sollten das Wiederherstellungs Intervall und den Zurücksetzungs Zeitraum im [Dienststeuerungs-Manager (Service Control Manager, SCM)](/windows/desktop/Services/service-control-manager)angeben. Das Wiederherstellungs Intervall ist die Zeit in msekunden nach dem letzten Fehler, den der SCM vor dem Ausführen der Wiederherstellungs Aktion wartet. Der Zurücksetzungs Zeitraum ist die Zeit (in Sekunden) nach dem letzten Fehler, den der Dienststeuerungs-Manager wartet, bevor die Fehler Anzahl auf 0 zurückgesetzt wird. Dienste können die [**ChangeServiceConfig2**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a) -Funktion verwenden, um die Konfigurationseinstellungen zu ändern.

    [Kritische Dienste](critical-system-services.md) sollten die folgenden Wiederherstellungs Einstellungen verwenden, um anzugeben, dass der Dienst nach dem ersten Neustart des Diensts eine Minute neu gestartet wird, zwei Minuten nach dem zweiten Fehler neu gestartet und der Computer nach dem dritten Ausfall eine Minute neu gestartet wird. Die Fehler Anzahl wird nach 300 Sekunden auf 0 zurückgesetzt.

    <dl> Wiederherstellungs Aktionen: Restart/60000/Restart/120000/Reboot/60000 & Reset = 300  
    </dl>

    [Wichtige Dienste](critical-system-services.md) sollten vor nicht kritischen Diensten gestartet werden. Dienste, bei denen es sich nicht um kritische Dienste handelt, sollten die folgenden Wiederherstellungs Einstellungen verwenden, um anzugeben, dass der Dienst zwei Minuten nach dem ersten Neustart des Diensts neu gestartet werden soll. Der Dienst wird nach dem zweiten Fehler nicht neu gestartet, und ein Administrator muss in diesem Fall eingreifen. Die Fehler Anzahl wird nach 900 Sekunden auf 0 zurückgesetzt.

    <dl> Wiederherstellungs Aktionen: Restart/120000/Restart/300000/None/0 & Reset = 900  
    </dl>

 

 