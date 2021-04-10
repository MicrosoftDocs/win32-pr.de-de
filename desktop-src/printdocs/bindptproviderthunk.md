---
description: Öffnet eine Instanz eines Druck Ticket Anbieters.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: Bindptproviderthunk-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215864"
---
# <a name="bindptproviderthunk-function"></a><span data-ttu-id="4fe55-103">Bindptproviderthunk-Funktion</span><span class="sxs-lookup"><span data-stu-id="4fe55-103">BindPTProviderThunk function</span></span>

<span data-ttu-id="4fe55-104">\[Diese Funktion wird nicht unterstützt und wird in zukünftigen Versionen von Windows möglicherweise deaktiviert oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4fe55-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="4fe55-105">[**Ptoperproviderex**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) bietet gleichwertige Funktionen und sollte stattdessen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="4fe55-105">[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="4fe55-106">Öffnet eine Instanz eines Druck Ticket Anbieters.</span><span class="sxs-lookup"><span data-stu-id="4fe55-106">Opens an instance of a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fe55-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fe55-107">Syntax</span></span>


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a><span data-ttu-id="4fe55-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fe55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fe55-109">*pszprintername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fe55-109">*pszPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe55-110">Der vollständige Name einer Druck Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="4fe55-110">The full name of a print queue.</span></span>

</dd> <dt>

<span data-ttu-id="4fe55-111">*MaxVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fe55-111">*maxVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe55-112">Die neueste Version des [Druck Schemas](./printschema.md) , das der Aufrufer unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4fe55-112">The latest version of the [Print Schema](./printschema.md) that the caller supports.</span></span>

</dd> <dt>

<span data-ttu-id="4fe55-113">*präfesversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fe55-113">*prefVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe55-114">Die vom Aufrufer angeforderte Version des [Druck Schemas](./printschema.md) .</span><span class="sxs-lookup"><span data-stu-id="4fe55-114">The version of the [Print Schema](./printschema.md) requested by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="4fe55-115">*phprovider* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4fe55-115">*phProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe55-116">Ein Zeiger auf ein Handle für den Druck ticketanbieter.</span><span class="sxs-lookup"><span data-stu-id="4fe55-116">A pointer to a handle to the print ticket provider.</span></span>

</dd> <dt>

<span data-ttu-id="4fe55-117">*usedversion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4fe55-117">*usedVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe55-118">Die Version des [Druck Schemas](./printschema.md) , das der Druck ticketanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="4fe55-118">The version of the [Print Schema](./printschema.md) that the print ticket provider will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fe55-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fe55-119">Return value</span></span>

<span data-ttu-id="4fe55-120">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück; andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4fe55-120">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="4fe55-121">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="4fe55-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4fe55-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fe55-122">Remarks</span></span>

<span data-ttu-id="4fe55-123">Vor dem Aufrufen dieser Funktion muss der aufrufenden Thread com durch Aufrufen von [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)initialisieren.</span><span class="sxs-lookup"><span data-stu-id="4fe55-123">Before calling this function, the calling thread must initialize COM by calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fe55-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fe55-124">Requirements</span></span>



| <span data-ttu-id="4fe55-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fe55-125">Requirement</span></span> | <span data-ttu-id="4fe55-126">Wert</span><span class="sxs-lookup"><span data-stu-id="4fe55-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe55-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fe55-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4fe55-128">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fe55-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4fe55-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fe55-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4fe55-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fe55-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4fe55-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4fe55-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fe55-132"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fe55-132"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fe55-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fe55-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fe55-134">Druck Schema</span><span class="sxs-lookup"><span data-stu-id="4fe55-134">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="4fe55-135">**Ptopzuproviderex**</span><span class="sxs-lookup"><span data-stu-id="4fe55-135">**PTOpenProviderEx**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[<span data-ttu-id="4fe55-136">Drucken</span><span class="sxs-lookup"><span data-stu-id="4fe55-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4fe55-137">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="4fe55-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

