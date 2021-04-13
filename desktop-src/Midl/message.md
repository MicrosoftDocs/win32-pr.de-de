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
# <a name="message-attribute"></a><span data-ttu-id="47e0a-104">Message-Attribut</span><span class="sxs-lookup"><span data-stu-id="47e0a-104">message attribute</span></span>

<span data-ttu-id="47e0a-105">Das **\[ Message \]** -Attribut gibt an, dass der Remote Prozedur Aufrufe als Nachricht vom Client an den Server behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="47e0a-105">The **\[message\]** attribute indicates that the remote procedure call is to be treated as a message from the client to the server.</span></span>

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="47e0a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="47e0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47e0a-107">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="47e0a-107">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="47e0a-108">Andere Attribute, die auf die Funktion angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="47e0a-108">Other attributes that apply to the function.</span></span> <span data-ttu-id="47e0a-109">Nur die **\[** Attribute " [**local**](local.md)" **\]** , " **\[** [**NoCode**](nocode.md)", " **\]** **\[** [**Code**](code.md)**\]** " und " **\[** [**optimieren**](optimize.md) " **\]** können mit dem **\[ Message \]** -Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47e0a-109">Only the **\[**[**local**](local.md)**\]**, **\[**[**nocode**](nocode.md)**\]**, **\[**[**code**](code.md)**\],** and **\[**[**optimize**](optimize.md)**\]** attributes may be used with the **\[message\]** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="47e0a-110">*function-name*</span><span class="sxs-lookup"><span data-stu-id="47e0a-110">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="47e0a-111">Der Name der Funktion, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="47e0a-111">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="47e0a-112">*optionale Parameter-Attribute*</span><span class="sxs-lookup"><span data-stu-id="47e0a-112">*optional-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="47e0a-113">NULL oder mehr Mittelwert Attribute, die auf den-Parameter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="47e0a-113">Zero or more MIDL attributes that will be applied to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="47e0a-114">*Param-Name*</span><span class="sxs-lookup"><span data-stu-id="47e0a-114">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="47e0a-115">Der Name des Parameters, wie er in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="47e0a-115">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47e0a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47e0a-116">Remarks</span></span>

<span data-ttu-id="47e0a-117">Beim Senden von Nachrichten vom Client werden Remote Prozedur Aufrufe mit dem **\[ \] Message** -Attribut asynchron über den [**ncadg \_ MQ**](ncadg-mq.md) -Nachrichten Warteschlangen-Transport an den Server übermittelt.</span><span class="sxs-lookup"><span data-stu-id="47e0a-117">As messages from the client, remote procedure calls with the **\[message\]** attribute are delivered to the server asynchronously over the [**ncadg\_mq**](ncadg-mq.md) message-queuing transport.</span></span> <span data-ttu-id="47e0a-118">Sie können das Messaging im synchronen Modus angeben, indem Sie das **ncadg \_ MQ** -Transportprotokoll angeben, ohne das **\[ Message \]** -Attribut zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="47e0a-118">You can indicate synchronous-mode messaging by specifying the **ncadg\_mq** transport protocol without using the **\[message\]** attribute.</span></span>

<span data-ttu-id="47e0a-119">Durch die Angabe des asynchronen Nachrichten Modus ermöglicht das **\[ Message \]** -Attribut dem Client, den Remote Prozedur Aufrufe auszuführen und sofort zurückzukehren, auch wenn die Serveranwendung nicht antwortet.</span><span class="sxs-lookup"><span data-stu-id="47e0a-119">By specifying asynchronous-mode messaging, the **\[message\]** attribute allows the client to make the remote procedure call and return immediately, even when the server application is not responding.</span></span> <span data-ttu-id="47e0a-120">Wenn der Zielserver nicht verfügbar ist, wird der-Vorgang so lange gespeichert, bis der Server verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="47e0a-120">If the target server is not available, the call will be stored until the server becomes available.</span></span>

<span data-ttu-id="47e0a-121">Darüber hinaus können Sie mit dem asynchronen Modus-Messaging die Nachrichten Warteschlangen Eigenschaften der Empfangs Warteschlange für den Server steuern.</span><span class="sxs-lookup"><span data-stu-id="47e0a-121">In addition, asynchronous-mode messaging lets you control message-queue properties of the receive queue for the server.</span></span> <span data-ttu-id="47e0a-122">Weitere Informationen zum Auswählen von Quality of Service, der Telefon Priorität und der Lebensdauer des Aufrufs für den Server Prozess finden Sie unter [**rpcbindingsetoption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) .</span><span class="sxs-lookup"><span data-stu-id="47e0a-122">See [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) for more information on selecting quality of service, call priority, and call lifetime for the server process.</span></span>

<span data-ttu-id="47e0a-123">Die folgenden Einschränkungen gelten auch für das **\[ Message \]** -Attribut:</span><span class="sxs-lookup"><span data-stu-id="47e0a-123">The following restrictions also apply to the **\[message\]** attribute:</span></span>

-   <span data-ttu-id="47e0a-124">Microsoft Message Queuing müssen in den Client-und Serversystemen implementiert werden, und die Systeme müssen zueinander sichtbar sein, wie im Rahmen der Installation der Nachrichten Warteschlange festgelegt.</span><span class="sxs-lookup"><span data-stu-id="47e0a-124">Microsoft Message Queuing must be implemented in the client and server systems and the systems must be visible to each other as determined by the scope of the message queue installation.</span></span>
-   <span data-ttu-id="47e0a-125">Die Bindung muss bekannte Endpunkte und das [**ncadg \_ MQ**](ncadg-mq.md) -Transportprotokoll verwenden.</span><span class="sxs-lookup"><span data-stu-id="47e0a-125">The binding must use well-known endpoints and the [**ncadg\_mq**](ncadg-mq.md) transport protocol.</span></span>
-   <span data-ttu-id="47e0a-126">Die Funktion darf keine Ausgabeparameter oder einen anderen Rückgabetyp als [**void**](void.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="47e0a-126">The function cannot contain output parameters or a return type other than [**void**](void.md).</span></span> <span data-ttu-id="47e0a-127">Beachten Sie, dass die letztere Einschränkung zu diesem Zeitpunkt das **\[ Message \]** -Attribut für COM-Schnittstellen Methoden (Object) ungeeignet macht.</span><span class="sxs-lookup"><span data-stu-id="47e0a-127">Note that the latter restriction makes the **\[message\]** attribute unsuitable for COM (object) interface methods, at this time.</span></span> <span data-ttu-id="47e0a-128">Die nächste Version von "Mittel l" ermöglicht **\[ Nachrichten \]** Funktionen, den Fehler \_ Status "t" oder "HRESULT" zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="47e0a-128">The next release of MIDL will permit **\[message\]** functions to return error\_status\_t or HRESULT.</span></span>
-   <span data-ttu-id="47e0a-129">Alle Schnittstellen, die mindestens einen **\[ Nachrichten \]** Aufruf enthalten, müssen registriert werden, indem [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) oder [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) aufgerufen wird, bevor [**rpcserveruseprotsetqepex (ncadg \_ mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="47e0a-129">Any interface that contains at least one **\[message\]** call must be registered by calling [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) or [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) before calling [**RpcServerUseProtseqEpEx(ncadg\_mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex).</span></span> <span data-ttu-id="47e0a-130">Andernfalls werden Aufrufe, die auf die Warteschlange für den Server gewartet haben, gelesen, bevor die Schnittstelle registriert wird, und die Aufrufe können nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="47e0a-130">Otherwise, calls that were waiting on the queue for the server will be read before the interface is registered, and the calls will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="47e0a-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47e0a-131">Examples</span></span>

``` syntax
[message] void DisplayString(
    [in, string] char * p1);
 
[message] void VarDataArray(
    [in, size_is(iSize)] ARRAY_TYPE lpMyArray,
    [in] int iSize,
    [in] unsigned long ulChksum);
```

## <a name="see-also"></a><span data-ttu-id="47e0a-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="47e0a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e0a-133">**Ordnung**</span><span class="sxs-lookup"><span data-stu-id="47e0a-133">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="47e0a-134">**nah**</span><span class="sxs-lookup"><span data-stu-id="47e0a-134">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="47e0a-135">**ncadg \_ MQ**</span><span class="sxs-lookup"><span data-stu-id="47e0a-135">**ncadg\_mq**</span></span>](ncadg-mq.md)
</dt> <dt>

[<span data-ttu-id="47e0a-136">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="47e0a-136">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="47e0a-137">**optimiert**</span><span class="sxs-lookup"><span data-stu-id="47e0a-137">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="47e0a-138">RPC-Message Queuing</span><span class="sxs-lookup"><span data-stu-id="47e0a-138">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="47e0a-139">**Rpcbindingsetoption**</span><span class="sxs-lookup"><span data-stu-id="47e0a-139">**RpcBindingSetOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[<span data-ttu-id="47e0a-140">**Rpcbindinginqoption**</span><span class="sxs-lookup"><span data-stu-id="47e0a-140">**RpcBindingInqOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[<span data-ttu-id="47e0a-141">**void**</span><span class="sxs-lookup"><span data-stu-id="47e0a-141">**void**</span></span>](void.md)
</dt> </dl>

 

 