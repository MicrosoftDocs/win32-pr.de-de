---
title: Schlichter PrivilegeType-Typ
description: Berechtigungen bestimmen den Typ der System Vorgänge, die ein Benutzerkonto ausführen kann. Ein Administrator weist Benutzer-und Gruppenkonten Berechtigungen zu. Zu den Berechtigungen des Benutzers gehören die Berechtigungen, die dem Benutzer gewährt wurden, sowie die Gruppen, zu denen der Benutzer gehört.
ms.assetid: 813b0886-ca76-4523-a1e6-42ca656851a7
keywords:
- privilegiertype Simple Type Taskplaner
topic_type:
- apiref
api_name:
- privilegeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4864364a4752d72bd5305c5c2591b7d27391517f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342412"
---
# <a name="privilegetype-simple-type"></a>Schlichter PrivilegeType-Typ

Berechtigungen bestimmen den Typ der System Vorgänge, die ein Benutzerkonto ausführen kann. Ein Administrator weist Benutzer-und Gruppenkonten Berechtigungen zu. Zu den Berechtigungen des Benutzers gehören die Berechtigungen, die dem Benutzer gewährt wurden, sowie die Gruppen, zu denen der Benutzer gehört.

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

Der einfache Typ **PrivilegeType** definiert die folgenden Werte.



