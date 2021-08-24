---
title: FetchReportFailedPerUserSummaryEntries-Methode der Win32_TSLicenseReport-Klasse
description: Ruft zusammenfassende Informationen zu fehlgeschlagenen Remotedesktopdienste Clientzugriffslizenzen pro Benutzer ab (RDS \ 160; Pro Benutzer-CALs) aus dem Bericht.
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- FetchReportFailedPerUserSummaryEntries-Methode Remotedesktopdienste
- FetchReportFailedPerUserSummaryEntries-Methode Remotedesktopdienste , Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste , FetchReportFailedPerUserSummaryEntries-Methode
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
ms.openlocfilehash: cc42cb36ad0d203389dd115eb6bf02b1135982f1c490a0f669e19d2f64e937ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737550"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a>FetchReportFailedPerUserSummaryEntries-Methode der Win32 \_ TSLicenseReport-Klasse

Ruft zusammenfassende Informationen zu fehlgeschlagenen Remotedesktopdienste Clientzugriffslizenzen pro Benutzer (RDS pro Benutzer-CALs) aus dem Bericht ab.

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

*StartIndex* \[ In\]
</dt> <dd>

Der Index des ersten abzurufenden Berichtseintrags. Der erste Berichtseintrag weist den Index 0 (null) auf.

</dd> <dt>

*Anzahl* \[ in, out\]
</dt> <dd>

Die Anzahl der Berichtseinträge, die aus dem Berichtsobjekt abgerufen werden sollen. Der Wert 0 (null) gibt an, dass alle Berichtseinträge, die bei *StartIndex* beginnen, abgerufen werden sollen. Enthält bei der Rückgabe die Anzahl der Einträge im *ReportFailedPerUserSummaryEntries-Array.*

</dd> <dt>

*ReportFailedPerUserSummaryEntries* \[ out\]
</dt> <dd>

Ein Array von [**Win32 \_ TSLicenseReportFailedPerUserSummaryEntry-Klassen,**](win32-tslicensereportfailedperusersummaryentry.md) die die abgerufenen Lizenzeinträge darstellen. Der *Count-Parameter* enthält die Anzahl der Elemente in diesem Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> </dl>

 

 





