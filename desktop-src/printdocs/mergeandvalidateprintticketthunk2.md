---
description: Führt zwei Druck Tickets zusammen und gibt ein gültiges, brauchbares Druck Ticket zurück.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: MergeAndValidatePrintTicketThunk2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 4a21b9e505e39d64e8e0c696a3b8a6432a012d76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369047"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a><span data-ttu-id="dad96-103">MergeAndValidatePrintTicketThunk2-Funktion</span><span class="sxs-lookup"><span data-stu-id="dad96-103">MergeAndValidatePrintTicketThunk2 function</span></span>

<span data-ttu-id="dad96-104">\[Diese Funktion wird nicht unterstützt und wird in zukünftigen Versionen von Windows möglicherweise deaktiviert oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dad96-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="dad96-105">[**Ptmergeandvalidateprintticket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) bietet entsprechende Funktionen und sollte stattdessen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="dad96-105">[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="dad96-106">Führt zwei Druck Tickets zusammen und gibt ein gültiges, brauchbares Druck Ticket zurück.</span><span class="sxs-lookup"><span data-stu-id="dad96-106">Merges two print tickets and returns a valid, viable print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="dad96-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dad96-107">Syntax</span></span>


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="dad96-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dad96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dad96-109">*hprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dad96-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dad96-110">Ein Handle für einen geöffneten Druck ticketanbieter.</span><span class="sxs-lookup"><span data-stu-id="dad96-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="dad96-111">Dieses Handle wird von der [**bindptproviderthunk**](bindptproviderthunk.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dad96-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="dad96-112">*pbaseprintticket* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dad96-112">*pBasePrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dad96-113">Der Puffer, der die grundlegenden Druck Ticketdaten enthält, wie im [Druck Schema](./printschema.md)beschrieben, in XML ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="dad96-113">The buffer that contains the base print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="dad96-114">*baseprintticketlength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dad96-114">*basePrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dad96-115">Die Größe (in Bytes) des Puffers, auf den *pbaseprintticket* verweist.</span><span class="sxs-lookup"><span data-stu-id="dad96-115">The size, in bytes, of the buffer referenced by *pBasePrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="dad96-116">*pdelta-PrintTicket* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="dad96-116">*pDeltaPrintTicket* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dad96-117">Der Puffer, der das zu Merge Ende Druck Ticket enthält.</span><span class="sxs-lookup"><span data-stu-id="dad96-117">The buffer that contains the print ticket to merge.</span></span> <span data-ttu-id="dad96-118">Die Druck Ticketdaten werden in XML ausgedrückt, wie im [Print-Schema](./printschema.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dad96-118">The print ticket data is expressed in XML as described in the [Print Schema](./printschema.md).</span></span> <span data-ttu-id="dad96-119">Der Wert dieses Parameters kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="dad96-119">The value of this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dad96-120">*Delta printticketlength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dad96-120">*deltaPrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dad96-121">Die Größe (in Bytes) des Puffers, auf den *pdelta-PrintTicket* verweist.</span><span class="sxs-lookup"><span data-stu-id="dad96-121">The size, in bytes, of the buffer referenced by *pDeltaPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="dad96-122">*Bereich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dad96-122">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dad96-123">Der-Wert, der angibt, ob der Bereich von *pdelta-PrintTicket* und *ppvalidatedprintticket* eine einzelne Seite, ein gesamtes Dokument oder alle Dokumente im Druckauftrag ist.</span><span class="sxs-lookup"><span data-stu-id="dad96-123">The value that specifies whether the scope of *pDeltaPrintTicket* and *ppValidatedPrintTicket* is a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="dad96-124">Der Wert dieses Parameters muss ein Member der [**eprintticketscope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) -Enumeration sein, die als **DWORD** umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="dad96-124">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="dad96-125">*ppvalidatedprintticket* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dad96-125">*ppValidatedPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dad96-126">Die Adresse des Puffers, der das zusammengeführte und validierte Druck Ticket enthält.</span><span class="sxs-lookup"><span data-stu-id="dad96-126">The address of the buffer that contains the merged and validated print ticket.</span></span> <span data-ttu-id="dad96-127">Diese Funktion Ruft die [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) -Funktion auf, um diesen Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="dad96-127">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="dad96-128">Wenn der Puffer nicht mehr benötigt wird, muss der Aufrufer ihn durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.</span><span class="sxs-lookup"><span data-stu-id="dad96-128">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="dad96-129">*pvalidatedprintticketlength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dad96-129">*pValidatedPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dad96-130">Die Größe des von *ppvalidatedprintticket* referenzierten Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="dad96-130">The size, in bytes, of the buffer referenced by *ppValidatedPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="dad96-131">*pbstrauerrormessage* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="dad96-131">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dad96-132">Ein Zeiger auf eine Zeichenfolge, die angibt, was, wenn überhaupt, für das Druck Ticket in *pbaseprintticket* oder *pdelta Info Ticket* ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="dad96-132">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pBasePrintTicket* or *pDeltaPrintTicket*.</span></span> <span data-ttu-id="dad96-133">Wenn beide gültig sind, ist dieser Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="dad96-133">If they are both valid, this value is **NULL**.</span></span> <span data-ttu-id="dad96-134">Wenn *pbstrauerrormessage* bei Rückgabe der Funktion nicht **null** ist, muss der Aufrufer die Zeichenfolge mit [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)freigeben.</span><span class="sxs-lookup"><span data-stu-id="dad96-134">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dad96-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dad96-135">Return value</span></span>

<span data-ttu-id="dad96-136">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück; andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dad96-136">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="dad96-137">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="dad96-137">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dad96-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dad96-138">Requirements</span></span>



| <span data-ttu-id="dad96-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dad96-139">Requirement</span></span> | <span data-ttu-id="dad96-140">Wert</span><span class="sxs-lookup"><span data-stu-id="dad96-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dad96-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dad96-141">Minimum supported client</span></span><br/> | <span data-ttu-id="dad96-142">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dad96-142">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dad96-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dad96-143">Minimum supported server</span></span><br/> | <span data-ttu-id="dad96-144">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dad96-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dad96-145">DLL</span><span class="sxs-lookup"><span data-stu-id="dad96-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dad96-146"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dad96-146"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dad96-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dad96-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad96-148">Druck Schema</span><span class="sxs-lookup"><span data-stu-id="dad96-148">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="dad96-149">**Ptmergeandvalidateprintticket**</span><span class="sxs-lookup"><span data-stu-id="dad96-149">**PTMergeAndValidatePrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[<span data-ttu-id="dad96-150">Drucken</span><span class="sxs-lookup"><span data-stu-id="dad96-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="dad96-151">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="dad96-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

