---
description: Erläutert die Interaktionen zwischen Winlogon und Netzwerkanbietern.
ms.assetid: 09d0b5ce-e2ac-40d7-bc35-272c5f831788
title: Interaktion mit Netzwerkanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab78e17536df4446ac1f57291ec77bc6ba273a825b4911e4c8bee10d389e008f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015740"
---
# <a name="interaction-with-network-providers"></a>Interaktion mit Netzwerkanbietern

Sie können ein System so konfigurieren, dass keine oder mehrere Netzwerkanbieter unterstützt werden. Jeder dieser Netzwerkanbieter kann angeben, dass eine spezielle interaktive Authentifizierungsverarbeitung erforderlich ist. Diese Funktion ermöglicht es installierten Netzwerken, spezifische Identifikations- und Authentifizierungsinformationen für jedes Netzwerk zu sammeln, ermöglicht es ihnen jedoch, sie während der normalen Anmeldung und unter dem sicheren Schirm des Kontexts und Desktops von [*Winlogon*](../secgloss/w-gly.md) [](../secgloss/c-gly.md) zu erfassen.

Winlogon ruft Netzwerkanbieter unter verschiedenen Umständen auf. Nach einer erfolgreichen Anmeldung ruft Winlogon Netzwerkanbieter auf, damit sie Anmeldeinformationen sammeln und den Benutzer für sein Netzwerk authentifizieren können. [](../secgloss/c-gly.md) Winlogon ruft auch Netzwerkanbieter auf, wenn Benutzer ihre Kennwörter ändern. Dadurch kann jeder Benutzer ein einzelnes Kennwort für die Verwendung in allen Netzwerken verwalten.

Die [**WLX \_ MPR \_ NOTIFY \_ INFO-Struktur**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) wird verwendet, um Identifikations- und Authentifizierungsinformationen in den relevanten GINA-Funktionen zur Verfügung zu stellen. Diese Struktur enthält die folgenden Member.



| Member             | Beschreibung                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **pszUserName**    | Der Kontoname des angemeldeten Benutzers.                                                                                                                                                      |
| **pszDomain**      | Der Domänenname des angemeldeten Benutzers. Nicht alle Authentifizierungsmodelle verfügen über ein Domänenkonzept (oder das entsprechende), sodass dieser Member NULL sein **kann.**                                              |
| **pszPassword**    | Wenn der Benutzer während der Authentifizierung ein Klartextkennwort gegeben hat, können andere Netzwerkanbieter dasselbe Kennwort verwenden (um eine einmalige Anmeldung zu erreichen), ohne den Benutzer dazu aufzugeben.    |
| **pszOldPassword** | Nach einer Kennwortänderung können Netzwerkanbieter durch Die Angabe des ursprünglichen Kennworts hier und des neuen Kennworts im **pszPassword-Mitglied** ihre Kennwörter aktualisieren, ohne dass der Benutzer dazu aufgefordert wird. |



 

Eine [*GINA*](../secgloss/g-gly.md) muss diese Informationen nicht an Netzwerkanbieter bereitstellen. Wenn anstelle eines gültigen Strukturzeigers ein **NULL-Zeiger** übergeben wird, werden die Netzwerkanbieter den Benutzer zur Eingabe von Informationen auffordern.

 

 
