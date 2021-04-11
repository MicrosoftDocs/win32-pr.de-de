---
description: Verwenden von VDS
ms.assetid: aa4be499-625d-4dbd-828c-4a55ff2dba2c
title: Verwenden von VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c648c5cc2507c4819f98367c367099248a0e723f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218174"
---
# <a name="using-vds"></a>Verwenden von VDS

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

VDS bietet eine Schnittstelle für die Skripterstellung und GUI-Entwicklung, die die Aktivitäten vereinfachen kann, die von einem Windows Server-Administrator ausgeführt werden, der einen heterogenen Satz von Speichersystemen verwaltet und Daten über verschiedene Hardware Konfigurationen hinweg migriert. Wenn Sie mit den in der VDS-Entwicklung verwendeten Objekten nicht vertraut sind, lesen Sie das [VDS-Objektmodell](vds-object-model.md).

Einige Punkte, bevor Sie beginnen:

-   Während VDS einen Softwareanbieter enthält, müssen Sie einen Hardware Anbieter und die zugehörige Hardware separat erwerben, um die Hardware Anbieter Vorgänge nutzen zu können. Installationsanweisungen finden Sie in der Dokumentation, die vom Hardwarehersteller bereitgestellt wird.
-   Für einige Vorgänge sind NTFS-formatierte Volumes erforderlich. Wenn Sie z. b. ein Volume in einem vorhandenen Verzeichnis einbinden, muss das Volume, das das Verzeichnis enthält, mit NTFS formatiert sein. Dieser Vorgang wird von anderen Dateisystemen nicht unterstützt. Informationen zu Vorgängen, die NTFS erfordern, finden Sie auf der Seite jeder Methode in der [VDS-Referenz](vds-reference.md).

## <a name="programming-languages"></a>Programmiersprachen

Verwenden Sie jede beliebige Programmiersprache, die für die Entwicklung mit com geeignet ist, z. b. die Programmiersprache C oder C++.

## <a name="security"></a>Sicherheit

Die Windows-Firewall ist standardmäßig aktiviert. Dies kann dazu führen, dass die Authentifizierung für Rückruf Schnittstellen fehlschlägt, z. b. [**ivdsadvisesink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink), die Remote ausgeführt werden können. Wenn die Windows-Firewall auf dem Client oder auf dem Server aktiviert ist, müssen Sie die Remotevolumeverwaltung der Registerkarte **Ausnahmen** in der Windows-Firewall hinzufügen.

**Windows Server 2003:** Wenn in Windows Server 2003 mit Service Pack 2 (SP2) und Windows Server 2003 mit Service Pack 1 (SP1) die Windows-Firewall auf dem Client oder auf dem Server aktiviert ist und der Server für die Verwendung der NTLM-Authentifizierung konfiguriert ist, müssen Sie die folgenden Einstellungen der Registerkarte **Ausnahmen** in der Windows-Firewall für den entsprechenden Computer hinzufügen.

| Computer                 | Ausnahmen Einstellungen                                                                 |
|--------------------------|-------------------------------------------------------------------------------------|
| Client Computer (lokal)  | Dmremote.exe<br/> Mmc.exe<br/> Vdsldr.exe<br/> TCP 135<br/> |
| Server Computer (Remote) | Dmadmin.exe<br/> Vds.exe<br/> TCP 135<br/>                        |



 

Beachten Sie, dass die Windows-Firewall bis Windows Server 2003 mit SP1 standardmäßig nicht aktiviert ist.

Eine Anwendung, die VDS verwendet, muss unter dem Konto "Backup Operator" oder "Administratoren" ausgeführt werden. Ohne die entsprechenden Berechtigungen kann eine Anwendung ein Service Loader-Objekt erstellen, aber das Objekt lädt keine VDS. Stattdessen wird ein Fehler zurückgegeben, der angibt, dass der Zugriff auf VDS verweigert wird.

Wenn das Netzwerk die NTLM-Authentifizierung verwendet, sollte der Client Computer den anonymen Zugriff zulassen. In diesem Fall ist der anonyme Zugriff standardmäßig aktiviert, wenn auf dem Client Computer ein Windows Server-Betriebssystem ausgeführt wird. Wenn ein Windows-Client Betriebssystem ausgeführt wird, muss der anonyme Zugriff mithilfe von Dcomcnfg.exe aktiviert werden.

## <a name="configuration-and-query-operations"></a>Konfigurations-und Abfrage Vorgänge

Konfigurations-und Abfrage Vorgänge werden durch den relevantesten Computer, Anbieter, Subsystem oder Paket definiert. Abfragen durchlaufen nur einen Anbieter oder eine Ebene der Bindungs Hierarchie. Zum Erstellen einer vollständigen Ansicht muss der Aufrufer jede Ebene über-und Abfragen. Die folgende Liste enthält Beispiele:

-   Zum Anzeigen aller Datenträger auf einem Computer müssen Aufrufer alle Softwareanbieter für die Datenträger Abfragen, die von diesen Anbietern beansprucht werden.
-   Um zu ermitteln, welche Datenträger zu einem Software gestapelten Volume beitragen, bestimmen Aufrufer zuerst die Beitragenden plexes und Fragen dann die Datenträger Blöcke für die einzelnen Plex ab.
-   Um alle Laufwerke anzuzeigen, die an ein bestimmtes Subsystem angefügt sind, müssen Aufrufer das Subsystem Abfragen.
-   Um alle LUNs anzuzeigen, die von einem bestimmten Subsystem verfügbar gemacht werden, müssen Aufrufer das Subsystem Abfragen.
-   Um den gesamten Speicher in einem SAN oder Cluster anzuzeigen, müssen Aufrufer jeden Computer nach allen Hardwareanbietern Abfragen, jeden Anbieter nach allen Subsystemen Abfragen und dann jedes Subsystem Abfragen.

Obwohl jede einzelne Abfrage keine Duplikate zurückgibt, können wiederholte Abfragen über mehrere Computer oder über Anbieter hinweg Duplikate anhäufen. Aufrufer müssen alle Filter implementieren. Beachten Sie auch, dass San-Verwaltungs Anwendungen die Active Directory oder ein Repository zum Beibehalten von Konfigurationsinformationen verwenden können. Es ist möglicherweise nicht erforderlich, jeden Computer abzufragen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dienst für virtuelle Datenträger](virtual-disk-service-portal.md)
</dt> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> <dt>

[VDS-Referenz](vds-reference.md)
</dt> </dl>

 

