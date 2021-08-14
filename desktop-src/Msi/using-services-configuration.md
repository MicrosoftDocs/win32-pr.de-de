---
description: Die Dienstkonfiguration ermöglicht es dem Windows Installer, die Dienste auf einem Computer anzupassen.
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

Mit der Dienstkonfiguration kann der Windows Installer die [Dienste](../services/services.md) auf einem Computer anpassen. Entwickler können ein Windows Installer-Paket erstellen, um Dienste während einer Installation zu installieren, zu beenden, zu starten und zu löschen, indem sie die Tabellen [ServiceControl](servicecontrol-table.md) und [ServiceInstall](serviceinstall-table.md) sowie die Aktionen [InstallServices,](installservices-action.md) [StopServices](stopservices-action.md) und [DeleteServices](deleteservices-action.md) verwenden.

Ab Paketen, die für Windows Installer 5.0 geschrieben wurden, können Entwickler auch die [MsiConfigureServices-Standardaktion](msiconfigureservices-action.md) und die [MsiServiceConfig-Tabelle](msiserviceconfig-table.md) verwenden, um die erweiterten Dienstanpassungsoptionen zu konfigurieren, die mit Windows 7 und Windows Server 2008 R2 und Windows Vista und Windows Server 2008 verfügbar sind. Vorhandene Installationspakete, die für Versionen des Windows Installers geschrieben wurden, die die MsiServiceConfig-Tabelle nicht enthalten, können weiterhin mit Windows Installer 5.0 installiert werden. Das Dienstkonfigurationsfeature des Windows Installers kann keine Netzwerkdienstkonten konfigurieren, prozesse für freigegebene Diensthosts (svchost) installieren oder Dienste, die im Rahmen der Installation beendet wurden, neu starten.

**Windows XP und Windows Server 2003 oder früher:** Wird nicht unterstützt. Die Dienstkonfigurationstabellen und Standardaktionen sind ab Windows Installer 5.0 verfügbar, der auf Windows 7 und Windows Server 2008 R2 und Windows Installer 4.5 unter Windows Vista und Windows Server 2008 ausgeführt wird.

Sie müssen die [MsiConfigureServices-Aktion](msiconfigureservices-action.md) in die [Tabelle InstallExecuteSequence](installexecutesequence-table.md) einschließen, um die Dienstkonfigurationen anzufordern, die Sie in der [MsiServiceConfig-Tabelle](msiserviceconfig-table.md)angeben. Der Windows Installer verwendet die Informationen in der MsiServiceConfig-Tabelle nur, wenn die MsiConfigureServices-Standardaktion in einer Sequenztabelle enthalten ist. Die MsiConfigureServices-Standardaktion verwendet auch Informationen in den Tabellen [ServiceControl](servicecontrol-table.md) und [ServiceInstall.](serviceinstall-table.md)

Um anzufordern, dass das System nur die erforderlichen Berechtigungen für einen bestimmten Dienst gewährt, geben Sie den Dienst und die Konfigurationsoption **SERVICE \_ CONFIG \_ REQUIRED PRIVILEGES \_ \_ INFO** in der [MsiServiceConfig-Tabelle](msiserviceconfig-table.md)an. Entfernen Sie die nicht benötigten Berechtigungen aus dem Prozesstoken des Diensts. Diese Option kann verwendet werden, um Dienste zu konfigurieren, die im Sicherheitskontext der Benutzerkonten des LocalSystem-, LocalService- oder [NetworkService-Diensts](../services/service-user-accounts.md)ausgeführt werden.

Um anzufordern, dass das System den automatischen Start eines Diensts für einen Zeitraum nach dem Start aller anderen Automatischstartdienste verzögert, geben Sie den Dienst und die Option **SERVICE \_ CONFIG \_ DELAYED \_ AUTO \_ START** in der [MsiServiceConfig-Tabelle](msiserviceconfig-table.md)an. Der verzögerte Dienst muss vom aktuellen Paket installiert werden, wobei \_ SERVICE AUTO START in der Tabelle \_ [ServiceInstall](serviceinstall-table.md) angegeben ist, oder der Dienst muss bereits als Dienst für den automatischen Start installiert sein.

Um anzufordern, dass das System eine Ressource für die exklusive Verwendung eines bestimmten Diensts reserviert, geben Sie den Dienst, den Dienst-SID-Typ und die Konfigurationsoption **\_ SERVICE CONFIG SERVICE SID \_ \_ \_ INFO** in der [MsiServiceConfig-Tabelle](msiserviceconfig-table.md)an. Fügen Sie die SID des Diensts zur Access Control Liste (ACL) der Ressource für die Ressource hinzu.

Um anzufordern, dass der [Dienststeuerungs-Manager (Service Control Manager,](../services/service-control-manager.md) SCM) nach dem Senden der **SERVICE CONTROL \_ \_ PRESHUTDOWN-Benachrichtigung** an einen Dienst wartet, gehen Sie folgendermaßen vor. Geben Sie den Dienst, die Wartezeit des SCM und die Konfigurationsoption **SERVICE \_ CONFIG \_ PRESHUTDOWN \_ INFO** in der [MsiServiceConfig-Tabelle](msiserviceconfig-table.md)an.

Um zu konfigurieren, wann das System Aktionen nach dem Ausfall eines Diensts ausführen soll, geben Sie den Dienst und die OPTION **SERVICE \_ CONFIG \_ FAILURE ACTIONS \_ \_ FLAG** in der [MsiServiceConfig-Tabelle](msiserviceconfig-table.md)an. Fügen Sie die auszuführenden Aktionen der [MsiServiceConfigFailureActions-Tabelle](msiserviceconfigfailureactions-table.md)hinzu.

Weitere Informationen zu den erweiterten Dienstanpassungsfunktionen, die mit den Betriebssystemen Windows Vista und Windows Server 2008 eingeführt wurden, finden Sie unter [Dienständerungen für Windows Vista.](../services/service-changes-for-windows-vista.md)

 

 
