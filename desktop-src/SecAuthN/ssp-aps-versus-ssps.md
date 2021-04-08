---
description: Erläutert die Unterschiede zwischen SSP/APS und SSPs.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/APS im Vergleich zu SSPs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d089a27da6b0ab5d4228af924f738f27a1d728
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960385"
---
# <a name="sspaps-vs-ssps"></a>SSP/APS im Vergleich zu SSPs

[*Sicherheitspakete*](../secgloss/s-gly.md) werden in einem der folgenden Typen von Dynamic Link Libraries (DLLs) bereitgestellt:

-   [SSP/APS](#sspaps-vs-ssps)
-   [SSPs](#sspaps-vs-ssps)

Ob sich ein Sicherheitspaket in einem Security Support Provider-[*/Authentifizierungspaket*](../secgloss/a-gly.md) (SSP/AP) oder einer [*Security Support Provider*](../secgloss/s-gly.md) (SSP)-dll befindet, hängt von den Typen der Sicherheitsdienste ab, die es bereitstellt, sowie davon, in welchem Umfang eine Integration in die [*Lokale Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) Diese Unterschiede legen außerdem fest, welche API in einem benutzerdefinierten Sicherheitspaket implementiert ist.

## <a name="sspaps"></a>SSP/APS

Ein SSP/AP ist eine DLL, die mindestens ein [*Sicherheitspaket*](../secgloss/s-gly.md) enthält und als SSP für Client-/Server-Anwendungen und als [Authentifizierungs Paket](authentication-packages.md) für Anmelde Anwendungen fungieren kann. Um in beiden Rollen zu funktionieren, werden SSP/APS beim Systemstart in den LSA-Prozessbereich geladen und können auch in Client/Server-Anwendungsprozesse geladen werden.

Benutzerdefinierte SSP/AP-Sicherheitspakete müssen sowohl die Funktionen implementieren, die [von SSP/APS im Benutzermodus implementiert](authentication-functions.md)werden, als auch Funktionen, die [von SSP/APS implementiert](authentication-functions.md)werden. Diese Funktions Implementierungen können LSA-Unterstützungsfunktionen verwenden, um erweiterte Sicherheitsfunktionen wie die Tokenerstellung, [*ergänzende Anmelde*](../secgloss/s-gly.md) Informationen und die Passthrough-Authentifizierung bereitzustellen.

Wenn ein benutzerdefiniertes SSP/AP-Sicherheitspaket den vollständigen Bereich der Nachrichten [*Integrität*](../secgloss/i-gly.md) und Datenschutzfunktionen bereitstellt, werden auch die Funktionen implementiert, die [von SSP/APS im Benutzermodus implementiert](authentication-functions.md)werden.

## <a name="ssps"></a>SSPs

Ein SSP ist eine DLL-Datei, die mindestens ein Sicherheitspaket enthält, das authentifizierte Verbindungen, Nachrichten Integrität und Nachrichten Verschlüsselungsdienste für Client-/Serveranwendungen bereitstellt. SSPs implementieren SSPI-Funktionen ( [Security Support Provider Interface](sspi.md) ). Anwendungen können auf die Sicherheitspakete in einem SSP zugreifen, indem Sie die SSPI-Funktionen direkt aufrufen. SSPs werden in die Client-und Server Prozesse geladen; Sie sind nicht in die LSA integriert.

 

 
