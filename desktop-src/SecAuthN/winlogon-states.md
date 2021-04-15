---
description: Winlogon behält den Arbeitsstations Status bei, der von Gina verwendet wird, um zu bestimmen, welche Authentifizierungs Aktionen erforderlich sind.
ms.assetid: e04175c4-bb43-4f76-8ceb-50282a1ebed0
title: Winlogon-Zustände
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d2e4ec690d6bdda15fb8e350969b36e01d5c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554662"
---
# <a name="winlogon-states"></a>Winlogon-Zustände

[*Winlogon*](../secgloss/w-gly.md) behält den Arbeitsstations Status bei, der von [*Gina*](../secgloss/g-gly.md) verwendet wird, um zu bestimmen, welche Authentifizierungs Aktionen erforderlich sind.

Der Winlogon-Dienst befindet sich zu einem beliebigen Zeitpunkt in einem von drei Zuständen:

-   [Abgemeldet](#logged-off-state)
-   [Angemeldeter Status](#logged-on-state)
-   [Arbeitsstations-gesperrt](#workstation-locked-state)

Diese drei Zustände werden in der folgenden Abbildung dargestellt.

![Winlogon-Status](images/winlogonst.png)

## <a name="logged-off-state"></a>Logged-Off Status

Wenn sich Winlogon im abgerufenen Zustand befindet, werden Benutzer aufgefordert, sich selbst zu identifizieren und Authentifizierungsinformationen bereitzustellen. Wenn ein Benutzer korrekte Benutzerkontoinformationen und keine Einschränkungen zur Verfügung stellt, wird der Benutzer angemeldet, und ein Shellprogramm (z. b. Windows-Explorer) wird auf dem Anwendungs Desktop ausgeführt. Winlogon wechselt in den angemeldeten Zustand.

## <a name="logged-on-state"></a>Logged-On Status

Wenn sich Winlogon im angemeldeten Zustand befindet, können Benutzer mit der Shell interagieren, zusätzliche Anwendungen aktivieren und ihre Arbeit erledigen. Aus dem angemeldeten Zustand können Benutzer entweder die gesamte Arbeit beenden und abmelden oder Ihre Arbeitsstationen Sperren (sodass die gesamte Arbeit nicht mehr vorhanden ist). Wenn sich der Benutzer entscheidet, sich abzumelden, beendet Winlogon alle Prozesse, die dieser [*Anmelde Sitzung*](../secgloss/l-gly.md) zugeordnet sind, und die Arbeitsstation wird für einen anderen Benutzer verfügbar sein. Wenn der Benutzer stattdessen die Sperre der Arbeitsstation beschließt, wechselt Winlogon in den Zustand der Arbeitsstation.

## <a name="workstation-locked-state"></a>Workstation-Locked Status

Wenn sich Winlogon im Zustand "Arbeitsstations gesperrt" befindet, wird ein sicherer Desktop angezeigt, bis der Benutzer die Arbeitsstation entsperrt, indem er die gleichen Identifikations-und Authentifizierungsinformationen wie der Benutzer, der sich ursprünglich angemeldet hat, bereitstellt, oder bis ein Administrator eine Abmeldung erzwingt. Wenn die Arbeitsstation entsperrt ist, wird der Anwendungs Desktop angezeigt, und die Arbeit kann fortgesetzt werden. Wenn ein Administrator jedoch die Arbeitsstation entsperrt (indem er die Identifikations-und Authentifizierungsinformationen eines Administrator Kontos bereitstellt), werden die Prozesse des angemeldeten Benutzers beendet, und Winlogon wechselt in den abangemeldeten Zustand.

In jedem der Winlogon-Zustände können verschiedene Aktionen ausgeführt werden. Eine Gina-DLL kann Aktionen implementieren, die nicht Teil des standardmäßigen Windows-Betriebssystems sind. Beispielsweise könnte ein hoch Sicherheitssystem eine Arbeitsstation automatisch alle 10 Minuten Sperren und erzwingen, dass sich die Benutzer erneut authentifizieren.

Weitere Informationen zum Erstellen von Desktops und zum Registrieren einer Sicherheits-und Registrierungs [*Sequenz*](../secgloss/s-gly.md) finden Sie unter [Initialisieren von Winlogon](initializing-winlogon.md). Weitere Informationen zu Timeout Vorgängen finden [Sie unter Unterstützte Dialog Feld-Dienstnutzungsdauer-out-Vorgänge](supported-dialog-box-service-time-out-operations.md). Informationen zum Senden von Nachrichten an die Gina, während ein Dialogfeld angezeigt wird, finden [Sie unter Senden von Nachrichten an die Gina](sending-messages-to-the-gina.md). Weitere Informationen zu Unterstützungsfunktionen finden Sie unter [Winlogon-Unterstützungsfunktionen](authentication-functions.md).

 

 
