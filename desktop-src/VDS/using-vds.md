---
description: Verwenden von VDS
ms.assetid: aa4be499-625d-4dbd-828c-4a55ff2dba2c
title: Verwenden von VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6406e938a8fb49314511047bb038ec94a5af9151f5c077ad1fb14984e74474f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125866"
---
# <a name="using-vds"></a>Verwenden von VDS

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

VDS stellt eine Schnittstelle für die Skripterstellung und GUI-Entwicklung bereit, die die Aktivitäten vereinfachen kann, die von einem Windows-Serveradministrator ausgeführt werden, der einen heterogenen Satz von Speichersystemen verwaltet und Daten im Laufe der Zeit über verschiedene Hardwarekonfigurationen migriert. Wenn Sie mit den Objekten, die in der VDS-Entwicklung verwendet werden, nicht vertraut sind, finden Sie weitere Informationen unter [VDS-Objektmodell.](vds-object-model.md)

Einige Punkte, bevor Sie beginnen:

-   VdS umfasst zwar einen Softwareanbieter, Sie müssen jedoch einen Hardwareanbieter und die zugehörige Hardware separat erwerben, um die Hardwareanbietervorgänge nutzen zu können. Installationsanweisungen finden Sie in der Dokumentation des Hardwareherstellers.
-   Einige Vorgänge erfordern NTFS-formatierte Volumes. Wenn Sie beispielsweise ein Volume in einem vorhandenen Verzeichnis einbinden, muss das Volume, das das Verzeichnis enthält, mit NTFS formatiert werden. Andere Dateisysteme unterstützen diesen Vorgang nicht. Informationen zu Vorgängen, die NTFS erfordern, finden Sie auf jeder Methodenseite in [der VDS-Referenz.](vds-reference.md)

## <a name="programming-languages"></a>Programmiersprachen

Verwenden Sie eine beliebige Programmiersprache, die für die Entwicklung mit COM geeignet ist, z. B. C oder C++.

## <a name="security"></a>Sicherheit

Windows Die Firewall ist standardmäßig aktiviert. Dies kann dazu führen, dass die Authentifizierung für Rückrufschnittstellen wie [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)fehlschlägt, die remote ausgeführt werden können. Wenn Windows Firewall auf dem Client oder dem Server aktiviert ist, müssen Sie die Remotevolumeverwaltung zur Registerkarte **Ausnahmen** in Windows Firewall hinzufügen.

**Windows Server 2003:** Wenn Windows Server 2003 mit Service Pack 2 (SP2) und Windows Server 2003 mit Service Pack 1 (SP1) Windows Firewall entweder auf dem Client oder dem Server aktiviert ist und der Server für die Verwendung der NTLM-Authentifizierung konfiguriert ist, müssen Sie die folgenden Einstellungen auf der Registerkarte **Ausnahmen** in Windows Firewall für den entsprechenden Computer hinzufügen.

| Computer                 | Ausnahmeneinstellungen                                                                 |
|--------------------------|-------------------------------------------------------------------------------------|
| Clientcomputer (lokal)  | Dmremote.exe<br/> Mmc.exe<br/> Vdsldr.exe<br/> TCP 135<br/> |
| Servercomputer (Remote) | Dmadmin.exe<br/> Vds.exe<br/> TCP 135<br/>                        |



 

Beachten Sie, dass Windows Firewall erst Windows Server 2003 mit SP1 standardmäßig aktiviert ist.

Eine Anwendung, die VDS verwendet, muss unter dem Gruppenkonto "Sicherungsoperator" oder "Administratoren" ausgeführt werden. Ohne die entsprechenden Berechtigungen kann eine Anwendung ein Dienstladeprogrammobjekt erstellen, aber das Objekt lädt VDS nicht. Stattdessen wird ein Fehler zurückgegeben, der angibt, dass der Zugriff auf VDS verweigert wird.

Wenn das Netzwerk die NTLM-Authentifizierung verwendet, sollte der Clientcomputer anonymen Zugriff zulassen. In diesem Fall ist der anonyme Zugriff standardmäßig aktiviert, wenn auf dem Clientcomputer ein Windows Server-Betriebssystem ausgeführt wird. Wenn ein Windows Clientbetriebssystem ausgeführt wird, muss der anonyme Zugriff über Dcomcnfg.exe aktiviert werden.

## <a name="configuration-and-query-operations"></a>Konfigurations- und Abfragevorgänge

Konfigurations- und Abfragevorgänge werden vom relevantesten Computer, Anbieter, Subsystem oder Paket erfasst. Abfragen durchlaufen nur einen Anbieter oder eine Ebene der Bindungshierarchie. Um eine vollständige Ansicht zu erstellen, muss der Aufrufer jede Ebene abfragen. Die folgende Liste enthält Beispiele:

-   Um alle Datenträger auf einem Computer anzuzeigen, müssen Aufrufer alle Softwareanbieter nach den Datenträgern abfragen, die von diesen Anbietern beansprucht werden.
-   Um zu bestimmen, welche Datenträger zu einem mit Software gestapelten Volume beitragen, bestimmen Aufrufer zunächst die mitwirkenden Plexes und fragen dann die Datenträger-Erweiterungen für jedes Plex ab.
-   Um alle Laufwerke anzuzeigen, die an ein bestimmtes Subsystem angefügt sind, müssen Aufrufer das Subsystem abfragen.
-   Um alle LUNs anzuzeigen, die von einem bestimmten Subsystem verfügbar gemacht werden, müssen Aufrufer das Subsystem abfragen.
-   Um den gesamten Speicher in einem SAN oder Cluster anzuzeigen, müssen Aufrufer jeden Computer nach allen Hardwareanbietern abfragen, jeden Anbieter für alle Subsysteme abfragen und dann jedes Subsystem abfragen.

Während jede einzelne Abfrage keine Duplikate zurückgibt, können wiederholte Abfragen computer- oder anbieterübergreifend Duplikate sammeln. Aufrufer müssen filtering implementieren. Beachten Sie auch, dass SAN-Verwaltungsanwendungen Active Directory oder ein Repository verwenden können, um Konfigurationsinformationen dauerhaft zu speichern. Es ist möglicherweise nicht erforderlich, jeden Computer abzufragen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dienst für virtuelle Datenträger](virtual-disk-service-portal.md)
</dt> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> <dt>

[VDS-Referenz](vds-reference.md)
</dt> </dl>

 

