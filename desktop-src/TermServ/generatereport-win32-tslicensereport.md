---
title: GenerateReport-Methode der Win32_TSLicenseReport-Klasse (GPMgmt. h)
description: GenerateReport ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- GenerateReport-Methode Remotedesktopdienste
- GenerateReport-Methode Remotedesktopdienste, Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste, GenerateReport-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5231c87d379decac8d4f6491042bff735c1ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392079"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a>GenerateReport-Methode der Win32- \_ Klasse "zlicensereport"

\[**GenerateReport** ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar. Verwenden Sie stattdessen [**generatereportex**](generatereportex-win32-tslicensereport.md).\]

Diese Methode wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008:** Generiert einen aktuellen Bericht pro Benutzer-Lizenz Verwendung auf dem Remotedesktop-Lizenzserver.

## <a name="syntax"></a>Syntax


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ScopeType* \[ in\]
</dt> <dd>

Bereich des Lizenz Verwendungs Berichts. Die folgenden Werte sind möglich:

<dt>

1
</dt> <dd>

Der Bericht wird für die gesamte Domäne generiert.

</dd> <dt>

2
</dt> <dd>

Der Bericht wird für die Organisationseinheit (OU) generiert, die im Parameter " *scopevalue* " angegeben ist.

</dd> <dt>

3
</dt> <dd>

Der Bericht wird für alle vertrauenswürdigen Domänen generiert.

</dd> </dl> </dd> <dt>

 Bereich \[ in\]
</dt> <dd>

Wenn der *ScopeType* -Parameter 2 ist, gibt *ScopeType* die Organisationseinheit an, für die der Bericht generiert wird. Sie müssen *scopevalue* mit dem Format **OU =**_OUName1_*_, ou =_*_OUName2_*_._*.. angeben.

</dd> <dt>

*Dateiname* \[ vorgenommen\]
</dt> <dd>

Der Dateiname des generierten Berichts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **WBEM \_ E \_ nicht \_ unterstützt** zurück.

**Windows Server 2008 R2 und Windows Server 2008:** Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Dies ist eine statische Methode.

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                                 |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                         |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| Header<br/>                   | <dl> <dt>GPMgmt. h</dt> </dl>       |
| MOF<br/>                      | <dl> <dt>Tltaumiprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Datei- \_ /licensereport**](win32-tslicensereport.md)
</dt> </dl>

 

