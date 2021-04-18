---
title: Die Methode "hustedinstallmethod" der MDM_EnterpriseModernAppManagement_AppInstallation01_01-Klasse
description: Methode, mit der ein App-Paket von einem gehosteten Speicherort, z. b. einem lokalen Laufwerk, einer UNC-oder HTTPS-Datenquelle, installiert wird. Siehe auch "horstedinstall".
ms.assetid: 1ec16315-75ce-4613-804e-6b587c4071d6
keywords:
- Methode "hustedinstallmethod"
- Methode "" der Methode "", "MDM_EnterpriseModernAppManagement_AppInstallation01_01 Klasse"
- MDM_EnterpriseModernAppManagement_AppInstallation01_01-Klasse, Methode "" der Methode ""
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.HostedInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597f748a2b5695fd2703f187cfe50db7ad0aa85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344084"
---
# <a name="hostedinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>Methode "hustedinstallmethod" der MDM \_ enterprismodernappmanagement \_ AppInstallation01 \_ 01-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Methode, mit der ein App-Paket von einem gehosteten Speicherort, z. b. einem lokalen Laufwerk, einer UNC-oder HTTPS-Datenquelle, installiert wird. Siehe auch " [horstedinstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp)".

## <a name="syntax"></a>Syntax


```mof
uint32 HostedInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*param* \[ in\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ MDM- \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Dmwmibridgeprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MDM \_ enterprinappmanagement \_ AppInstallation01 \_ 01**](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

