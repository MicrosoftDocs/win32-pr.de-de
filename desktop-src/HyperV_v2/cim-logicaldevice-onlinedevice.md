---
description: Die OnlineDevice-Methode ist veraltet und nicht mehr die allgemeinere RequestStateChange-Methode, die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überschneidet.
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: OnlineDevice-Methode der CIM_LogicalDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f34d08ad72bd04cd94e35ac229fde82ca4847ec13410e35d57d0de0778d50af2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695510"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a>OnlineDevice-Methode der CIM \_ LogicalDevice-Klasse

Die **OnlineDevice-Methode** ist veraltet und nicht mehr die allgemeinere **RequestStateChange-Methode,** die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überschneidet.

## <a name="syntax"></a>Syntax


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Online* \[ In\]
</dt> <dd>

True **gibt an,** dass das Gerät online geschaltet wird, wenn **FALSE,** das Gerät offline schalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




