---
title: Benutzer Funktionen für Arbeitsstationen und Arbeitsstationen
description: Die Arbeitsstationen der Netzwerk Verwaltungs Arbeitsstation führen administrative Aufgaben auf einer lokalen oder Remote Arbeitsstation aus.
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd445746bca51abaa0cd72877bdf03dd4d00d338
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339509"
---
# <a name="workstation-and-workstation-user-functions"></a>Benutzer Funktionen für Arbeitsstationen und Arbeitsstationen

Die Arbeitsstationen der Netzwerk Verwaltungs Arbeitsstation führen administrative Aufgaben auf einer lokalen oder Remote Arbeitsstation aus. Nur ein Benutzer oder eine Anwendung mit Administrator Gruppenmitgliedschaft auf einem lokalen Server oder einem Remote Server kann administrative Aufgaben auf einer Arbeitsstation ausführen, um den Betrieb, den Benutzer Zugriff und die Ressourcen Freigabe zu steuern. Weitere Informationen zum Aufrufen von Funktionen, für die Administratorrechte erforderlich sind, finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).

Die Arbeitsstations Funktionen sind nachfolgend aufgeführt.



| Funktion                                   | BESCHREIBUNG                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [**Netwkstagetinfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | Gibt Informationen zu den Konfigurationselementen für eine Arbeitsstation zurück. |
| [**Netwkstasetinfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | Konfiguriert eine Arbeitsstation.                                               |



 

Die Arbeitsstations Funktionen ermöglichen den Zugriff auf zwei diskrete Typen von Arbeitsstations Informationen:

-   Systeminformationen
-   Plattformspezifische Informationen

Innerhalb jedes Typs werden die Daten nach Sicherheits Zugriff kategorisiert. Daten, auf die der Gast Zugriff hat, sind eine Teilmenge der Daten, auf die der Benutzer zugreifen kann, was wiederum eine Teilmenge der Daten ist, auf die vom Administrator zugegriffen werden kann.

Arbeitsstations Informationen sind auf folgenden Ebenen verfügbar:

-   [**Wksta- \_ Informationen \_ 100**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [**Wksta- \_ Informationen \_ 101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [**Wksta- \_ Informationen \_ 102**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

Die Benutzer Funktionen der Netzwerk Verwaltungs Arbeitsstation ermöglichen den Zugriff auf benutzerspezifische Informationen. Die benutzerspezifischen Informationen werden von den Arbeitsstations Informationen getrennt, da es mehr als einen Benutzer auf einer Arbeitsstation geben kann.

Die Benutzer Funktionen der Arbeitsstation sind nachfolgend aufgeführt.



| Funktion                                           | BESCHREIBUNG                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Netwkstauserereration**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | Listet Informationen zu allen Benutzern, die zurzeit auf der Arbeitsstation angemeldet sind.           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | Gibt Informationen zu einem aktuell angemeldeten Benutzer zurück.                             |
| [**Netwkstauserot**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | Legt die benutzerspezifischen Informationen für die Konfigurationselemente einer Arbeitsstation fest. |



 

Die Benutzerinformationen für die Arbeitsstation sind auf folgenden Ebenen verfügbar:

-   [**Wksta- \_ Benutzer \_ Informationen \_ 0**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [**Wksta- \_ Benutzer \_ Informationen \_ 1**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [**Wksta- \_ Benutzer \_ Informationen \_ 1101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 