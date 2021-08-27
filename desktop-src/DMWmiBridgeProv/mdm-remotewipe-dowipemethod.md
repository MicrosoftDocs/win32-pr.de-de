---
title: doWipeMethod-Methode der MDM_RemoteWipe-Klasse
description: Löst das Gerät aus, um die Remotelöschung zu starten.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- doWipeMethod-Methode
- doWipeMethod-Methode, MDM_RemoteWipe-Klasse
- MDM_RemoteWipe, doWipeMethod-Methode
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cff9cb831931c96fa8df1b376f96ea4c20b05bafdb12a85dec00b4f505af4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045640"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a>doWipeMethod-Methode der MDM \_ RemoteWipe-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Löst das Gerät aus, um die Remotelöschung zu starten. Siehe auch [doWipe](/windows/client-management/mdm/remotewipe-csp).

## <a name="syntax"></a>Syntax


```mof
uint32 doWipeMethod(
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
| Namespace<br/>                | \\ \\ Stamm-CIMv2-MDM-DMMap \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MDM \_ RemoteWipe**](mdm-remotewipe.md)
</dt> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge-Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

