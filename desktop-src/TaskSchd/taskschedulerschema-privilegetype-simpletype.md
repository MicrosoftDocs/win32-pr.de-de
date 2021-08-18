---
title: privilegeType Simple Type
description: Berechtigungen bestimmen den Typ der Systemvorgänge, die ein Benutzerkonto ausführen kann. Ein Administrator weist Benutzer- und Gruppenkonten Berechtigungen zu. Die Berechtigungen jedes Benutzers umfassen die Berechtigungen, die dem Benutzer und den Gruppen gewährt werden, zu denen der Benutzer gehört.
ms.assetid: 813b0886-ca76-4523-a1e6-42ca656851a7
keywords:
- privilegeType simple type Taskplaner
topic_type:
- apiref
api_name:
- privilegeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4502c22e31ca131dabd6d776337c3693a4d4bf4d7753734cf0e6291cf234fbe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002288"
---
# <a name="privilegetype-simple-type"></a>privilegeType Simple Type

Berechtigungen bestimmen den Typ der Systemvorgänge, die ein Benutzerkonto ausführen kann. Ein Administrator weist Benutzer- und Gruppenkonten Berechtigungen zu. Die Berechtigungen jedes Benutzers umfassen die Berechtigungen, die dem Benutzer und den Gruppen gewährt werden, zu denen der Benutzer gehört.

