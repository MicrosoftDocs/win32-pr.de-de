---
title: Fetchreportfailedperusersummaryentries-Methode der Win32_TSLicenseReport-Klasse
description: Hiermit werden zusammenfassende Informationen zu fehlerhaften Remotedesktopdienste pro Benutzer-Client Zugriffs Lizenzen abgerufen (RDS \ 160; Pro Benutzer-CALs) aus dem Bericht.
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- Die fetchreportfailedperusersummaryentries-Methode Remotedesktopdienste
- Fetchreportfailedperusersummaryentries-Methode Remotedesktopdienste, Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste, fetchreportfailedperusersummaryentries-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219c2c854e04dabf8b5bfe0b5b70a07bbc3c57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342475"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a>Fetchreportfailedperusersummaryentries-Methode der Win32- \_ Klasse "zlicensereport"

Hiermit werden zusammenfassende Informationen zu fehlerhaften Remotedesktopdienste pro Benutzer-Client Zugriffs Lizenzen (RDS pro Benutzer-CALs) aus dem Bericht abgerufen.

## <a name="syntax"></a>Syntax


```mof
uint32 FetchReportFailedPerUserSummaryEntries(
  [in]      uint32                                         StartIndex,
  [in, out] uint32                                         Count,
  [out]     Win32_TSLicenseReportFailedPerUserSummaryEntry ReportFailedPerUserSummaryEntries[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartIndex* \[ in\]
</dt> <dd>

Der Index des ersten Berichts Eintrags, der abgerufen werden soll. Der erste Berichts Eintrag weist einen Index von 0 (null) auf.

</dd> <dt>

*Anzahl* \[ in, out\]
</dt> <dd>

Die Anzahl der Berichts Einträge, die aus dem Berichts Objekt abgerufen werden sollen. Der Wert 0 (null) gibt an, dass alle Berichts Einträge, die bei *startIndex* beginnen, abgerufen werden sollen. Enthält bei der Rückgabe die Anzahl der Einträge im *reportfailedperusersummaryentries* -Array.

</dd> <dt>

*Reportfailedperusersummaryentries* \[ vorgenommen\]
</dt> <dd>

Ein Array von Win32-Klassen vom Typ " [**\_ zlicensereportfailedperusersummaryentry**](win32-tslicensereportfailedperusersummaryentry.md) ", die die abgerufenen Lizenzeinträge darstellen. Der *count* -Parameter enthält die Anzahl der Elemente in diesem Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

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

[**Win32-Datei- \_ /licensereport**](win32-tslicensereport.md)
</dt> </dl>

 

 





