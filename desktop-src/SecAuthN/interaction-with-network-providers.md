---
description: Erläutert die Interaktionen zwischen Winlogon und Netzwerkanbietern.
ms.assetid: 09d0b5ce-e2ac-40d7-bc35-272c5f831788
title: Interaktion mit Netzwerkanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d3eeadb7a9f4d8137e1d9b1ef7ff2430910cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867856"
---
# <a name="interaction-with-network-providers"></a>Interaktion mit Netzwerkanbietern

Sie können ein System so konfigurieren, dass NULL oder mehr Netzwerkanbieter unterstützt werden. Jeder dieser Netzwerkanbieter kann angeben, dass eine besondere interaktive Authentifizierungs Verarbeitung erforderlich ist. Diese Funktion ermöglicht es installierten Netzwerken, Identifikations-und Authentifizierungsinformationen für jedes Netzwerk zu erfassen. Sie können Sie aber auch während der normalen Anmeldung und unter dem sicheren Sonnenschirm des [*Kontexts*](../secgloss/c-gly.md) und Desktops von [*Winlogon*](../secgloss/w-gly.md) erfassen.

Winlogon Ruft unter mehreren Umständen Netzwerkanbieter auf. Nach einer erfolgreichen Anmeldung Ruft die Winlogon Netzwerkanbieter auf, damit Sie [*Anmelde*](../secgloss/c-gly.md) Informationen erfassen und den Benutzer für Ihr Netzwerk authentifizieren können. Winlogon ruft auch Netzwerkanbieter auf, wenn Benutzer ihre Kenn Wörter ändern. Dadurch kann jeder Benutzer ein einzelnes Kennwort für die Verwendung in allen Netzwerken verwalten.

Die [**wlx \_ MPR \_ Notify \_ Info**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) -Struktur wird verwendet, um Identifikations-und Authentifizierungsinformationen in den relevanten Gina-Funktionen bereitzustellen. Diese Struktur enthält die folgenden Member.



| Member             | BESCHREIBUNG                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **pszusername**    | Der Kontoname des angemeldeten Benutzers.                                                                                                                                                      |
| **pszdomain**      | Der Domänen Name des angemeldeten Benutzers. Nicht alle Authentifizierungs Modelle verfügen über ein Domänen Konzept (oder das entsprechende), sodass dieser Member **null** sein kann.                                              |
| **pszpassword**    | Wenn der Benutzer während der Authentifizierung ein Klartext-Kennwort angegeben hat, können andere Netzwerkanbieter das gleiche Kennwort verwenden (um die einmalige Anmeldung zu erreichen), ohne den Benutzer aufzufordern.    |
| **pszoldpassword** | Wenn Sie nach einer Kenn Wort Änderung das ursprüngliche Kennwort und das neue Kennwort im **pszpassword** -Mitglied bereitstellen, können Netzwerkanbieter ihre Kenn Wörter aktualisieren, ohne den Benutzer aufzufordern. |



 

Eine [*Gina*](../secgloss/g-gly.md) muss diese Informationen nicht für Netzwerkanbieter bereitstellen. Wenn ein **null** -Zeiger anstelle eines gültigen Struktur Zeigers übermittelt wird, fordert der Netzwerkanbieter den Benutzer zur Eingabe von Informationen auf.

 

 
