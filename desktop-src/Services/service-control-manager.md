---
description: Der Dienststeuerungs-Manager (Service Control Manager, SCM) wird beim Systemstart gestartet. Es handelt sich um einen RPC-Server (RemoteProzeduraufruf), damit Dienstkonfigurations- und Dienststeuerungsprogramme Dienste auf Remotecomputern bearbeiten können.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Dienststeuerungs-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37d651a96f9685fa82b5ea92ebb3a0b72d80bfc62cd0db80729ec1cb95acc45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889033"
---
# <a name="service-control-manager"></a>Dienststeuerungs-Manager

Der Dienststeuerungs-Manager (Service Control Manager, SCM) wird beim Systemstart gestartet. Es handelt sich um einen RPC-Server (RemoteProzeduraufruf), damit Dienstkonfigurations- und Dienststeuerungsprogramme Dienste auf Remotecomputern bearbeiten können.

Die Dienstfunktionen stellen eine Schnittstelle für die folgenden Aufgaben bereit, die vom SCM ausgeführt werden:

-   Verwalten der Datenbank der installierten Dienste.
-   Starten von Diensten und Treiberdiensten entweder beim Systemstart oder bei Bedarf.
-   Aufzählen installierter Dienste und Treiberdienste.
-   Verwalten von Statusinformationen zum Ausführen von Diensten und Treiberdiensten.
-   Übertragen von Steuerungsanforderungen an ausgeführte Dienste.
-   Sperren und Entsperren der Dienstdatenbank.

In den folgenden Abschnitten wird der SCM ausführlicher beschrieben:

-   [Datenbank der installierten Dienste](database-of-installed-services.md)
-   [Automatisches Starten von Diensten](automatically-starting-services.md)
-   [Starten von Diensten bei Bedarf](starting-services-on-demand.md)
-   [Dienstdatensatzliste](service-record-list.md)
-   [SCM-Handles](scm-handles.md)

 

 



