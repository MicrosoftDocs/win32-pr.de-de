---
title: GenerateReport-Methode der Win32_TSLicenseReport-Klasse (Gpmgmt.h)
description: GenerateReport ist ab Windows Server 2012 nicht mehr für die Verwendung verfügbar.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- GenerateReport-Methode Remotedesktopdienste
- GenerateReport-Methode Remotedesktopdienste , Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport Klasse Remotedesktopdienste , GenerateReport-Methode
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
ms.openlocfilehash: a619da8130187a4ab5d39de390315dd99b3ee7a171005a4cf66e7bb5677ae87c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130779"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a>GenerateReport-Methode der Win32 \_ TSLicenseReport-Klasse

\[**GenerateReport** ist ab Windows Server 2012 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen [**GenerateReportEx.**](generatereportex-win32-tslicensereport.md)\]

Diese Methode wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008:** Generiert einen aktuellen Benutzerlizenznutzungsbericht auf dem Remotedesktop Lizenzserver.

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

*ScopeType* \[ In\]
</dt> <dd>

Bereich des Lizenznutzungsberichts. Sie kann die folgenden Werte aufweisen.

<dt>

1
</dt> <dd>

Der Bericht wird für die gesamte Domäne generiert.

</dd> <dt>

2
</dt> <dd>

Der Bericht wird für die Organisationseinheit (OU) generiert, die im *ScopeValue-Parameter* angegeben ist.

</dd> <dt>

3
</dt> <dd>

Der Bericht wird für alle vertrauenswürdigen Domänen generiert.

</dd> </dl> </dd> <dt>

*ScopeValue* \[ In\]
</dt> <dd>

Wenn der *ScopeType-Parameter* 2 ist, gibt *ScopeType* die Organisationseinheit an, für die der Bericht generiert wird. Sie müssen *ScopeValue* angeben, indem Sie das Format **OU=**_OUName1_*_,OU=_*_OUName2_...*_verwenden._*

</dd> <dt>

*FileName* \[ out\]
</dt> <dd>

Der Dateiname des generierten Berichts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **WBEM \_ E NICHT UNTERSTÜTZT \_ \_ zurück.**

**Windows Server 2008 R2 und Windows Server 2008:** Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Bemerkungen

Dies ist eine statische Methode.

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                                 |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                         |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Gpmgmt.h</dt> </dl>       |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> </dl>

 

