---
title: Win32_TSLicenseReportFailedPerUserSummaryEntry-Klasse
description: Gibt Details zu den Domänen an, für die pro Benutzer eine Ausstellung fehlgeschlagen ist.
ms.assetid: f7265734-ac4d-439f-ae8b-3694e6f81f2a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserSummaryEntry-Klasse Remotedesktopdienste
- Win32_TSLicenseReportFailedPerUserSummaryEntry Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserSummaryEntry
- Win32_TSLicenseReportFailedPerUserSummaryEntry.DomainName
- Win32_TSLicenseReportFailedPerUserSummaryEntry.FailedIssuanceCount
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f086d275c064f5df18ee01a3a38639a40913f3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949477"
---
# <a name="win32_tslicensereportfailedperusersummaryentry-class"></a>Win32- \_ Klasse "slicensereportfailedperusersummaryentry"

Gibt Details zu den Domänen an, für die pro Benutzer eine Ausstellung fehlgeschlagen ist.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserSummaryEntry
{
  string DomainName;
  uint32 FailedIssuanceCount;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ zlicensereportfailedperusersummaryentry** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ slicensereportfailedperusersummaryentry** " verfügt über diese Eigenschaften.

<dl> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Gibt den Domänen Namen an, für den die Lizenz Ausstellung fehlgeschlagen ist.

</dd> <dt>

**Faileabschreck-Anzahl**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der fehlgeschlagenen issuances.

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

[**Fetchreportfailedperusersummaryentries**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md)
</dt> </dl>

 

