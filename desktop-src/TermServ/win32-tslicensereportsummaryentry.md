---
title: Win32_TSLicenseReportSummaryEntry-Klasse
description: Bietet eine Zusammenfassung der installierten und ausgestellten Remotedesktopdienste pro-Benutzer-Client Zugriffs Lizenzen (RDS \ 160; Pro Benutzer-CALs).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportSummaryEntry-Klasse Remotedesktopdienste
- Win32_TSLicenseReportSummaryEntry Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34482e9c6199ef6586024d43d586421a54071ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339122"
---
# <a name="win32_tslicensereportsummaryentry-class"></a>Win32-Klasse "-Klasse (Klasse)" \_

Bietet eine Zusammenfassung der installierten und ausgestellten Remotedesktopdienste pro Benutzer-Client Zugriffs Lizenzen (RDS pro Benutzer-CALs).

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ tylicensereportsummaryentry** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ stilicensereportsummaryentry** " verfügt über diese Eigenschaften.

<dl> <dt>

**Installedlicenses**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der installierten RDS-pro-Benutzer-CALs.

</dd> <dt>

**Issuedlicenses**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der ausgegebenen RDS-Client Zugriffs Lizenzen pro Benutzer.

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

**Tscalavailability**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Verfügbarkeit der RDS pro Benutzer-CALs. Dabei handelt es sich um einen der folgenden Werte.

<dt>

Frei
</dt> <dd>

Die RDS-Client Zugriffs Lizenzen pro Benutzer sind verfügbar.

</dd> <dt>

GmbH
</dt> <dd>

Die Verfügbarkeit der RDS pro Benutzer-CALs ist beschränkt.

</dd> <dt>

"None"
</dt> <dd>

Die RDS pro Benutzer-CALs sind nicht verfügbar.

</dd> <dt>

"Nicht nachverfolgt"
</dt> <dd>

Die Verfügbarkeit der RDS-Client Zugriffs Lizenzen pro Benutzer wird nicht nachverfolgt.

</dd> </dl>

</dd> <dt>

**Tscaltype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der RDS pro Benutzer-CALs. Dabei handelt es sich um einen der folgenden Werte.

<dt>

"Pro Gerät"
</dt> <dd>

Die RDS-Client Zugriffs Lizenzen pro Benutzer werden pro Gerät ausgestellt.

</dd> <dt>

"Pro Benutzer"
</dt> <dd>

Die RDS-Client Zugriffs Lizenzen pro Benutzer werden pro Benutzer ausgegeben.

</dd> <dt>

Unbekannter
</dt> <dd>

Der Typ der RDS pro Benutzer-CALs ist unbekannt.

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Tltaumiprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



 

 





