---
description: Winlogon verwaltet den Arbeitsstationsstatus, der von der GINA verwendet wird, um zu bestimmen, welche Authentifizierungsaktionen erforderlich sind.
ms.assetid: e04175c4-bb43-4f76-8ceb-50282a1ebed0
title: Winlogon-Zustände
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fef22cdd172572b1d5032990abae929712dc0be29a926524520c7ce6f9bbfe69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915053"
---
# <a name="winlogon-states"></a>Winlogon-Zustände

[*Winlogon verwaltet*](../secgloss/w-gly.md) den Arbeitsstationsstatus, der von [*der GINA*](../secgloss/g-gly.md) verwendet wird, um zu bestimmen, welche Authentifizierungsaktionen erforderlich sind.

Winlogon befindet sich zu einem beliebigen Zeitpunkt in einem von drei Zuzuständen:

-   [Status "Abgemeldet"](#logged-off-state)
-   [Angemeldeter Status](#logged-on-state)
-   [Gesperrter Status der Arbeitsstation](#workstation-locked-state)

Diese drei Zustände sind in der folgenden Abbildung dargestellt.

![WinLogon-Zustände](images/winlogonst.png)

## <a name="logged-off-state"></a>Logged-Off Status

Wenn sich Winlogon im abgemeldeten Zustand befindet, werden Benutzer aufgefordert, sich selbst zu identifizieren und Authentifizierungsinformationen zur Verfügung zu stellen. Wenn ein Benutzer die richtigen Benutzerkontoinformationen enthält und keine Einschränkungen dies verhindern, wird der Benutzer angemeldet, und ein Shellprogramm (z. B. Windows Explorer) wird auf dem Anwendungsdesktop ausgeführt. Winlogon ändert sich in den angemeldeten Zustand.

## <a name="logged-on-state"></a>Logged-On Status

Wenn sich Winlogon im angemeldeten Zustand befindet, können Benutzer mit der Shell interagieren, zusätzliche Anwendungen aktivieren und ihre Arbeit tun. Vom angemeldeten Zustand aus können Benutzer entweder alle Arbeitsstationen beenden und sich abmelden oder ihre Arbeitsstationen sperren (alle Arbeitsstationen bleiben an Ort und Stelle). Wenn sich der Benutzer abmelden soll, beendet Winlogon alle Prozesse, die dieser Anmeldesitzung zugeordnet sind, und die Arbeitsstation steht einem anderen Benutzer zur Verfügung. [](../secgloss/l-gly.md) Wenn der Benutzer stattdessen entscheidet, die Arbeitsstation zu sperren, ändert sich winlogon in den gesperrten Status der Arbeitsstation.

## <a name="workstation-locked-state"></a>Workstation-Locked Status

Wenn winlogon sich im gesperrten Zustand der Arbeitsstation befindet, wird ein sicherer Desktop angezeigt, bis der Benutzer die Arbeitsstation entsperrt, indem er die gleichen Identifikations- und Authentifizierungsinformationen wie der benutzer, der sich ursprünglich angemeldet hat, oder bis ein Administrator eine Abmelde erzwingt. Wenn die Arbeitsstation entsperrt ist, wird der Anwendungsdesktop angezeigt, und die Arbeit kann fortgesetzt werden. Wenn ein Administrator die Arbeitsstation jedoch entsperrt (durch Angabe der Identifikations- und Authentifizierungsinformationen eines Administratorkontos), werden die Prozesse des angemeldeten Benutzers beendet, und Winlogon ändert sich in den abgemeldeten Zustand.

In jedem winlogon-Zustände können verschiedene Aktionen ausgeführt werden. Eine GINA-DLL kann Aktionen implementieren, die nicht Teil des Standardbetriebssystems Windows sind. Beispielsweise könnte ein System mit hoher Sicherheit eine Arbeitsstation automatisch alle 10 Minuten sperren und benutzer zwingen, sich selbst erneut zu authentifizieren.

Informationen zum Erstellen von Desktops und zum Registrieren einer [*Secure Attention Sequence*](../secgloss/s-gly.md) (SAS) finden Sie unter [Initialisieren von Winlogon](initializing-winlogon.md). Informationen zu Time out-Vorgängen finden Sie unter [Supported Dialog Box Service Time-out Operations](supported-dialog-box-service-time-out-operations.md). Informationen zum Senden von Nachrichten an die GINA, während ein Dialogfeld angezeigt wird, finden Sie unter Senden von [Nachrichten an die GINA.](sending-messages-to-the-gina.md) Informationen zu Unterstützungsfunktionen finden Sie unter [Winlogon-Unterstützungsfunktionen.](authentication-functions.md)

 

 
