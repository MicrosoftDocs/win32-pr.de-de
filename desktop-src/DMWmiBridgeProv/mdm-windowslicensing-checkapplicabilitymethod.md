---
title: Checkapplicabilitymethod-Methode der MDM_WindowsLicensing-Klasse
description: Überprüft, ob der eingegebene Product Key für ein Editions Upgrade, eine Aktivierung oder Änderung einer Product Key von Windows 10 für Desktop Geräte verwendet werden kann. Siehe auch Check Anwendbarkeit.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- Checkapplicabilitymethod-Methode
- Checkapplicabilitymethod-Methode, MDM_WindowsLicensing-Klasse
- MDM_WindowsLicensing-Klasse, checkapplicabilitymethod-Methode
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae08c4a13d036a7d1185a3d53dee846ea460e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104942"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a>Checkapplicabilitymethod-Methode der MDM \_ windowslicensing-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Überprüft, ob der eingegebene Product Key für ein Editions Upgrade, eine Aktivierung oder Änderung einer Product Key von Windows 10 für Desktop Geräte verwendet werden kann. Siehe auch [Check Anwendbarkeit](/windows/client-management/mdm/windowslicensing-csp).

## <a name="syntax"></a>Syntax


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*param* \[ in\]
</dt> <dd>

Der Product Key.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

TRUE oder FALSE

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

[**MDM- \_ windowslicensing**](mdm-windowslicensing.md)
</dt> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

