---
description: Konvertiert eine DEVMODE-Struktur in ein Druck Ticket.
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: ConvertDevModeToPrintTicketThunk2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertDevModeToPrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: f13d597a11a4d6cfd1ad6f5d70b3a386560f5106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358872"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a><span data-ttu-id="a0986-103">ConvertDevModeToPrintTicketThunk2-Funktion</span><span class="sxs-lookup"><span data-stu-id="a0986-103">ConvertDevModeToPrintTicketThunk2 function</span></span>

<span data-ttu-id="a0986-104">\[Diese Funktion wird nicht unterstützt und wird in zukünftigen Versionen von Windows möglicherweise deaktiviert oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a0986-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="a0986-105">[**Ptconvertdevmodetoprintticket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) bietet gleichwertige Funktionen und sollte stattdessen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="a0986-105">[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="a0986-106">Konvertiert eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur in ein Druck Ticket.</span><span class="sxs-lookup"><span data-stu-id="a0986-106">Converts a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to a print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0986-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0986-107">Syntax</span></span>


```C++
HRESULT ConvertDevModeToPrintTicketThunk2(
  _In_  HPTPROVIDER hProvider,
  _In_  BYTE        *pDevmode,
  _In_  ULONG       cbSize,
  _In_  DWORD       scope,
  _Out_ BYTE        **ppPrintTicket,
  _Out_ INT         *pcbPrintTicketLength
);
```



## <a name="parameters"></a><span data-ttu-id="a0986-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0986-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0986-109">*hprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0986-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0986-110">Ein Handle für einen geöffneten Druck ticketanbieter.</span><span class="sxs-lookup"><span data-stu-id="a0986-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="a0986-111">Dieses Handle wird von der [**bindptproviderthunk**](bindptproviderthunk.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a0986-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a0986-112">*pdevmode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0986-112">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0986-113">Ein Zeiger auf den zu konvertierenden [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Typ.</span><span class="sxs-lookup"><span data-stu-id="a0986-113">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to convert.</span></span>

</dd> <dt>

<span data-ttu-id="a0986-114">*CBSIZE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0986-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0986-115">Die Größe (in Bytes) des [**DEVMODE-Ausdrucks**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , der im *pdevmode-Modus* übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a0986-115">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="a0986-116">*Bereich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0986-116">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0986-117">Ein-Wert, der den Bereich von *ppprintticket* angibt.</span><span class="sxs-lookup"><span data-stu-id="a0986-117">A value that specifies the scope of *ppPrintTicket*.</span></span> <span data-ttu-id="a0986-118">Dieser Wert kann eine einzelne Seite, ein gesamtes Dokument oder alle Dokumente im Druckauftrag angeben.</span><span class="sxs-lookup"><span data-stu-id="a0986-118">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="a0986-119">Der Wert dieses Parameters muss ein Member der [**eprintticketscope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) -Enumeration sein, die als **DWORD** umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="a0986-119">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="a0986-120">*ppprintticket* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a0986-120">*ppPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0986-121">Die Adresse des Puffers, der ein Druck Ticket enthält, das den im *pdevmode* weiter gegebenen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Wert darstellt.</span><span class="sxs-lookup"><span data-stu-id="a0986-121">The address of the buffer that contains a print ticket that represents the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span> <span data-ttu-id="a0986-122">Diese Funktion Ruft die [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) -Funktion auf, um diesen Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a0986-122">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="a0986-123">Wenn der Puffer nicht mehr benötigt wird, muss der Aufrufer ihn durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.</span><span class="sxs-lookup"><span data-stu-id="a0986-123">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="a0986-124">*pcbprintticketlength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a0986-124">*pcbPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0986-125">Die Größe (in Bytes) des in *ppprintticket* zurückgegebenen Druck Tickets.</span><span class="sxs-lookup"><span data-stu-id="a0986-125">The size, in bytes, of the print ticket returned in *ppPrintTicket*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0986-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0986-126">Return value</span></span>

<span data-ttu-id="a0986-127">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück; andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a0986-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="a0986-128">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="a0986-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0986-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0986-129">Requirements</span></span>



| <span data-ttu-id="a0986-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0986-130">Requirement</span></span> | <span data-ttu-id="a0986-131">Wert</span><span class="sxs-lookup"><span data-stu-id="a0986-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0986-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0986-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a0986-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0986-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a0986-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0986-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a0986-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0986-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a0986-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a0986-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0986-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0986-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0986-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0986-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0986-139">Druck Schema</span><span class="sxs-lookup"><span data-stu-id="a0986-139">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="a0986-140">**Ptconvertdevmodetoprintticket**</span><span class="sxs-lookup"><span data-stu-id="a0986-140">**PTConvertDevModeToPrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[<span data-ttu-id="a0986-141">Drucken</span><span class="sxs-lookup"><span data-stu-id="a0986-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a0986-142">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a0986-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

