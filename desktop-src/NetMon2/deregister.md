---
description: Die Funktion zum Aufheben der Aufhebung der Funktion gibt die Ressourcen frei, die zum Erstellen der Protokoll Eigenschaften Datenbank verwendet werden. Die Parser-DLL muss die deregipperimplementierung implementieren.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Deregiester-Rückruffunktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Deregister
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 9458ff74f29cd8eb7a75da0a3628a2dd1519ba43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215889"
---
# <a name="deregister-callback-function"></a><span data-ttu-id="195da-104">Deregiester-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="195da-104">Deregister callback function</span></span>

<span data-ttu-id="195da-105">Die **Funktion zum Aufheben** der Aufhebung der Funktion gibt die Ressourcen frei, die zum Erstellen der Protokoll [*Eigenschaften Datenbank*](p.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="195da-105">The **Deregister** export function frees the resources used to create the protocol [*property database*](p.md).</span></span> <span data-ttu-id="195da-106">Die Parser-DLL muss die **deregipperimplementierung** implementieren.</span><span class="sxs-lookup"><span data-stu-id="195da-106">The parser DLL must implement **Deregister**.</span></span>

## <a name="syntax"></a><span data-ttu-id="195da-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="195da-107">Syntax</span></span>


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="195da-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="195da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="195da-109">*hprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="195da-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="195da-110">Handle des Protokolls für eine bestimmte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="195da-110">Handle of the protocol for a specific database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="195da-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="195da-111">Return value</span></span>

<span data-ttu-id="195da-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="195da-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="195da-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="195da-113">Remarks</span></span>

<span data-ttu-id="195da-114">Netzwerkmonitor Ruft die **deregitenregistrierung** auf, nachdem alle Aufzeichnungs Informationen an die Parser-DLL übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="195da-114">Network Monitor calls **Deregister** after passing all the capture information to the parser DLL.</span></span> <span data-ttu-id="195da-115">Die Parser-DLL muss eine **deregiester** -Funktion für jedes Protokoll implementieren, das der Parser unterstützt.</span><span class="sxs-lookup"><span data-stu-id="195da-115">The parser DLL must implement a **Deregister** function for each protocol that the parser supports.</span></span>

<span data-ttu-id="195da-116">Beim Implementieren von **deregistern** muss die Parser-DLL die Funktion " [destroypropertydatabase](destroypropertydatabase.md) " aufrufen, um die [*Eigenschaften Daten Bank*](p.md) Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="195da-116">When implementing **Deregister**, the parser DLL must call the [DestroyPropertyDatabase](destroypropertydatabase.md) function to release the [*property database*](p.md) resources.</span></span>



| <span data-ttu-id="195da-117">Für Informationen zu</span><span class="sxs-lookup"><span data-stu-id="195da-117">For information on</span></span>                                        | <span data-ttu-id="195da-118">Siehe</span><span class="sxs-lookup"><span data-stu-id="195da-118">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="195da-119">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="195da-119">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="195da-120">Parser</span><span class="sxs-lookup"><span data-stu-id="195da-120">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="195da-121">Welche Einstiegspunkte in der Parser-DLL enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="195da-121">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="195da-122">Architektur der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="195da-122">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="195da-123">Zum Implementieren der **deregiester**  gehört ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="195da-123">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="195da-124">Implementieren von deregistern</span><span class="sxs-lookup"><span data-stu-id="195da-124">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="195da-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="195da-125">Requirements</span></span>



| <span data-ttu-id="195da-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="195da-126">Requirement</span></span> | <span data-ttu-id="195da-127">Wert</span><span class="sxs-lookup"><span data-stu-id="195da-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="195da-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="195da-128">Minimum supported client</span></span><br/> | <span data-ttu-id="195da-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="195da-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="195da-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="195da-130">Minimum supported server</span></span><br/> | <span data-ttu-id="195da-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="195da-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="195da-132">Header</span><span class="sxs-lookup"><span data-stu-id="195da-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="195da-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="195da-133"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="195da-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="195da-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="195da-135">Destroypropertydatabase</span><span class="sxs-lookup"><span data-stu-id="195da-135">DestroyPropertyDatabase</span></span>](destroypropertydatabase.md)
</dt> </dl>

 

 




