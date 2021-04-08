---
title: XTYP_DISCONNECT Transaktion (Ddeml. h)
description: Die DDE Dynamischer Datenaustausch-Rückruffunktion (DDE Callback) einer Anwendung empfängt die XYP \_ Disconnect-Transaktion, wenn der Partner der Anwendung in einer Konversation die DDE Disconnect-Funktion verwendet, um die Konversation zu beenden.
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- XTYP_DISCONNECT Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e73bc0446989ac572a27f394e594924573711d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740329"
---
# <a name="xtyp_disconnect-transaction"></a><span data-ttu-id="43a38-104">XYP- \_ Disconnect-Transaktion</span><span class="sxs-lookup"><span data-stu-id="43a38-104">XTYP\_DISCONNECT transaction</span></span>

<span data-ttu-id="43a38-105">Die DDE Dynamischer Datenaustausch-Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) einer Anwendung empfängt die **XYP \_ Disconnect** -Transaktion, wenn der Partner der Anwendung in einer Konversation die [**DDE Disconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) -Funktion verwendet, um die Konversation zu beenden.</span><span class="sxs-lookup"><span data-stu-id="43a38-105">An application's Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_DISCONNECT** transaction when the application's partner in a conversation uses the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function to terminate the conversation.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="43a38-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43a38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a38-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="43a38-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="43a38-108">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="43a38-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="43a38-109">*UF*</span><span class="sxs-lookup"><span data-stu-id="43a38-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="43a38-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="43a38-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="43a38-111">*has*</span><span class="sxs-lookup"><span data-stu-id="43a38-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="43a38-112">Ein Handle für die Beendigung der Konversation.</span><span class="sxs-lookup"><span data-stu-id="43a38-112">A handle to that the conversation was terminated.</span></span>

</dd> <dt>

<span data-ttu-id="43a38-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="43a38-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="43a38-114">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="43a38-114">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="43a38-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="43a38-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="43a38-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="43a38-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="43a38-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="43a38-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="43a38-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="43a38-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="43a38-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="43a38-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="43a38-120">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="43a38-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="43a38-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="43a38-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="43a38-122">Gibt an, ob es sich bei den Partnern in der Konversation um dieselbe Anwendungs Instanz handelt.</span><span class="sxs-lookup"><span data-stu-id="43a38-122">Specifies whether the partners in the conversation are the same application instance.</span></span> <span data-ttu-id="43a38-123">Wenn dieser Parameter 1 ist, handelt es sich bei den Partnern um dieselbe Instanz.</span><span class="sxs-lookup"><span data-stu-id="43a38-123">If this parameter is 1, the partners are the same instance.</span></span> <span data-ttu-id="43a38-124">Wenn dieser Parameter 0 ist, sind die Partner unterschiedliche Instanzen.</span><span class="sxs-lookup"><span data-stu-id="43a38-124">If this parameter is 0, the partners are different instances.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43a38-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43a38-125">Remarks</span></span>

<span data-ttu-id="43a38-126">Diese Transaktion wird gefiltert, wenn die Anwendung das Flag " **CBF \_ Skip \_ Disconnects** " in der Funktion " [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) " angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="43a38-126">This transaction is filtered if the application specified the **CBF\_SKIP\_DISCONNECTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="43a38-127">Die Anwendung kann den Status der beendeten Konversation abrufen, indem die [**ddequeryperformanfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) -Funktion aufgerufen wird, während diese Transaktion verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="43a38-127">The application can obtain the status of the terminated conversation by calling the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function while processing this transaction.</span></span> <span data-ttu-id="43a38-128">Das Konversations Handle wird ungültig, nachdem die Rückruffunktion zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="43a38-128">The conversation handle becomes invalid after the callback function returns.</span></span>

<span data-ttu-id="43a38-129">Der Transaktionstyp kann von einer Anwendung nicht blockiert werden. der Rückgabecode des **CBR- \_ Blocks** wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="43a38-129">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a38-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43a38-130">Requirements</span></span>



| <span data-ttu-id="43a38-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43a38-131">Requirement</span></span> | <span data-ttu-id="43a38-132">Wert</span><span class="sxs-lookup"><span data-stu-id="43a38-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a38-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43a38-133">Minimum supported client</span></span><br/> | <span data-ttu-id="43a38-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43a38-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="43a38-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43a38-135">Minimum supported server</span></span><br/> | <span data-ttu-id="43a38-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43a38-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="43a38-137">Header</span><span class="sxs-lookup"><span data-stu-id="43a38-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="43a38-138"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43a38-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43a38-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43a38-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="43a38-140">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="43a38-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="43a38-141">**DDE Disconnect**</span><span class="sxs-lookup"><span data-stu-id="43a38-141">**DdeDisconnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[<span data-ttu-id="43a38-142">**DDEInitialize**</span><span class="sxs-lookup"><span data-stu-id="43a38-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="43a38-143">**Dabqueryüberzeugungs Info**</span><span class="sxs-lookup"><span data-stu-id="43a38-143">**DdeQueryConvInfo**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

<span data-ttu-id="43a38-144">**Licher**</span><span class="sxs-lookup"><span data-stu-id="43a38-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="43a38-145">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43a38-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

