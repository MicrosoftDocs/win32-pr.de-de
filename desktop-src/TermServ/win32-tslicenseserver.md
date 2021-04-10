---
title: Win32_TSLicenseServer-Klasse
description: Stellt Methoden und Eigenschaften zum Anzeigen und konfigurieren Remotedesktop Lizenzierung (RD-Lizenzierung) auf einem Remotedesktop Lizenzserver bereit.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseServer-Klasse Remotedesktopdienste
- Win32_TSLicenseServer Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 31951b943723e620414b2f714327db8c786f9ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956746"
---
# <a name="win32_tslicenseserver-class"></a>Win32-Klasse "-Klasse (Klasse)" \_

Stellt Methoden und Eigenschaften zum Anzeigen und konfigurieren Remotedesktop Lizenzierung (RD-Lizenzierung) auf einem Remotedesktop Lizenzserver bereit.

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

Die Win32-Klasse " **\_ zlicenseserver** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ zlicenseserver** " verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Activateserver**](activateserver-win32-tslicenseserver.md)                           | Aktiviert den Remotedesktop Lizenzserver mit einer Remotedesktop Lizenzserver-ID, die über das Telefon oder das Internet abgerufen wird.<br/>                                                                                           |
| [**Activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md)         | Aktiviert den Remotedesktop Lizenzserver automatisch über das Internet. Die Eigenschaften " **FirstName**", " **LastName**", " **Company**" und " **CountryRegion** " dürfen nicht leer sein, wenn diese Methode aufgerufen wird, oder die Methode schlägt fehl.<br/> |
| [**Addlstozlsgroup**](addlstotslsgroup-win32-tslicenseserver.md)                       | Fügt den Remotedesktop-Lizenzserver der Gruppe Remotedesktop Lizenzserver auf einem Domänen Controller in derselben Domäne wie der Lizenzserver hinzu.<br/>                                                                                |
| [**ChangeRole**](changerole-win32-tslicenseserver.md)                                   | Ändert den Ermittlungs Bereich des Remotedesktop Lizenzservers.<br/>                                                                                                                                                                  |
| [**"Kreatetscgroup"**](createtscgroup-win32-tslicenseserver.md)                           | Diese Methode wird nicht unterstützt.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Erstellt die lokale Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenz Server.<br/>                                               |
| [**Geräteserver**](deactivateserver-win32-tslicenseserver.md)                       | Deaktiviert den Remotedesktop Lizenzserver mithilfe eines Bestätigungs Codes, der über das Telefon empfangen wird.<br/>                                                                                                                        |
| [**"Deaktiviert"**](deactivateserverautomatic-win32-tslicenseserver.md)     | Deaktiviert den Remotedesktop Lizenzserver über das Internet. Die Eigenschaften " **FirstName** " und " **LastName** " dürfen nicht leer sein, wenn diese Methode aufgerufen wird, oder die Methode schlägt fehl.<br/>                                              |
| [**Getactivationstatus**](getactivationstatus-win32-tslicenseserver.md)                 | Ruft den aktuellen Aktivierungs Status ab.<br/>                                                                                                                                                                                           |
| [**Getlicenseserverid**](getlicenseserverid-win32-tslicenseserver.md)                   | Ruft eine Remotedesktop Lizenzserver-ID ab, wenn der Server zurzeit aktiviert ist.<br/>                                                                                                                                                 |
| [**Islsinzlsgroup**](islsintslsgroup-win32-tslicenseserver.md)                         | Ruft ab, ob der Remotedesktop Lizenzserver Mitglied der Gruppe Remotedesktop Lizenzserver auf einem Domänen Controller in einer bestimmten Domäne ist.<br/>                                                                              |
| [**Islsondc**](islsondc-win32-tslicenseserver.md)                                       | Ruft ab, ob RD-Lizenzierung auf einem Domänen Controller installiert ist.<br/>                                                                                                                                                                |
| [**Isllexventupgradegpabled**](islspreventupgradegpenabled-win32-tslicenseserver.md) | Ruft ab, ob die Gruppenrichtlinien Einstellung "Lizenz Upgrade verhindern" auf dem Remotedesktop-Lizenzserver aktiviert ist.<br/>                                                                                                              |
| [**Islspublished**](islspublished-win32-tslicenseserver.md)                             | Ruft ab, ob der Remotedesktop Lizenzserver in Active Directory Domain Services (AD DS) veröffentlicht wird.<br/>                                                                                                                      |
| [**Islsregistereddescp**](win32-tslicenseserver-islsregisteredtoscp.md)                 | Ruft ab, ob der Remotedesktop Lizenzserver als Dienst Verbindungspunkt in Active Directory Domain Services registriert ist.<br/>                                                                                               |
| [**Islssecgrpgpabled**](islssecgrpgpenabled-win32-tslicenseserver.md)                 | Ruft ab, ob die Gruppenrichtlinien Einstellung "Lizenzserver-Sicherheitsgruppe" auf dem Remotedesktop-Lizenzserver aktiviert ist.<br/>                                                                                                        |
| [**Issecureaccessallowed**](issecureaccessallowed-win32-tslicenseserver.md)             | Ruft ab, ob ein RD-Sitzungshost Server Remotedesktopdienste Client Zugriffs Lizenzen (RDS-CALs) vom Remotedesktop Lizenzserver anfordern darf.<br/>                                                                |
| [**Istscgrouppresent**](istscgrouppresent-win32-tslicenseserver.md)                     | Diese Methode wird nicht unterstützt.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Ruft ab, ob die lokale Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenz Server vorhanden ist.<br/>                              |
| [**Istsintscgroup**](istsintscgroup-win32-tslicenseserver.md)                           | Ruft ab, ob ein RD-Sitzungshost Server Mitglied der lokalen Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenzserver ist.<br/>                                                                                         |
| [**Publishls**](publishls-win32-tslicenseserver.md)                                     | Veröffentlicht den Remotedesktop Lizenzserver in AD DS.<br/>                                                                                                                                                                              |
| [**Reactivateserver**](reactivateserver-win32-tslicenseserver.md)                       | Reaktiviert den Remotedesktop Lizenzserver, indem eine neue Remotedesktop Lizenzserver-ID verwendet wird, die über das Telefon oder das Internet abgerufen wird.<br/>                                                                                     |
| [**Reactivateserverautomatic**](reactivateserverautomatic-win32-tslicenseserver.md)     | Aktiviert den Remotedesktop Lizenzserver über das Internet erneut. Die Eigenschaften " **FirstName** " und " **LastName** " dürfen nicht leer sein, wenn diese Methode aufgerufen wird, oder die Methode schlägt fehl.<br/>                                              |
| [**Registerlstoscp**](win32-tslicenseserver-registerlstoscp.md)                         | Registriert den Remotedesktop-Lizenzserver als Dienst Verbindungspunkt in Active Directory Domain Services.<br/>                                                                                                                     |
| [**Removelsfromzlsgroup**](removelsfromtslsgroup-win32-tslicenseserver.md)             | Hierdurch wird der Remotedesktop Lizenzserver aus der Gruppe Remotedesktop Lizenzserver auf einem Domänen Controller in derselben Domäne wie der Lizenzserver entfernt.<br/>                                                                           |
| [**Removetscgroup**](removetscgroup-win32-tslicenseserver.md)                           | Diese Methode wird nicht unterstützt.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Entfernt die lokale Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenz Server.<br/>                                             |
| [**Nicht publishls**](unpublishls-win32-tslicenseserver.md)                                 | Veröffentlichung eines Remotedesktop Lizenzservers aus AD DS.<br/>                                                                                                                                                                            |
| [**Unregisterlsfromscp**](win32-tslicenseserver-unregisterlsfromscp.md)                 | Entfernt den Remotedesktop-Lizenzserver als Dienst Verbindungspunkt in Active Directory Domain Services.<br/>                                                                                                                       |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse "Klasse- **\_ licenseserver** " verfügt über diese Eigenschaften.

