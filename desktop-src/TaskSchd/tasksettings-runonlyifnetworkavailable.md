---
title: TaskSettings.RunOnlyIfNetworkAvailable (Eigenschaft)
description: Für die Skripterstellung ruft einen booleschen Wert ab, der angibt, dass der Taskplaner die Aufgabe nur dann ausführen wird, wenn ein Netzwerk verfügbar ist, oder legt diesen fest.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- RunOnlyIfNetworkAvailable-Eigenschaft Taskplaner
- RunOnlyIfNetworkAvailable-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Taskplaner , RunOnlyIfNetworkAvailable-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 193d235276ffc37513c95b5ae0a4cef5a6e84cd0bc7d8bea7fab67a262110080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354847"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a>TaskSettings.RunOnlyIfNetworkAvailable (Eigenschaft)

Für die Skripterstellung ruft einen booleschen Wert ab, der angibt, dass der Taskplaner die Aufgabe nur dann ausführen wird, wenn ein Netzwerk verfügbar ist, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass der Taskplaner task nur dann ausgeführt wird, wenn ein Netzwerk verfügbar ist. Die Standardeinstellung lautet „false“.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**RunOnlyIfNetworkAvailable-Element**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





