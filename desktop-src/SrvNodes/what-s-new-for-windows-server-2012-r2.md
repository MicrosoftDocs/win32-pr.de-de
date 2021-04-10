---
description: In der folgenden Liste werden neue und aktualisierte Funktionsbereiche für Windows Server 2012 und Windows Server 2012 R2 beschrieben. Weitere Informationen zu neuen Technologien für Windows 8 und Windows 8.1 finden Sie unter Windows 8 und Windows 8.1 Technologies.
ms.assetid: bd8b4dd8-e0b7-4340-a6bd-1baa42d9a1dd
title: 'Neuerungen: Windows Server 2012 R2 & Windows Server 2012'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ba276ea8256299c5e667cbb5a1d2b0872bb282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866623"
---
# <a name="whats-new-windows-server-2012-r2--windows-server-2012"></a>Neuerungen: Windows Server 2012 R2 & Windows Server 2012

In der folgenden Liste werden neue und aktualisierte Funktionsbereiche für Windows Server 2012 und Windows Server 2012 R2 beschrieben. Weitere Informationen zu neuen Technologien für Windows 8 und Windows 8.1 finden Sie unter [Windows 8 und Windows 8.1 Technologies](/previous-versions/windows/desktop/whatsnew/windows-8-technologies).

## <a name="whats-new-for-windows-server-2012-r2"></a>Neuerungen in Windows Server 2012 R2

