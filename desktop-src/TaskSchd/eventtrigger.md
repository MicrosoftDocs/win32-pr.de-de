---
title: EventTrigger-Objekt (Windows.ui.xaml.h)
description: Skriptobjekt, das einen Trigger darstellt, der eine Aufgabe startet, wenn ein Systemereignis auftritt.
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- Ereignistrigger Taskplaner , Objekt
- EventTrigger-Objekt Taskplaner
- EventTrigger-Objekt Taskplaner beschrieben
topic_type:
- apiref
api_name:
- EventTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a355106ee4fcd6756e7aaf59c19664f91204ffb1caae6ebc2dbe45575a5f2ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060167"
---
# <a name="eventtrigger-object"></a>EventTrigger-Objekt

Skriptobjekt, das einen Trigger darstellt, der eine Aufgabe startet, wenn ein Systemereignis auftritt.

## <a name="members"></a>Member

Das **EventTrigger-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **EventTrigger-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögern**](eventtrigger-delay.md)<br/>                      | Lesen/Schreiben<br/> | Ruft einen Wert ab, der die Zeitspanne zwischen dem Eintreten des Ereignisses und dem Start der Aufgabe angibt, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                            |
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft einen booleschen Wert ab, der angibt, ob der Trigger aktiviert ist, oder legt diesen fest.<br/>                                                                                                                                                                                                                                             |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft das Datum und die Uhrzeit der Deaktivierung des Triggers ab oder legt diese fest. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.<br/>                                                                                                                                                                                              |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft die maximale Zeit ab, die der durch diesen Trigger gestartete Task ausführen darf, oder legt diese fest.<br/>                                                                                                                                                                                                                       |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft den Bezeichner für den Trigger ab oder legt den Bezeichner fest.<br/>                                                                                                                                                                                                                                                                            |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft ab oder legt fest, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.<br/>                                                                                                                                                                                                       |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft das Datum und die Uhrzeit der Aktivierung des Triggers ab oder legt diese fest.<br/>                                                                                                                                                                                                                                                           |
| [**Subscription**](eventtrigger-subscription.md)<br/>        | Lesen/Schreiben<br/> | Ruft die XPath-Abfragezeichenfolge ab, die das Ereignis identifiziert, das den Trigger auslöst, oder legt sie fest.<br/>                                                                                                                                                                                                                                                                                         |
| [**type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Schreibgeschützt<br/>  | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft den Typ des Triggers ab.<br/>                                                                                                                                                                                                                                                                                           |
| [**ValueQueries**](eventtrigger-valuequeries.md)<br/>        | Lesen/Schreiben<br/> | Ruft eine Auflistung benannter XPath-Abfragen ab oder legt diese fest. Jede Abfrage in der Auflistung wird auf die letzte übereinstimmende Ereignis-XML angewendet, die von der Abonnementabfrage zurückgegeben wird, die in der [**Subscription-Eigenschaft**](eventtrigger-subscription.md) angegeben ist. Der Name der Abfrage kann als Variable in der Nachricht einer [**ShowMessageAction-Aktion**](showmessageaction.md) verwendet werden.<br/> |



 

## <a name="remarks"></a>Hinweise

Es können maximal 500 Aufgaben mit Ereignisabonnements erstellt werden. Ein Ereignisabonnement, das eine Vielzahl von Ereignissen abfragt, kann verwendet werden, um eine Aufgabe auszulösen, die die gleiche Aktion als Reaktion auf die protokollierten Ereignisse verwendet.

Beim Lesen oder Schreiben eigener XML-Daten für eine Aufgabe wird ein Ereignistrigger mithilfe des [**EventTrigger-Elements**](taskschedulerschema-eventtrigger-triggergroup-element.md) des Taskplaner Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und ein Codebeispiel für dieses Skriptobjekt finden Sie unter [Ereignisauslöserbeispiel (Skripterstellung).](/previous-versions//aa446887(v=vs.85))

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Windows.ui.xaml.h</dt> </dl> |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[**Triggercollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

