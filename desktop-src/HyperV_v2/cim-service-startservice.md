---
description: Platziert den Dienst in den Gestartet-Zustand.
ms.assetid: 8977b806-150c-4ddc-a471-3fdafdcb4a55
title: StartService-Methode der CIM_Service -Klasse (Hyper-V-Verwaltung)
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
ms.openlocfilehash: c0e30adbece838cb913f215abedc4aa86a2762d00f046a54bf2717eaeecdb56e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561810"
---
# <a name="startservice-method-of-the-cim_service-class-hyper-v-management"></a>StartService-Methode der CIM_Service -Klasse (Hyper-V-Verwaltung)

Platziert den Dienst in den Gestartet-Zustand.

> [!Note]
>
> Die Semantik dieser Methode überschneidet sich mit der **RequestStateChange-Methode,** die von [**CIM \_ EnabledLogicalElement geerbt wird.**](cim-enabledlogicalelement.md) Diese Methode wird beibehalten, da sie weit verbreitet implementiert wurde und ihre einfache "Start"-Semantik praktisch zu verwenden ist.

 

## <a name="syntax"></a>Syntax


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

[**\_CIM-Dienst**](cim-service.md)
</dt> </dl>

 

 




