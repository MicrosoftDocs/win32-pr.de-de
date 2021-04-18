---
description: Ruft die Druckerfunktionen ab, die in Übereinstimmung mit dem XML-Druck Schema formatiert sind.
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: GetPrintCapabilitiesThunk2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintCapabilitiesThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: eb60f1cdabad6287e236fc099fc304e9e7de83ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368793"
---
# <a name="getprintcapabilitiesthunk2-function"></a><span data-ttu-id="54300-103">GetPrintCapabilitiesThunk2-Funktion</span><span class="sxs-lookup"><span data-stu-id="54300-103">GetPrintCapabilitiesThunk2 function</span></span>

<span data-ttu-id="54300-104">\[Diese Funktion wird nicht unterstützt und wird in zukünftigen Versionen von Windows möglicherweise deaktiviert oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="54300-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="54300-105">[**Ptgetprintworks**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) bietet entsprechende Funktionen und sollte stattdessen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="54300-105">[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="54300-106">Ruft die Funktionen des Druckers ab, die in Übereinstimmung mit dem XML- [Druck Schema](./printschema.md)formatiert sind.</span><span class="sxs-lookup"><span data-stu-id="54300-106">Retrieves the printer's capabilities formatted in compliance with the XML [Print Schema](./printschema.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="54300-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="54300-107">Syntax</span></span>


```C++
HRESULT GetPrintCapabilitiesThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      INT         cbPrintTicket,
  _Out_     BYTE        **ppbPrintCapabilities,
  _Out_     INT         *pcbPrintCapabilitiesLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="54300-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="54300-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54300-109">*hprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54300-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54300-110">Ein Handle für einen geöffneten Druck ticketanbieter.</span><span class="sxs-lookup"><span data-stu-id="54300-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="54300-111">Dieses Handle wird von der [**bindptproviderthunk**](bindptproviderthunk.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="54300-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="54300-112">*pprintticket* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54300-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54300-113">Der Puffer, der die Druck Ticketdaten enthält, wie im [Druck Schema](./printschema.md)beschrieben, in XML ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="54300-113">The buffer that contains the print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="54300-114">*cbprintticket* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54300-114">*cbPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54300-115">Die Größe (in Bytes) des Puffers, auf den *pprintticket* verweist.</span><span class="sxs-lookup"><span data-stu-id="54300-115">The size, in bytes, of the buffer referenced by *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="54300-116">*ppbprint-Funktionen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="54300-116">*ppbPrintCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54300-117">Die Adresse des Puffers, der von dieser Funktion zugeordnet wird, und enthält die gültigen Druck Funktions Informationen, die als XML codiert sind.</span><span class="sxs-lookup"><span data-stu-id="54300-117">The address of the buffer that is allocated by this function and contains the valid print capabilities information, encoded as XML.</span></span> <span data-ttu-id="54300-118">Diese Funktion Ruft die [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) -Funktion auf, um diesen Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="54300-118">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="54300-119">Wenn der Puffer nicht mehr benötigt wird, muss der Aufrufer ihn durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.</span><span class="sxs-lookup"><span data-stu-id="54300-119">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="54300-120">*pcbprintcapabilitieslength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="54300-120">*pcbPrintCapabilitiesLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54300-121">Die Größe (in Bytes) des Puffers, auf den *ppbprint-Funktionen* verweist.</span><span class="sxs-lookup"><span data-stu-id="54300-121">The size, in bytes, of the buffer referenced by *ppbPrintCapabilities*.</span></span>

</dd> <dt>

<span data-ttu-id="54300-122">*pbstrauerrormessage* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="54300-122">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="54300-123">Ein Zeiger auf eine Zeichenfolge, die angibt, was, wenn nichts, für *pprintticket* ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="54300-123">A pointer to a string that specifies what, if anything, is invalid about *pPrintTicket*.</span></span> <span data-ttu-id="54300-124">Wenn Sie gültig ist, ist dieser Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="54300-124">If it is valid, this value is **NULL**.</span></span> <span data-ttu-id="54300-125">Wenn *pbstrauerrormessage* bei Rückgabe der Funktion nicht **null** ist, muss der Aufrufer die Zeichenfolge mit [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)freigeben.</span><span class="sxs-lookup"><span data-stu-id="54300-125">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54300-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54300-126">Return value</span></span>

<span data-ttu-id="54300-127">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück; andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="54300-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="54300-128">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="54300-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54300-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54300-129">Requirements</span></span>



| <span data-ttu-id="54300-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54300-130">Requirement</span></span> | <span data-ttu-id="54300-131">Wert</span><span class="sxs-lookup"><span data-stu-id="54300-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54300-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54300-132">Minimum supported client</span></span><br/> | <span data-ttu-id="54300-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54300-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="54300-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54300-134">Minimum supported server</span></span><br/> | <span data-ttu-id="54300-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54300-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="54300-136">DLL</span><span class="sxs-lookup"><span data-stu-id="54300-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54300-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54300-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54300-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54300-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54300-139">**Ptgetprint-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="54300-139">**PTGetPrintCapabilities**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[<span data-ttu-id="54300-140">Druck Schema</span><span class="sxs-lookup"><span data-stu-id="54300-140">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="54300-141">Drucken</span><span class="sxs-lookup"><span data-stu-id="54300-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="54300-142">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="54300-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

