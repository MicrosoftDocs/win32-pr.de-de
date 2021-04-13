---
title: Message-Attribut
description: Das Attribut \ Message \ gibt an, dass der Remote Prozedur Aufrufe als Nachricht vom Client an den Server behandelt werden soll.
ms.assetid: ec616bf5-a845-4e7e-9f39-20947d2074f7
keywords:
- Nachrichten Attribut-Mittel l
topic_type:
- apiref
api_name:
- message
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964f8dfd8652547bdf5bef25d1abe9acde8189a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472940"
---
# <a name="message-attribute"></a>Message-Attribut

Das **\[ Message \]** -Attribut gibt an, dass der Remote Prozedur Aufrufe als Nachricht vom Client an den Server behandelt werden soll.

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*optional-Attribut-List* 
</dt> <dd>

Andere Attribute, die auf die Funktion angewendet werden. Nur die **\[** Attribute " [**local**](local.md)" **\]** , " **\[** [**NoCode**](nocode.md)", " **\]** **\[** [**Code**](code.md)**\]** " und " **\[** [**optimieren**](optimize.md) " **\]** können mit dem **\[ Message \]** -Attribut verwendet werden.

</dd> <dt>

*function-name* 
</dt> <dd>

Der Name der Funktion, wie in der IDL-Datei definiert.

</dd> <dt>

*optionale Parameter-Attribute* 
</dt> <dd>

NULL oder mehr Mittelwert Attribute, die auf den-Parameter angewendet werden.

</dd> <dt>

*Param-Name* 
</dt> <dd>

Der Name des Parameters, wie er in der IDL-Datei definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beim Senden von Nachrichten vom Client werden Remote Prozedur Aufrufe mit dem **\[ \] Message** -Attribut asynchron über den [**ncadg \_ MQ**](ncadg-mq.md) -Nachrichten Warteschlangen-Transport an den Server übermittelt. Sie können das Messaging im synchronen Modus angeben, indem Sie das **ncadg \_ MQ** -Transportprotokoll angeben, ohne das **\[ Message \]** -Attribut zu verwenden.

Durch die Angabe des asynchronen Nachrichten Modus ermöglicht das **\[ Message \]** -Attribut dem Client, den Remote Prozedur Aufrufe auszuführen und sofort zurückzukehren, auch wenn die Serveranwendung nicht antwortet. Wenn der Zielserver nicht verfügbar ist, wird der-Vorgang so lange gespeichert, bis der Server verfügbar wird.

Darüber hinaus können Sie mit dem asynchronen Modus-Messaging die Nachrichten Warteschlangen Eigenschaften der Empfangs Warteschlange für den Server steuern. Weitere Informationen zum Auswählen von Quality of Service, der Telefon Priorität und der Lebensdauer des Aufrufs für den Server Prozess finden Sie unter [**rpcbindingsetoption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) .

Die folgenden Einschränkungen gelten auch für das **\[ Message \]** -Attribut:

-   Microsoft Message Queuing müssen in den Client-und Serversystemen implementiert werden, und die Systeme müssen zueinander sichtbar sein, wie im Rahmen der Installation der Nachrichten Warteschlange festgelegt.
-   Die Bindung muss bekannte Endpunkte und das [**ncadg \_ MQ**](ncadg-mq.md) -Transportprotokoll verwenden.
-   Die Funktion darf keine Ausgabeparameter oder einen anderen Rückgabetyp als [**void**](void.md)enthalten. Beachten Sie, dass die letztere Einschränkung zu diesem Zeitpunkt das **\[ Message \]** -Attribut für COM-Schnittstellen Methoden (Object) ungeeignet macht. Die nächste Version von "Mittel l" ermöglicht **\[ Nachrichten \]** Funktionen, den Fehler \_ Status "t" oder "HRESULT" zurückzugeben \_ .
-   Alle Schnittstellen, die mindestens einen **\[ Nachrichten \]** Aufruf enthalten, müssen registriert werden, indem [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) oder [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) aufgerufen wird, bevor [**rpcserveruseprotsetqepex (ncadg \_ mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex)aufgerufen wird. Andernfalls werden Aufrufe, die auf die Warteschlange für den Server gewartet haben, gelesen, bevor die Schnittstelle registriert wird, und die Aufrufe können nicht ausgeführt werden.

## <a name="examples"></a>Beispiele

``` syntax
[message] void DisplayString(
    [in, string] char * p1);
 
[message] void VarDataArray(
    [in, size_is(iSize)] ARRAY_TYPE lpMyArray,
    [in] int iSize,
    [in] unsigned long ulChksum);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Ordnung**](code.md)
</dt> <dt>

[**nah**](local.md)
</dt> <dt>

[**ncadg \_ MQ**](ncadg-mq.md)
</dt> <dt>

[**NoCode**](nocode.md)
</dt> <dt>

[**optimiert**](optimize.md)
</dt> <dt>

[RPC-Message Queuing](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[**Rpcbindingsetoption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**Rpcbindinginqoption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 