``` syntax
<xs:simpleType name="privilegeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="SeCreateTokenPrivilege"
         />
        <xs:enumeration
            value="SeAssignPrimaryTokenPrivilege"
         />
        <xs:enumeration
            value="SeLockMemoryPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseQuotaPrivilege"
         />
        <xs:enumeration
            value="SeUnsolicitedInputPrivilege"
         />
        <xs:enumeration
            value="SeMachineAccountPrivilege"
         />
        <xs:enumeration
            value="SeTcbPrivilege"
         />
        <xs:enumeration
            value="SeSecurityPrivilege"
         />
        <xs:enumeration
            value="SeTakeOwnershipPrivilege"
         />
        <xs:enumeration
            value="SeLoadDriverPrivilege"
         />
        <xs:enumeration
            value="SeSystemProfilePrivilege"
         />
        <xs:enumeration
            value="SeSystemtimePrivilege"
         />
        <xs:enumeration
            value="SeProfileSingleProcessPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseBasePriorityPrivilege"
         />
        <xs:enumeration
            value="SeCreatePagefilePrivilege"
         />
        <xs:enumeration
            value="SeCreatePermanentPrivilege"
         />
        <xs:enumeration
            value="SeBackupPrivilege"
         />
        <xs:enumeration
            value="SeRestorePrivilege"
         />
        <xs:enumeration
            value="SeShutdownPrivilege"
         />
        <xs:enumeration
            value="SeDebugPrivilege"
         />
        <xs:enumeration
            value="SeAuditPrivilege"
         />
        <xs:enumeration
            value="SeSystemEnvironmentPrivilege"
         />
        <xs:enumeration
            value="SeChangeNotifyPrivilege"
         />
        <xs:enumeration
            value="SeRemoteShutdownPrivilege"
         />
        <xs:enumeration
            value="SeUndockPrivilege"
         />
        <xs:enumeration
            value="SeSyncAgentPrivilege"
         />
        <xs:enumeration
            value="SeEnableDelegationPrivilege"
         />
        <xs:enumeration
            value="SeManageVolumePrivilege"
         />
        <xs:enumeration
            value="SeImpersonatePrivilege"
         />
        <xs:enumeration
            value="SeCreateGlobalPrivilege"
         />
        <xs:enumeration
            value="SeTrustedCredManAccessPrivilege"
         />
        <xs:enumeration
            value="SeRelabelPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseWorkingSetPrivilege"
         />
        <xs:enumeration
            value="SeTimeZonePrivilege"
         />
        <xs:enumeration
            value="SeCreateSymbolicLinkPrivilege"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Enumerationswerte

Der **einfache privilegeType-Typ** definiert die folgenden Werte.



| Wert                           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SeCreateTokenPrivilege          | Erforderlich, um ein primäres Token zu erstellen. Benutzerrecht: Erstellen Sie ein Tokenobjekt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeAssignPrimaryTokenPrivilege   | Erforderlich, um das primäre Token eines Prozesses zu zuweisen. Benutzerrecht: Ersetzen Sie ein Token auf Prozessebene.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeLockMemoryPrivilege           | Erforderlich, um physische Seiten im Arbeitsspeicher zu sperren. Benutzerrecht: Sperren Sie Seiten im Arbeitsspeicher. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeIncreaseQuotaPrivilege        | Erforderlich, um das einem Prozess zugewiesene Kontingent zu erhöhen. Benutzerrecht: Passen Sie die Arbeitsspeicherkontingente für einen Prozess an. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeUnsolicitedInputPrivilege     | Erforderlich, um nicht angeforderte Eingaben von einem Terminalgerät zu lesen. Benutzerrecht: Nicht zutreffend. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SeMachineAccountPrivilege       | Erforderlich, um ein Computerkonto zu erstellen. Benutzerrecht: Fügen Sie Arbeitsstationen zur Domäne hinzu. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeTcbPrivilege                  | Diese Berechtigung identifiziert den Besitzer als Teil der vertrauenswürdigen Computerbasis. Einigen vertrauenswürdigen geschützten Subsystemen wird diese Berechtigung gewährt. Benutzerrecht: Als Teil des Betriebssystems fungieren. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SeSecurityPrivilege             | Erforderlich, um eine Reihe von sicherheitsbezogenen Funktionen auszuführen, z. B. Steuern und Anzeigen von Überwachungsmeldungen. Diese Berechtigung identifiziert den Besitzer als Sicherheitsoperator. Benutzerrecht: Verwalten Sie die Überwachung und das Sicherheitsprotokoll. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeTakeOwnershipPrivilege        | Erforderlich, um den Besitz eines Objekts zu übernehmen, ohne dass ihm ein diskreter Zugriff gewährt wird. Mit dieser Berechtigung kann der Besitzerwert nur auf die Werte festgelegt werden, die der Besitzer berechtigterweise als Besitzer eines Objekts zuweisen kann. Benutzerrecht: Übernehmen Sie den Besitz von Dateien oder anderen Objekten. <br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| SeLoadDriverPrivilege           | Erforderlich zum Laden oder Entladen eines Gerätetreibers. Benutzerrecht: Laden und Entladen von Gerätetreibern. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemProfilePrivilege        | Erforderlich, um Profilerstellungsinformationen für das gesamte System zu sammeln. Benutzerrecht: Profilieren der Systemleistung. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemtimePrivilege           | Erforderlich, um die Systemzeit zu ändern. Benutzerrecht: Ändern Sie die Systemzeit. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeProfileSingleProcessPrivilege | Erforderlich, um Profilerstellungsinformationen für einen einzelnen Prozess zu sammeln. Benutzerrecht: Profil für einen einzelnen Prozess. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseBasePriorityPrivilege | Erforderlich, um die Basispriorität eines Prozesses zu erhöhen. Benutzerrecht: Erhöhen Sie die Planungspriorität. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeCreatePagefilePrivilege       | Erforderlich, um eine Auslagerungsdatei zu erstellen. Benutzerrecht: Erstellen Sie eine Auslagerungsdatei. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| SeCreatePermanentPrivilege      | Erforderlich, um ein permanentes -Objekt zu erstellen. Benutzerrecht: Erstellen Sie permanente freigegebene Objekte. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| SeBackupPrivilege               | Erforderlich, um Sicherungsvorgänge durchzuführen. Diese Berechtigung bewirkt, dass das System allen Dateien Lesezugriffssteuerung gewährt, unabhängig von der für die Datei angegebenen Zugriffssteuerungsliste (Access Control List, ACL). Jede andere Zugriffsanforderung als "Read" wird weiterhin mit der ACL ausgewertet. Diese Berechtigung ist für die RegSaveKey- und RegSaveKeyExnctions erforderlich. Die folgenden Zugriffsrechte werden gewährt, wenn diese Berechtigung erteilt wird: READ \_ CONTROL, ACCESS \_ SYSTEM \_ SECURITY, FILE \_ GENERIC \_ READ, FILE \_ TRAVERSE. Benutzerrecht: Sichern Sie Dateien und Verzeichnisse. <br/>                                                                                                                                     |
| SeRestorePrivilege              | Erforderlich, um Wiederherstellungsvorgänge durchzuführen. Diese Berechtigung bewirkt, dass das System jede Schreibzugriffssteuerung für jede Datei unabhängig von der für die Datei angegebenen Zugriffssteuerungsliste gewährt. Jede andere Zugriffsanforderung als "write" wird weiterhin mit der ACL ausgewertet. Darüber hinaus können Sie mit dieser Berechtigung einen gültigen Benutzer oder eine gültige Gruppensicherheits-ID (SID) als Besitzer einer Datei festlegen. Diese Berechtigung ist für die RegLoadKey-Funktion erforderlich. Die folgenden Zugriffsrechte werden gewährt, wenn diese Berechtigung erteilt wird: WRITE \_ DAC, WRITE \_ OWNER, ACCESS \_ SYSTEM \_ SECURITY, FILE \_ GENERIC \_ WRITE, FILE ADD \_ \_ FILE, FILE ADD \_ \_ SUBDIRECTORY, DELETE. Benutzerrecht: Dateien und Verzeichnisse wiederherstellen. <br/> |
| SeShutdownPrivilege             | Erforderlich, um ein lokales System herunterfahren zu können. Benutzerrecht: Fahren Sie das System herunter. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeDebugPrivilege                | Erforderlich zum Debuggen und Anpassen des Arbeitsspeichers eines Prozesses, der sich im Besitz eines anderen Kontos befindet. Benutzerrecht: Programme debuggen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeAuditPrivilege                | Erforderlich zum Generieren von Überwachungsprotokolleinträgen. Geben Sie diese Berechtigung, um Server zu schützen. Benutzerrecht: Generiert Sicherheitsüberprüfungen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| SeSystemEnvironmentPrivilege    | Erforderlich, um den nicht unwillingsfreien RAM von Systemen zu ändern, die diesen Speichertyp zum Speichern von Konfigurationsinformationen verwenden. Benutzerrecht: Ändern Sie die Werte der Firmwareumgebung. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeChangeNotifyPrivilege         | Erforderlich, um Benachrichtigungen über Änderungen an Dateien oder Verzeichnissen zu erhalten. Diese Berechtigung bewirkt auch, dass das System alle Traversalzugriffsüberprüfungen überspringt. Sie ist standardmäßig für alle Benutzer aktiviert. Benutzerrecht: Durchquerungsüberprüfung umgehen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeRemoteShutdownPrivilege       | Erforderlich, um ein System mithilfe einer Netzwerkanforderung herunterfahren zu können. Benutzerrecht: Erzwingen Sie das Herunterfahren von einem Remotesystem aus. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SeUndockPrivilege               | Erforderlich, um einen Laptop abzudocken. Benutzerrecht: Entfernen Sie den Computer aus der Dockingstation. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeSyncAgentPrivilege            | Erforderlich, damit ein Domänencontroller die LDAP-Verzeichnissynchronisierungsdienste verwenden kann. Mit dieser Berechtigung kann der Besitzer alle Objekte und Eigenschaften im Verzeichnis lesen, unabhängig vom Schutz der Objekte und Eigenschaften. Standardmäßig wird sie den Konten Administrator und LocalSystem auf Domänencontrollern zugewiesen. Benutzerrecht: Synchronisieren von Verzeichnisdienstdaten. <br/>                                                                                                                                                                                                                                                                                |
| SeEnableDelegationPrivilege     | Erforderlich, um Benutzer- und Computerkonten als vertrauenswürdig für die Delegierung zu kennzeichnen. Benutzerrecht: Aktivieren Sie Computer- und Benutzerkonten, damit sie für die Delegierung als vertrauenswürdig eingestuft werden. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeManageVolumePrivilege         | Erforderlich, um Volumeverwaltungsberechtigungen zu aktivieren. Benutzerrecht: Verwalten Sie die Dateien auf einem Volume. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeImpersonatePrivilege          | Erforderlich, um die Identität zu annehmen. Benutzerrecht: Annehmen der Identität eines Clients nach der Authentifizierung. Windows XP/2000: Diese Berechtigung wird nicht unterstützt. <br/> Beachten Sie, dass dieser Wert ab Windows Server 2003, Windows XP mit SP2 und Windows 2000 mit SP4 unterstützt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateGlobalPrivilege         | Erforderlich, um benannte Dateizuordnungsobjekte im globalen Namespace während Terminaldienstesitzungen zu erstellen. Diese Berechtigung ist standardmäßig für Administratoren, Dienste und das lokale Systemkonto aktiviert. Benutzerrecht: Erstellen sie globale Objekte. Windows XP/2000: Diese Berechtigung wird nicht unterstützt. <br/> Beachten Sie, dass dieser Wert ab Windows Server 2003, Windows XP mit SP2 und Windows 2000 mit SP4 unterstützt wird.<br/>                                                                                                                                                                                                                                        |
| SeTrustedCredManAccessPrivilege | Erforderlich, um als vertrauenswürdiger Aufrufer auf Anmeldeinformationsverwaltung zuzugreifen. Benutzerrecht: Zugriff Anmeldeinformationsverwaltung als vertrauenswürdiger Aufrufer. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeRelabelPrivilege              | Erforderlich, um die erforderliche Integritätsebene eines Objekts zu ändern. Benutzerrecht: Ändern sie eine Objektbezeichnung. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseWorkingSetPrivilege   | Erforderlich, um mehr Arbeitsspeicher für Anwendungen zuzuweisen, die im Kontext von Benutzern ausgeführt werden. Benutzerrecht: Erhöhen Sie ein Prozessarbeitssatz. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| SeTimeZonePrivilege             | Erforderlich, um die Zeitzone anzupassen, die der internen Uhr des Computers zugeordnet ist. Benutzerrecht: Ändern Sie die Zeitzone. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateSymbolicLinkPrivilege   | Erforderlich, um eine symbolische Verknüpfung zu erstellen. Benutzerrecht: Erstellen Sie symbolische Verknüpfungen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



 

 





