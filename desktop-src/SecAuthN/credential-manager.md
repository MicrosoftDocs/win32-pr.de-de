---
description: Ein Anmelde Informations Verwalter ähnelt einem Netzwerkanbieter darin, dass er Einstiegspunkte bereitstellt, die vom Multianbieter Router (MPR) aufgerufen werden. Tatsächlich sind einige Netzwerkanbieter auch Anmelde Informationen-Manager.
ms.assetid: a1105754-a57f-4a0d-9797-bec22b99900c
title: Anmeldeinformationsverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20165a5e6145de0a2c042c38923c41d793bd641d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042488"
---
# <a name="credential-manager"></a>Anmeldeinformationsverwaltung

Ein Anmelde Informations Verwalter ähnelt einem Netzwerkanbieter darin, dass er Einstiegspunkte bereitstellt, die vom [*Multianbieter Router*](/windows/desktop/SecGloss/m-gly) (MPR) aufgerufen werden. Tatsächlich sind einige Netzwerkanbieter auch Anmelde Informationen-Manager.

Ob Sie die Funktionen zur Verwaltung von Anmelde Informationen in derselben DLL wie die Netzwerkanbieter Funktionen implementieren, hängt von den Anforderungen der Anwendung ab. Anmelde Informationsmanager erhalten Benachrichtigungen, wenn sich Authentifizierungsinformationen ändern. Anmelde Informationsmanager werden z. b. benachrichtigt, wenn sich ein Benutzer anmeldet oder ein Konto Kennwort geändert wird. Wenn sich bei einem Anmeldevorgang, z. b. [*Winlogon*](/windows/desktop/SecGloss/w-gly), das anmelden oder Ändern des Kennworts für ein Konto befindet, wird die entsprechende MPR-Windows-Netzwerkfunktion (WNET) aufgerufen. Der MPR ruft dann den entsprechenden Einstiegspunkt für jeden Anmelde Informationen-Manager auf. Diese Funktionen für die Verwaltung von Anmelde Informationen werden immer im Systemkontext "LocalSystem" statt im Benutzer Kontext aufgerufen. Weitere Informationen zu WNET-Funktionen finden Sie unter [Windows-Netzwerke](/windows/desktop/WNet/windows-networking-wnet-). Weitere Informationen über die Schnittstelle, die Anmelde Informations-Manager implementieren müssen, finden Sie unter [**Anmelde Informationen Management-API**](credential-management-api.md).

 

 
