---
title: Win32_TSIssuedLicense-Klasse
description: Beschreibt Instanzen von Remotedesktopdienste Client Zugriffs Lizenzen pro Gerät (RDS \ 160; Pro-Gerät-CALs), die von einem Remotedesktop Lizenzserver ausgestellt werden.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Win32_TSIssuedLicense-Klasse Remotedesktopdienste
- Win32_TSIssuedLicense Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense
- Win32_TSIssuedLicense.LicenseId
- Win32_TSIssuedLicense.KeyPackId
- Win32_TSIssuedLicense.sIssuedToUser
- Win32_TSIssuedLicense.sIssuedToComputer
- Win32_TSIssuedLicense.LicenseStatus
- Win32_TSIssuedLicense.IssueDate
- Win32_TSIssuedLicense.ExpirationDate
- Win32_TSIssuedLicense.sHardwareId
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d08a68ddcc15a912de4c674403928211a297e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337934"
---
# <a name="win32_tsissuedlicense-class"></a>Win32- \_ Klasse "tsissuedlicense"

Beschreibt Instanzen von Remotedesktopdienste pro Geräte-Client Zugriffs Lizenzen (RDS pro Gerät CALs), die von einem Remotedesktop Lizenzserver ausgestellt werden.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSIssuedLicense
{
  uint32   LicenseId;
  uint32   KeyPackId;
  string   sIssuedToUser;
  string   sIssuedToComputer;
  uint32   LicenseStatus;
  DATETIME IssueDate;
  DATETIME ExpirationDate;
  string   sHardwareId;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ tsissuedlicense** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ tsissuedlicense** " verfügt über diese Methoden.



| Methode                                         | BESCHREIBUNG                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Erteilte**](revoke-win32-tsissuedlicense.md) | Widerruft die RDS-CALs pro Gerät, die durch das Win32-Objekt " **\_ tsissuedlicense** " dargestellt werden.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ tsissuedlicense** " verfügt über diese Eigenschaften.

<dl> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt das Datum an, an dem die Lizenz abläuft.

</dd> <dt>

**IssueDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt das Datum an, an dem die Lizenz ausgestellt wurde.

</dd> <dt>

**Keypackid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifiziert das Remotedesktopdienste License Key Pack.

</dd> <dt>

**Licenseid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Eindeutiger Bezeichner für diese Lizenz.

</dd> <dt>

**LicenseStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Status der Lizenz.

<dt>

0
</dt> <dd>

Der Lizenzstatus ist unbekannt.

</dd> <dt>

1
</dt> <dd>

Die Lizenz ist eine temporäre Lizenz.

</dd> <dt>

2
</dt> <dd>

Die Lizenz ist aktiv.

</dd> <dt>

3
</dt> <dd>

Die Lizenz ist eine Upgradelizenz.

</dd> <dt>

4
</dt> <dd>

Die Lizenz wurde widerrufen.

</dd> <dt>

5
</dt> <dd>

Der Lizenzstatus ist "Ausstehend".

</dd> <dt>

6
</dt> <dd>

Die Lizenz ist eine gleichzeitige Lizenz.

</dd> </dl>

</dd> <dt>

**shardwareid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Hardware Bezeichner, für den die Lizenz ausgestellt wurde.

</dd> <dt>

**sissuedto Computer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, für den die Lizenz ausgestellt wurde.

</dd> <dt>

**sissuedtouser**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Benutzername, für den die Lizenz ausgestellt wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.

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

[**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32-Datei- \_ /licensereport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32-Wert für "- \_ Lizenzserver"**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32- \_ Lizenznehmer**](win32-tslicenseserver.md)
</dt> </dl>

 

