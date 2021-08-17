---
title: Win32_TSLicenseServer-Klasse
description: Stellt Methoden und Eigenschaften zum Anzeigen und Konfigurieren Remotedesktop Lizenzierung (RD-Lizenzierung) auf einem Remotedesktop Lizenzserver bereit.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseServer-Klassen-Remotedesktopdienste
- Win32_TSLicenseServer -Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer
- Win32_TSLicenseServer.FirstName
- Win32_TSLicenseServer.LastName
- Win32_TSLicenseServer.Company
- Win32_TSLicenseServer.CountryRegion
- Win32_TSLicenseServer.eMail
- Win32_TSLicenseServer.OrgUnit
- Win32_TSLicenseServer.Address
- Win32_TSLicenseServer.City
- Win32_TSLicenseServer.State
- Win32_TSLicenseServer.PostalCode
- Win32_TSLicenseServer.ServerRole
- Win32_TSLicenseServer.DatabasePath
- Win32_TSLicenseServer.ProductId
- Win32_TSLicenseServer.Version
- Win32_TSLicenseServer.VersionNumber
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7c73c1d1a48bbc76b4988afca8a07fd9ce505d0633c74f67306901259d9f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126510"
---
# <a name="win32_tslicenseserver-class"></a>Win32 \_ TSLicenseServer-Klasse

Stellt Methoden und Eigenschaften zum Anzeigen und Konfigurieren Remotedesktop Lizenzierung (RD-Lizenzierung) auf einem Remotedesktop Lizenzserver bereit.

## <a name="syntax"></a>Syntax

