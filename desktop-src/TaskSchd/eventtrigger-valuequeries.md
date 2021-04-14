---
title: EventTrigger. valuequeries (Eigenschaft)
description: Ruft bei der Skripterstellung eine Auflistung von benannten XPath-Abfragen ab oder legt diese fest. Jede Abfrage in der Auflistung wird auf das letzte übereinstimmende Ereignis-XML angewendet, das von der Abonnement Abfrage zurückgegeben wird, die in der Abonnement-Eigenschaft angegeben ist.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- Valuequeries-Eigenschaft Taskplaner
- Valuequeries-Eigenschaft Taskplaner, EventTrigger-Objekt
- EventTrigger-Objekt Taskplaner, valuequeries-Eigenschaft
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd2061f9d910e67855cc0dcb6d64248067fcb9e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518509"
---
# <a name="eventtriggervaluequeries-property"></a>EventTrigger. valuequeries (Eigenschaft)

Ruft bei der Skripterstellung eine Auflistung von benannten XPath-Abfragen ab oder legt diese fest. Jede Abfrage in der Auflistung wird auf das letzte übereinstimmende Ereignis-XML angewendet, das von der Abonnement Abfrage zurückgegeben wird, die in der [**Abonnement**](eventtrigger-subscription.md) -Eigenschaft angegeben ist.

## <a name="syntax"></a>Syntax


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a>Eigenschaftswert

Eine Auflistung von Name-Wert-Paaren. Jedes Name/Wert-Paar in der Auflistung definiert einen eindeutigen Namen für einen Eigenschafts Wert des Ereignisses, das den Ereignis Trigger auslöst. Der Eigenschafts Wert des Ereignisses wird als XPath-Ereignis Abfrage definiert. Weitere Informationen zu XPath-Ereignis Abfragen finden Sie unter [Ereignis Auswahl](/previous-versions//aa385231(v=vs.85)).

## <a name="remarks"></a>Bemerkungen

Der Name der Abfrage kann in den folgenden Aktions Eigenschaften als Variable verwendet werden:

-   [**Showmessageaction. MessageBody**](showmessageaction-messagebody.md)
-   [**Showmessageaction. Title**](showmessageaction-title.md)
-   [**Execaction. Arguments**](execaction-arguments.md)
-   [**Execaction. WorkingDirectory**](execaction-workingdirectory.md)
-   [**Emailaction. Server**](emailaction-server.md)
-   [**Emailaction. Subject**](emailaction-subject.md)
-   [**EmailAction.To**](emailaction-to.md)
-   [**EmailAction.Cc**](emailaction-cc.md)
-   [**Emailaction. BCC**](emailaction-bcc.md)
-   [**Emailaction. ReplyTo**](emailaction-replyto.md)
-   [**Emailaction. from**](emailaction-from.md)
-   [**Emailaction. Body**](emailaction-body.md)
-   [**Comhandleraction. Data**](comhandleraction-data.md)

In den folgenden Codebeispiel Zeichenfolgen werden zwei Name-Wert-Paare angezeigt, die in einer Name/Wert-Auflistung verwendet werden können. Die von den XPath-Abfragen zurückgegebenen Werte können Variablen in der-Eigenschaft einer Aktion ersetzen. Auf die Werte wird anhand des Namens mit `$(user)` und `$(machine)` in der Action-Eigenschaft verwiesen. Wenn beispielsweise die `$(user)` Variablen und `$(machine)` in der Zeichenfolge [**showmessageaction. MessageBody**](showmessageaction-messagebody.md) verwendet werden, ersetzt der Wert der XPath-Abfragen die Variablen in der Zeichenfolge.

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

Weitere Informationen zum Schreiben einer Abfrage Zeichenfolge für bestimmte Ereignisse finden Sie unter [Ereignis Auswahl](/previous-versions//aa385231(v=vs.85)) und [Abonnieren von Ereignissen](../wes/subscribing-to-events.md).

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

 

