---
description: Versetzt den Dienst in den Zustand "gestartet".
ms.assetid: 8977b806-150c-4ddc-a471-3fdafdcb4a55
title: Start Service-Methode der CIM_Service-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 73b89f7fc789639fb45acbde61da4c7962650177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345137"
---
# <a name="startservice-method-of-the-cim_service-class-hyper-v-management"></a>Start Service-Methode der CIM_Service-Klasse (Hyper-V-Verwaltung)

Versetzt den Dienst in den Zustand "gestartet".

> [!Note]
>
> Die Semantik dieser Methode überschneidet sich mit der **requestStateChange** -Methode, die von [**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md)geerbt wird. Diese Methode wird beibehalten, da Sie weitgehend implementiert wurde und ihre einfache "Start"-Semantik praktisch verwendet werden kann.

 

## <a name="syntax"></a>Syntax


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

[**CIM- \_ Dienst**](cim-service.md)
</dt> </dl>

 

 




