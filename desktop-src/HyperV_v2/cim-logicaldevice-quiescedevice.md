---
description: Die Methode "quiescedevice" wurde als veraltet markiert, anstelle der allgemeineren Methode "requestStateChange", die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überlappt.
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: Quiescedevice-Methode der CIM_LogicalDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 82041b36592f00bf71dc7e2d744fcf94b7a666c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347808"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a>Quiescedevice-Methode der CIM \_ LogicalDevice-Klasse

Die Methode " **quiescedevice** " wurde als veraltet markiert, anstelle der allgemeineren Methode " **requestStateChange** ", die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überlappt.

## <a name="syntax"></a>Syntax


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Inaktiven Status  \[ in\]
</dt> <dd>

Bei Festlegung auf **true** beenden Sie alle Aktivitäten ordnungsgemäß, wenn die Aktivität **false** fortsetzen.

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

 

 




