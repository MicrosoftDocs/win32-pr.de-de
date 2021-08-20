---
title: UpgradeEditionWithLicenseMethod-Methode der MDM_WindowsLicensing-Klasse
description: Methode zum Bereitstellen einer Lizenz für ein Editionsupgrade von Windows 10 mobilen Geräten. Siehe auch UpgradeEditionWithLicense.
ms.assetid: 1a57fb71-eea6-41bf-bc44-6d3a816096a4
keywords:
- UpgradeEditionWithLicenseMethod-Methode
- UpgradeEditionWithLicenseMethod-Methode, MDM_WindowsLicensing-Klasse
- MDM_WindowsLicensing-Klasse, UpgradeEditionWithLicenseMethod-Methode
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26329c98bc73919d374787deea21841a2912a9df3fded8fdcde0637d8798c92f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913260"
---
# <a name="upgradeeditionwithlicensemethod-method-of-the-mdm_windowslicensing-class"></a>UpgradeEditionWithLicenseMethod-Methode der \_ MDM-WindowsLicensing-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Methode zum Bereitstellen einer Lizenz für ein Editionsupgrade von Windows 10 mobilen Geräten. Siehe auch [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp).

## <a name="syntax"></a>Syntax


```mof
uint32 UpgradeEditionWithLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*param* \[ In\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MDM \_ WindowsLicensing**](mdm-windowslicensing.md)
</dt> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge-Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

