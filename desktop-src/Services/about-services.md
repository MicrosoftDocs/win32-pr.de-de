---
description: Der Dienststeuerungs-Manager (Service Control Manager, SCM) verwaltet eine Datenbank installierter Dienste und Treiber Dienste und bietet eine einheitliche und sichere Möglichkeit, Sie zu steuern.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: Informationen zu Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87aeec6dfcdc4e2dc0cc0ab3ef084b7927b2c3bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960117"
---
# <a name="about-services"></a>Informationen zu Diensten

Der [Dienststeuerungs-Manager (Service Control Manager](service-control-manager.md) , SCM) verwaltet eine Datenbank installierter Dienste und Treiber Dienste und bietet eine einheitliche und sichere Möglichkeit, Sie zu steuern. Die Datenbank enthält Informationen darüber, wie die einzelnen Dienst-oder Treiber Dienste gestartet werden sollten. Außerdem ermöglicht es Systemadministratoren, die Sicherheitsanforderungen für jeden Dienst anzupassen und damit den Zugriff auf den Dienst zu steuern.

In den folgenden Programmtypen werden die vom SCM bereitgestellten Funktionen verwendet.



| type                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dienstprogramm               | Ein Programm, das ausführbaren Code für einen oder mehrere Dienste bereitstellt. Dienstprogramme verwenden Funktionen, die eine Verbindung mit dem SCM herstellen und Statusinformationen an den SCM senden.                                                                                                                                                                          |
| Dienst Konfigurationsprogramm | Ein Programm, das die Dienst Datenbank abfragt oder ändert. Dienst Konfigurationsprogramme verwenden Funktionen, die die Datenbank öffnen, Dienste in der Datenbank installieren oder löschen und die Konfigurations-und Sicherheitsparameter für installierte Dienste Abfragen oder ändern. Dienst Konfigurationsprogramme verwalten sowohl Dienste als auch Treiber Dienste. |
| Dienst Steuerungsprogramm       | Ein Programm, das Dienste und Treiber Dienste startet und steuert. Dienst Steuerungsprogramme verwenden Funktionen, die Anforderungen an den SCM senden, der die Anforderung ausführt.                                                                                                                                                                     |



 

In dieser Übersicht werden die folgenden Themen behandelt:

-   [Dienststeuerungs-Manager](service-control-manager.md)
-   [Dienstprogramme](service-programs.md)
-   [Dienst Konfigurationsprogramme](service-configuration-programs.md)
-   [Dienst Steuerungsprogramme](service-control-programs.md)
-   [Dienst Benutzerkonten](service-user-accounts.md)
-   [Interaktive Dienste](interactive-services.md)
-   [Dienst Sicherheit und Zugriffsrechte](service-security-and-access-rights.md)
-   [Debugging a Service (Debuggen eines Diensts)](debugging-a-service.md)
-   [Dienst Triggerereignisse](service-trigger-events.md)

 

 



