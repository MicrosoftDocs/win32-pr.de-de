---
title: XTYP_POKE Transaktion (Ddeml. h)
description: Ein Client verwendet die XYP \_ Poke-Transaktion, um nicht angeforderte Daten an den Server zu senden. Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion (DDE Callback) empfängt diese Transaktion, wenn ein Client xType \_ poke in der DDE clienttransaction-Funktion angibt.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- XTYP_POKE Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e538f72b7a736ed9be5cf3e1d83e8729f42ef83d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949789"
---
# <a name="xtyp_poke-transaction"></a><span data-ttu-id="13b9f-105">XYP- \_ Poke-Transaktion</span><span class="sxs-lookup"><span data-stu-id="13b9f-105">XTYP\_POKE transaction</span></span>

<span data-ttu-id="13b9f-106">Ein Client verwendet die **XYP \_ Poke** -Transaktion, um nicht angeforderte Daten an den Server zu senden.</span><span class="sxs-lookup"><span data-stu-id="13b9f-106">A client uses the **XTYP\_POKE** transaction to send unsolicited data to the server.</span></span> <span data-ttu-id="13b9f-107">Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, wenn ein Client **xType \_ Poke** in der [**DDE clienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="13b9f-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_POKE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="13b9f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="13b9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13b9f-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="13b9f-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="13b9f-110">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="13b9f-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="13b9f-111">*UF*</span><span class="sxs-lookup"><span data-stu-id="13b9f-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="13b9f-112">Das Format der vom Server gesendeten Daten.</span><span class="sxs-lookup"><span data-stu-id="13b9f-112">The format of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="13b9f-113">*has*</span><span class="sxs-lookup"><span data-stu-id="13b9f-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="13b9f-114">Ein Handle für die Konversation.</span><span class="sxs-lookup"><span data-stu-id="13b9f-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="13b9f-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="13b9f-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="13b9f-116">Ein Handle für den Themen Namen.</span><span class="sxs-lookup"><span data-stu-id="13b9f-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="13b9f-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="13b9f-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="13b9f-118">Ein Handle für den Elementnamen.</span><span class="sxs-lookup"><span data-stu-id="13b9f-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="13b9f-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="13b9f-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="13b9f-120">Ein Handle für die Daten, die vom Client an den Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="13b9f-120">A handle to the data that the client is sending to the server.</span></span>

</dd> <dt>

<span data-ttu-id="13b9f-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="13b9f-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="13b9f-122">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="13b9f-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="13b9f-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="13b9f-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="13b9f-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="13b9f-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13b9f-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13b9f-125">Return value</span></span>

<span data-ttu-id="13b9f-126">Eine Server Rückruffunktion sollte das **DDE- \_ faktorflag** zurückgeben, wenn diese Transaktion verarbeitet wird, das **DDE \_ fbusy** -Flag, wenn es zu stark ausgelastet ist, um diese Transaktion zu verarbeiten, oder das **DDE \_ fnotverarbeitete** -Flag, wenn es diese Transaktion ablehnt.</span><span class="sxs-lookup"><span data-stu-id="13b9f-126">A server callback function should return the **DDE\_FACK** flag if it processes this transaction, the **DDE\_FBUSY** flag if it is too busy to process this transaction, or the **DDE\_FNOTPROCESSED** flag if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="13b9f-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13b9f-127">Remarks</span></span>

<span data-ttu-id="13b9f-128">Diese Transaktion wird gefiltert, wenn von der Serveranwendung das Flag " **CBF \_ Fail \_ Pokes** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="13b9f-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_POKES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="13b9f-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13b9f-129">Requirements</span></span>



| <span data-ttu-id="13b9f-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13b9f-130">Requirement</span></span> | <span data-ttu-id="13b9f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="13b9f-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13b9f-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13b9f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="13b9f-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13b9f-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="13b9f-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13b9f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="13b9f-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13b9f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="13b9f-136">Header</span><span class="sxs-lookup"><span data-stu-id="13b9f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="13b9f-137"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13b9f-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13b9f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13b9f-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="13b9f-139">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="13b9f-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="13b9f-140">**DDE clienttransaction**</span><span class="sxs-lookup"><span data-stu-id="13b9f-140">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="13b9f-141">**DDEInitialize**</span><span class="sxs-lookup"><span data-stu-id="13b9f-141">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="13b9f-142">**Licher**</span><span class="sxs-lookup"><span data-stu-id="13b9f-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="13b9f-143">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="13b9f-143">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