| Wert                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SeCreateTokenPrivilege          | Erforderlich, um ein primäres Token zu erstellen. Benutzerrecht: Erstellen Sie ein Tokenobjekt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeAssignPrimaryTokenPrivilege   | Erforderlich, um das primäre Token eines Prozesses zuzuweisen. Benutzerrecht: Ersetzen Sie ein Token auf Prozessebene.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeLockMemoryPrivilege           | Erforderlich, um physische Seiten im Arbeitsspeicher zu sperren. Benutzerrecht: Sperren von Seiten im Speicher. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeIncreaseQuotaPrivilege        | Erforderlich, um das einem Prozess zugewiesene Kontingent zu erhöhen. Benutzerrecht: passen Sie Arbeitsspeicher Kontingente für einen Prozess an. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| "Bunsolicitedinputprivilege"     | Erforderlich zum Lesen von nicht angeforderten Eingaben von einem Terminal Gerät. Benutzerrecht: nicht zutreffend. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SeMachineAccountPrivilege       | Zum Erstellen eines Computer Kontos erforderlich. Benutzerrecht: Arbeitsstationen zur Domäne hinzufügen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeTcbPrivilege                  | Dieses Privileg identifiziert seinen Inhaber als Teil der vertrauenswürdigen Computer Basis. Einigen vertrauenswürdigen geschützten Subsystemen wird dieses Privileg erteilt. Benutzerrecht: fungieren Sie als Teil des Betriebssystems. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SeSecurityPrivilege             | Ist erforderlich, um eine Reihe von sicherheitsbezogenen Funktionen auszuführen, z. b. das Steuern und Anzeigen von Überwachungs Nachrichten. Dieses Privileg identifiziert seinen Inhaber als Sicherheits Operator. Benutzerrecht: Verwalten der Überwachung und des Sicherheitsprotokolls. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeTakeOwnershipPrivilege        | Erforderlich, um den Besitz eines Objekts zu übernehmen, ohne freigegebenen Zugriff zu erhalten. Diese Berechtigung ermöglicht es, dass der Besitzer Wert nur auf die Werte festgelegt wird, die der Inhaber rechtmäßig als Besitzer eines Objekts zuweisen kann. Benutzerrecht: übernehmen Sie den Besitz von Dateien oder anderen Objekten. <br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| SeLoadDriverPrivilege           | Erforderlich zum Laden oder Entladen eines Gerätetreibers. Benutzerrecht: Gerätetreiber laden und entladen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemProfilePrivilege        | Erforderlich, um Profil Erstellungs Informationen für das gesamte System zu erfassen. Benutzerrecht: Profilsystem Leistung. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemtimePrivilege           | Erforderlich, um die Systemzeit zu ändern. Benutzerrecht: Ändern Sie die Systemzeit. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeProfileSingleProcessPrivilege | Erforderlich, um Profil Erstellungs Informationen für einen einzelnen Prozess zu erfassen. Benutzerrecht: Profil für einen einzelnen Prozess. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseBasePriorityPrivilege | Erforderlich, um die Basis Priorität eines Prozesses zu erhöhen. Benutzerrecht: erhöhen Sie die Planungs Priorität. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeCreatePagefilePrivilege       | Erforderlich zum Erstellen einer Auslagerungs Datei. Benutzerrecht: Erstellen Sie eine Pagefile-Datei. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| SeCreatePermanentPrivilege      | Erforderlich, um ein dauerhaftes Objekt zu erstellen. Benutzerrecht: Erstellen Sie permanente freigegebene Objekte. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| SeBackupPrivilege               | Zum Ausführen von Sicherungs Vorgängen erforderlich. Diese Berechtigung bewirkt, dass das System allen Dateien alle Lese Zugriffs Steuerungen zuweist, unabhängig von der Zugriffs Steuerungs Liste (ACL), die für die Datei angegeben wurde. Alle anderen Zugriffs Anforderungen als Read werden weiterhin mit der ACL ausgewertet. Diese Berechtigung wird von regsavekey und regsavekeyexfunctions benötigt. Wenn diese Berechtigung gewährt wird, werden die folgenden Zugriffsrechte gewährt: Lese \_ Kontrolle, Zugriffs \_ System \_ Sicherheit, dateigenerischer Lesevorgang \_ \_ , Datei \_ Durchlauf. Benutzerrecht: Sichern Sie Dateien und Verzeichnisse. <br/>                                                                                                                                     |
| SeRestorePrivilege              | Zum Ausführen von Wiederherstellungs Vorgängen erforderlich. Diese Berechtigung bewirkt, dass das System alle Schreibzugriffs Berechtigungen allen Dateien erteilt, unabhängig von der für die Datei angegebenen ACL. Alle anderen Zugriffs Anforderungen als Write werden weiterhin mit der ACL ausgewertet. Darüber hinaus können Sie mit dieser Berechtigung einen beliebigen gültigen Benutzer-oder Gruppen Sicherheits Bezeichner (SID) als Besitzer einer Datei festlegen. Diese Berechtigung ist für die RegLoadKey-Funktion erforderlich. Die folgenden Zugriffsrechte werden gewährt, wenn dieses Privileg besteht: Schreiben von \_ DAC, Schreiben von \_ Besitzern, zugreifen auf \_ System \_ Sicherheit, Datei \_ generischer \_ Schreibvorgang, Datei Datei \_ Hinzufügen \_ , Datei \_ Hinzufügen \_ Unterverzeichnis, löschen. Benutzerrecht: Stellen Sie Dateien und Verzeichnisse wieder her. <br/> |
| SeShutdownPrivilege             | Ist erforderlich, um ein lokales System herunterzufahren. Benutzerrecht: fahren Sie das System herunter. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeDebugPrivilege                | Erforderlich, um den Arbeitsspeicher eines Prozesses zu Debuggen und anzupassen, der im Besitz eines anderen Kontos ist Benutzerrecht: Debuggen von Programmen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeAuditPrivilege                | Erforderlich, um Überwachungs Protokolleinträge zu generieren. Stellen Sie diese Berechtigung sicheren Servern zur Verfügung. Benutzerrecht: Generieren von Sicherheits Überwachungen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| SeSystemEnvironmentPrivilege    | Erforderlich, um den nicht flüchtigen RAM von Systemen zu ändern, die diese Art von Arbeitsspeicher zum Speichern von Konfigurationsinformationen verwenden. Benutzerrecht: Ändern Sie die Werte der Firmware-Umgebung. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeChangeNotifyPrivilege         | Erforderlich, um Benachrichtigungen über Änderungen an Dateien oder Verzeichnissen zu empfangen. Diese Berechtigung bewirkt auch, dass das System alle Überprüfungen des Durchlaufs überspringt. Sie ist standardmäßig für alle Benutzer aktiviert. Benutzerrecht: Umgehung der traversierungs Überprüfung. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeRemoteShutdownPrivilege       | Zum Herunterfahren eines Systems mit einer Netzwerk Anforderung erforderlich. Benutzerrecht: Erzwingen des herunter Fahrens von einem Remote System aus. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SeUndockPrivilege               | Erforderlich zum Abdocken eines Laptops. Benutzerrecht: Entfernen Sie den Computer aus der Docking Station. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeSyncAgentPrivilege            | Erforderlich für einen Domänen Controller zur Verwendung der LDAP-Verzeichnis Synchronisierungs Dienste. Diese Berechtigung ermöglicht es dem Inhaber, alle Objekte und Eigenschaften im Verzeichnis zu lesen, unabhängig vom Schutz der Objekte und Eigenschaften. Standardmäßig wird Sie den Konten "Administrator" und "LocalSystem" auf Domänen Controllern zugewiesen. Benutzerrecht: Synchronisieren von Verzeichnisdienst Daten. <br/>                                                                                                                                                                                                                                                                                |
| SeEnableDelegationPrivilege     | Erforderlich, um Benutzer-und Computer Konten als vertrauenswürdig für die Delegierung zu markieren. Benutzerrecht: Aktivieren Sie Computer-und Benutzerkonten für die Delegierung als vertrauenswürdig. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeManageVolumePrivilege         | Erforderlich zum Aktivieren von Volumen Verwaltungs Berechtigungen. Benutzerrecht: Verwalten Sie die Dateien auf einem Volume. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeImpersonatePrivilege          | Erforderlich, um einen Identitätswechsel auszuführen. Benutzerrecht: Identität eines Clients nach der Authentifizierung annehmen Windows XP/2000: dieses Privileg wird nicht unterstützt. <br/> Beachten Sie, dass dieser Wert ab Windows Server 2003, Windows XP mit SP2 und Windows 2000 mit SP4 unterstützt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateGlobalPrivilege         | Erforderlich zum Erstellen benannter Datei Zuordnung-Objekte im globalen Namespace während der Terminal Dienste-Sitzungen. Diese Berechtigung ist für Administratoren, Dienste und das lokale Systemkonto standardmäßig aktiviert. Benutzerrecht: Erstellen Sie globale Objekte. Windows XP/2000: dieses Privileg wird nicht unterstützt. <br/> Beachten Sie, dass dieser Wert ab Windows Server 2003, Windows XP mit SP2 und Windows 2000 mit SP4 unterstützt wird.<br/>                                                                                                                                                                                                                                        |
| SeTrustedCredManAccessPrivilege | Muss als vertrauenswürdiger Aufrufer auf Credential Manager zugreifen können. Benutzerrecht: greifen Sie als vertrauenswürdiger Aufrufer auf Credential Manager zu. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeRelabelPrivilege              | Erforderlich zum Ändern der obligatorischen Integritäts Stufe eines Objekts. Benutzerrecht: Ändern Sie eine Objekt Bezeichnung. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseWorkingSetPrivilege   | Erforderlich, um mehr Arbeitsspeicher für Anwendungen zuzuweisen, die im Kontext von Benutzern ausgeführt werden. Benutzerrecht: erhöhen Sie einen Prozess Arbeitssatz. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| SeTimeZonePrivilege             | Erforderlich, um die Zeitzone anzupassen, die der internen Uhr des Computers zugeordnet ist. Benutzerrecht: Ändern Sie die Zeitzone. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateSymbolicLinkPrivilege   | Erforderlich, um eine symbolische Verknüpfung zu erstellen. Benutzerrecht: Erstellen Sie symbolische Verknüpfungen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

 





