---
title: ncadg_mq-Attribut
description: Das ncadg \_ MQ-Schlüsselwort identifiziert Microsoft Message Queuing Services (MSMQ) als Transportprotokoll für den Endpunkt. Dieses Protokoll ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0acc433b55ba9f3c6d8919bef9b8db470bc0f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948657"
---
# <a name="ncadg_mq-attribute"></a><span data-ttu-id="e6b12-105">ncadg \_ MQ-Attribut</span><span class="sxs-lookup"><span data-stu-id="e6b12-105">ncadg\_mq attribute</span></span>

<span data-ttu-id="e6b12-106">Das **ncadg \_ MQ** -Schlüsselwort identifiziert Microsoft Message Queuing Services (MSMQ) als Transportprotokoll für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="e6b12-106">The **ncadg\_mq** keyword identifies Microsoft Message Queuing Services (MSMQ) as the transport protocol for the endpoint.</span></span> <span data-ttu-id="e6b12-107">Dieses Protokoll ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6b12-107">This protocol is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a><span data-ttu-id="e6b12-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6b12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6b12-109">*Servername*</span><span class="sxs-lookup"><span data-stu-id="e6b12-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e6b12-110">Gibt den Namen des Servers oder Hosts an.</span><span class="sxs-lookup"><span data-stu-id="e6b12-110">Specifies the name of the server, or host, computer.</span></span> <span data-ttu-id="e6b12-111">Der Name ist eine Zeichenfolge und kann ein voll qualifizierter Domänen Name sein.</span><span class="sxs-lookup"><span data-stu-id="e6b12-111">The name is a character string and may be a fully qualified domain name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6b12-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6b12-112">Remarks</span></span>

<span data-ttu-id="e6b12-113">Um das **ncadg \_ MQ** -Transportprotokoll verwenden zu können, müssen die MSMQ-Komponenten vollständig installiert sein, und die Client-und Serversysteme müssen über die MQ-Protokolle erreichbar sein.</span><span class="sxs-lookup"><span data-stu-id="e6b12-113">In order to use the **ncadg\_mq** transport protocol, the MSMQ components must be fully installed and the client and server systems must be reachable through the MQ protocols.</span></span>

<span data-ttu-id="e6b12-114">Das **ncadg \_ MQ** -Protokoll unterstützt keine dynamischen Endpunkte oder [**Broadcast**](broadcast.md) Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="e6b12-114">The **ncadg\_mq** protocol does not support dynamic endpoints or [**broadcast**](broadcast.md) calls.</span></span> <span data-ttu-id="e6b12-115">Wie bei anderen datagrammprotokollen unterstützt **ncadg \_ MQ** keine Rückrufe. alle Funktionen, die das [**Rückruf**](callback.md) Attribut verwenden, schlagen fehl.</span><span class="sxs-lookup"><span data-stu-id="e6b12-115">As with other datagram protocols, **ncadg\_mq** does not support callbacks; any functions using the [**callback**](callback.md) attribute will fail.</span></span>

> [!Note]  
> <span data-ttu-id="e6b12-116">Diese Protokollfamilie wird in Windows XP nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e6b12-116">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e6b12-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6b12-117">Examples</span></span>

<span data-ttu-id="e6b12-118">Die Syntax des Message-Queue-Protokolls wird unabhängig von der IDL-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="e6b12-118">The syntax of the message-queue protocol is defined independently of the IDL specification.</span></span> <span data-ttu-id="e6b12-119">Der mittlerer l-Compiler führt einige Syntax Überprüfungen durch, garantiert jedoch nicht, dass die Endpunkt Spezifikation korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="e6b12-119">The MIDL compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="e6b12-120">Einige Fehler werden möglicherweise zur Laufzeit gemeldet, nicht während der Kompilierung.</span><span class="sxs-lookup"><span data-stu-id="e6b12-120">Some errors may be reported at run time rather than during compilation.</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_mq:rainier") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="e6b12-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6b12-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6b12-122">**aus**</span><span class="sxs-lookup"><span data-stu-id="e6b12-122">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="e6b12-123">**Rückruf**</span><span class="sxs-lookup"><span data-stu-id="e6b12-123">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="e6b12-124">**Dreher**</span><span class="sxs-lookup"><span data-stu-id="e6b12-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="e6b12-125">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="e6b12-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e6b12-126">**Nachricht**</span><span class="sxs-lookup"><span data-stu-id="e6b12-126">**message**</span></span>](message.md)
</dt> <dt>

[<span data-ttu-id="e6b12-127">RPC-Message Queuing</span><span class="sxs-lookup"><span data-stu-id="e6b12-127">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="e6b12-128">Zeichen folgen Bindung</span><span class="sxs-lookup"><span data-stu-id="e6b12-128">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 