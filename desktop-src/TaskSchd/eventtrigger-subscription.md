---
title: EventTrigger. Abonnement (Eigenschaft)
description: Ruft bei der Skripterstellung eine Abfrage Zeichenfolge ab, die das Ereignis identifiziert, das den-Triggern auslöst
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Abonnement Eigenschaft Taskplaner
- Abonnement Eigenschaft Taskplaner, EventTrigger-Objekt
- EventTrigger-Objekt Taskplaner, Abonnement Eigenschaft
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
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338781"
---
# <a name="eventtriggersubscription-property"></a>EventTrigger. Abonnement (Eigenschaft)

Ruft bei der Skripterstellung eine Abfrage Zeichenfolge ab, die das Ereignis identifiziert, das den-Triggern auslöst

## <a name="syntax"></a>Syntax


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a>Eigenschaftswert

Eine Abfrage Zeichenfolge, die das Ereignis identifiziert, das den-Triggern auslöst.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird das Ereignis Abonnement mit dem [**Abonnement**](taskschedulerschema-subscription-eventtriggertype-element.md) -Element des Taskplaner-Schemas angegeben.

Weitere Informationen zum Schreiben einer Abfrage Zeichenfolge für bestimmte Ereignisse finden Sie unter [Ereignis Auswahl](/previous-versions//aa385231(v=vs.85)) und [Abonnieren von Ereignissen](../wes/subscribing-to-events.md).

## <a name="examples"></a>Beispiele

Die folgende Abfrage Zeichenfolge definiert ein Abonnement für alle Ereignisse der Ebene 2 im System Kanal:


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

