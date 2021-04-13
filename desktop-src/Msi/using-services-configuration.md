---
description: Die Dienst Konfiguration ermöglicht dem Windows Installer, die Dienste auf einem Computer anzupassen.
ms.assetid: 164280b2-1c75-49d2-ac04-c3654be84134
title: Verwenden der Dienst Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6e3040d51b1056a370490fc5328a6bafe07555
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484187"
---
# <a name="using-services-configuration"></a>Verwenden der Dienst Konfiguration

Die Dienst Konfiguration ermöglicht dem Windows Installer, die [Dienste](../services/services.md) auf einem Computer anzupassen. Entwickler können ein Windows Installer Paket zum Installieren, beenden, starten und Löschen von Diensten während einer Installation erstellen, indem Sie die Tabellen [ServiceControl](servicecontrol-table.md) und [ServiceInstall](serviceinstall-table.md) sowie die Aktionen [installservices](installservices-action.md), [Stop Services](stopservices-action.md) und [Delta Service](deleteservices-action.md) verwenden.

Beginnend mit Paketen, die für Windows Installer 5,0 geschrieben wurden, können Entwickler die [msikonfigurireservices](msiconfigureservices-action.md) -Standardaktion und die [msiserviceconfig-Tabelle](msiserviceconfig-table.md) verwenden, um die erweiterten Dienst Anpassungsoptionen zu konfigurieren, die unter Windows 7 und Windows Server 2008 R2 und Windows Vista und Windows Server 2008 verfügbar sind. Vorhandene Installationspakete, die für Versionen der Windows Installer geschrieben wurden, die die msiserviceconfig-Tabelle nicht enthalten haben, können weiterhin mit Windows Installer 5,0 installiert werden. Das Dienst Konfigurations Feature des Windows Installer kann keine Netzwerkdienst Konten konfigurieren, Shared Service Host-Prozesse (SVCHOST) installieren oder Dienste neu starten, die im Rahmen der Installation beendet wurden.

**Windows XP und Windows Server 2003 oder früher:** Nicht unterstützt. Die Dienst Konfigurationstabellen und-Standard Aktionen sind ab Windows Installer 5,0 unter Windows 7 und Windows Server 2008 R2 und Windows Installer 4,5 unter Windows Vista und Windows Server 2008 verfügbar.

Sie müssen die [msikonfigurireservices](msiconfigureservices-action.md) -Aktion in der [InstallExecuteSequence](installexecutesequence-table.md) -Tabelle einschließen, um die Dienst Konfigurationen anzufordern, die Sie in der [Tabelle "msiserviceconfig](msiserviceconfig-table.md)" angeben. Der Windows Installer verwendet die Informationen in der msiserviceconfig-Tabelle nur dann, wenn die msikonfigurireservices-Standardaktion in einer Sequenz Tabelle enthalten ist. Die msikonfigurireservices-Standardaktion verwendet auch Informationen in den Tabellen [ServiceControl](servicecontrol-table.md) und [ServiceInstall](serviceinstall-table.md) .

Um anzufordern, dass dem System nur die erforderlichen Berechtigungen für einen bestimmten Dienst erteilt werden, geben Sie den Dienst und die Konfigurationsoption " **\_ \_ erforderliche \_ Berechtigungen \_ für die Dienst Konfiguration erforderlich** " in der [Tabelle "msiserviceconfig](msiserviceconfig-table.md)" an. Entfernen Sie die nicht benötigten Berechtigungen aus dem Prozess Token des Diensts. Diese Option kann verwendet werden, um Dienste zu konfigurieren, die im Sicherheitskontext der [Benutzerkonten](../services/service-user-accounts.md)"LocalSystem", "LocalService" oder "Network Service" ausgeführt werden.

Um anzufordern, dass das System den automatischen Start eines Diensts für einen Zeitraum nach dem Start aller anderen automatischen Start Dienste verzögern soll, geben Sie den Dienst und **die \_ \_ verzögerte \_ automatische \_ Startoption "Service config** " in der Tabelle " [msiserviceconfig](msiserviceconfig-table.md)" an. Der zu verzögerte Dienst muss vom aktuellen Paket mit dem \_ automatischen Dienst \_ Start in der Tabelle [ServiceInstall](serviceinstall-table.md) installiert werden, oder der Dienst muss bereits als Dienst für automatisches Starten installiert sein.

Geben Sie den Dienst, den Dienst-SID-Typ und die Konfigurationsoption " **Dienst \_ Konfigurations \_ Dienst-SID- \_ \_ Info** " in der [Tabelle "msiserviceconfig](msiserviceconfig-table.md)" an, um anzufordern, dass das System eine Ressource für die ausschließliche Verwendung eines bestimmten Dienstanbieter reserviert. Fügen Sie die Dienst-SID der Access Control Liste (ACL) der Ressource für die Ressource hinzu.

Gehen Sie folgendermaßen vor, um anzufordern, dass der [Dienststeuerungs-Manager](../services/service-control-manager.md) (SCM) nach dem Senden der Benachrichtigung zum **\_ \_ vorab Herunterfahren der Dienst Kontrolle** an einen Dienst warten muss. Geben Sie den Dienst, den Zeitraum, den der SCM warten soll, und die Konfigurationsoption " **Dienst Konfiguration vor dem \_ \_ herunter \_** fahren" in der [Tabelle "msiserviceconfig](msiserviceconfig-table.md)" an.

Um zu konfigurieren, wann das System nach dem Fehler eines Dienstanbieter Aktionen ausführen soll, geben Sie den Dienst und die **Flag "Service \_ config \_ Failure \_ \_ Actions** " in der [Tabelle "msiserviceconfig](msiserviceconfig-table.md)" an. Fügen Sie die auszuführenden Aktionen der [Tabelle msiserviceconfigfailureactions](msiserviceconfigfailureactions-table.md)hinzu.

Weitere Informationen zu den erweiterten Dienst Anpassungsfunktionen, die mit den Betriebssystemen Windows Vista und Windows Server 2008 eingeführt wurden, finden Sie unter [Dienst Änderungen für Windows Vista](../services/service-changes-for-windows-vista.md).

 

 
