---
description: Der Dienststeuerungs-Manager (SCM) wird beim Systemstart gestartet. Dabei handelt es sich um einen RPC-Server (Remote Procedure Aufruf), sodass Dienst Konfiguration und Dienst Steuerungsprogramme Dienste auf Remote Computern bearbeiten können.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Dienststeuerungs-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8a35fd34bd2714d22d40ccf618c89a8b66a6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343277"
---
# <a name="service-control-manager"></a>Dienststeuerungs-Manager

Der Dienststeuerungs-Manager (SCM) wird beim Systemstart gestartet. Dabei handelt es sich um einen RPC-Server (Remote Procedure Aufruf), sodass Dienst Konfiguration und Dienst Steuerungsprogramme Dienste auf Remote Computern bearbeiten können.

Die Dienstfunktionen stellen eine Schnittstelle für die folgenden vom SCM ausgeführten Aufgaben bereit:

-   Die Datenbank der installierten Dienste wird beibehalten.
-   Starten von Diensten und Treiber Diensten entweder beim Systemstart oder nach Bedarf.
-   Die installierten Dienste und Treiber Dienste werden aufgelistet.
-   Verwalten von Statusinformationen für die Ausführung von Diensten und Treiber Diensten
-   Übertragen von Steuerungsanforderungen an die laufenden Dienste
-   Sperren und Entsperren der Dienst Datenbank.

In den folgenden Abschnitten wird der SCM ausführlicher beschrieben:

-   [Datenbank der installierten Dienste](database-of-installed-services.md)
-   [Dienste werden automatisch gestartet](automatically-starting-services.md)
-   [Starten von Diensten bei Bedarf](starting-services-on-demand.md)
-   [Dienst Daten Satz Liste](service-record-list.md)
-   [SCM-Handles](scm-handles.md)

 

 



