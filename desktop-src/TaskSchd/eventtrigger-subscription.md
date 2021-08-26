---
title: EventTrigger.Subscription-Eigenschaft
description: Ruft für die Skripterstellung eine Abfragezeichenfolge ab, die das Ereignis identifiziert, das den Trigger auslöst, oder legt diese fest.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Taskplaner der Abonnementeigenschaft
- Subscription-Eigenschaft Taskplaner , EventTrigger-Objekt
- EventTrigger-Objekt Taskplaner , Subscription-Eigenschaft
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d83225faa022de6e4a0823be3db971c71da503a885a46c1941fc1e5578f711b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100230"
---
# <a name="eventtriggersubscription-property"></a>EventTrigger.Subscription-Eigenschaft

Ruft für die Skripterstellung eine Abfragezeichenfolge ab, die das Ereignis identifiziert, das den Trigger auslöst, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a>Eigenschaftswert

Eine Abfragezeichenfolge, die das Ereignis identifiziert, das den Trigger auslöst.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben Eigener XML-Code für eine Aufgabe wird das Ereignisabonnement mithilfe des [**Subscription-Elements**](taskschedulerschema-subscription-eventtriggertype-element.md) des Taskplaner Schemas angegeben.

Weitere Informationen zum Schreiben einer Abfragezeichenfolge für bestimmte Ereignisse finden Sie unter [Ereignisauswahl](/previous-versions//aa385231(v=vs.85)) und [Abonnieren von Ereignissen.](../wes/subscribing-to-events.md)

## <a name="examples"></a>Beispiele

Die folgende Abfragezeichenfolge definiert ein Abonnement für alle Ereignisse der Ebene 2 im Systemkanal:


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

