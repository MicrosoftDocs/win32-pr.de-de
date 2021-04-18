---
title: XTYP_ADVSTOP Transaktion (Ddeml. h)
description: Ein Client verwendet die xtipp- \_ advend-Transaktion, um eine Empfehlung-Schleife mit einem Server zu beenden. Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion (DDE Callback) empfängt diese Transaktion, wenn ein Client xType \_ advstopps in der DDE clienttransaction-Funktion angibt.
ms.assetid: 67dfa463-6a44-43a5-93be-a39c19c87c1c
keywords:
- XTYP_ADVSTOP Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_ADVSTOP
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61292683377cd6c7243c3e41c5dbd9332a671163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338547"
---
# <a name="xtyp_advstop-transaction"></a><span data-ttu-id="29e34-105">Xtipp- \_ advendtransaktion</span><span class="sxs-lookup"><span data-stu-id="29e34-105">XTYP\_ADVSTOP transaction</span></span>

<span data-ttu-id="29e34-106">Ein Client verwendet die **xtipp- \_ advend** -Transaktion, um eine Empfehlung-Schleife mit einem Server zu beenden.</span><span class="sxs-lookup"><span data-stu-id="29e34-106">A client uses the **XTYP\_ADVSTOP** transaction to end an advise loop with a server.</span></span> <span data-ttu-id="29e34-107">Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, wenn ein Client **xType \_ advstopps** in der [**DDE clienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="29e34-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTOP** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_ADVSTOP            (0x0040 | XCLASS_NOTIFICATION)
```



## <a name="parameters"></a><span data-ttu-id="29e34-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="29e34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29e34-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="29e34-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="29e34-110">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="29e34-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="29e34-111">*UF*</span><span class="sxs-lookup"><span data-stu-id="29e34-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="29e34-112">Das Datenformat, das der zu Beendigungs enden Empfehlung-Schleife zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="29e34-112">The data format associated with the advise loop being ended.</span></span>

</dd> <dt>

<span data-ttu-id="29e34-113">*has*</span><span class="sxs-lookup"><span data-stu-id="29e34-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="29e34-114">Ein Handle für die Konversation.</span><span class="sxs-lookup"><span data-stu-id="29e34-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="29e34-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="29e34-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="29e34-116">Ein Handle für den Themen Namen.</span><span class="sxs-lookup"><span data-stu-id="29e34-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="29e34-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="29e34-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="29e34-118">Ein Handle für den Elementnamen.</span><span class="sxs-lookup"><span data-stu-id="29e34-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="29e34-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="29e34-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="29e34-120">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="29e34-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="29e34-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="29e34-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="29e34-122">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="29e34-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="29e34-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="29e34-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="29e34-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="29e34-124">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29e34-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29e34-125">Remarks</span></span>

<span data-ttu-id="29e34-126">Diese Transaktion wird gefiltert, wenn von der Serveranwendung das Flag " **CBF \_ Fail \_** " in der Funktion " [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) " angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="29e34-126">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="29e34-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29e34-127">Requirements</span></span>



| <span data-ttu-id="29e34-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29e34-128">Requirement</span></span> | <span data-ttu-id="29e34-129">Wert</span><span class="sxs-lookup"><span data-stu-id="29e34-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29e34-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29e34-130">Minimum supported client</span></span><br/> | <span data-ttu-id="29e34-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29e34-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="29e34-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29e34-132">Minimum supported server</span></span><br/> | <span data-ttu-id="29e34-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29e34-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="29e34-134">Header</span><span class="sxs-lookup"><span data-stu-id="29e34-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="29e34-135"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29e34-135"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29e34-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29e34-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="29e34-137">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="29e34-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="29e34-138">**DDE clienttransaction**</span><span class="sxs-lookup"><span data-stu-id="29e34-138">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="29e34-139">**DDEInitialize**</span><span class="sxs-lookup"><span data-stu-id="29e34-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="29e34-140">**DDE postadvise**</span><span class="sxs-lookup"><span data-stu-id="29e34-140">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="29e34-141">**Licher**</span><span class="sxs-lookup"><span data-stu-id="29e34-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="29e34-142">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="29e34-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

