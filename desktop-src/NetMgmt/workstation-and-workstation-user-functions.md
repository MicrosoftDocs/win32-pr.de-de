---
title: Arbeitsstations- und Arbeitsstationsbenutzerfunktionen
description: Die Arbeitsstationsfunktionen der Netzwerkverwaltung führen administrative Aufgaben auf einer lokalen Arbeitsstation oder einer Remotearbeitsstation aus.
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d156c062bf65cafd96bbb1dffe3f89333ad9732b1760209dfc3d6f473d1a94c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983067"
---
# <a name="workstation-and-workstation-user-functions"></a>Arbeitsstations- und Arbeitsstationsbenutzerfunktionen

Die Arbeitsstationsfunktionen der Netzwerkverwaltung führen administrative Aufgaben auf einer lokalen Arbeitsstation oder einer Remotearbeitsstation aus. Nur ein Benutzer oder eine Anwendung mit Administratorgruppenmitgliedschaft auf einem lokalen Server oder Remoteserver kann administrative Aufgaben auf einer Arbeitsstation ausführen, um den Betrieb, den Benutzerzugriff und die Ressourcenfreigabe zu steuern. Weitere Informationen zum Aufrufen von Funktionen, die Administratorrechte erfordern, finden Sie unter [Ausführen mit speziellen Berechtigungen.](/windows/desktop/SecBP/running-with-special-privileges)

Die Arbeitsstationsfunktionen sind im Folgenden aufgeführt.



| Funktion                                   | Beschreibung                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | Gibt Informationen zu den Konfigurationselementen für eine Arbeitsstation zurück. |
| [**NetWkstaSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | Konfiguriert eine Arbeitsstation.                                               |



 

Die Arbeitsstationsfunktionen ermöglichen den Zugriff auf zwei diskrete Typen von Arbeitsstationsinformationen:

-   Systeminformationen
-   Plattformspezifische Informationen

Innerhalb jedes Typs werden die Daten nach Sicherheitszugriff kategorisiert. Daten, auf die auf Gastbenutzer zugegriffen werden kann, sind eine Teilmenge der Daten, auf die der Benutzer zugriffen kann. Dies ist wiederum eine Teilmenge der Daten, auf die der Administrator zugriff kann.

Informationen zur Arbeitsstation sind auf den folgenden Ebenen verfügbar:

-   [**WKSTA \_ INFO \_ 100**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [**WKSTA \_ INFO \_ 101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [**WKSTA \_ INFO \_ 102**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

Die Benutzerfunktionen der Netzwerkverwaltungsarbeitsstation ermöglichen den Zugriff auf benutzerspezifische Informationen. Die benutzerspezifischen Informationen sind von den Arbeitsstationsinformationen getrennt, da auf einer Arbeitsstation mehrere Benutzer enthalten sein können.

Die Arbeitsstationsbenutzerfunktionen sind im Folgenden aufgeführt.



| Funktion                                           | Beschreibung                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | Listet Informationen zu allen Benutzern auf, die derzeit an der Arbeitsstation angemeldet sind.           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | Gibt Informationen zu einem derzeit angemeldeten Benutzer zurück.                             |
| [**NetWkstaUserSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | Legt die benutzerspezifischen Informationen für die Konfigurationselemente einer Arbeitsstation fest. |



 

Benutzerinformationen zur Arbeitsstation sind auf den folgenden Ebenen verfügbar:

-   [**\_WKSTA-BENUTZERINFORMATIONEN \_ \_ 0**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [**\_WKSTA-BENUTZERINFORMATIONEN \_ \_ 1**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [**\_WKSTA-BENUTZERINFORMATIONEN \_ \_ 1101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 