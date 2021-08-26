---
title: Win32_TSLicenseReportPerDeviceEntry-Klasse
description: Enthält Details zur fehlgeschlagenen Remotedesktopdienste Clientzugriffslizenz pro Gerät (RDS \ 160; Pro Geräte-CAL).
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportPerDeviceEntry-Remotedesktopdienste
- Win32_TSLicenseReportPerDeviceEntry klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbcdad271a346820b318c94bed7ce6b9b9527d3fdd7df9cc3f1dc9d9a97aae3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008420"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a>Win32 \_ TSLicenseReportPerDeviceEntry-Klasse

Enthält Details zur fehlgeschlagenen Remotedesktopdienste Clientzugriffslizenz pro Gerät (RDS pro Geräte-CAL).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSLicenseReportPerDeviceEntry-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSLicenseReportPerDeviceEntry-Klasse** verfügt über diese Eigenschaften.

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

"TS oder RDS per User CAL"

"Abonnementlizenz für VDI Standard Suite pro Gerät"

"Abonnementlizenz Premium VDI-Suite pro Gerät"

"RDS pro Geräte-CAL"

"RDS pro Benutzer-CAL"

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Datentyp: **DATETIME**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Ablaufdatum der Lizenz.

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

Nur Server mit Windows Server 2008 R2 oder Windows Server 2008 werden mit dieser Lizenz unterstützt.

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

Produktversionsbezeichner für Remotedesktopdienste Lizenzschlüsselpaket.

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

**sHardwareId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Die Hardware-ID des Computers.

</dd> <dt>

**sIssuedToComputer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, für den die Lizenzausstellung versucht wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 

