---
description: Die onlinedevice-Methode wurde als veraltet markiert, anstelle der allgemeineren requestStateChange-Methode, die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überlappt.
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: Onlinedevice-Methode der CIM_LogicalDevice-Klasse
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
ms.openlocfilehash: 56e5fae557198a713aec338f92ad8f2865b2c351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351041"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a>Onlinedevice-Methode der CIM \_ LogicalDevice-Klasse

Die **onlinedevice** -Methode wurde als veraltet markiert, anstelle der allgemeineren **requestStateChange** -Methode, die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überlappt.

## <a name="syntax"></a>Syntax


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Online* \[ in\]
</dt> <dd>

Wenn der Wert **true** ist, schalten Sie das Gerät online, und schalten Sie das Gerät bei **false** offline.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