-   [Datendeduplizierung](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    Bei der Datendeduplizierung werden Duplikate innerhalb von Daten auf einem Volume gefunden und entfernt. gleichzeitig wird sichergestellt, dass die Daten korrekt und fertig bleiben Auf diese Weise können mehr Dateidaten mit weniger Speicherplatz auf dem Volume gespeichert werden. Für Windows Server 2012 R2 wurden eine Reihe von Parametern und Fehlercodes aktiviert, und die [**MSFT \_ dedupfilemetadata**](/previous-versions/windows/desktop/dedup/msft-dedupfilemetadata) -Klasse wurde hinzugefügt.

-   [Softwareinventurprotokollierung](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)

    **Neu!** Bei der Protokollierung des Software Bestands werden Lizenzierungs Daten zu Software gesammelt, die auf einem Windows-Server installiert ist, und Remote Zugriff auf die Daten ermöglicht, sodass Sie problemlos von einem Rechenzentrum aggregiert werden können.

-   [iSCSI-Zielserver](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    Die iSCSI-Zielserver-API stellt Windows-Verwaltungsinstrumentation (WMI)-Anbieter für die Verwaltung des Microsoft iSCSI-Zielservers zur Verfügung, z. b. zum Erstellen virtueller Datenträger und zum Bereitstellen dieser auf dem Client. Für Windows Server 2012 R2 wurden eine Reihe neuer Funktionen hinzugefügt.

-   [Registrierung für die Verwaltung mobiler Geräte](../mdmreg/mobile-device-management-registration-portal.md)

    **Neu!** Ein Branchentrend wurde entwickelt, bei dem Mitarbeiter Ihre persönlichen mobilen Computergeräte mit dem Unternehmensnetzwerk und den Ressourcen (entweder lokal oder über die Cloud) verbinden, um Arbeitsplatz Aufgaben auszuführen. Dieser Trend erfordert Unterstützung für die einfache Konfiguration von Netzwerk und Ressourcen, sodass Mitarbeiter persönliche Geräte für arbeitsbezogene Zwecke beim Unternehmen registrieren können. Anwendungen und Technologien zur Unterstützung von Easy Configuration müssen IT-Experten außerdem die Verwaltung des Risikos ermöglichen, das mit dem Unternehmensnetzwerk verbunden ist, das mit dem Unternehmensnetzwerk verbunden ist. Bei der Registrierung mobiler Geräte (Mobile Device Management, MDM) wird ein Gerät in einem Verwaltungsdienst registriert.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell ist eine aufgabenbasierte Befehlszeilenshell und Skriptsprache, die speziell für die Systemverwaltung entwickelt wurde. Windows PowerShell V4 ist neu in Windows Server 2012 R2 und unterstützt die Konfiguration des gewünschten Zustands, eine neue Verwaltungsplattform in Windows PowerShell, die die Bereitstellung und Verwaltung von Konfigurationsdaten für Software Dienste und die Verwaltung der Umgebung ermöglicht, in der diese Dienste ausgeführt werden.

## <a name="whats-new-for-windows-server-2012"></a>Neuerungen in Windows Server 2012

-   [Windows-Clustering](/previous-versions/windows/desktop/mscs/windows-clustering)

    Windows-Clustering ermöglicht Ihnen die Verwaltung von Netzwerk Lastenausgleich-Clustern sowie von Failoverclustern. In dieser Version wurden eine Reihe neuer Funktionen hinzugefügt, einschließlich neuer Gruppen Verwaltungsfunktionen, allgemeiner Eigenschaften und der Integration in WMI.

-   [Benutzerzugriffsprotokollierung](/previous-versions/windows/desktop/ual/user-access-logging)

    **Neu!** Die Benutzer Zugriffs Protokollierung (User Access Logging, UAL) ist ein gängiges Framework für Windows Server-Rollen, mit dem ihre jeweiligen Nutzungs Dieses UAL-Framework ist eine grundlegende und wichtige Komponente der größeren Lizenzierungs Verwaltungs Lösung.

-   [Windows-Remoteverwaltung](../winrm/portal.md)

    Bei der Windows-Remoteverwaltung (Windows Remote Management, WinRM) handelt es sich um die Microsoft-Implementierung des WS-Verwaltungsprotokolls – ein standardmäßiges, SOAP-basiertes und firewallfreundliches Protokoll, das die Zusammenarbeit von Hardware und Betriebssystemen unterschiedlicher Anbieter ermöglicht. Windows Server 2012 enthält eine Reihe von Verbindungs-APIs, die sich auf die Interaktion mit laufenden Instanzen und Shells konzentrieren.

-   [Windows-Verwaltungsinfrastruktur](/previous-versions/windows/desktop/wmi_v2/what-s-new-in-mi)

    **Neu!** Die Funktionen der Windows-Verwaltungsinfrastruktur (Windows Management Infrastructure, Mi) stellen die neueste Version der WMI-Technologien (Windows-Verwaltungsinstrumentation) dar, die auf dem CIM-Standard von DMTF basieren (verteilte Verwaltungs Task Force). Mi ist vollständig kompatibel mit früheren Versionen von WMI und bietet eine Reihe von Features und Vorteilen, mit denen das Entwerfen und entwickeln von Anbietern und Clients einfacher als je zuvor ist.

-   [Datendeduplizierung](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    **Neu!** Bei der Datendeduplizierung werden Duplikate innerhalb von Daten auf einem Volume gefunden und entfernt. gleichzeitig wird sichergestellt, dass die Daten korrekt und fertig bleiben Auf diese Weise können mehr Dateidaten mit weniger Speicherplatz auf dem Volume gespeichert werden.

-   [iSCSI-Zielserver](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    **Neu!** Die iSCSI-Zielserver-API stellt Windows-Verwaltungsinstrumentation (WMI)-Anbieter für die Verwaltung des Microsoft iSCSI-Zielservers zur Verfügung, z. b. zum Erstellen virtueller Datenträger und zum Bereitstellen dieser auf dem Client.

-   [NFS-Anbieter für WMI](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)

    **Neu!** Der NFS-WMI-Anbieter bietet die Möglichkeit, NFS-Server-und-Client Einstellungen, Dateifreigaben, Netzwerk Gruppen und Client Gruppen zu verwalten.

-   [Offlinedateien](../devnotes/offline-files.md)

    Die Offlinedateien-API ermöglicht es Anwendungen, das Verhalten von Offlinedateien Programm gesteuert zu steuern und zu überwachen. In Windows Server 2012 werden die Funktionen [**offlinefilesqueryanusex**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex), [**offlinefilesstart**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart) und [**RenameItem**](/previous-versions/windows/desktop/offlinefiles/win32-offlinefilescache-renameitem) hinzugefügt.

-   [SMB-Verwaltung](/previous-versions/windows/desktop/smb/smb-management-api-portal)

    **Neu!** Die SMB-Verwaltungs-API stellt WMI-Klassen und-Methoden zum Verwalten von Freigaben und Freigabe Zugriff bereit.

-   [Server Core](/previous-versions/windows/desktop/legacy/hh846323(v=vs.85))

    Windows Server stellt minimale Server Installationsoptionen für Computer bereit, die unter dem Betriebssystem Windows Server 2008 oder höher ausgeführt werden. Windows Server 2012 bietet Server Core sowohl als Konfiguration als auch Installationsoptionen.

-   [Windows Server-Sicherung](/previous-versions/windows/desktop/wsb/windows-server-backup-portal)

    Das Windows Server-Sicherung Feature sichert automatisch Anwendungsdaten und stellt diese wieder her. Windows Server 2012 enthält die Cloud Backup Provider-API.

-   [Windows-Desktop Freigabe](/previous-versions/windows/desktop/rdp/rdp-portal)

    Die Windows-Desktop Freigabe ist eine Technologie für die Bildschirm Freigabe mehrerer Parteien. Windows Server 2012 implementiert diese Technologie mithilfe der Windows-Duplizierungs-API.

-   [Remotedesktopdienste (RDS)](../termserv/terminal-services-portal.md)

    Die Windows-Desktop Freigabe ermöglicht dem Benutzer den Remote Zugriff auf eine Instanz des Betriebssystems. Windows Server 2012 umfasst eine Reihe neuer Features, darunter untergeordnete Sitzungen, remotefx-Medien Umleitung und der Remotedesktop Broker-Client.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell ist eine aufgabenbasierte Befehlszeilenshell und Skriptsprache, die speziell für die Systemverwaltung entwickelt wurde. Windows PowerShell v3 ist neu in Windows Server 2012 und unterstützt den Windows PowerShell-Workflow, der die Vorteile von Windows Workflow Foundation nutzt, um die Automatisierung von Aufgaben mit langer Ausführungszeit zu ermöglichen.

-   [Odata-Verwaltung](/powershell/scripting/developer/webservices/creating-a-management-odata-web-service?view=powershell-7&preserve-view=true)

    **Neu!** Auch bekannt als Windows PowerShell-Webdienste, Management odata, neu in Windows PowerShell v3, ermöglicht die Erstellung eines ASP.NET-Webdienst-Endpunkts, der Verwaltungsdaten verfügbar macht, die durch Windows PowerShell-Befehle als odata-Webdienst Entitäten bereitstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Server 2012 R2 auf TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 und Windows Server 2012 in der TechNet-Bibliothek](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 auf Microsoft.com](https://www.microsoft.com/evalcenter/evaluate-windows-server-2012-r2-essentials)
</dt> </dl>

 

 
