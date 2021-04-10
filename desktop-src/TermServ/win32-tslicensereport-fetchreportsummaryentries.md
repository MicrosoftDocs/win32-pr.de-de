---
title: Fetchreportsummaryentries-Methode der Win32_TSLicenseReport-Klasse
description: Hiermit werden Zusammenfassungen von Remotedesktopdienste Client Zugriffs Lizenzen pro Benutzer abgerufen (RDS \ 160; Pro Benutzer-CALs) aus dem Bericht.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- Die fetchreportsummaryentries-Methode Remotedesktopdienste
- Fetchreportsummaryentries-Methode Remotedesktopdienste, Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste, fetchreportsummaryentries-Methode
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
ms.openlocfilehash: e47100c71e195cacb6a1004975955eae778765a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103010"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a>Fetchreportsummaryentries-Methode der Win32- \_ Klasse "zlicensereport"

Ruft Zusammenfassungen von Remotedesktopdienste Client Zugriffs Lizenzen pro Benutzer (RDS pro Benutzer-CALs) aus dem Bericht ab.

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

*StartIndex* \[ in\]
</dt> <dd>

Der Index des ersten Berichts Eintrags, der empfangen werden soll. Der erste Berichts Eintrag weist einen Index von 0 (null) auf.

</dd> <dt>

*Anzahl* \[ in, out\]
</dt> <dd>

Anzahl der Berichts Einträge, die aus dem Berichts Objekt abgerufen werden sollen. Der Wert 0 (null) gibt an, dass alle Berichts Einträge, die bei *startIndex* beginnen, abgerufen werden sollen. Enthält bei der Rückgabe die Anzahl der Einträge im *reportsummaryentries* -Array.

</dd> <dt>

*Reportsummaryentries* \[ vorgenommen\]
</dt> <dd>

Gibt ein Array von Win32-Klassen vom Typ " [**\_ tlicensereportsummaryentry**](win32-tslicensereportsummaryentry.md) " zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Der Wert **lserver \_ I \_ No \_ \_ Data** (0x4001) gibt an, dass keine weiteren Berichts Einträge vorhanden sind.

## <a name="remarks"></a>Bemerkungen

Dabei handelt es sich nicht um eine statische Methode. Diese Methode muss von einem Bericht Objekt pro Benutzer-Lizenz Verwendung aufgerufen werden.

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Tltaumiprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Datei- \_ /licensereport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32-Datei Eintrag ("-Name)" \_**](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

