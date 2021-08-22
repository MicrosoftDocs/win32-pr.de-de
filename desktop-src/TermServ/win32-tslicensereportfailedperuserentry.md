---
title: Win32_TSLicenseReportFailedPerUserEntry-Klasse
description: Enthält Details zur fehlgeschlagenen Remotedesktopdienste Pro Benutzer-Clientzugriffslizenz (RDS \ 160; Pro Benutzer-CAL).
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserEntry-Remotedesktopdienste
- Win32_TSLicenseReportFailedPerUserEntry klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserEntry
- Win32_TSLicenseReportFailedPerUserEntry.User
- Win32_TSLicenseReportFailedPerUserEntry.TriedIssuanceOn
- Win32_TSLicenseReportFailedPerUserEntry.CALType
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersion
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02d56c1a7e2c715f068d808d45ac6ae3295b16bb7382179ec0e32c93beee096
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119420840"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a>Win32 \_ TSLicenseReportFailedPerUserEntry-Klasse

Enthält Details zur fehlgeschlagenen Remotedesktopdienste Clientzugriffslizenz pro Benutzer (RDS per User CAL).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserEntry
{
  string   User;
  DATETIME TriedIssuanceOn;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSLicenseReportFailedPerUserEntry-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSLicenseReportFailedPerUserEntry-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ der ausgestellten CAL an. Dies ist einer der folgenden Werte.

"Integrierte TS pro Geräte-CAL"

"TS pro Geräte-CAL"

"TS Internet Connector CAL"

"TS Pro Benutzer-CAL"

"TS oder RDS pro Geräte-CAL"

"TS oder RDS pro Benutzer-CAL"

"Abonnementlizenz für VDI Standard Suite pro Gerät"

"Abonnementlizenz Premium VDI-Suite pro Gerät"

"RDS pro Geräte-CAL"

"RDS pro Benutzer-CAL"

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version von Remotedesktopdienste, für die die RDS-CAL pro Benutzer ausgestellt wurde. Dies ist einer der folgenden Werte.

<dt>

"Windows Server 2012"
</dt> <dd>

Nur Server mit Windows Server 2012, Windows Server 2008 R2 oder Windows Server 2008 werden mit dieser Lizenz unterstützt.

</dd> <dt>

"Windows Server 7"
</dt> <dd>

Nur Server, auf denen Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

Nur Server mit Windows Server 2008 werden mit dieser Lizenz unterstützt.

</dd> </dl>

</dd> <dt>

**ProductVersionID**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Produktversions-ID für Remotedesktopdienste Lizenzschlüsselpaket.

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

**TriedIssuanceOn**
</dt> <dd> <dl> <dt>

Datentyp: **DATETIME**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum, an dem die Lizenzausstellung versucht wurde.

</dd> <dt>

**Benutzer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Name des Benutzers, für den die Lizenzausstellung versucht wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 

