---
title: Changeproductkeymethod-Methode der MDM_WindowsLicensing-Klasse
description: Mit dieser Methode wird eine Product Key für Windows 10-Desktop Geräte installiert. Punkt nicht neu starten. Siehe auch changeproductkey.
ms.assetid: 1d9e3243-2ca4-427b-bda2-d33e1e70c80d
keywords:
- Changeproductkeymethod-Methode
- Changeproductkeymethod-Methode, MDM_WindowsLicensing-Klasse
- MDM_WindowsLicensing-Klasse, changeproductkeymethod-Methode
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
ms.openlocfilehash: 1e00345fb0e23655b457e0540c70289a169c54ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478045"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>Changeproductkeymethod-Methode der MDM \_ windowslicensing-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Mit dieser Methode wird eine Product Key für Windows 10-Desktop Geräte installiert. Punkt nicht neu starten. Siehe auch [changeproductkey](/windows/client-management/mdm/windowslicensing-csp)

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeProductKeyMethod(
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

[**MDM- \_ windowslicensing**](mdm-windowslicensing.md)
</dt> </dl>

 

