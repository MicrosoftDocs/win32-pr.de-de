---
title: Win32_TSLicenseReportSummaryEntry-Klasse
description: Enthält eine Zusammenfassung der installierten und ausgestellten Remotedesktopdienste Clientzugriffslizenzen pro Benutzer (RDS \ 160; Pro Benutzer-CALs).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportSummaryEntry-Klassen-Remotedesktopdienste
- Win32_TSLicenseReportSummaryEntry -Klasse Remotedesktopdienste beschrieben
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
ms.openlocfilehash: 58efc2c70019037219d8eca986fa8afd81e4dc2d06cd638ee24fc59947e3bf3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137798"
---
# <a name="win32_tslicensereportsummaryentry-class"></a>Win32 \_ TSLicenseReportSummaryEntry-Klasse

Enthält eine Zusammenfassung der installierten und ausgestellten Remotedesktopdienste Clientzugriffslizenzen pro Benutzer (RDS pro Benutzer-CALs).

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

Die **Win32 \_ TSLicenseReportSummaryEntry-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSLicenseReportSummaryEntry-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der installierten RDS-CALs pro Benutzer.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der ausgestellten RDS-CALs pro Benutzer.

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

Nur Server, auf denen Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.

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

**TSCALAvailability**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Verfügbarkeit der RDS-CALs pro Benutzer. Dies ist einer der folgenden Werte.

<dt>

"Verfügbar"
</dt> <dd>

Die RDS-CALs pro Benutzer sind verfügbar.

</dd> <dt>

"Begrenzt"
</dt> <dd>

Die Verfügbarkeit der RDS-CALs pro Benutzer ist eingeschränkt.

</dd> <dt>

"None"
</dt> <dd>

Die RDS-CALs pro Benutzer sind nicht verfügbar.

</dd> <dt>

"Nicht nachverfolgen"
</dt> <dd>

Die Verfügbarkeit der RDS-CALs pro Benutzer wird nicht nachverfolgt.

</dd> </dl>

</dd> <dt>

**TSCALType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der RDS-CALs pro Benutzer. Dies ist einer der folgenden Werte.

<dt>

"Pro Gerät"
</dt> <dd>

Die RDS-CALs pro Benutzer werden pro Gerät ausgegeben.

</dd> <dt>

"Pro Benutzer"
</dt> <dd>

Die RDS-CALs pro Benutzer werden pro Benutzer ausgegeben.

</dd> <dt>

"Unbekannt"
</dt> <dd>

Der Typ der RDS-CALs pro Benutzer ist unbekannt.

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



 

 





