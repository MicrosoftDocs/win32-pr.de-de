---
description: Erläutert die zwei Arten von Anmelde Informationen, mit denen die Anmelde Informations Verwaltungs-API funktioniert.
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: Arten von Anmelde Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30968484b2cfc89b9238f624d9299fb75c72bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959919"
---
# <a name="kinds-of-credentials"></a>Arten von Anmelde Informationen

Die Verwaltungs-API für Anmelde Informationen funktioniert mit zwei Arten von Anmelde Informationen:

-   [Anmeldeinformationen für die Domäne](#domain-credentials)
-   [Generische Anmelde Informationen](#generic-credentials)

## <a name="domain-credentials"></a>Anmeldeinformationen für die Domäne

Domänen Anmelde Informationen werden vom Betriebssystem verwendet und von der lokalen Sicherheits Autorität (Local Security Authority, LSA) authentifiziert. In der Regel werden Domänen Anmelde Informationen für einen Benutzer eingerichtet, wenn ein registriertes Sicherheitspaket, z. b. das Kerberos-Protokoll, Anmeldedaten authentifiziert, die vom Benutzer bereitgestellt werden. Die Anmelde Informationen werden vom Betriebssystem zwischengespeichert, sodass eine Single Sign-on dem Benutzer den Zugriff auf viele verschiedene Ressourcen gewährt. Beispielsweise können Netzwerkverbindungen transparent erfolgen, und der Zugriff auf geschützte Systemobjekte kann basierend auf den zwischengespeicherten Domänen Anmelde Informationen des Benutzers erteilt werden.

Verwaltungsfunktionen für Anmelde Informationen bieten einen Mechanismus, mit dem Anwendungen nach der Anmeldung des Benutzers Anmelde Informationen für die Domäne eingeben und das Betriebssystem die vom Benutzer bereitgestellten Informationen authentifizieren können.

Der geheime Teil der Domänen Anmelde Informationen, das Kennwort, wird durch das Betriebssystem geschützt. Nur Code, der in-Process mit der LSA ausgeführt wird, kann Domänen Anmelde Informationen lesen und schreiben. Anwendungen sind auf das Schreiben von Domänen Anmelde Informationen beschränkt.

Windows unterstützt die Erweiterte Verwendung von Smartcard-und Zertifikat Anmelde Informationen. Um die Sicherheit zu gewährleisten, speichert die Anmelde Informations Verwaltungs-API die Smartcard-PIN niemals auf dem Computer.

## <a name="generic-credentials"></a>Generische Anmelde Informationen

Generische Anmelde Informationen werden von Anwendungen definiert und authentifiziert, die die Autorisierung und Sicherheit direkt verwalten, anstatt diese Aufgaben an das Betriebssystem zu delegieren. Beispielsweise kann eine Anwendung verlangen, dass Benutzer einen Benutzernamen und ein Kennwort eingeben, die von der Anwendung bereitgestellt werden, oder ein [*Zertifikat*](../secgloss/c-gly.md) für den Zugriff auf eine Website bereitstellen.

Anwendungen verwenden Anmelde Informationen Verwaltungsfunktionen, um Benutzer zur Eingabe von Anwendungs definierten, generischen Anmelde Informationen, z. b. Benutzername, Zertifikat, Smartcard oder Kennwort, aufzufordern. Die vom Benutzer eingegebenen Informationen werden zur Authentifizierung an die Anwendung zurückgegeben.

Die Verwaltung von Anmelde Informationen ermöglicht die anpassbare Cache Verwaltung und die langfristige Speicherung allgemeiner Anmelde Informationen. Generische Anmelde Informationen können von Benutzer Prozessen gelesen und geschrieben werden.

 

 
