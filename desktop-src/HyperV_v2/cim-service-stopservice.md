---
description: Beschleunigt den Dienst im Zustand "Beendet".
ms.assetid: d7469643-bccc-4f55-b2fc-d2bc2e392d84
title: StopService-Methode der CIM_Service-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b36cab1054e99ac306fb1b21fe9f08e0820974a0883e90655a180b07035b7f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647583"
---
# <a name="stopservice-method-of-the-cim_service-class-hyper-v-management"></a>StopService-Methode der CIM_Service-Klasse (Hyper-V-Verwaltung)

Beschleunigt den Dienst im Zustand "Beendet".

> [!Note]
>
> Die Semantik dieser Methode überschneidet sich mit der **RequestStateChange-Methode,** die von [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)geerbt wird. Diese Methode wird beibehalten, da sie umfassend implementiert wurde und ihre einfache "Stop"-Semantik praktisch zu verwenden ist.

 

## <a name="syntax"></a>Syntax


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 zurück. andernfalls wird ein Fehler zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Dienst**](cim-service.md)
</dt> </dl>

 

 




