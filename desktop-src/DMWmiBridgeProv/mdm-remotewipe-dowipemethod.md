---
title: dowipeer Method-Methode der MDM_RemoteWipe-Klasse
description: Hiermit wird das Gerät ausgelöst, um die Remote Löschung zu starten.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- dowipeer Method-Methode
- dowipeer Method-Methode, MDM_RemoteWipe-Klasse
- MDM_RemoteWipe-Klasse, dowipeer Method-Methode
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
ms.openlocfilehash: 2f31dcc9dde2fe51ca0d8677df8b27637edd06c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475285"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a>dowipeer Method-Methode der MDM \_ RemoteWipe-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Hiermit wird das Gerät ausgelöst, um die Remote Löschung zu starten. Siehe auch [dowipe](/windows/client-management/mdm/remotewipe-csp).

## <a name="syntax"></a>Syntax


```mof
uint32 doWipeMethod(
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
| Namespace<br/>                | Root \\ CIMv2 \\ MDM- \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Dmwmibridgeprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MDM- \_ Remotelöschung**](mdm-remotewipe.md)
</dt> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

