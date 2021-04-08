---
description: Die Anbieter Winlogon, Gina und Network sind die Teile des interaktiven Anmelde Modells.
ms.assetid: d049d83f-b962-4c47-a79a-da556831e319
title: Winlogon und Gina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a683077f275dc9bf38efca6649cbd8131e0b9334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862392"
---
# <a name="winlogon-and-gina"></a>Winlogon und Gina

Die Anbieter [*Winlogon*](../secgloss/w-gly.md), [*Gina*](../secgloss/g-gly.md)und Network sind die Teile des interaktiven Anmelde Modells. Das interaktive Anmeldeverfahren wird normalerweise von Winlogon-, MSGina.dll-und Netzwerkanbietern gesteuert. Um das interaktive Anmeldeverfahren zu ändern, können MSGina.dll durch eine angepasste Gina-dll ersetzt werden.

Um mit Winlogon, dem Gina und den Netzwerkanbietern arbeiten zu können, sollten Sie über eine starke Kenntnis der Windows-Sicherheitsarchitektur verfügen, insbesondere in Bezug auf [*Token*](../secgloss/a-gly.md), [*Authentifizierungs Pakete*](../secgloss/a-gly.md)und verwandte Aspekte.

> [!Note]  
> Gina-DLLs werden in Windows Vista ignoriert.

 

Informationen zu bestimmten Funktionen und Strukturen finden Sie unter [Authentifizierungs Referenz](authentication-reference.md). Dieser Referenz Abschnitt enthält Beschreibungen der Funktionen, die eine Gina-DLL implementieren muss, die von der Gina-DLL aufzurufenden Winlogon-Unterstützungsfunktionen und die Datenstrukturen, die zum Übergeben von Informationen zwischen Winlogon und Gina verwendet werden.

Ein Beispiel für Gina-Code finden Sie in den Sicherheits Beispielen für das Platform Software Development Kit (SDK). Die Beispiele enthalten C-Code für die Implementierung eines Gina-Stubs und eines Gina-Hooks. Weitere Informationen zur benutzerdefinierten Gina DLL-Entwicklung erhalten Sie, wenn Sie eine e-Mail-Nachricht an senden ginareqs@microsoft.com .

Weitere Informationen über das von Windows unterstützte Authentifizierungs Modell und ausführliche Informationen zu den Diensten der [*lokalen Sicherheits Autorität*](../secgloss/l-gly.md) (LSA) und zu [*Authentifizierungs Paketen*](../secgloss/a-gly.md) finden Sie unter [LSA-Authentifizierung](lsa-authentication.md).

Informationen zu den Aspekten der lokalen Sicherheits Autorität, die sich auf die Verwaltung der Sicherheitsrichtlinien beziehen, einschließlich Vertrauens Stellungen mit anderen Computern und Domänen, der Zuweisung von Berechtigungen, der Steuerung der Überwachungs Generierung, der systembarrierefreiheit und anderen ähnlichen Themen finden Sie unter [LSA Policy](../secmgmt/lsa-policy.md).

Weitere Informationen zu Winlogon und Gina finden Sie in den folgenden Themen.



| Thema                                                                              | BESCHREIBUNG                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Winlogon](winlogon.md)                                                           | Winlogon bietet eine Reihe von Unterstützungsfunktionen für die Gina-DLL.<br/>                                                                                                                                                                 |
| [Gina](gina.md)                                                                   | Eine Gina-dll bietet anpassbare benutzeridentifizierungs-und Authentifizierungsverfahren.<br/>                                                                                                                                            |
| [Terminal Dienste-Gina-Funktionen](terminal-services-gina-functions.md)           | Wenn terminaldienstedienste aktiviert sind, muss die Gina Winlogon-Unterstützungsfunktionen anrufen, um verschiedene Aufgaben auszuführen.<br/>                                                                                                                   |
| [Interaktion mit Netzwerkanbietern](interaction-with-network-providers.md)       | Sie können ein System so konfigurieren, dass NULL oder mehr Netzwerkanbieter unterstützt werden.<br/>                                                                                                                                                          |
| [Zuständigkeiten und Features](responsibilities-and-features.md)                 | Jeder Teil des interaktiven Anmelde Prozesses hat eine Reihe von Zuständigkeiten.<br/>                                                                                                                                                      |
| [Interaktion zwischen Winlogon und Gina](interaction-between-winlogon-and-gina.md) | Der Status von Winlogon bestimmt, welche Gina-Funktion aufgerufen wird, um ein bestimmtes SAS-Ereignis ( [*Secure Attention Sequence*](../secgloss/s-gly.md) ) zu verarbeiten.<br/> |
| [Winlogon-Benachrichtigungs Pakete](winlogon-notification-packages.md)               | Sie können ein Benachrichtigungs Paket implementieren, um Winlogon-Ereignisse zu überwachen und darauf zu reagieren.<br/>                                                                                                                                            |



 

 

 
