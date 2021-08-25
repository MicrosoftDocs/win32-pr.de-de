---
description: In der folgenden Liste werden neue und aktualisierte Featurebereiche für Windows Server 2012 und Windows Server 2012 R2 beschrieben. Weitere Informationen zu neuen Windows 8- und Windows 8.1-Technologien finden Sie unter Windows 8- und Windows 8.1-Technologien.
ms.assetid: bd8b4dd8-e0b7-4340-a6bd-1baa42d9a1dd
title: 'Neuerungen: Windows Server 2012 R2-& Windows Server 2012'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df654e7c448ef4e4f6f4f1599204883cad11bf5e56ccd13c47c76d204f7587f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867501"
---
# <a name="whats-new-windows-server-2012-r2--windows-server-2012"></a>Neuerungen: Windows Server 2012 R2-& Windows Server 2012

In der folgenden Liste werden neue und aktualisierte Featurebereiche für Windows Server 2012 und Windows Server 2012 R2 beschrieben. Weitere Informationen zu neuen Windows 8- und Windows 8.1-Technologien finden Sie unter [Windows 8 und Windows 8.1 Technologies](/previous-versions/windows/desktop/whatsnew/windows-8-technologies).

## <a name="whats-new-for-windows-server-2012-r2"></a>Neuerungen bei Windows Server 2012 R2

