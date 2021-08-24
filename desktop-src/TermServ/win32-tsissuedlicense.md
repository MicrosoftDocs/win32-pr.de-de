---
title: Win32_TSIssuedLicense-Klasse
description: Beschreibt Instanzen von Remotedesktopdienste Clientzugriffslizenzen pro Gerät (RDS \ 160; CaLs pro Gerät), die von einem lizenzseitigen Remotedesktop ausgestellt werden.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Win32_TSIssuedLicense-Remotedesktopdienste
- Win32_TSIssuedLicense klasse Remotedesktopdienste , beschrieben
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
ms.openlocfilehash: b76127d41c6a571b6bc75bc74378b21f76f4b38c05f0a223d36e979dccf89a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656160"
---
# <a name="win32_tsissuedlicense-class"></a>Win32 \_ TSIssuedLicense-Klasse

Beschreibt Instanzen von Remotedesktopdienste Clientzugriffslizenzen pro Gerät (RDS per Device CALs), die von einem Remotedesktop ausgestellt werden.

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

Die **Win32 \_ TSIssuedLicense-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSIssuedLicense-Klasse** verfügt über diese Methoden.



| Methode                                         | Beschreibung                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Widerrufen**](revoke-win32-tsissuedlicense.md) | Widerruft die RDS-CALs pro Gerät, die durch das **Win32 \_ TSIssuedLicense-Objekt dargestellt** werden.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSIssuedLicense-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Datentyp: **DATETIME**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt das Datum an, an dem die Lizenz abläuft.

</dd> <dt>

**IssueDate**
</dt> <dd> <dl> <dt>

Datentyp: **DATETIME**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt das Datum an, an dem die Lizenz ausgestellt wurde.

</dd> <dt>

**KeyPackId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifiziert das Remotedesktopdienste Lizenzschlüsselpaket.

</dd> <dt>

**LicenseId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Eindeutiger Bezeichner für diese Lizenz.

</dd> <dt>

**LicenseStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Status der Lizenz.

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

Der Lizenzstatus steht aus.

</dd> <dt>

6
</dt> <dd>

Die Lizenz ist eine gleichzeitige Lizenz.

</dd> </dl>

</dd> <dt>

**sHardwareId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Hardwarebezeichner, für den die Lizenz ausgestellt wurde.

</dd> <dt>

**sIssuedToComputer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Computername, für den die Lizenz ausgestellt wurde.

</dd> <dt>

**sIssuedToUser**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Benutzername, für den die Lizenz ausgestellt wurde.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Klasse verwenden zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

