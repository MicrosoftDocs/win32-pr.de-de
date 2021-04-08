---
title: XTYP_REQUEST Transaktion (Ddeml. h)
description: Ein Client verwendet die XYP- \_ Anforderungs Transaktion, um Daten von einem Server anzufordern. Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion (DDE Callback) empfängt diese Transaktion, wenn ein Client eine \_ xType-Anforderung in der DDE clienttransaction-Funktion angibt.
ms.assetid: e776b995-6a64-4398-9e29-c151f3ef4c1d
keywords:
- XTYP_REQUEST Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_REQUEST
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e902c1525a8837f6ace6ef9bceb0607a608cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740328"
---
# <a name="xtyp_request-transaction"></a><span data-ttu-id="ad8e4-105">XYP- \_ Anforderungs Transaktion</span><span class="sxs-lookup"><span data-stu-id="ad8e4-105">XTYP\_REQUEST transaction</span></span>

<span data-ttu-id="ad8e4-106">Ein Client verwendet die **XYP- \_ Anforderungs** Transaktion, um Daten von einem Server anzufordern.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-106">A client uses the **XTYP\_REQUEST** transaction to request data from a server.</span></span> <span data-ttu-id="ad8e4-107">Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, wenn ein Client eine **xType- \_ Anforderung** in der [**DDE clienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_REQUEST** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYP_REQUEST            (0x00B0 | XCLASS_DATA          )
```



## <a name="parameters"></a><span data-ttu-id="ad8e4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad8e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad8e4-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="ad8e4-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="ad8e4-110">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="ad8e4-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="ad8e4-111">*UF*</span><span class="sxs-lookup"><span data-stu-id="ad8e4-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="ad8e4-112">Das Format, in dem der Serverdaten an den Client übermitteln soll.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-112">The format in which the server should submit data to the client.</span></span>

</dd> <dt>

<span data-ttu-id="ad8e4-113">*has*</span><span class="sxs-lookup"><span data-stu-id="ad8e4-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="ad8e4-114">Ein Handle für die Konversation.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="ad8e4-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="ad8e4-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="ad8e4-116">Ein Handle für den Themen Namen.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="ad8e4-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="ad8e4-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="ad8e4-118">Ein Handle für den Elementnamen.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="ad8e4-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="ad8e4-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="ad8e4-120">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad8e4-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="ad8e4-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="ad8e4-122">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad8e4-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="ad8e4-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="ad8e4-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad8e4-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad8e4-125">Return value</span></span>

<span data-ttu-id="ad8e4-126">Der Server sollte die [**ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) -Funktion aufrufen, um ein Daten Handle zu erstellen, das die Daten identifiziert und dann das Handle zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-126">The server should call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the data and then return the handle.</span></span> <span data-ttu-id="ad8e4-127">Der Server sollte **null** zurückgeben, wenn die Transaktion nicht abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-127">The server should return **NULL** if it is unable to complete the transaction.</span></span> <span data-ttu-id="ad8e4-128">Wenn der Server **null** zurückgibt, empfängt der Client ein DDE-Flag mit der Bezeichnung "DDE" \_ .</span><span class="sxs-lookup"><span data-stu-id="ad8e4-128">If the server returns **NULL**, the client will receive a DDE\_FNOTPROCESSED flag.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad8e4-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad8e4-129">Remarks</span></span>

<span data-ttu-id="ad8e4-130">Diese Transaktion wird gefiltert, wenn die Serveranwendung das Flag " **CBF \_ Fail \_ Requests** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-130">This transaction is filtered if the server application specified the **CBF\_FAIL\_REQUESTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="ad8e4-131">Wenn die Reaktion auf diese Transaktion lange Verarbeitung erfordert, kann der Server den Rückgabecode des CBR-Blocks zurückgeben, \_ um zukünftige Transaktionen für die aktuelle Konversation anzuhalten und die Transaktion dann asynchron zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-131">If responding to this transaction requires lengthy processing, the server can return the CBR\_BLOCK return code to suspend future transactions on the current conversation and then process the transaction asynchronously.</span></span> <span data-ttu-id="ad8e4-132">Nachdem der Server beendet wurde und die Daten an den Client übergeben werden können, kann der Server die [**DDE enablecallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) -Funktion zum Fortsetzen der Konversation aufruft.</span><span class="sxs-lookup"><span data-stu-id="ad8e4-132">When the server has finished and the data is ready to pass to the client, the server can call the [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) function to resume the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad8e4-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad8e4-133">Requirements</span></span>



| <span data-ttu-id="ad8e4-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad8e4-134">Requirement</span></span> | <span data-ttu-id="ad8e4-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ad8e4-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad8e4-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad8e4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ad8e4-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad8e4-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ad8e4-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad8e4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ad8e4-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad8e4-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="ad8e4-140">Header</span><span class="sxs-lookup"><span data-stu-id="ad8e4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad8e4-141"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad8e4-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad8e4-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad8e4-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad8e4-143">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ad8e4-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ad8e4-144">**DDE clienttransaction**</span><span class="sxs-lookup"><span data-stu-id="ad8e4-144">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="ad8e4-145">**Ddecreatedatahandle**</span><span class="sxs-lookup"><span data-stu-id="ad8e4-145">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="ad8e4-146">**DDE enablecallback**</span><span class="sxs-lookup"><span data-stu-id="ad8e4-146">**DdeEnableCallback**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)
</dt> <dt>

[<span data-ttu-id="ad8e4-147">**DDEInitialize**</span><span class="sxs-lookup"><span data-stu-id="ad8e4-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="ad8e4-148">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ad8e4-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ad8e4-149">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ad8e4-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