<dl> <dt>

**Adresse**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Adresse des Kontakts für RD-Lizenzierung. Diese Eigenschaft wird verwendet, wenn die [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) -Methode aufgerufen wird. (Diese Eigenschaft ist optional, wenn die **activateserverautomatic** -Methode verwendet wird.)

</dd> <dt>

**City (Ort)**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Stadt des Kontakts für RD-Lizenzierung. Diese Eigenschaft wird verwendet, wenn die [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) -Methode aufgerufen wird. (Diese Eigenschaft ist optional, wenn die **activateserverautomatic** -Methode verwendet wird.)

</dd> <dt>

**Company**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Unternehmen des Kontakts für RD-Lizenzierung. Diese Eigenschaft wird verwendet (und erforderlich), wenn die [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) -Methode aufgerufen wird.

</dd> <dt>

**CountryRegion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Land/Region des Kontakts für RD-Lizenzierung. Diese Eigenschaft wird verwendet (und erforderlich), wenn die [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) -Methode aufgerufen wird.

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad der RDS-Lizenzierungs Datenbank.

</dd> <dt>

**E-Mail**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

E-Mail-Adresse des Kontakts für RD-Lizenzierung. Diese Eigenschaft wird verwendet, wenn die Methoden [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md), [**reactivateserverautomatic**](reactivateserverautomatic-win32-tslicenseserver.md)oder [**deactivateserverautomatic**](deactivateserverautomatic-win32-tslicenseserver.md) aufgerufen werden. (Diese Eigenschaft ist für diese Methodenaufrufe optional.)

