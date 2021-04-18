---
title: Informationen zur Remote Zugriffs Dienst-Verwaltung
description: Windows 2000 und spätere Betriebssysteme stellen eine Reihe von Funktionen für die Verwaltung von Benutzerberechtigungen und Ports auf RAS-Servern bereit.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- RRAS für den Routing-und RAS-Dienst, RAS-Verwaltung
- RRAS für den Routing-und RAS-Dienst, RAS-Verwaltung, beschrieben
- RAS-Verwaltungs-RRAS
- RRAS für RAS-Verwaltung, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bdb55049e99b6d3df9980fc35879341b488531
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337788"
---
# <a name="about-remote-access-service-administration"></a>Informationen zur Remote Zugriffs Dienst-Verwaltung

Windows 2000 und spätere Betriebssysteme stellen eine Reihe von Funktionen für die Verwaltung von Benutzerberechtigungen und Ports auf RAS-Servern bereit. Mithilfe dieser Funktionen können Sie eine RAS-Server-Verwaltungs Anwendung entwickeln, um die folgenden Aufgaben auszuführen:

-   Listet die Benutzer auf, die über einen angegebenen Satz von RAS-Berechtigungen verfügen.
-   Zuweisen oder widerrufen von RAS-Berechtigungen für einen angegebenen Benutzer
-   Auflisten der konfigurierten Ports auf einem RAS-Server
-   Informationen und Statistiken zu einem angegebenen Port auf einem RAS-Server
-   Zurücksetzen der Statistik Zähler für einen angegebenen Port
-   Trennen der Verbindung mit einem angegebenen Port

Sie können auch eine RAS-Server-Verwaltungs-dll zum Überwachen von Benutzer Verbindungen und Zuweisen von IP-Adressen zu einwählbenutzern installieren. Die dll exportiert eine Reihe von Funktionen, die der RAS-Server aufruft, wenn ein Benutzer versucht, eine Verbindung herzustellen oder die Verbindung zu trennen.

In dieser Dokumentation werden die folgenden Themen beschrieben:

-   [Funktions Vergleich: Windows 2000 und RRAS Redistributable](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [RAS-Benutzerverwaltung](ras-user-administration.md)
-   [RAS-Server und-Port Verwaltung](ras-server-and-port-administration.md)
-   [RAS-Verwaltungs-dll](ras-administration-dll.md)
-   [Registrierungs Einrichtung der RAS-Verwaltungs-dll](ras-administration-dll-registry-setup.md)

 

 




