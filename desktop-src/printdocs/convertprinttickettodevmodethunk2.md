---
description: Konvertiert ein Druck Ticket in eine DEVMODE-Struktur.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: ConvertPrintTicketToDevModeThunk2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: cf05ab6739dad09332ebc6746a05f3c40ef32de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042635"
---
# <a name="convertprinttickettodevmodethunk2-function"></a><span data-ttu-id="491e8-103">ConvertPrintTicketToDevModeThunk2-Funktion</span><span class="sxs-lookup"><span data-stu-id="491e8-103">ConvertPrintTicketToDevModeThunk2 function</span></span>

<span data-ttu-id="491e8-104">\[Diese Funktion wird nicht unterstützt und wird in zukünftigen Versionen von Windows möglicherweise deaktiviert oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="491e8-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="491e8-105">[**Ptconvertprintticketdedevmode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) bietet gleichwertige Funktionen und sollte stattdessen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="491e8-105">[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="491e8-106">Konvertiert ein Druck Ticket in eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="491e8-106">Converts a print ticket to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="491e8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="491e8-107">Syntax</span></span>


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
);
```



## <a name="parameters"></a><span data-ttu-id="491e8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="491e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="491e8-109">*hprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="491e8-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="491e8-110">Ein Handle für einen geöffneten Druck ticketanbieter.</span><span class="sxs-lookup"><span data-stu-id="491e8-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="491e8-111">Dieses Handle wird von der [**bindptproviderthunk**](bindptproviderthunk.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="491e8-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="491e8-112">*pprintticket* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="491e8-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="491e8-113">Der Puffer, der das zu konvertierende Druck Ticket enthält.</span><span class="sxs-lookup"><span data-stu-id="491e8-113">The buffer that contains the print ticket to convert.</span></span>

</dd> <dt>

<span data-ttu-id="491e8-114">*CBSIZE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="491e8-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="491e8-115">Die Größe (in Bytes) des Puffers, der in *pprintticket* übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="491e8-115">The size, in bytes, of the buffer passed in *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="491e8-116">*BaseType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="491e8-116">*baseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="491e8-117">Ein Wert, der angibt, ob der standardmäßige [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) des Benutzers oder der standardmäßige **DEVMODE** der Druck Warteschlange verwendet wird, um Werte für den **DEVMODE** -Ausgabemodus bereitzustellen, wenn *pprintticket* nicht jede mögliche Einstellung für einen **DEVMODE**-Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="491e8-117">A value indicating whether the user's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) or the print queue's default **DEVMODE** is used to provide values to the output **DEVMODE** when *pPrintTicket* does not specify every possible setting for a **DEVMODE**.</span></span> <span data-ttu-id="491e8-118">Der Wert dieses Parameters muss ein Member der [**edefaultdevmodetype**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) -Enumeration sein, der als **int** umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="491e8-118">The value of this parameter must be a member of the [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) enumeration, cast as an **INT**.</span></span>

</dd> <dt>

<span data-ttu-id="491e8-119">*Bereich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="491e8-119">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="491e8-120">Ein-Wert, der den Bereich von *pprintticket* angibt.</span><span class="sxs-lookup"><span data-stu-id="491e8-120">A value that specifies the scope of *pPrintTicket*.</span></span> <span data-ttu-id="491e8-121">Dieser Wert kann eine einzelne Seite, ein gesamtes Dokument oder alle Dokumente im Druckauftrag angeben.</span><span class="sxs-lookup"><span data-stu-id="491e8-121">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="491e8-122">Der Wert dieses Parameters muss ein Member der [**eprintticketscope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) -Enumeration sein, die als **DWORD** umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="491e8-122">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="491e8-123">*ppdevmode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="491e8-123">*ppDevmode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="491e8-124">Die Adresse des neu erstellten [**DEVMODE-Ausdrucks**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span><span class="sxs-lookup"><span data-stu-id="491e8-124">The address of the newly created [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span> <span data-ttu-id="491e8-125">Diese Funktion Ruft die [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) -Funktion auf, um diesen Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="491e8-125">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="491e8-126">Wenn der Puffer nicht mehr benötigt wird, muss der Aufrufer ihn durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.</span><span class="sxs-lookup"><span data-stu-id="491e8-126">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="491e8-127">*pcbdevmodelength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="491e8-127">*pcbDevModeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="491e8-128">Die Größe (in Bytes) des [**DEVMODE-Ausdrucks**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , der in *ppdevmode* zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="491e8-128">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) returned in *ppDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="491e8-129">*errmsg* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="491e8-129">*errMsg* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="491e8-130">Ein Zeiger auf eine Zeichenfolge, die angibt, was, wenn überhaupt, für das Druck Ticket in *pprintticket* ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="491e8-130">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pPrintTicket*.</span></span> <span data-ttu-id="491e8-131">Wenn Sie gültig ist, ist dies **null**.</span><span class="sxs-lookup"><span data-stu-id="491e8-131">If it is valid, this is **NULL**.</span></span> <span data-ttu-id="491e8-132">Wenn *errmsg* bei Rückgabe der Funktion nicht **null** ist, muss der Aufrufer die Zeichenfolge mit [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)freigeben.</span><span class="sxs-lookup"><span data-stu-id="491e8-132">If *errMsg* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="491e8-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="491e8-133">Return value</span></span>

<span data-ttu-id="491e8-134">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück; andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="491e8-134">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="491e8-135">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="491e8-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="491e8-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="491e8-136">Requirements</span></span>



| <span data-ttu-id="491e8-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="491e8-137">Requirement</span></span> | <span data-ttu-id="491e8-138">Wert</span><span class="sxs-lookup"><span data-stu-id="491e8-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="491e8-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="491e8-139">Minimum supported client</span></span><br/> | <span data-ttu-id="491e8-140">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="491e8-140">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="491e8-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="491e8-141">Minimum supported server</span></span><br/> | <span data-ttu-id="491e8-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="491e8-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="491e8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="491e8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="491e8-144"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="491e8-144"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="491e8-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="491e8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="491e8-146">Druck Schema</span><span class="sxs-lookup"><span data-stu-id="491e8-146">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="491e8-147">**Ptconvertprintticketdedevmode**</span><span class="sxs-lookup"><span data-stu-id="491e8-147">**PTConvertPrintTicketToDevMode**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[<span data-ttu-id="491e8-148">Drucken</span><span class="sxs-lookup"><span data-stu-id="491e8-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="491e8-149">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="491e8-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