``` syntax
[singleton, dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseServer
{
  string FirstName;
  string LastName;
  string Company;
  string CountryRegion;
  string eMail;
  string OrgUnit;
  string Address;
  string City;
  string State;
  string PostalCode;
  uint32 ServerRole;
  string DatabasePath;
  string ProductId;
  string Version;
  string VersionNumber;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSLicenseServer-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSLicenseServer-Klasse** verfügt über diese Methoden.



| Methode                                                                                   | Beschreibung                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateServer**](activateserver-win32-tslicenseserver.md)                           | Aktiviert den Remotedesktop Lizenzserver mithilfe einer Remotedesktop Lizenzserver-ID, die über das Telefon oder das Internet abgerufen wird.<br/>                                                                                           |
| [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)         | Aktiviert den Remotedesktop Lizenzserver automatisch über das Internet. Die Eigenschaften **FirstName,** **LastName,** **Company** und **CountryRegion** dürfen nicht leer sein, wenn diese Methode aufgerufen wird. Andernfalls schlägt die Methode fehl.<br/> |
| [**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)                       | Fügt den Remotedesktop Lizenzserver der Gruppe Remotedesktop Lizenzserver auf einem Domänencontroller in derselben Domäne wie der Lizenzserver hinzu.<br/>                                                                                |
| [**ChangeRole**](changerole-win32-tslicenseserver.md)                                   | Ändert den Ermittlungsbereich des Remotedesktop Lizenzservers.<br/>                                                                                                                                                                  |
| [**CreateTSCGroup**](createtscgroup-win32-tslicenseserver.md)                           | Diese Methode wird nicht unterstützt.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Erstellt die lokale Gruppe Terminalservercomputer auf dem Remotedesktop Lizenzserver.<br/>                                               |
| [**DeactivateServer**](deactivateserver-win32-tslicenseserver.md)                       | Deaktiviert den Remotedesktop Lizenzserver mithilfe eines Bestätigungscodes, der über das Telefon empfangen wird.<br/>                                                                                                                        |
| [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md)     | Deaktiviert den Remotedesktop Lizenzserver über das Internet. Die Eigenschaften **FirstName** und **LastName** dürfen nicht leer sein, wenn diese Methode aufgerufen wird. Andernfalls schlägt die Methode fehl.<br/>                                              |
| [**GetActivationStatus**](getactivationstatus-win32-tslicenseserver.md)                 | Ruft den aktuellen Aktivierungsstatus ab.<br/>                                                                                                                                                                                           |
| [**GetLicenseServerId**](getlicenseserverid-win32-tslicenseserver.md)                   | Ruft eine Remotedesktop Lizenzserver-ID ab, wenn der Server derzeit aktiviert ist.<br/>                                                                                                                                                 |
| [**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)                         | Ruft ab, ob der Remotedesktop Lizenzserver Mitglied der Gruppe Remotedesktop Lizenzserver auf einem Domänencontroller in einer bestimmten Domäne ist.<br/>                                                                              |
| [**IsLSonDC**](islsondc-win32-tslicenseserver.md)                                       | Ruft ab, ob die RD-Lizenzierung auf einem Domänencontroller installiert ist.<br/>                                                                                                                                                                |
| [**IsLSPreventUpgradeGPEnabled**](islspreventupgradegpenabled-win32-tslicenseserver.md) | Ruft ab, ob die Gruppenrichtlinieneinstellung "Lizenzupgrade verhindern" auf dem Remotedesktop Lizenzserver aktiviert ist.<br/>                                                                                                              |
| [**IsLSPublished**](islspublished-win32-tslicenseserver.md)                             | Ruft ab, ob der Remotedesktop Lizenzserver in Active Directory Domain Services (AD DS) veröffentlicht wird.<br/>                                                                                                                      |
| [**IsLSRegisteredToSCP**](win32-tslicenseserver-islsregisteredtoscp.md)                 | Ruft ab, ob der Remotedesktop Lizenzserver als Dienstverbindungspunkt in Active Directory Domain Services registriert ist.<br/>                                                                                               |
| [**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)                 | Ruft ab, ob die Gruppenrichtlinieneinstellung "Lizenzserversicherheitsgruppe" auf dem Remotedesktop Lizenzserver aktiviert ist.<br/>                                                                                                        |
| [**IsSecureAccessAllowed**](issecureaccessallowed-win32-tslicenseserver.md)             | Ruft ab, ob ein RD-Sitzungshost Server Remotedesktopdienste Clientzugriffslizenzen (RDS CALs) vom Remotedesktop Lizenzserver anfordern darf.<br/>                                                                |
| [**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)                     | Diese Methode wird nicht unterstützt.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Ruft ab, ob die lokale Gruppe Terminalservercomputer auf dem Remotedesktop Lizenzserver vorhanden ist.<br/>                              |
| [**IsTSinTSCGroup**](istsintscgroup-win32-tslicenseserver.md)                           | Ruft ab, ob ein RD-Sitzungshost Server Mitglied der lokalen Gruppe Terminalservercomputer auf dem Remotedesktop Lizenzserver ist.<br/>                                                                                         |
| [**PublishLS**](publishls-win32-tslicenseserver.md)                                     | Veröffentlicht den Remotedesktop Lizenzserver in AD DS.<br/>                                                                                                                                                                              |
| [**ReactivateServer**](reactivateserver-win32-tslicenseserver.md)                       | Reaktiviert den Remotedesktop Lizenzserver mithilfe einer neuen Remotedesktop Lizenzserver-ID, die über das Telefon oder das Internet abgerufen wird.<br/>                                                                                     |
| [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)     | Reaktiviert den Remotedesktop Lizenzserver über das Internet. Die Eigenschaften **FirstName** und **LastName** dürfen nicht leer sein, wenn diese Methode aufgerufen wird. Andernfalls schlägt die Methode fehl.<br/>                                              |
| [**RegisterLSToSCP**](win32-tslicenseserver-registerlstoscp.md)                         | Registriert den Remotedesktop Lizenzserver als Dienstverbindungspunkt in Active Directory Domain Services.<br/>                                                                                                                     |
| [**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)             | Entfernt den Remotedesktop Lizenzserver aus der Gruppe Remotedesktop Lizenzserver auf einem Domänencontroller in derselben Domäne wie der Lizenzserver.<br/>                                                                           |
| [**RemoveTSCGroup**](removetscgroup-win32-tslicenseserver.md)                           | Diese Methode wird nicht unterstützt.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Entfernt die lokale Gruppe Terminalservercomputer vom Remotedesktop Lizenzserver.<br/>                                             |
| [**UnpublishLS**](unpublishls-win32-tslicenseserver.md)                                 | Aufheben der Veröffentlichung eines Remotedesktop Lizenzservers aus AD DS.<br/>                                                                                                                                                                            |
| [**UnRegisterLSFromSCP**](win32-tslicenseserver-unregisterlsfromscp.md)                 | Entfernt den Remotedesktop Lizenzserver als Dienstverbindungspunkt in Active Directory Domain Services.<br/>                                                                                                                       |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSLicenseServer-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Adresse**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Adresse des Kontakts für die RD-Lizenzierung. Diese Eigenschaft wird verwendet, wenn die [**ActivateServerAutomatic-Methode**](activateserverautomatic-win32-tslicenseserver.md) aufgerufen wird. (Diese Eigenschaft ist bei Verwendung der **ActivateServerAutomatic-Methode** optional.)

</dd> <dt>

**City (Ort)**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ort des Kontakts für die RD-Lizenzierung. Diese Eigenschaft wird verwendet, wenn die [**ActivateServerAutomatic-Methode**](activateserverautomatic-win32-tslicenseserver.md) aufgerufen wird. (Diese Eigenschaft ist bei Verwendung der **ActivateServerAutomatic-Methode** optional.)

</dd> <dt>

**Company**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Unternehmen des Kontakts für die RD-Lizenzierung. Diese Eigenschaft wird verwendet (und erforderlich), wenn die [**ActivateServerAutomatic-Methode**](activateserverautomatic-win32-tslicenseserver.md) aufgerufen wird.

</dd> <dt>

**Countryregion**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Land/Region des Kontakts für die RD-Lizenzierung. Diese Eigenschaft wird verwendet (und erforderlich), wenn die [**ActivateServerAutomatic-Methode**](activateserverautomatic-win32-tslicenseserver.md) aufgerufen wird.

</dd> <dt>

**Databasepath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Pfad der RDS-Lizenzierungsdatenbank.

</dd> <dt>

**E-Mail**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

E-Mail-Adresse des Kontakts für die RD-Lizenzierung. Diese Eigenschaft wird verwendet, wenn die [**Methoden ActivateServerAutomatic,**](activateserverautomatic-win32-tslicenseserver.md) [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)oder [**DeactivateServerAutomatic aufgerufen**](deactivateserverautomatic-win32-tslicenseserver.md) werden. (Diese Eigenschaft ist für diese Methodenaufrufe optional.)

</dd> <dt>

**Vorname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Vorname des Kontakts für die RD-Lizenzierung. Diese Eigenschaft wird verwendet (und erforderlich), wenn die [**Methoden ActivateServerAutomatic,**](activateserverautomatic-win32-tslicenseserver.md) [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)oder [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) aufgerufen werden.

</dd> <dt>

**Nachname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nachname des Kontakts für die RD-Lizenzierung. Diese Eigenschaft wird verwendet (und erforderlich), wenn die [**Methoden ActivateServerAutomatic,**](activateserverautomatic-win32-tslicenseserver.md) [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)oder [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) aufgerufen werden.

</dd> <dt>

**OrgUnit**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Organisationseinheit des Kontakts für die RD-Lizenzierung. Diese Eigenschaft wird verwendet, wenn [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) aufgerufen wird. (Diese Eigenschaft ist optional, wenn die **ActivateServerAutomatic-Methode verwendet** wird.)

</dd> <dt>

**PostalCode**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Postleitzahl des Kontakts für die RD-Lizenzierung. Diese Eigenschaft wird verwendet, wenn die [**ActivateServerAutomatic-Methode**](activateserverautomatic-win32-tslicenseserver.md) aufgerufen wird. (Diese Eigenschaft ist optional, wenn die **ActivateServerAutomatic-Methode verwendet** wird.)

</dd> <dt>

**ProductId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Produkt-ID des Remotedesktop Lizenzservers.

</dd> <dt>

**Serverrole**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt den Lizenzierungsbereich für den Remotedesktop Lizenzserver innerhalb der Organisation.

<dt>

0
</dt> <dd>

RD-Sitzungshost Server in derselben Arbeitsgruppe können den Lizenzserver finden.

</dd> <dt>

1
</dt> <dd>

RD-Sitzungshost Server in derselben Domäne können den Lizenzserver entdecken.

</dd> <dt>

2
</dt> <dd>

RD-Sitzungshost Server aus mehreren Domänen in derselben Gesamtstruktur können den Lizenzserver entdecken.

</dd> </dl>

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Status des Kontakts für die RD-Lizenzierung. Diese Eigenschaft wird verwendet, wenn die [**ActivateServerAutomatic-Methode**](activateserverautomatic-win32-tslicenseserver.md) aufgerufen wird. (Diese Eigenschaft ist optional, wenn die **ActivateServerAutomatic-Methode verwendet** wird.)

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Version des Remotedesktop Lizenzservers.

</dd> <dt>

**VersionNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Versionsnummer des Remotedesktop Lizenzservers.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Klasse ist eine [Singletonklasse](/windows/desktop/WmiSdk/standard-wmi-qualifiers) und kann nur eine Instanz haben. Alle in dieser Klasse enthaltenen Methoden sind statisch.

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Klasse verwenden zu können. Wenn der Aufrufer kein Mitglied der Gruppe Administratoren ist, sind die zurückgegebenen Eigenschaften leer.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> </dl>

 

