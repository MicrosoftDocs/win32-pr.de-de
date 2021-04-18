---
title: Win32_TSLicenseReportEntry-Klasse
description: Enthält Details zur Client Zugriffslizenz für die ausgestellten Remotedesktopdienste pro Benutzer (RDS \ 160; Pro Benutzer-CAL).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportEntry-Klasse Remotedesktopdienste
- Win32_TSLicenseReportEntry Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 44fa97a91561a9d4cf3fd571c773288796754858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391559"
---
# <a name="win32_tslicensereportentry-class"></a>Win32-Klasse "-Klasse (Klasse)" \_

Stellt Details der pro Benutzer-Client Zugriffslizenz ausgestellten Remotedesktopdienste (RDS pro Benutzer-CAL) bereit.

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

Die Win32-Klasse " **\_ zlicensereportentry** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ stilicensereportentry** " verfügt über diese Eigenschaften.

<dl> <dt>

**Caltype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ der ausgegebene Cal an. Dabei handelt es sich um einen der folgenden Werte.

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft wird nicht unterstützt.

"Integrierte TS pro Gerät CAL"

"TS-CAL pro Gerät"

"TS Internet Connector CAL"

"TS pro Benutzer-CAL"

"TS-oder RDS-CAL pro Gerät"

"TS-oder RDS-pro-Benutzer-CAL"

"VDI Standard Suite pro Device Abonnement License"

"VDI Premium Suite pro Device Abonnement License"

"RDS pro Gerät CAL"

"RDS pro Benutzer-CAL"

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ablaufdatum der Lizenz, die für den Benutzer ausgestellt wurde.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version von Remotedesktopdienste, für die die RDS-Client Zugriffslizenz pro Benutzer ausgestellt wurde.

<dt>

"Windows Server 2012"
</dt> <dd>

Nur Server, auf denen Windows Server 2012, Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.

</dd> <dt>

"Windows Server 7"
</dt> <dd>

Nur Server, auf denen Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

Nur Server, auf denen Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.

</dd> </dl>

</dd> <dt>

**Productversionid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Produkt Versions Kennung für das Remotedesktopdienste License Key Pack.

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

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Name des Benutzers, für den die Lizenz ausgestellt wurde.

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

[**Fetchreportentries**](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[**Win32-" \_ tsissuedlicense"**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32-Datei- \_ /licensereport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32- \_ Lizenznehmer**](win32-tslicenseserver.md)
</dt> </dl>

 

