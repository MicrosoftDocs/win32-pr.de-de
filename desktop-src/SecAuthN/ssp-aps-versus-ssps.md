---
description: Erläutert die Unterschiede zwischen SSP/APs und SSPs.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/APs im Vergleich zu SSPs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c471e529a478cadbfcc385a1b0d699a4539e7bc80beeb2d40e01e2f7e9f428d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917266"
---
# <a name="sspaps-vs-ssps"></a>SSP/APs im Vergleich zu SSPs

[*Sicherheitspakete*](../secgloss/s-gly.md) werden in einem der folgenden Typen von Dynamic Link Libraries (DLLs) bereitgestellt:

-   [SSP/APs](#sspaps-vs-ssps)
-   [Ssps](#sspaps-vs-ssps)

Ob sich ein Sicherheitspaket in einem Sicherheitssupportanbieter/-Authentifizierungspaket [*(Security*](../secgloss/a-gly.md) Support Provider, SSP/AP) oder einer SSP-DLL (Security [*Support*](../secgloss/s-gly.md) Provider) befindet, richtet sich nach den Typen der bereitgestellten Sicherheitsdienste und dem Umfang, in dem eine Integration in die lokale Sicherheitsstelle [*(LSA)*](../secgloss/l-gly.md) erforderlich ist. Diese Unterschiede bestimmen auch die API, die in einem benutzerdefinierten Sicherheitspaket implementiert ist.

## <a name="sspaps"></a>SSP/APs

Ein SSP/AP ist eine DLL, [](../secgloss/s-gly.md) die mindestens ein Sicherheitspaket enthält und als SSP für Client-/Serveranwendungen und als Authentifizierungspaket für Anmeldeanwendungen verwendet werden kann. [](authentication-packages.md) Um in beiden Rollen zu funktionieren, werden SSP/APs beim Systemstart in den LSA-Prozessbereich geladen und können auch in Client-/Serveranwendungsprozesse geladen werden.

Benutzerdefinierte SSP/AP-Sicherheitspakete müssen sowohl die Funktionen implementieren, die von [SSP/APs](authentication-functions.md)im Benutzermodus implementiert werden, als auch funktionen, die von [SSP/APs implementiert werden.](authentication-functions.md) Diese Funktionsimplementierungen können LSA-Unterstützungsfunktionen nutzen, um [](../secgloss/s-gly.md) erweiterte Sicherheitsfeatures wie die Tokenerstellung, die Unterstützung zusätzlicher Anmeldeinformationen und die Pass-Through-Authentifizierung zu bieten.

Wenn ein benutzerdefiniertes SSP/AP-Sicherheitspaket [](../secgloss/i-gly.md) den vollständigen Bereich der Nachrichtenintegritäts- und Datenschutzfunktionen bietet, implementiert es auch die Funktionen, die von [SSP/APs](authentication-functions.md)im Benutzermodus implementiert werden.

## <a name="ssps"></a>Ssps

Ein SSP ist eine DLL, die ein oder mehrere Sicherheitspakete enthält, die authentifizierte Verbindungen, Nachrichtenintegrität und Nachrichtenverschlüsselungsdienste für Client-/Serveranwendungen bereitstellen. SSPs implementieren SSPI-Funktionen [(Security Support Provider Interface).](sspi.md) Anwendungen können auf die Sicherheitspakete in einem SSP zugreifen, indem sie die SSPI-Funktionen direkt aufrufen. SSPs werden in die Client- und Serverprozesse geladen. sie sind nicht in das LSA integriert.

 

 
