---
title: Win32_TSLicenseReportEntry-Klasse
description: Enthält Details zur ausgestellten Remotedesktopdienste Pro Benutzer-Clientzugriffslizenz (RDS \ 160; Pro Benutzer-CAL).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportEntry-Klassen-Remotedesktopdienste
- Win32_TSLicenseReportEntry-Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e08041ac0878f3466712001a0a5e2cc90eb74ea1e360da9785b5d84805574389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126520"
---
# <a name="win32_tslicensereportentry-class"></a>Win32 \_ TSLicenseReportEntry-Klasse

Enthält Details zur ausgestellten Remotedesktopdienste Clientzugriffslizenz pro Benutzer (RDS per User CAL).

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSLicenseReportEntry-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSLicenseReportEntry-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ der ausgegebenen CAL an. Dies ist einer der folgenden Werte.

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft wird nicht unterstützt.

"Integrierte TS pro Geräte-CAL"

"TS per Device CAL"

"TS Internet Connector CAL"

"TS Per User CAL"

"TS oder RDS pro Geräte-CAL"

"TS oder RDS pro Benutzer-CAL"

"Abonnementlizenz für VDI Standard Suite pro Gerät"

"Abonnementlizenz für VDI Premium Suite pro Gerät"

"RDS pro Geräte-CAL"

"RDS pro Benutzer-CAL"

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Datentyp: **DATETIME**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ablaufdatum der Lizenz, die dem Benutzer ausgestellt wurde.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Version von Remotedesktopdienste, für die die RDS-CAL pro Benutzer ausgegeben wurde.

<dt>

"Windows Server 2012"
</dt> <dd>

Mit dieser Lizenz werden nur Server unterstützt, auf denen Windows Server 2012, Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird.

</dd> <dt>

"Windows Server 7"
</dt> <dd>

Mit dieser Lizenz werden nur Server unterstützt, auf denen Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird.

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

Mit dieser Lizenz werden nur Server unterstützt, auf denen Windows Server 2008 ausgeführt wird.

</dd> </dl>

</dd> <dt>

**ProductVersionID**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Produktversionsbezeichner für das Remotedesktopdienste Lizenzschlüsselpaket.

<dt>

4
</dt> <dd>

Windows Server 2012

</dd> <dt>

3
</dt> <dd>

Windows Server 2008 R2

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> <dt>

1
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

0
</dt> <dd>

Wird nicht unterstützt.

</dd> </dl>

</dd> <dt>

**Benutzer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name des Benutzers, für den die Lizenz ausgestellt wurde.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Klasse verwenden zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

