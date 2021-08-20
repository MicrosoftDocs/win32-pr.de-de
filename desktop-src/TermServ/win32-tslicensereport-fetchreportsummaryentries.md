---
title: FetchReportSummaryEntries-Methode der Win32_TSLicenseReport-Klasse
description: Ruft Zusammenfassungen der Clientzugriffslizenzen für Remotedesktopdienste pro Benutzer ab (RDS \ 160; Pro Benutzer-CALs) aus dem Bericht.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- FetchReportSummaryEntries-Methode Remotedesktopdienste
- FetchReportSummaryEntries-Methode Remotedesktopdienste , Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste , FetchReportSummaryEntries-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094d7fe1f7aa3d5acabce7d7d248c16601b5005d09f2583cc23c7390c3642361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348575"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a>FetchReportSummaryEntries-Methode der Win32 \_ TSLicenseReport-Klasse

Ruft Zusammenfassungen Remotedesktopdienste Clientzugriffslizenzen pro Benutzer (RDS pro Benutzer-CALs) aus dem Bericht ab.

## <a name="syntax"></a>Syntax


```mof
uint32 FetchReportSummaryEntries(
  [in]      uint32                            StartIndex,
  [in, out] uint32                            Count,
  [out]     Win32_TSLicenseReportSummaryEntry ReportSummaryEntries[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartIndex* \[ In\]
</dt> <dd>

Index des ersten zu empfangenden Berichtseintrags. Der erste Berichtseintrag weist den Index 0 (null) auf.

</dd> <dt>

*Anzahl* \[ in, out\]
</dt> <dd>

Anzahl der Berichtseinträge, die aus dem Berichtsobjekt abgerufen werden sollen. Der Wert 0 (null) gibt an, dass alle Berichtseinträge, die bei *StartIndex* beginnen, abgerufen werden sollen. Enthält bei der Rückgabe die Anzahl der Einträge im *ReportSummaryEntries-Array.*

</dd> <dt>

*ReportSummaryEntries* \[ out\]
</dt> <dd>

Gibt ein Array von [**Win32 \_ TSLicenseReportSummaryEntry-Klassen**](win32-tslicensereportsummaryentry.md) zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Der Wert **LSERVER \_ I NO MORE \_ \_ \_ DATA** (0x4001) gibt an, dass keine Berichtseinträge mehr vorhanden sind.

## <a name="remarks"></a>Hinweise

Dies ist keine statische Methode. Diese Methode muss von einem Benutzerlizenznutzungsbericht-Objekt aufgerufen werden.

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportSummaryEntry**](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

