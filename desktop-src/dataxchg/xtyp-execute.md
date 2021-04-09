---
title: XTYP_EXECUTE Transaktion (Ddeml. h)
description: Ein Client verwendet die xtyp- \_ Execute-Transaktion, um eine Befehls Zeichenfolge an den Server zu senden. Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion (DDE Callback) empfängt diese Transaktion, wenn ein Client xType \_ Execute in der DDE clienttransaction-Funktion angibt.
ms.assetid: 6001eb7d-59c0-49ec-97ce-26132891188c
keywords:
- XTYP_EXECUTE Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_EXECUTE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff08bfa60d07f3b8333f1de808359f77984cbba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040863"
---
# <a name="xtyp_execute-transaction"></a><span data-ttu-id="0b767-105">XYP- \_ Ausführungs Transaktion</span><span class="sxs-lookup"><span data-stu-id="0b767-105">XTYP\_EXECUTE transaction</span></span>

<span data-ttu-id="0b767-106">Ein Client verwendet die **xtyp- \_ Execute** -Transaktion, um eine Befehls Zeichenfolge an den Server zu senden.</span><span class="sxs-lookup"><span data-stu-id="0b767-106">A client uses the **XTYP\_EXECUTE** transaction to send a command string to the server.</span></span> <span data-ttu-id="0b767-107">Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, wenn ein Client **xType \_ Execute** in der [**DDE clienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="0b767-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_EXECUTE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_EXECUTE            (0x0050 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="0b767-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b767-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b767-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="0b767-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="0b767-110">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="0b767-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="0b767-111">*UF*</span><span class="sxs-lookup"><span data-stu-id="0b767-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="0b767-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b767-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b767-113">*has*</span><span class="sxs-lookup"><span data-stu-id="0b767-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="0b767-114">Ein Handle für die Konversation.</span><span class="sxs-lookup"><span data-stu-id="0b767-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="0b767-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="0b767-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="0b767-116">Ein Handle für den Themen Namen.</span><span class="sxs-lookup"><span data-stu-id="0b767-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="0b767-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="0b767-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="0b767-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b767-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b767-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="0b767-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="0b767-120">Ein Handle für die Befehls Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0b767-120">A handle to the command string.</span></span>

</dd> <dt>

<span data-ttu-id="0b767-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="0b767-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="0b767-122">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b767-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b767-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="0b767-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="0b767-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b767-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b767-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b767-125">Return value</span></span>

<span data-ttu-id="0b767-126">Eine Server Rückruffunktion sollte **DDE \_ fakk** zurückgeben, wenn Sie diese Transaktion verarbeitet, **DDE \_ fausgelastet** , wenn Sie zu stark ausgelastet ist, um diese Transaktion zu verarbeiten, oder **DDE \_ fnotverarbeitete** , wenn Sie diese Transaktion ablehnt.</span><span class="sxs-lookup"><span data-stu-id="0b767-126">A server callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b767-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b767-127">Remarks</span></span>

<span data-ttu-id="0b767-128">Diese Transaktion wird gefiltert, wenn die Serveranwendung das Flag für die **CBF- \_ \_ Ausführung** in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="0b767-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_EXECUTES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="0b767-129">Eine Anwendung muss das Daten handle freigeben, das während dieser Transaktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="0b767-129">An application must free the data handle obtained during this transaction.</span></span> <span data-ttu-id="0b767-130">Eine Anwendung muss jedoch die dem Daten Handle zugeordnete Befehls Zeichenfolge kopieren, wenn die Anwendung die Zeichenfolge verarbeiten muss, nachdem die Rückruffunktion zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="0b767-130">An application must, however, copy the command string associated with the data handle if the application must process the string after the callback function returns.</span></span> <span data-ttu-id="0b767-131">Eine Anwendung kann die [**DDE GetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) -Funktion verwenden, um die Daten zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="0b767-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

<span data-ttu-id="0b767-132">Da die meisten Client Anwendungen erwarten, dass eine Serveranwendung eine **XYP- \_ Execute** -Transaktion synchron ausführt, sollte ein Server versuchen, die gesamte Verarbeitung der **Xder- \_ Execute** -Transaktion entweder aus der DDE-Rückruffunktion oder durch die Rückgabe des **CBR- \_ Block** Rückgabecodes auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0b767-132">Because most client applications expect a server application to perform an **XTYP\_EXECUTE** transaction synchronously, a server should attempt to perform all processing of the **XTYP\_EXECUTE** transaction either from within the DDE callback function or by returning the **CBR\_BLOCK** return code.</span></span> <span data-ttu-id="0b767-133">Wenn der *hdata* -Parameter ein Befehl ist, der den Server anweist, zu beenden, sollte der Server dies nach der Verarbeitung der **xD- \_ Ausführungs** Transaktion tun.</span><span class="sxs-lookup"><span data-stu-id="0b767-133">If the *hdata* parameter is a command that instructs the server to terminate, the server should do so after processing the **XTYP\_EXECUTE** transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b767-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b767-134">Requirements</span></span>



| <span data-ttu-id="0b767-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b767-135">Requirement</span></span> | <span data-ttu-id="0b767-136">Wert</span><span class="sxs-lookup"><span data-stu-id="0b767-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b767-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b767-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0b767-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b767-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0b767-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b767-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0b767-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b767-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="0b767-141">Header</span><span class="sxs-lookup"><span data-stu-id="0b767-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b767-142"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b767-142"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b767-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b767-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="0b767-144">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0b767-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0b767-145">**DDE clienttransaction**</span><span class="sxs-lookup"><span data-stu-id="0b767-145">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="0b767-146">**DDE GetData**</span><span class="sxs-lookup"><span data-stu-id="0b767-146">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="0b767-147">**DDEInitialize**</span><span class="sxs-lookup"><span data-stu-id="0b767-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="0b767-148">**Licher**</span><span class="sxs-lookup"><span data-stu-id="0b767-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0b767-149">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b767-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

