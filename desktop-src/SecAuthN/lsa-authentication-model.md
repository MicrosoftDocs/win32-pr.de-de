---
description: Erläutert das LSA-Authentifizierungs Modell.
ms.assetid: 0b2b868f-51a7-4f74-be4f-5f8db04d43ad
title: LSA-Authentifizierungs Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27f5a44a20284a7285eb7fcffe1d1f8f6bf1f286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363283"
---
# <a name="lsa-authentication-model"></a>LSA-Authentifizierungs Modell

Das Authentifizierungs Modell der [*lokalen Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) verfügt über die folgenden Features:

-   Die LSA-Authentifizierung unterstützt benutzerdefinierte [Authentifizierungs Pakete](authentication-packages.md). Dadurch können Endkunden und unabhängige Softwarehersteller (ISVs) Authentifizierungs Routinen anpassen oder ersetzen, um die Anforderungen zu erfüllen, die von den standardmäßigen Microsoft-Authentifizierungs Paketen bereitgestellt werden. Obwohl die von Microsoft bereitgestellten Authentifizierungs Pakete Benutzername und Kennwort-Anmeldedaten erfordern, kann ein benutzerdefiniertes Authentifizierungs Paket andere Formen von Anmeldedaten verwenden, z. b. ATM-Smartcardinformationen und eine persönliche Identifikationsnummer (PIN). Ein benutzerdefiniertes Authentifizierungs Paket kann auch zum Implementieren eines neuen [*Sicherheitsprotokolls*](../secgloss/s-gly.md)verwendet werden.
-   Die LSA unterstützt benutzerdefinierte Sicherheitspakete, die als Anbieter für Sicherheitsunterstützung für verteilte Anwendungen fungieren, und als Authentifizierungs Pakete für Anwendungen, die Authentifizierungsdienste erfordern. Der Zugriff auf die Authentifizierungs Funktionalität erfolgt über die gleiche Schnittstelle wie ein eigenständiges Authentifizierungs Paket, während auf die Security Support Provider Funktionalität mithilfe der [Security Support Provider-Schnittstelle (Security Support Provider Interface](sspi.md) , SSPI) zugegriffen wird. Der Satz von LSA-Unterstützungsfunktionen, die für benutzerdefinierte Sicherheitspakete verfügbar sind, ermöglicht Ihnen die Bereitstellung erweiterter Sicherheitsfunktionen, wie z. b. Tokenerstellung und [*ergänzende Anmelde*](../secgloss/s-gly.md) Informationen
-   Die LSA unterstützt die Verwaltung heterogener Anmelde Informationen, um mit nicht-Microsoft-Produkten wie Netzwerken und Datenbanken zu verbinden. Da solche Produkte häufig über eigene Sicherheits Anmelde Informationen verfügen, stellt die LSA Funktionen bereit, die Authentifizierungs Pakete verwenden können, um Windows-Prozessen nicht-Microsoft-Anmelde Informationen zuzuordnen. Benutzerdefinierte Authentifizierungs Pakete können bei Bedarf Dienste zum Abfragen dieser Anmelde Informationen bereitstellen, z. b. Wenn ein Netzwerk-Redirector versucht, eine Verbindung mit einem Remote System herzustellen.
-   Jede Klasse von LOGON-Geräten, die auf einem System installiert ist, kann über einen eigenen Anmeldevorgang verfügen. Geräteklassen enthalten in der Regelgeräte, z. b. Smartcardleser; im Hinblick auf die [*LSA*](../secgloss/l-gly.md) -Authentifizierung werden verbundene Netzwerke jedoch auch als Geräte behandelt. Standardmäßig stellt das Windows-Betriebssystem den Anmeldeprozess bereit, der die Anmeldung von Benutzernamen und Kenn Wörtern mithilfe einer Tastatur unterstützt. Entwickler können Unterstützung für andere Geräte hinzufügen, z. b. [*Smartcard*](../secgloss/s-gly.md) - [*Leser*](../secgloss/r-gly.md). Weitere Informationen zu Smartcards finden Sie unter [Smartcard-Authentifizierung](smart-card-authentication.md). Weitere Informationen zur Unterstützung von Anmelde Geräten finden Sie unter [Winlogon und Gina](winlogon-and-gina.md).

 

 
