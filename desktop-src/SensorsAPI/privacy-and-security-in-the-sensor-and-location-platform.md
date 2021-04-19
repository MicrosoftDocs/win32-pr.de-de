---
description: Die Windows-Sensor-und-Speicherort Plattform beinhaltet Datenschutzeinstellungen zum Schutz der persönlichen Benutzerinformationen.
ms.assetid: 24425ed2-7b94-4b05-b117-9118d2074f49
title: Datenschutz und Sicherheit auf der Plattform für Windows-Sensoren und-Orte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb0bf50cd27de1fc7fd4f42bd7a8455a549eea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346503"
---
# <a name="privacy-and-security-in-the-windows-sensor-and-location-platform"></a>Datenschutz und Sicherheit auf der Plattform für Windows-Sensoren und-Orte

Die Windows-Sensor-und-Speicherort Plattform beinhaltet Datenschutzeinstellungen zum Schutz der persönlichen Benutzerinformationen.

Mithilfe der-Plattform können Sie sicherstellen, dass die Sensordaten auf folgende Weise privat bleiben, wenn der Datenschutz erforderlich ist:

-   Standardmäßig sind Sensoren deaktiviert. Da der Platt Form Entwurf voraussetzt, dass jeder Sensor persönliche Daten bereitstellen kann, wird jeder Sensor so lange deaktiviert, bis der Benutzer die explizite Zustimmung zum Zugriff auf die Sensordaten bereitstellt.
-   Windows stellt offen legungs Meldungen und Hilfe Inhalte für den Benutzer bereit. Dieser Inhalt hilft Benutzern zu verstehen, wie sich Sensoren auf den Datenschutz Ihrer persönlichen Daten auswirken können, und hilft Benutzern dabei, fundierte Entscheidungen zu treffen.
-   Zum Erteilen von Berechtigungen für einen Sensor sind Administratorrechte erforderlich.
-   Wenn Sie aktiviert ist, kann ein Sensorgerät für alle Programme verwendet werden, die unter einem bestimmten Benutzerkonto ausgeführt werden (oder für alle Benutzerkonten). Dies schließt nicht interaktive Benutzer und Dienste ein, z. b. ASPNET oder System. Wenn Sie z. b. einen GPS-Sensor für Ihr Benutzerkonto aktivieren, haben nur Programme, die unter Ihrem Benutzerkonto ausgeführt werden, Zugriff auf das GPS. Wenn Sie das GPS für alle Benutzer aktivieren, kann jedes Programm, das unter einem beliebigen Benutzerkonto ausgeführt wird, auf das GPS zugreifen.
-   Programme, die Sensoren verwenden, können eine Methode zum Öffnen eines System Dialogfelds aufzurufen, in dem Benutzer aufgefordert werden, benötigte Sensorgeräte zu aktivieren. Mit dieser Funktion können Entwickler und Benutzer auf einfache Weise sicherstellen, dass die Sensoren funktionieren, wenn Programme Sie benötigen, während Sie die Kontrolle über die Offenlegung von Sensordaten behalten.
-   Sensor Treiber verwenden ein spezielles Objekt, das alle e/a-Anforderungen verarbeitet. Dieses Objekt stellt sicher, dass nur Programme mit Benutzer Berechtigung auf Sensordaten zugreifen können.

 

 



