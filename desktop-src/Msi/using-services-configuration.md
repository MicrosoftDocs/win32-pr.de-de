---
description: Die Dienstkonfiguration ermöglicht dem Windows, die Dienste auf einem Computer anzupassen.
ms.assetid: 164280b2-1c75-49d2-ac04-c3654be84134
title: Verwenden der Dienstkonfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe1e34cce317ee00c3cc9d6ee4aac449e500499dc2dee4e97df65ba91bca2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012704"
---
# <a name="using-services-configuration"></a>Verwenden der Dienstkonfiguration

Die Dienstkonfiguration ermöglicht dem Windows, die Dienste [auf einem](../services/services.md) Computer anzupassen. Entwickler können ein Windows Installer-Paket erstellen, um Dienste während einer Installation zu installieren, zu beenden, zu starten und zu löschen, indem sie die Tabellen [ServiceControl](servicecontrol-table.md) und [ServiceInstall](serviceinstall-table.md) sowie die Aktionen [InstallServices,](installservices-action.md) [StopServices](stopservices-action.md) und [DeleteServices](deleteservices-action.md) verwenden.

Ab Paketen, die für Windows Installer 5.0 geschrieben wurden, können Entwickler auch die Standardaktion [MsiConfigureServices](msiconfigureservices-action.md) und die [Tabelle MsiServiceConfig](msiserviceconfig-table.md) verwenden, um die erweiterten Dienstanpassungsoptionen zu konfigurieren, die mit Windows 7 und Windows Server 2008 R2 sowie Windows Vista und Windows Server 2008 verfügbar sind. Vorhandene Installationspakete, die für Versionen des Windows Installers geschrieben wurden, die nicht die MsiServiceConfig-Tabelle enthalten, können weiterhin mithilfe von Windows Installer 5.0 installiert werden. Das Dienstkonfigurationsfeature des Windows-Installers kann keine Netzwerkdienstkonten konfigurieren, Shared Service Host-Prozesse (svchost) installieren oder Dienste neu starten, die im Rahmen der Installation beendet wurden.

**Windows XP und Windows Server 2003 oder früher:** Nicht unterstützt. Die Dienstkonfigurationstabellen und Standardaktionen sind ab Windows Installer 5.0 verfügbar, das unter Windows 7 und Windows Server 2008 R2 und Windows Installer 4.5 unter Windows Vista und Windows Server 2008 ausgeführt wird.

Sie müssen die [MsiConfigureServices-Aktion](msiconfigureservices-action.md) in die [Tabelle InstallExecuteSequence](installexecutesequence-table.md) einfügen, um die Dienstkonfigurationen an fordern, die Sie in der [MsiServiceConfig-Tabelle angeben.](msiserviceconfig-table.md) Der Windows Installer verwendet die Informationen in der MsiServiceConfig-Tabelle nur, wenn die Standardaktion MsiConfigureServices in einer Sequenztabelle enthalten ist. Die Standardaktion MsiConfigureServices verwendet auch Informationen in den [Tabellen ServiceControl](servicecontrol-table.md) und [ServiceInstall.](serviceinstall-table.md)

Geben Sie den Dienst und die **Konfigurationsoption SERVICE \_ CONFIG \_ REQUIRED \_ PRIVILEGES \_ INFO** in der [MsiServiceConfig-Tabelle](msiserviceconfig-table.md)an, um vom System nur die erforderlichen Berechtigungen für einen bestimmten Dienst an fordern zu lassen. Entfernen Sie die nicht erforderlichen Berechtigungen aus dem Prozesstoken des Diensts. Diese Option kann verwendet werden, um Dienste zu konfigurieren, die im Sicherheitskontext der Benutzerkonten des LocalSystem-, LocalService- oder [NetworkService-Diensts ausgeführt werden.](../services/service-user-accounts.md)

Um an anzugeben, dass das System den automatischen Start eines Diensts nach dem Start aller anderen Automatischstartdienste für eine Zeit verzögert, geben Sie den Dienst und die **Option SERVICE \_ CONFIG DELAYED AUTO \_ \_ \_ START** in der [MsiServiceConfig-Tabelle an.](msiserviceconfig-table.md) Der zu verzögernde Dienst muss vom aktuellen Paket mit SERVICE AUTO START installiert werden, das in der Tabelle ServiceInstall angegeben ist, oder der Dienst muss bereits als \_ \_ Automatischstartdienst installiert sein. [](serviceinstall-table.md)

Wenn Sie anfordern möchten, dass das System eine Ressource für die exklusive Verwendung eines bestimmten Diensts reservieren soll, geben Sie den Dienst, den Dienst-SID-Typ und die **Konfigurationsoption SERVICE \_ CONFIG \_ SERVICE SID \_ \_ INFO** in der [MsiServiceConfig-Tabelle an.](msiserviceconfig-table.md) Fügen Sie die SID des Diensts zur Ressourcen-Access Control-Liste (ACL) für die Ressource hinzu.

Gehen Sie wie folgt vor, um an fordern, dass der [Dienststeuerungs-Manager](../services/service-control-manager.md) (Service Control Manager, SCM) nach dem Senden der **SERVICE CONTROL \_ \_ PRESHUTDOWN-Benachrichtigung** an einen Dienst wartet. Geben Sie den Dienst, die Wartezeit des SCM und die Konfigurationsoption **\_ SERVICE CONFIG \_ PRESHUTDOWN \_ INFO** in der [Tabelle MsiServiceConfig an.](msiserviceconfig-table.md)

Um zu konfigurieren, wann das System Aktionen nach dem Ausfall eines Diensts ausführen soll, geben Sie den Dienst und die **OPTION SERVICE \_ CONFIG FAILURE ACTIONS \_ \_ \_ FLAG** in der [MsiServiceConfig-Tabelle an.](msiserviceconfig-table.md) Fügen Sie die aktionen, die ausgeführt werden sollen, der [Tabelle MsiServiceConfigFailureActions hinzu.](msiserviceconfigfailureactions-table.md)

Weitere Informationen zu den erweiterten Dienstanpassungsfunktionen, die mit den Betriebssystemen Windows Vista und Windows Server 2008 eingeführt wurden, finden Sie unter Dienständerungen für [Windows Vista.](../services/service-changes-for-windows-vista.md)

 

 
