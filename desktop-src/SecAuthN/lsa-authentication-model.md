---
description: Erläutert das LSA-Authentifizierungsmodell.
ms.assetid: 0b2b868f-51a7-4f74-be4f-5f8db04d43ad
title: LSA-Authentifizierungsmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3762595332252c22141aebdc7f3ecbe168e49a83795830a0cb03e49eb5da73ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140943"
---
# <a name="lsa-authentication-model"></a>LSA-Authentifizierungsmodell

Das Authentifizierungsmodell der [*lokalen Sicherheitsautorität*](../secgloss/l-gly.md) (Local Security Authority, LSA) verfügt über die folgenden Features:

-   Die LSA-Authentifizierung unterstützt benutzerdefinierte [Authentifizierungspakete.](authentication-packages.md) Dadurch können Endkunden und unabhängige Softwarehersteller (Independent Software Vendors, ISVs) Authentifizierungsroutinen anpassen oder ersetzen, um Anforderungen zu erfüllen, die über die standardbasierten Microsoft-Authentifizierungspakete hinausgehen. Während die von Microsoft bereitgestellten Authentifizierungspakete Einen Benutzernamen und Kennwortanmeldedaten erfordern, kann ein benutzerdefiniertes Authentifizierungspaket andere Formen von Anmeldedaten annehmen, z. B. AtM-Karteninformationen und eine persönliche Identifikationsnummer (PIN). Ein benutzerdefiniertes Authentifizierungspaket kann auch verwendet werden, um ein neues [*Sicherheitsprotokoll*](../secgloss/s-gly.md)zu implementieren.
-   Die LSA unterstützt benutzerdefinierte Sicherheitspakete, die als Anbieter für die Sicherheitsunterstützung für verteilte Anwendungen und als Authentifizierungspakete für Anwendungen fungieren, die Authentifizierungsdienste erfordern. Der Zugriff auf die Authentifizierungsfunktionalität erfolgt über die gleiche Schnittstelle wie bei einem eigenständigen Authentifizierungspaket, während auf die Funktionalität des Sicherheitssupportanbieters über die [Security Support Provider Interface](sspi.md) (SSPI) zugegriffen wird. Der Satz von LSA-Unterstützungsfunktionen, die für benutzerdefinierte Sicherheitspakete verfügbar sind, ermöglicht es ihnen, erweiterte Sicherheitsfeatures wie die Tokenerstellung und [*die zusätzliche Verwaltung von Anmeldeinformationen*](../secgloss/s-gly.md) zur Verfügung zu stellen.
-   Das LSA unterstützt die heterogene Verwaltung von Anmeldeinformationen für die Schnittstellen mit Nicht-Microsoft-Produkten wie Netzwerken und Datenbanken. Da solche Produkte häufig über eigene Sicherheitsanmeldeinformationen verfügen, stellt die LSA Funktionen bereit, mit denen Authentifizierungspakete Nicht-Microsoft-Anmeldeinformationen Windows Prozessen zuordnen können. Benutzerdefinierte Authentifizierungspakete können Dienste zum Abfragen dieser Anmeldeinformationen bei Bedarf bereitstellen, z. B. wenn ein Netzwerkumleitungsversuch versucht, eine Verbindung mit einem Remotesystem herzustellen.
-   Jede Klasse von Anmeldegeräten, die auf einem System installiert sind, kann über einen eigenen Anmeldeprozess verfügen. Geräteklassen enthalten in der Regel Geräte wie Smartcardleser. Für die [*LSA-Authentifizierung*](../secgloss/l-gly.md) werden verbundene Netzwerke jedoch auch als Geräte behandelt. Standardmäßig stellt das Windows Betriebssystem den Anmeldevorgang bereit, der Benutzernamen- und Kennwortanmeldungen über eine Tastatur unterstützt. Entwickler können Unterstützung für andere Geräte hinzufügen, z. B. [](../secgloss/s-gly.md) [*Smartcardleser.*](../secgloss/r-gly.md) Weitere Informationen zu Smartcards finden Sie unter [Smartcard-Authentifizierung.](smart-card-authentication.md) Weitere Informationen zur Unterstützung von Anmeldegeräten finden Sie unter [Winlogon und GINA.](winlogon-and-gina.md)

 

 