</dd> <dt>

**Vorname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Vorname des Kontakts für RD-Lizenzierung. Diese Eigenschaft wird (und erforderlich) verwendet, wenn die Methoden [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md), [**reactivateserverautomatic**](reactivateserverautomatic-win32-tslicenseserver.md)oder [**deactivateserverautomatic**](deactivateserverautomatic-win32-tslicenseserver.md) aufgerufen werden.

</dd> <dt>

**Nachname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nachname des Kontakts für RD-Lizenzierung. Diese Eigenschaft wird (und erforderlich) verwendet, wenn die Methoden [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md), [**reactivateserverautomatic**](reactivateserverautomatic-win32-tslicenseserver.md)oder [**deactivateserverautomatic**](deactivateserverautomatic-win32-tslicenseserver.md) aufgerufen werden.

</dd> <dt>

**Organisationseinheit**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Organisationseinheit des Kontakts für RD-Lizenzierung. Diese Eigenschaft wird verwendet, wenn [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) aufgerufen wird. (Diese Eigenschaft ist optional, wenn die **activateserverautomatic** -Methode verwendet wird.)

</dd> <dt>

**PostalCode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Postleitzahl des Kontakts für RD-Lizenzierung. Diese Eigenschaft wird verwendet, wenn die [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) -Methode aufgerufen wird. (Diese Eigenschaft ist optional, wenn die **activateserverautomatic** -Methode verwendet wird.)

</dd> <dt>

**ProductId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Produkt-ID des Remotedesktop Lizenzservers.

</dd> <dt>

**ServerRole**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt den Lizenzierungs Bereich für den Remotedesktop Lizenzserver innerhalb der Organisation.

<dt>

0
</dt> <dd>

RD-Sitzungshost Server in derselben Arbeitsgruppe können den Lizenzserver ermitteln.

</dd> <dt>

1
</dt> <dd>

RD-Sitzungshost Server in derselben Domäne können den Lizenzserver ermitteln.

</dd> <dt>

2
</dt> <dd>

RD-Sitzungshost Server aus mehreren Domänen in derselben Gesamtstruktur können den Lizenzserver ermitteln.

</dd> </dl>

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Status des Kontakts für RD-Lizenzierung. Diese Eigenschaft wird verwendet, wenn die [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) -Methode aufgerufen wird. (Diese Eigenschaft ist optional, wenn die **activateserverautomatic** -Methode verwendet wird.)

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version des Remotedesktop Lizenzservers.

</dd> <dt>

**VersionNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Versionsnummer des Remotedesktop Lizenzservers.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bei dieser Klasse handelt es sich um eine [Singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) -Klasse, die nur eine Instanz aufweisen kann. Alle in dieser Klasse enthaltenen Methoden sind statisch.

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können. Wenn der Aufrufer kein Mitglied der Gruppe "Administratoren" ist, sind die zurückgegebenen Eigenschaften leer.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Tltaumiprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-" \_ tsissuedlicense"**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32-Datei- \_ /licensereport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32-Wert für "- \_ Lizenzserver"**](win32-tslicensereportentry.md)
</dt> </dl>

 

