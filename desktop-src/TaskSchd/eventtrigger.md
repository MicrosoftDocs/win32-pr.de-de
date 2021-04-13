---
title: EventTrigger-Objekt (Windows. UI. XAML. h)
description: Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn ein System Ereignis auftritt.
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- Taskplaner des Ereignis Auslösers, Objekt
- EventTrigger-Objekt Taskplaner
- EventTrigger-Objekt Taskplaner, beschrieben
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
ms.openlocfilehash: 77b80bc8336c4756dfedc041aea40f79fd5f868e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518605"
---
# <a name="eventtrigger-object"></a>EventTrigger-Objekt

Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn ein System Ereignis auftritt.

## <a name="members"></a>Member

Das **EventTrigger** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **EventTrigger** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögern**](eventtrigger-delay.md)<br/>                      | Lesen/Schreiben<br/> | Ruft einen Wert ab oder legt einen Wert fest, der die Zeitspanne zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe angibt.<br/>                                                                                                                                                                                                                                                            |
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.<br/>                                                                                                                                                                                                                                             |
| [**Endgrenze**](trigger-endboundary.md)<br/>               | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/>                                                                                                                                                                                              |
| [**Executiontimelimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft die maximale Zeitspanne ab, die der von diesem-Vorgang gestartete Task ausgeführt werden darf, oder legt diese fest.<br/>                                                                                                                                                                                                                       |
| [**Name**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Bezeichner für den-Typ ab oder legt ihn fest.<br/>                                                                                                                                                                                                                                                                            |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft ab oder legt fest, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.<br/>                                                                                                                                                                                                       |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.<br/>                                                                                                                                                                                                                                                           |
| [**Abonnement**](eventtrigger-subscription.md)<br/>        | Lesen/Schreiben<br/> | Ruft die XPath-Abfrage Zeichenfolge ab, die das Ereignis identifiziert, das den-Triggers auslöst<br/>                                                                                                                                                                                                                                                                                         |
| [**type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Schreibgeschützt<br/>  | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Typ des Auslösers ab.<br/>                                                                                                                                                                                                                                                                                           |
| [**Valuequeries**](eventtrigger-valuequeries.md)<br/>        | Lesen/Schreiben<br/> | Ruft eine Auflistung von benannten XPath-Abfragen ab oder legt diese fest. Jede Abfrage in der Auflistung wird auf das letzte übereinstimmende Ereignis-XML angewendet, das von der Abonnement Abfrage zurückgegeben wird, die in der [**Abonnement**](eventtrigger-subscription.md) -Eigenschaft angegeben ist. Der Name der Abfrage kann als Variable in der Nachricht einer [**showmessageaction**](showmessageaction.md) -Aktion verwendet werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Es können maximal 500 Tasks mit Ereignis Abonnements erstellt werden. Ein Ereignis Abonnement, das Abfragen für eine Vielzahl von Ereignissen verwendet, kann verwendet werden, um eine Aufgabe zu initiieren, die dieselbe Aktion als Reaktion auf die protokollierten Ereignisse verwendet.

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird ein Ereignis Trigger mit dem [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und ein Codebeispiel für dieses Skript Objekt finden Sie unter [Event-auslöserbeispiel (Skripterstellung)](/previous-versions//aa446887(v=vs.85)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Windows. UI. XAML. h</dt> </dl> |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