-   [Datendeduplizierung](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    Die Datendeduplizierung findet und entfernt die Duplizierung innerhalb von Daten auf einem Volume und stellt gleichzeitig sicher, dass die Daten korrekt und vollständig bleiben. Auf diese Weise können mehr Dateidaten mit weniger Speicherplatz auf dem Volume gespeichert werden. Für Windows Server 2012 R2 wurden eine Reihe von Parametern und Fehlercodes aktiviert, und die [**MSFT \_ DedupFileMetadata-Klasse**](/previous-versions/windows/desktop/dedup/msft-dedupfilemetadata) wurde hinzugefügt.

-   [Softwareinventurprotokollierung](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)

    **Neu!** Die Protokollierung des Softwarebestands sammelt Lizenzierungsdaten zu Software, die auf einem Windows Server installiert ist, und bietet Remotezugriff auf die Daten, sodass sie problemlos von einem Rechenzentrum aggregiert werden können.

-   [iSCSI-Zielserver](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    Die iSCSI-Zielserver-API stellt WMI-Anbieter (Windows Management Instrumentation) zum Verwalten der Microsoft iSCSI-Zielserver bereit, z. B. zum Erstellen virtueller Datenträger und zum Präsentieren dieser Datenträger an den Client. Für Windows Server 2012 R2 wurden eine Reihe neuer Features hinzugefügt.

-   [Mobile Geräteverwaltung-Registrierung](../mdmreg/mobile-device-management-registration-portal.md)

    **Neu!** Ein Branchentrend hat sich entwickelt, bei dem Mitarbeiter ihre persönlichen mobilen Computinggeräte mit dem Unternehmensnetzwerk und den Ressourcen (lokal oder über die Cloud) verbinden, um Arbeitsplatzaufgaben auszuführen. Dieser Trend erfordert Unterstützung für die einfache Konfiguration des Netzwerks und der Ressourcen, sodass Mitarbeiter persönliche Geräte für arbeitsbezogene Zwecke beim Unternehmen registrieren können. Anwendungen und Technologien zur Unterstützung der einfachen Konfiguration müssen IT-Experten auch die Verwaltung des Risikos ermöglichen, das mit unkontrollierten Geräten verbunden ist, die mit dem Unternehmensnetzwerk verbunden sind. Die Mobile Geräteverwaltung-Registrierung (MDM) registriert ein Gerät bei einem Verwaltungsdienst.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell ist eine aufgabenbasierte Befehlszeilenshell und Skriptsprache, die speziell für die Systemverwaltung entwickelt wurde. Neu in Windows Server 2012 R2 unterstützt Windows PowerShell v4 Desired State Configuration, eine neue Verwaltungsplattform in Windows PowerShell, die das Bereitstellen und Verwalten von Konfigurationsdaten für Softwaredienste und die Verwaltung der Umgebung ermöglicht, in der diese Dienste ausgeführt werden.

## <a name="whats-new-for-windows-server-2012"></a>Neuerungen bei Windows Server 2012

-   [Windows Clustering](/previous-versions/windows/desktop/mscs/windows-clustering)

    Windows Mit clustering können Sie sowohl Cluster mit Netzwerklastenausgleich als auch Failovercluster verwalten. In dieser Version wurden eine Reihe neuer Features hinzugefügt, darunter neue Gruppenverwaltungsfunktionen, allgemeine Eigenschaften und die Integration in WMI.

-   [Benutzerzugriffsprotokollierung](/previous-versions/windows/desktop/ual/user-access-logging)

    **Neu!** Die Benutzerzugriffsprotokollierung (User Access Logging, UAL) ist ein gängiges Framework für Windows Serverrollen, um ihre jeweiligen Nutzungsmetriken zu melden. Dieses UAL-Framework ist eine grundlegende und wichtige Komponente der größeren Lösung für die Lizenzierungsverwaltung.

-   [Windows-Remoteverwaltung](../winrm/portal.md)

    Bei der Windows-Remoteverwaltung (Windows Remote Management, WinRM) handelt es sich um die Microsoft-Implementierung des WS-Verwaltungsprotokolls – ein standardmäßiges, SOAP-basiertes und firewallfreundliches Protokoll, das die Zusammenarbeit von Hardware und Betriebssystemen unterschiedlicher Anbieter ermöglicht. Windows Server 2012 enthält eine Reihe von Verbindungs-APIs, die sich auf die Interaktion mit ausgeführten Instanzen und Shells konzentrieren.

-   [Windows Verwaltungsinfrastruktur](/previous-versions/windows/desktop/wmi_v2/what-s-new-in-mi)

    **Neu!** Die Features der Windows Management Infrastructure (MI) stellen die neueste Version der WMI-Technologien (Windows Management Instrumentation) dar, die auf dem CIM-Standard von DMTF (Distributed Management Task Force) basieren. MI ist vollständig kompatibel mit früheren Versionen von WMI und bietet eine Vielzahl von Features und Vorteilen, die das Entwerfen und Entwickeln von Anbietern und Clients einfacher als je zuvor machen.

-   [Datendeduplizierung](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    **Neu!** Die Datendeduplizierung findet und entfernt die Duplizierung innerhalb von Daten auf einem Volume und stellt gleichzeitig sicher, dass die Daten korrekt und vollständig bleiben. Auf diese Weise können mehr Dateidaten mit weniger Speicherplatz auf dem Volume gespeichert werden.

-   [iSCSI-Zielserver](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    **Neu!** Die iSCSI-Zielserver-API stellt WMI-Anbieter (Windows Management Instrumentation) zum Verwalten der Microsoft iSCSI-Zielserver bereit, z. B. zum Erstellen virtueller Datenträger und zum Präsentieren dieser Datenträger an den Client.

-   [NFS-Anbieter für WMI](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)

    **Neu!** Der NFS-WMI-Anbieter bietet eine Möglichkeit zum Verwalten von NFS-Server- und Clienteinstellungen, Dateifreigaben, Netgroups und Clientgruppen.

-   [Offlinedateien](../devnotes/offline-files.md)

    Mit der Offlinedateien-API können Anwendungen das Verhalten von Offlinedateien programmgesteuert steuern und überwachen. Windows Server 2012 fügt die Funktionen [**OfflineFilesQueryStatusEx,**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex) [**OfflineFilesStart**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart) und [**RenameItem**](/previous-versions/windows/desktop/offlinefiles/win32-offlinefilescache-renameitem) hinzu.

-   [SMB-Verwaltung](/previous-versions/windows/desktop/smb/smb-management-api-portal)

    **Neu!** Die SMB-Verwaltungs-API stellt WMI-Klassen und -Methoden zum Verwalten von Freigaben und zum Freigeben des Zugriffs bereit.

-   [Server Core](/previous-versions/windows/desktop/legacy/hh846323(v=vs.85))

    Windows Server bietet minimale Serverinstallationsoptionen für Computer, die unter dem Betriebssystem Windows Server 2008 oder höher ausgeführt werden. Windows Server 2012 bietet Server Core sowohl als Konfiguration als auch als Installationsoptionen an.

-   [Windows Server-Sicherung](/previous-versions/windows/desktop/wsb/windows-server-backup-portal)

    Mit dem Feature Windows Serversicherung werden Anwendungsdaten automatisch gesichert und wiederhergestellt. Windows Server 2012 enthält die Cloud Backup Provider-API.

-   [Windows Desktopfreigabe](/previous-versions/windows/desktop/rdp/rdp-portal)

    Windows Die Desktopfreigabe ist eine Bildschirmfreigabetechnologie mit mehreren Parteien. Windows Server 2012 implementiert diese Technologie mithilfe der Windows Duplizierungs-API.

-   [Remotedesktopdienste](../termserv/terminal-services-portal.md)

    Windows Mit der Desktopfreigabe kann der Benutzer remote auf eine Instanz des Betriebssystems zugreifen. Windows Server 2012 umfasst eine Reihe neuer Features, einschließlich untergeordneter Sitzungen, RemoteFX Medienumleitung und des Remotedesktop Broker-Clients.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell ist eine aufgabenbasierte Befehlszeilenshell und Skriptsprache, die speziell für die Systemverwaltung entwickelt wurde. Neu in Windows Server 2012 unterstützt Windows PowerShell v3 Windows PowerShell Workflow, der die Vorteile von Windows Workflow Foundation nutzt, um die Automatisierung zeitintensiver Aufgaben zu ermöglichen.

-   [Verwaltungs-OData](/powershell/scripting/developer/webservices/creating-a-management-odata-web-service?view=powershell-7&preserve-view=true)

    **Neu!** Auch bekannt als Windows PowerShell Webdienste, Verwaltungs-OData, neu in Windows PowerShell v3, ermöglicht die Erstellung eines ASP.NET Webdienstendpunkts, der Verwaltungsdaten verfügbar macht, die über Windows PowerShell Befehle als OData-Webdienstentitäten übertragen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Server 2012 R2 auf TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 und Windows Server 2012 in der TechNet-Bibliothek](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 auf Microsoft.Com](https://www.microsoft.com/evalcenter/evaluate-windows-server-2012-r2-essentials)
</dt> </dl>

 

 
