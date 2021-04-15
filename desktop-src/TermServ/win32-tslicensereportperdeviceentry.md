---
title: Win32_TSLicenseReportPerDeviceEntry-Klasse
description: Enthält Details zur Client Zugriffslizenz für das fehlgeschlagene Remotedesktopdienste pro Gerät (RDS \ 160; Pro-Gerät-CAL).
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportPerDeviceEntry-Klasse Remotedesktopdienste
- Win32_TSLicenseReportPerDeviceEntry Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: a120d477ff03675f160d94f1506f59cdf1462fa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475462"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a>Win32- \_ Klasse "zlicensereportperdeviceentry"

Enthält Details zu den fehlerhaften Remotedesktopdienste pro Geräte-Client Zugriffslizenz (RDS pro Gerät CAL).

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

Die Win32-Klasse " **\_ zlicensereportperdeviceentry** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ zlicensereportperdeviceentry** " verfügt über diese Eigenschaften.

<dl> <dt>

**Caltype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ der ausgegebene Cal an. Dabei handelt es sich um einen der folgenden Werte.

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

Das Ablaufdatum der Lizenz.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version von Remotedesktopdienste, für die die RDS-Client Zugriffslizenz pro Benutzer ausgestellt wurde. Dabei handelt es sich um einen der folgenden Werte.

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

**shardwareid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Die Hardware-ID des Computers.

</dd> <dt>

**sissuedto Computer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, für den die Lizenz Ausstellung versucht wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Tltaumiprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Fetchreportperdeviceentries**](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 

