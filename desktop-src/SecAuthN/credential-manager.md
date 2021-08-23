---
description: Ein Anmeldeinformations-Manager ähnelt einem Netzwerkanbieter, da er Einstiegspunkte bietet, die vom Multiple Provider Router (MPR) aufgerufen werden. Tatsächlich sind einige Netzwerkanbieter auch Anmeldeinformations-Manager.
ms.assetid: a1105754-a57f-4a0d-9797-bec22b99900c
title: Anmeldeinformationsverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a33b1a47ff17123a1974823d7fee1421df7755850d46d2992fec51f62f5fac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008828"
---
# <a name="credential-manager"></a>Anmeldeinformationsverwaltung

Ein Anmeldeinformations-Manager ähnelt einem Netzwerkanbieter, da er Einstiegspunkte bietet, die vom [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) aufgerufen werden. Tatsächlich sind einige Netzwerkanbieter auch Anmeldeinformations-Manager.

Ob Sie die Verwaltungsfunktionen für Anmeldeinformationen in derselben DLL wie die Netzwerkanbieterfunktionen implementieren, hängt von den Anforderungen Ihrer Anwendung ab. Anmeldeinformations-Manager erhalten Benachrichtigungen, wenn sich Authentifizierungsinformationen ändern. Beispielsweise werden Anmeldeinformations-Manager benachrichtigt, wenn sich ein Benutzer anmeldet oder sich ein Kontokennwort ändert. Wenn sich ein Anmeldevorgang wie [*Winlogon*](/windows/desktop/SecGloss/w-gly)anmeldet oder das Kennwort für ein Konto ändert, ruft er die entsprechende MPR-Funktion Windows Networking (WNet) auf. Der MPR ruft dann den entsprechenden Einstiegspunkt für jeden Anmeldeinformations-Manager auf. Diese Verwaltungsfunktionen für Anmeldeinformationen werden immer im Systemkontext LocalSystem und nicht im Benutzerkontext aufgerufen. Weitere Informationen zu WNet-Funktionen finden Sie unter [Windows Networking](/windows/desktop/WNet/windows-networking-wnet-). Weitere Informationen zur Schnittstelle, die Anmeldeinformations-Manager implementieren müssen, finden Sie unter [**Anmeldeinformationen Verwaltungs-API.**](credential-management-api.md)

 

 
