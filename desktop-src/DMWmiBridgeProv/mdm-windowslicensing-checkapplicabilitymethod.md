---
title: CheckApplicabilityMethod-Methode der MDM_WindowsLicensing-Klasse
description: Überprüft, ob der eingegebene Product Key für ein Editionsupgrade, die Aktivierung oder das Ändern eines Product Key von Windows 10 für Desktopgeräte verwendet werden kann. Siehe auch CheckApplicability.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- CheckApplicabilityMethod-Methode
- CheckApplicabilityMethod-Methode, MDM_WindowsLicensing-Klasse
- MDM_WindowsLicensing-Klasse, CheckApplicabilityMethod-Methode
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
ms.openlocfilehash: db236e05ffe7b5b6273e7cba594266c31720932b43a7df2de751a0fa66cced5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750150"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a>CheckApplicabilityMethod-Methode der \_ MDM-WindowsLicensing-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Überprüft, ob der eingegebene Product Key für ein Editionsupgrade, die Aktivierung oder das Ändern eines Product Key von Windows 10 für Desktopgeräte verwendet werden kann. Siehe auch [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).

## <a name="syntax"></a>Syntax


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*param* \[ In\]
</dt> <dd>

Der Product Key.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

TRUE oder FALSE

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MDM \_ WindowsLicensing**](mdm-windowslicensing.md)
</dt> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge-Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

