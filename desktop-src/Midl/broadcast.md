---
title: Broadcast-Attribut
description: Das Schlüsselwort \ Broadcast \ gibt an, dass Remote Prozedur Aufrufe an alle Server in einem lokalen Netzwerk gesendet werden.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- Broadcast Attribut-Mittel l
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c2bbb724fc292a5e3942bf2b6de61b5631cdc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312852"
---
# <a name="broadcast-attribute"></a><span data-ttu-id="fd488-104">Broadcast-Attribut</span><span class="sxs-lookup"><span data-stu-id="fd488-104">broadcast attribute</span></span>

<span data-ttu-id="fd488-105">Das Schlüsselwort **\[ Broadcast \]** gibt an, dass Remote Prozedur Aufrufe an alle Server in einem lokalen Netzwerk gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd488-105">The keyword **\[broadcast\]** specifies that remote procedure calls be sent to all servers on a local network.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [broadcast [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="fd488-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd488-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd488-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="fd488-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fd488-108">Gibt eine Liste von 0 (null) oder mehr IDL-Attributen an, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd488-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="fd488-109">Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="fd488-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-110">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="fd488-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fd488-111">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="fd488-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-112">*Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="fd488-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fd488-113">Gibt zusätzliche Attribute an, die auf die Funktion angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fd488-113">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="fd488-114">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="fd488-114">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-115">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="fd488-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="fd488-116">Gibt den Rückgabetyp der Funktion an.</span><span class="sxs-lookup"><span data-stu-id="fd488-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-117">*function-name*</span><span class="sxs-lookup"><span data-stu-id="fd488-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fd488-118">Gibt den Namen der Funktion an, auf die das **\[ Broadcast \]** -Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd488-118">Specifies the name of the function to which the **\[broadcast\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-119">*params*</span><span class="sxs-lookup"><span data-stu-id="fd488-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="fd488-120">Funktionsparameter Liste.</span><span class="sxs-lookup"><span data-stu-id="fd488-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd488-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd488-121">Remarks</span></span>

<span data-ttu-id="fd488-122">Das **\[ Broadcast \]** -Schlüsselwort gibt an, dass die Routine immer an alle Server im Netzwerk übermittelt wird, anstatt Sie an einen bestimmten Server zu übermitteln. Der Client empfängt die Ausgabe der ersten Antwort, um erfolgreich zurückzukehren, während nachfolgende Antworten verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="fd488-122">The **\[broadcast\]** keyword specifies that the routine is always broadcasted to all the servers on the network, rather than being delivered to one particular server.The client receives output from the first reply to return successfully, while subsequent replies are discarded.</span></span>

<span data-ttu-id="fd488-123">Ein Vorgang mit dem **\[ Broadcast \]** -Attribut ist implizit ein [**\[ idempotenter \]**](idempotent.md) Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fd488-123">An operation with the **\[broadcast\]** attribute is implicitly an [**\[idempotent\]**](idempotent.md) operation.</span></span> <span data-ttu-id="fd488-124">Das **\[ Broadcast \]** -Attribut gibt jedoch zusätzliche Eigenschaften an, die Funktionen mit dem **\[ idempotenten \]** Attribut nicht haben.</span><span class="sxs-lookup"><span data-stu-id="fd488-124">However, the **\[broadcast\]** attribute specifies additional properties that functions with the **\[idempotent\]** attribute don't have.</span></span> <span data-ttu-id="fd488-125">Funktionen, die das **\[ Broadcast \]** -Attribut verwenden, geben insbesondere an, dass die Routine mehrmals als Ergebnis eines Remote Prozedur Aufrufs aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd488-125">Specifically, functions using the **\[broadcast\]** attribute specify that the routine can be called multiple times as the result of one remote procedure call.</span></span> <span data-ttu-id="fd488-126">Gleichzeitig können Sie an mehrere Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd488-126">At the same time, they can be sent to multiple servers.</span></span> <span data-ttu-id="fd488-127">Dies unterscheidet sich vom **\[ idempotenten \]** Attribut, das nur angibt, dass ein Aufruf wiederholt werden kann, wenn er nicht abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fd488-127">This is different from the **\[idempotent\]** attribute, which specifies only that a call can be retried if it is not completed.</span></span>

<span data-ttu-id="fd488-128">Wenn eine Remote Prozedur ihren-Aufrufe an alle Hosts in einem lokalen Netzwerk überträgt, muss Sie entweder die [**ncadg \_ -IP- \_ UDP-**](ncadg-ip-udp.md) oder die [**ncadg- \_ IPX**](ncadg-ipx.md) -Protokoll Sequenz verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd488-128">If a remote procedure broadcasts its call to all hosts on a local network, it must use either the [**ncadg\_ip\_udp**](ncadg-ip-udp.md) or the [**ncadg\_ipx**](ncadg-ipx.md) protocol sequence.</span></span> <span data-ttu-id="fd488-129">Beachten Sie, dass die Größe eines **\[ Broadcast \]** Pakets durch den verwendeten Datagramm-Dienst bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="fd488-129">Note that the size of a **\[broadcast\]** packet is determined by the datagram service in use.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd488-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd488-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd488-131">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="fd488-131">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="fd488-132">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="fd488-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="fd488-133">**auch**</span><span class="sxs-lookup"><span data-stu-id="fd488-133">**maybe**</span></span>](maybe.md)
</dt> <dt>

[<span data-ttu-id="fd488-134">**ncadg \_ -IP- \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="fd488-134">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="fd488-135">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="fd488-135">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> </dl>

 

 




