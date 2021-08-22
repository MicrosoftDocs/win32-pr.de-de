---
title: EventTrigger.ValueQueries (Eigenschaft)
description: Für die Skripterstellung ruft eine Auflistung benannter XPath-Abfragen ab oder legt diese fest. Jede Abfrage in der Auflistung wird auf die zuletzt übereinstimmende Ereignis-XML angewendet, die von der in der Subscription-Eigenschaft angegebenen Abonnementabfrage zurückgegeben wird.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- ValueQueries-Taskplaner
- ValueQueries-Eigenschaft Taskplaner , EventTrigger-Objekt
- EventTrigger-Objekt Taskplaner , ValueQueries-Eigenschaft
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
ms.openlocfilehash: 9f8fd28cd616af56a9b51ecf4e709df5f07674c6d1f307320128645364f3bfc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253880"
---
# <a name="eventtriggervaluequeries-property"></a>EventTrigger.ValueQueries (Eigenschaft)

Für die Skripterstellung ruft eine Auflistung benannter XPath-Abfragen ab oder legt diese fest. Jede Abfrage in der Auflistung wird auf die zuletzt übereinstimmende Ereignis-XML angewendet, die von der in der Subscription-Eigenschaft angegebenen [**Abonnementabfrage zurückgegeben**](eventtrigger-subscription.md) wird.

## <a name="syntax"></a>Syntax


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a>Eigenschaftswert

Eine Auflistung von Name-Wert-Paaren. Jedes Name-Wert-Paar in der Auflistung definiert einen eindeutigen Namen für einen Eigenschaftswert des Ereignisses, das den Ereignistrigger auslöst. Der Eigenschaftswert des Ereignisses wird als XPath-Ereignisabfrage definiert. Weitere Informationen zu XPath-Ereignisabfragen finden Sie unter [Ereignisauswahl.](/previous-versions//aa385231(v=vs.85))

## <a name="remarks"></a>Hinweise

Der Name der Abfrage kann als Variable in den folgenden Aktionseigenschaften verwendet werden:

-   [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md)
-   [**ShowMessageAction.Title**](showmessageaction-title.md)
-   [**ExecAction.Arguments**](execaction-arguments.md)
-   [**ExecAction.WorkingDirectory**](execaction-workingdirectory.md)
-   [**EmailAction.Server**](emailaction-server.md)
-   [**EmailAction.Subject**](emailaction-subject.md)
-   [**EmailAction.To**](emailaction-to.md)
-   [**EmailAction.Cc**](emailaction-cc.md)
-   [**EmailAction.Bcc**](emailaction-bcc.md)
-   [**EmailAction.ReplyTo**](emailaction-replyto.md)
-   [**EmailAction.From**](emailaction-from.md)
-   [**EmailAction.Body**](emailaction-body.md)
-   [**ComHandlerAction.Data**](comhandleraction-data.md)

Die folgenden Codebeispielzeichenfolgen zeigen zwei Name-Wert-Paare, die in einer Name-Wert-Auflistung verwendet werden können. Die von den XPath-Abfragen zurückgegebenen Werte können Variablen in der -Eigenschaft einer Aktion ersetzen. Auf die Werte wird durch den Namen mit `$(user)` und `$(machine)` in der Aktionseigenschaft verwiesen. Wenn beispielsweise die Variablen und in der `$(user)` `$(machine)` [**Zeichenfolge ShowMessageAction.MessageBody**](showmessageaction-messagebody.md) verwendet werden, ersetzt der Wert der XPath-Abfragen die Variablen in der Zeichenfolge.

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

Weitere Informationen zum Schreiben einer Abfragezeichenfolge für bestimmte Ereignisse finden Sie unter [Ereignisauswahl](/previous-versions//aa385231(v=vs.85)) und Abonnieren [von Ereignissen.](../wes/subscribing-to-events.md)

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
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

