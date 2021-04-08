---
title: XTYP_ADVSTART Transaktion (Ddeml. h)
description: Ein Client verwendet die xtipp- \_ advstart-Transaktion, um eine Empfehlung-Schleife mit einem Server einzurichten.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- XTYP_ADVSTART Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852351ad902a0552ee012d6c1e5c4d61501e6e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741857"
---
# <a name="xtyp_advstart-transaction"></a><span data-ttu-id="c58a6-104">Xttyp- \_ advstart-Transaktion</span><span class="sxs-lookup"><span data-stu-id="c58a6-104">XTYP\_ADVSTART transaction</span></span>

<span data-ttu-id="c58a6-105">Ein Client verwendet die **xtipp- \_ advstart** -Transaktion, um eine Empfehlung-Schleife mit einem Server einzurichten.</span><span class="sxs-lookup"><span data-stu-id="c58a6-105">A client uses the **XTYP\_ADVSTART** transaction to establish an advise loop with a server.</span></span> <span data-ttu-id="c58a6-106">Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion ( [*ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, wenn ein Client **xType \_ advstart** als *wType* -Parameter der [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="c58a6-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTART** as the *wType* parameter of the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a><span data-ttu-id="c58a6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c58a6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c58a6-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="c58a6-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="c58a6-109">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="c58a6-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="c58a6-110">*UF*</span><span class="sxs-lookup"><span data-stu-id="c58a6-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="c58a6-111">Das vom Client angeforderte Datenformat.</span><span class="sxs-lookup"><span data-stu-id="c58a6-111">The data format requested by the client.</span></span>

</dd> <dt>

<span data-ttu-id="c58a6-112">*has*</span><span class="sxs-lookup"><span data-stu-id="c58a6-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="c58a6-113">Ein Handle für die Konversation.</span><span class="sxs-lookup"><span data-stu-id="c58a6-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="c58a6-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="c58a6-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="c58a6-115">Ein Handle für den Themen Namen.</span><span class="sxs-lookup"><span data-stu-id="c58a6-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="c58a6-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="c58a6-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="c58a6-117">Ein Handle für den Elementnamen.</span><span class="sxs-lookup"><span data-stu-id="c58a6-117">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="c58a6-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="c58a6-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="c58a6-119">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c58a6-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c58a6-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="c58a6-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="c58a6-121">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c58a6-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c58a6-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="c58a6-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="c58a6-123">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c58a6-123">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c58a6-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c58a6-124">Return value</span></span>

<span data-ttu-id="c58a6-125">Eine Server Rückruffunktion sollte **true** zurückgeben, um eine Empfehlung-Schleife für den angegebenen Themen Namen und das Element namens paar zuzulassen, oder **false** , um die Empfehlung-Schleife abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="c58a6-125">A server callback function should return **TRUE** to allow an advise loop on the specified topic name and item name pair, or **FALSE** to deny the advise loop.</span></span> <span data-ttu-id="c58a6-126">Wenn die Rückruffunktion **true** zurückgibt, bewirkt jeder nachfolgende Aufruf der [**ddepostadvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) -Funktion durch den Server für denselben Themen Namen und dasselbe Elementnamen Paar, dass das System [**xD \_ advreq**](xtyp-advreq.md) -Transaktionen an den Server sendet.</span><span class="sxs-lookup"><span data-stu-id="c58a6-126">If the callback function returns **TRUE**, any subsequent calls to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function by the server on the same topic name and item name pair causes the system to send [**XTYP\_ADVREQ**](xtyp-advreq.md) transactions to the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="c58a6-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c58a6-127">Remarks</span></span>

<span data-ttu-id="c58a6-128">Wenn ein Client eine Empfehlung-Schleife für einen Themen Namen, Elementnamen und ein Datenformat für eine bereits erstellte Empfehlung-Schleife anfordert, wird von der dynamischer Datenaustausch Management Library (Ddeml) keine doppelte Empfehlung-Schleife erstellt, sondern die Empfehlung-Schleifen-Flags (**xtypf \_ ackreq** und **xtypf \_ NODATA**) so geändert, dass Sie mit der aktuellen Anforderung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c58a6-128">If a client requests an advise loop on a topic name, item name, and data format for an advise loop that is already established, the Dynamic Data Exchange Management Library (DDEML) does not create a duplicate advise loop but instead alters the advise loop flags (**XTYPF\_ACKREQ** and **XTYPF\_NODATA**) to match the latest request.</span></span>

<span data-ttu-id="c58a6-129">Diese Transaktion wird gefiltert, wenn von der Serveranwendung das Flag " **CBF \_ Fail \_** " in der Funktion " [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) " angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c58a6-129">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c58a6-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c58a6-130">Requirements</span></span>



| <span data-ttu-id="c58a6-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c58a6-131">Requirement</span></span> | <span data-ttu-id="c58a6-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c58a6-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c58a6-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c58a6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c58a6-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c58a6-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c58a6-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c58a6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c58a6-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c58a6-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c58a6-137">Header</span><span class="sxs-lookup"><span data-stu-id="c58a6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c58a6-138"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c58a6-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c58a6-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c58a6-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="c58a6-140">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c58a6-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c58a6-141">**DDE clienttransaction**</span><span class="sxs-lookup"><span data-stu-id="c58a6-141">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="c58a6-142">**DDEInitialize**</span><span class="sxs-lookup"><span data-stu-id="c58a6-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="c58a6-143">**DDE postadvise**</span><span class="sxs-lookup"><span data-stu-id="c58a6-143">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="c58a6-144">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c58a6-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c58a6-145">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c58a6-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

