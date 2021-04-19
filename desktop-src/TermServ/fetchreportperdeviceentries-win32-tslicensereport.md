---
title: Fetchreportperdeviceentries-Methode der Win32_TSLicenseReport-Klasse
description: Abrufen von Informationen zu ausgestellten Remotedesktopdienste pro Geräte-Client Zugriffs Lizenzen (RDS \ 160; Pro Gerät CALs) aus dem Bericht.
ms.assetid: 3f632a65-d6e0-4efd-9498-d04a05f9ddec
ms.tgt_platform: multiple
keywords:
- Die fetchreportperdeviceentries-Methode Remotedesktopdienste
- Fetchreportperdeviceentries-Methode Remotedesktopdienste, Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste, fetchreportperdeviceentries-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportPerDeviceEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce77fce941dd0a24fb6ee17e0aeb67b4e78bdae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344098"
---
# <a name="fetchreportperdeviceentries-method-of-the-win32_tslicensereport-class"></a>Fetchreportperdeviceentries-Methode der Win32- \_ Klasse "zlicensereport"

Ruft Informationen zu ausgestellten Remotedesktopdienste pro Geräte-Client Zugriffs Lizenzen (RDS pro Gerät CALs) aus dem Bericht ab.

## <a name="syntax"></a>Syntax


```mof
uint32 FetchReportPerDeviceEntries(
  [in]      uint32                              StartIndex,
  [in, out] uint32                              Count,
  [out]     Win32_TSLicenseReportPerDeviceEntry ReportPerDeviceEntries[]
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

Die Anzahl der Berichts Einträge, die aus dem Berichts Objekt abgerufen werden sollen. Der Wert 0 (null) gibt an, dass alle Berichts Einträge, die bei *startIndex* beginnen, abgerufen werden sollen. Enthält bei der Rückgabe die Anzahl der Einträge im *reportperdeviceentries* -Array.

</dd> <dt>

*Reportperdeviceentries* \[ vorgenommen\]
</dt> <dd>

Ein Array von Win32-Klassen vom Typ " [**\_ zlicensereportperdeviceentry**](win32-tslicensereportperdeviceentry.md) ", die die abgerufenen Lizenzeinträge darstellen. Der *count* -Parameter enthält die Anzahl der Elemente in diesem Array.

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

 

 





