---
description: Der Dienststeuerungs-Manager (Service Control Manager, SCM) verwaltet eine Datenbank mit installierten Diensten und Treiberdiensten und bietet eine einheitliche und sichere Möglichkeit, diese zu steuern.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: Informationen zu Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58bcd2058ec8f8de5cbe56a521e2d83919a17532c00dab175d93305edd3684d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126480"
---
# <a name="about-services"></a>Informationen zu Diensten

Der [Dienststeuerungs-Manager](service-control-manager.md) (Service Control Manager, SCM) verwaltet eine Datenbank mit installierten Diensten und Treiberdiensten und bietet eine einheitliche und sichere Möglichkeit, diese zu steuern. Die Datenbank enthält Informationen dazu, wie die einzelnen Dienste oder Treiberdienste gestartet werden sollen. Außerdem können Systemadministratoren die Sicherheitsanforderungen für jeden Dienst anpassen und so den Zugriff auf den Dienst steuern.

Die folgenden Programmtypen verwenden die vom SCM bereitgestellten Funktionen.



| type                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dienstprogramm               | Ein Programm, das ausführbaren Code für einen oder mehrere Dienste bietet. Dienstprogramme verwenden Funktionen, die eine Verbindung mit dem SCM herstellen und Statusinformationen an den SCM senden.                                                                                                                                                                          |
| Dienstkonfigurationsprogramm | Ein Programm, das die Dienstdatenbank abfragt oder ändert. Dienstkonfigurationsprogramme verwenden Funktionen, die die Datenbank öffnen, Dienste in der Datenbank installieren oder löschen und die Konfigurations- und Sicherheitsparameter für installierte Dienste abfragen oder ändern. Dienstkonfigurationsprogramme verwalten sowohl Dienste als auch Treiberdienste. |
| Dienststeuerungsprogramm       | Ein Programm, das Dienste und Treiberdienste startet und steuert. Dienststeuerungsprogramme verwenden Funktionen, die Anforderungen an den SCM senden, der die Anforderung erfüllt.                                                                                                                                                                     |



 

In dieser Übersicht werden die folgenden Themen erläutert:

-   [Dienststeuerungs-Manager](service-control-manager.md)
-   [Dienstprogramme](service-programs.md)
-   [Dienstkonfigurationsprogramme](service-configuration-programs.md)
-   [Dienststeuerungsprogramme](service-control-programs.md)
-   [Dienstbenutzerkonten](service-user-accounts.md)
-   [Interaktive Dienste](interactive-services.md)
-   [Dienstsicherheit und Zugriffsrechte](service-security-and-access-rights.md)
-   [Debugging a Service (Debuggen eines Diensts)](debugging-a-service.md)
-   [Diensttriggerereignisse](service-trigger-events.md)

 

 



