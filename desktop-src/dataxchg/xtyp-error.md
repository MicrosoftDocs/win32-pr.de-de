---
title: XTYP_ERROR Transaktion (Ddeml. h)
description: Eine dynamischer Datenaustausch (DDE)-Rückruffunktion (DDE Callback) empfängt die xD- \_ Fehler Transaktion, wenn ein kritischer Fehler auftritt.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- XTYP_ERROR Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbad80cb23a37881e8954dee4a80a87f253e499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337328"
---
# <a name="xtyp_error-transaction"></a><span data-ttu-id="92009-104">XYP- \_ Fehler Transaktion</span><span class="sxs-lookup"><span data-stu-id="92009-104">XTYP\_ERROR transaction</span></span>

<span data-ttu-id="92009-105">Eine dynamischer Datenaustausch (DDE)-Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt die **xD- \_ Fehler** Transaktion, wenn ein kritischer Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="92009-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_ERROR** transaction when a critical error occurs.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="92009-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="92009-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92009-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="92009-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="92009-108">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="92009-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="92009-109">*UF*</span><span class="sxs-lookup"><span data-stu-id="92009-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="92009-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="92009-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="92009-111">*has*</span><span class="sxs-lookup"><span data-stu-id="92009-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="92009-112">Ein Handle für die Konversation, die dem Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="92009-112">A handle to the conversation associated with the error.</span></span> <span data-ttu-id="92009-113">Dieser Parameter ist **null** , wenn der Fehler nicht mit einer Konversation verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="92009-113">This parameter is **NULL** if the error is not associated with a conversation.</span></span>

</dd> <dt>

<span data-ttu-id="92009-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="92009-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="92009-115">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="92009-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="92009-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="92009-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="92009-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="92009-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="92009-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="92009-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="92009-119">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="92009-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="92009-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="92009-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="92009-121">Der Fehlercode im nieder wertigen Wort.</span><span class="sxs-lookup"><span data-stu-id="92009-121">The error code in the low-order word.</span></span> <span data-ttu-id="92009-122">Derzeit wird nur der folgende Fehlercode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="92009-122">Currently, only the following error code is supported.</span></span>



| <span data-ttu-id="92009-123">Wert</span><span class="sxs-lookup"><span data-stu-id="92009-123">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="92009-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="92009-124">Meaning</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <span data-ttu-id="92009-125"><dt>**dmlerr \_ wenig Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="92009-125"><dt>**DMLERR\_LOW\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="92009-126">Der Arbeitsspeicher ist niedrig. Daten vom Typ "Empfehlung", "Poke" oder "ausführen" können verloren gehen, oder das System schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="92009-126">Memory is low; advise, poke, or execute data may be lost, or the system may fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="92009-127">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="92009-127">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="92009-128">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="92009-128">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92009-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92009-129">Remarks</span></span>

<span data-ttu-id="92009-130">Der Transaktionstyp kann von einer Anwendung nicht blockiert werden. der Rückgabecode des **CBR- \_ Blocks** wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="92009-130">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span> <span data-ttu-id="92009-131">Die Ddeml (dynamischer Datenaustausch Management Library) versucht, Arbeitsspeicher freizugeben, indem nicht kritische Ressourcen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="92009-131">The Dynamic Data Exchange Management Library (DDEML) attempts to free memory by removing noncritical resources.</span></span> <span data-ttu-id="92009-132">Eine Anwendung, die blockierte Konversationen hat, sollte Sie entsperren.</span><span class="sxs-lookup"><span data-stu-id="92009-132">An application that has blocked conversations should unblock them.</span></span>

## <a name="requirements"></a><span data-ttu-id="92009-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92009-133">Requirements</span></span>



| <span data-ttu-id="92009-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92009-134">Requirement</span></span> | <span data-ttu-id="92009-135">Wert</span><span class="sxs-lookup"><span data-stu-id="92009-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92009-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92009-136">Minimum supported client</span></span><br/> | <span data-ttu-id="92009-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92009-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="92009-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92009-138">Minimum supported server</span></span><br/> | <span data-ttu-id="92009-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92009-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="92009-140">Header</span><span class="sxs-lookup"><span data-stu-id="92009-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="92009-141"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92009-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92009-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92009-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92009-143">Übersicht über die dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="92009-143">Dynamic Data Exchange Management Library Overview</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

