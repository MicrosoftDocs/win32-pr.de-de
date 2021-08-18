---
title: FetchReportEntries-Methode der Win32_TSLicenseReport-Klasse
description: Ruft Details zu clientzugriffslizenzen für Remotedesktopdienste pro Benutzer ab (RDS \ 160; Pro Benutzer-CALs) aus dem Bericht. Jeder Eintrag stellt ein RDS \ 160 dar. Pro Benutzer-CAL, die derzeit verwendet wird.
ms.assetid: 151ff95c-4ad3-4d19-936d-1cb08b4d5056
ms.tgt_platform: multiple
keywords:
- FetchReportEntries-Methode Remotedesktopdienste
- FetchReportEntries-Methode Remotedesktopdienste , Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport Klasse Remotedesktopdienste , FetchReportEntries-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e35c2af0578b0b130b5ef92bae5d374cc4ba2ba82c172689d00782e68b65c143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871730"
---
# <a name="fetchreportentries-method-of-the-win32_tslicensereport-class"></a>FetchReportEntries-Methode der Win32 \_ TSLicenseReport-Klasse

Ruft Details zu Remotedesktopdienste Clientzugriffslizenzen pro Benutzer (RDS pro Benutzer-CALs) aus dem Bericht ab. Jeder Eintrag stellt eine RDS-CAL pro Benutzer dar, die derzeit verwendet wird.

## <a name="syntax"></a>Syntax


```mof
uint32 FetchReportEntries(
  [in]      uint32                     StartIndex,
  [in, out] uint32                     Count,
  [out]     Win32_TSLicenseReportEntry ReportEntries[]
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

Anzahl der Berichtseinträge, die aus dem Berichtsobjekt abgerufen werden sollen. Der Wert 0 (null) gibt an, dass alle Berichtseinträge, die bei *StartIndex* beginnen, abgerufen werden sollen. Enthält bei der Rückgabe die Anzahl der Einträge im *ReportEntries-Array.*

</dd> <dt>

*Berichtseinträge* \[ out\]
</dt> <dd>

Gibt ein Array von [**Win32 \_ TSLicenseReportEntry-Klassen**](win32-tslicensereportentry.md) zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Der Wert **LSERVER \_ I NO MORE \_ \_ \_ DATA** (0x4001) gibt an, dass keine Berichtseinträge mehr vorhanden sind.

## <a name="remarks"></a>Hinweise

Dies ist keine statische Methode. Diese Methode muss von einem Benutzerlizenznutzungsbericht-Objekt aufgerufen werden.

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> </dl>

 

