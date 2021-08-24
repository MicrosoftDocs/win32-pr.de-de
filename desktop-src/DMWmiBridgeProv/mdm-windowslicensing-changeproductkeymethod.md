---
title: ChangeProductKeyMethod-Methode der MDM_WindowsLicensing Klasse
description: Diese Methode installiert einen Product Key für Windows 10 Desktopgeräte. Punkt nicht neu starten. Siehe auch ChangeProductKey.
ms.assetid: 1d9e3243-2ca4-427b-bda2-d33e1e70c80d
keywords:
- ChangeProductKeyMethod-Methode
- ChangeProductKeyMethod-Methode, MDM_WindowsLicensing Klasse
- MDM_WindowsLicensing, ChangeProductKeyMethod-Methode
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.ChangeProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c164a97061b5e558a199a7d7e19a6bf26d7efc5d2a82c0a00e3831985c1a1cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693350"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>ChangeProductKeyMethod-Methode der \_ MDM-WindowsLicensing-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Diese Methode installiert einen Product Key für Windows 10 Desktopgeräte. Punkt nicht neu starten. Siehe auch [ChangeProductKey.](/windows/client-management/mdm/windowslicensing-csp)

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeProductKeyMethod(
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

[**MDM \_ WindowsLizenzierung**](mdm-windowslicensing.md)
</dt> </dl>

 

