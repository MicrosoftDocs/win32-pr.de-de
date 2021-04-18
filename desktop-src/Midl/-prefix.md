---
title: /Prefix-Schalter
description: Der/prefix-Schalter leitet den mittelmäßigen Compiler zum Hinzufügen von Präfix Zeichenfolgen zu den Namen der Client-und/oder serverstubroutinen.
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- /Prefix-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516353"
---
# <a name="prefix-switch"></a><span data-ttu-id="d22d4-104">/Prefix-Schalter</span><span class="sxs-lookup"><span data-stu-id="d22d4-104">/prefix switch</span></span>

<span data-ttu-id="d22d4-105">Der **/prefix** -Schalter leitet den mittelmäßigen Compiler zum Hinzufügen von Präfix Zeichenfolgen zu den Namen der Client-und/oder serverstubroutinen.</span><span class="sxs-lookup"><span data-stu-id="d22d4-105">The **/prefix** switch directs the MIDL compiler to add prefix strings to the client and/or server stub routine names.</span></span> <span data-ttu-id="d22d4-106">Dies kann verwendet werden, um zuzulassen, dass ein einzelnes Programm sowohl ein Client als auch ein Server derselben Schnittstelle ist, ohne dass die Namen von Client-und serverseitigen Routinen miteinander in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="d22d4-106">This can be used to allow a single program to be both a client and server of the same interface, without having the client- and server-side routine names conflict with each other.</span></span>

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a><span data-ttu-id="d22d4-107">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="d22d4-107">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span data-ttu-id="d22d4-108"><span id="client"></span><span id="CLIENT"></span>Client \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d22d4-108"><span id="client"></span><span id="CLIENT"></span>\*\*\*\*client\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d22d4-109">Wirkt sich nur auf die Namen der Clientstub-Routine aus.</span><span class="sxs-lookup"><span data-stu-id="d22d4-109">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span data-ttu-id="d22d4-110"><span id="cstub"></span><span id="CSTUB"></span>cstub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d22d4-110"><span id="cstub"></span><span id="CSTUB"></span>\*\*\*\*cstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d22d4-111">Identisch mit dem *Client*.</span><span class="sxs-lookup"><span data-stu-id="d22d4-111">Same as *client*.</span></span> <span data-ttu-id="d22d4-112">Wirkt sich nur auf die Namen der Clientstub-Routine aus.</span><span class="sxs-lookup"><span data-stu-id="d22d4-112">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="d22d4-113"><span id="server"></span><span id="SERVER"></span>Server \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d22d4-113"><span id="server"></span><span id="SERVER"></span>\*\*\*\*server\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d22d4-114">Wirkt sich nur auf die Routine Namen aus, die von der Server-stubroutine aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d22d4-114">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span data-ttu-id="d22d4-115"><span id="sstub"></span><span id="SSTUB"></span>sstub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d22d4-115"><span id="sstub"></span><span id="SSTUB"></span>\*\*\*\*sstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d22d4-116">Identisch mit dem *Server*.</span><span class="sxs-lookup"><span data-stu-id="d22d4-116">Same as *server*.</span></span> <span data-ttu-id="d22d4-117">Wirkt sich nur auf die Routine Namen aus, die von der Server-stubroutine aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d22d4-117">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="d22d4-118"><span id="switch"></span><span id="SWITCH"></span>Switch \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d22d4-118"><span id="switch"></span><span id="SWITCH"></span>\*\*\*\*switch\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d22d4-119">Hat Auswirkungen auf einen zusätzlichen Prototyp, der der Header Datei hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d22d4-119">Affects an extra prototype added to the header file.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="d22d4-120"><span id="all"></span><span id="ALL"></span>Alle \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d22d4-120"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d22d4-121">Wirkt sich auf die Namen von Client-und Server-Stub-Routine aus</span><span class="sxs-lookup"><span data-stu-id="d22d4-121">Affects both the client and server stub routine names.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d22d4-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d22d4-122">Remarks</span></span>

<span data-ttu-id="d22d4-123">Wenn sich das Präfix für die Client seitigen Routinen vom Präfix für die serverseitigen Routinen unterscheidet, enthält die generierte Header Datei sowohl Client seitige Routine Prototypen als auch serverseitige Routine Prototypen.</span><span class="sxs-lookup"><span data-stu-id="d22d4-123">If the prefix for the client-side routines is different from the prefix for the server-side routines, the generated header file will have both client-side routine prototypes and server-side routine prototypes.</span></span>

<span data-ttu-id="d22d4-124">Der **/prefix** -Schalter ist nützlich, wenn eine einzelne Header Datei mit stubläufen aus mehreren Ausführungen des Mittelwert Compilers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d22d4-124">The **/prefix** switch is useful when a single header file will be used with stubs from multiple runs of the MIDL compiler.</span></span> <span data-ttu-id="d22d4-125">Dies erzwingt zusätzliche Routine Prototypen in der Header Datei.</span><span class="sxs-lookup"><span data-stu-id="d22d4-125">This forces additional routine prototypes in the header file.</span></span>

<span data-ttu-id="d22d4-126">In allen Fällen überschreiben die Client-, Server-und switchpräfixe ein all-Präfix.</span><span class="sxs-lookup"><span data-stu-id="d22d4-126">In all cases, the client, server, and switch prefixes will override an all prefix.</span></span>

## <a name="examples"></a><span data-ttu-id="d22d4-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d22d4-127">Examples</span></span>

<span data-ttu-id="d22d4-128">**Mittel l/Prefix Client "c \_ " Server "s \_ "**</span><span class="sxs-lookup"><span data-stu-id="d22d4-128">**midl /prefix client "c\_" server "s\_"**</span></span>

<span data-ttu-id="d22d4-129">**Mittel l/Prefix alle "moo \_ "**</span><span class="sxs-lookup"><span data-stu-id="d22d4-129">**midl /prefix all "moo\_"**</span></span>

<span data-ttu-id="d22d4-130">**Mittel l/Prefix Client "Bark \_ "**</span><span class="sxs-lookup"><span data-stu-id="d22d4-130">**midl /prefix client "bark\_"**</span></span>

## <a name="see-also"></a><span data-ttu-id="d22d4-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d22d4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d22d4-132">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="d22d4-132">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




