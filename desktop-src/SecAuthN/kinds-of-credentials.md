---
description: Erläutert die zwei Arten von Anmeldeinformationen, mit denen die Anmeldeinformationen Verwaltungs-API funktionieren.
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: Arten von Anmeldeinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d0e067b3918496310f3244153864abbf7548e5367569f4f2fbd06de40f207c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140933"
---
# <a name="kinds-of-credentials"></a>Arten von Anmeldeinformationen

Die Verwaltungs-API Anmeldeinformationen funktioniert mit zwei Arten von Anmeldeinformationen:

-   [Domänenanmeldeinformationen](#domain-credentials)
-   [Generische Anmeldeinformationen](#generic-credentials)

## <a name="domain-credentials"></a>Anmeldeinformationen für die Domäne

Domänenanmeldeinformationen werden vom Betriebssystem verwendet und von der lokalen Sicherheitsautorität (Local Security Authority, LSA) authentifiziert. In der Regel werden Domänenanmeldeinformationen für einen Benutzer eingerichtet, wenn ein registriertes Sicherheitspaket, z. B. das Kerberos-Protokoll, Anmeldedaten authentifiziert, die vom Benutzer bereitgestellt werden. Die Anmeldeinformationen werden vom Betriebssystem zwischengespeichert, sodass ein einmaliges Anmelden dem Benutzer Zugriff auf viele verschiedene Ressourcen gewährt. Netzwerkverbindungen können beispielsweise transparent erfolgen, und der Zugriff auf geschützte Systemobjekte kann basierend auf den zwischengespeicherten Domänenanmeldeinformationen des Benutzers gewährt werden.

Funktionen zur Verwaltung von Anmeldeinformationen stellen einen Mechanismus bereit, mit dem Anwendungen einen Benutzer zur Eingabe von Domänenanmeldeinformationen auffordern können, nachdem sich der Benutzer angemeldet hat, und damit das Betriebssystem die vom Benutzer bereitgestellten Informationen authentifiziert.

Der geheime Teil der Domänenanmeldeinformationen, das Kennwort, wird durch das Betriebssystem geschützt. Nur Code, der in-Process mit dem LSA ausgeführt wird, kann Domänenanmeldeinformationen lesen und schreiben. Anwendungen sind auf das Schreiben von Domänenanmeldeinformationen beschränkt.

Windows unterstützt die erweiterte Verwendung von Smartcard- und Zertifikatanmeldeinformationen. Um die Sicherheit zu gewährleisten, speichert die Anmeldeinformations-Verwaltungs-API niemals die Smartcard-PIN auf dem Computer.

## <a name="generic-credentials"></a>Generische Anmeldeinformationen

Generische Anmeldeinformationen werden von Anwendungen definiert und authentifiziert, die Autorisierung und Sicherheit direkt verwalten, anstatt diese Aufgaben an das Betriebssystem zu delegieren. Beispielsweise kann eine Anwendung erfordern, dass Benutzer einen Benutzernamen und ein Kennwort eingeben, die von der Anwendung bereitgestellt werden, oder ein [*Zertifikat*](../secgloss/c-gly.md) für den Zugriff auf eine Website erstellen.

Anwendungen verwenden Anmeldeinformationsverwaltungsfunktionen, um Benutzer zur Eingabe anwendungsdefinierter, generischer Anmeldeinformationen wie Benutzername, Zertifikat, Smartcard oder Kennwort aufzufordern. Die vom Benutzer eingegebenen Informationen werden zur Authentifizierung an die Anwendung zurückgegeben.

Credentials Management bietet anpassbare Cacheverwaltung und langfristige Speicherung für generische Anmeldeinformationen. Generische Anmeldeinformationen können von Benutzerprozessen gelesen und geschrieben werden.

 

 
