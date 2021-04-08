---
title: XTYP_UNREGISTER Transaktion (Ddeml. h)
description: Eine dynamischer Datenaustausch (DDE)-Rückruffunktion (ddecallback) empfängt die \_ xttunregister-Transaktion, wenn eine Ddeml-Serveranwendung (dynamischer Datenaustausch Management Library) die Funktion "DDENameService" verwendet, um die Registrierung eines Dienst namens aufzuheben, oder wenn eine nicht-Ddeml-Anwendung, die das System Thema unterstützt, beendet wird.
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- XTYP_UNREGISTER Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_UNREGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeba96b26c019aa0a3050a83f726745b749efa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742872"
---
# <a name="xtyp_unregister-transaction"></a><span data-ttu-id="30931-104">\_Xttunregister Transaktion</span><span class="sxs-lookup"><span data-stu-id="30931-104">XTYP\_UNREGISTER transaction</span></span>

<span data-ttu-id="30931-105">Eine dynamischer Datenaustausch (DDE)-Rückruffunktion ( [*ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt die **\_ xttunregister** -Transaktion, wenn eine Ddeml-Serveranwendung (dynamischer Datenaustausch Management Library) die Funktion " [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) " verwendet, um die Registrierung eines Dienst namens aufzuheben, oder wenn eine nicht-Ddeml-Anwendung, die das System Thema unterstützt, beendet wird.</span><span class="sxs-lookup"><span data-stu-id="30931-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_UNREGISTER** transaction whenever a Dynamic Data Exchange Management Library (DDEML) server application uses the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function to unregister a service name, or whenever a non-DDEML application that supports the System topic is terminated.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_UNREGISTER         (0x00D0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="30931-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30931-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30931-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="30931-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="30931-108">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="30931-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="30931-109">*UF*</span><span class="sxs-lookup"><span data-stu-id="30931-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="30931-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="30931-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="30931-111">*has*</span><span class="sxs-lookup"><span data-stu-id="30931-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="30931-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="30931-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="30931-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="30931-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="30931-114">Ein Handle für den Basis Dienstnamen, bei dem die Registrierung aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="30931-114">A handle to the base service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="30931-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="30931-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="30931-116">Ein Handle für den instanzspezifischen Dienstnamen, bei dem die Registrierung aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="30931-116">A handle to the instance-specific service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="30931-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="30931-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="30931-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="30931-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="30931-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="30931-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="30931-120">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="30931-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="30931-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="30931-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="30931-122">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="30931-122">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30931-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30931-123">Remarks</span></span>

<span data-ttu-id="30931-124">Diese Transaktion wird gefiltert, wenn die Anwendung das Flag " **CBF \_ Skip \_ Registrierungen** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="30931-124">This transaction is filtered if the application specified the **CBF\_SKIP\_REGISTRATIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="30931-125">Eine-Anwendung kann diesen Transaktionstyp nicht blockieren; der Rückgabecode des CBR- \_ Blocks wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="30931-125">A application cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

<span data-ttu-id="30931-126">Eine Anwendung sollte den *hsz1* -Parameter verwenden, um den Dienstnamen aus der Liste der für den Benutzer verfügbaren Server zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="30931-126">An application should use the *hsz1* parameter to remove the service name from the list of servers available to the user.</span></span> <span data-ttu-id="30931-127">Eine Anwendung sollte den *hsz2* -Parameter verwenden, um zu ermitteln, welche Anwendungs Instanz beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="30931-127">An application should use the *hsz2* parameter to identify which application instance has terminated.</span></span>

## <a name="requirements"></a><span data-ttu-id="30931-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30931-128">Requirements</span></span>



| <span data-ttu-id="30931-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30931-129">Requirement</span></span> | <span data-ttu-id="30931-130">Wert</span><span class="sxs-lookup"><span data-stu-id="30931-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30931-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30931-131">Minimum supported client</span></span><br/> | <span data-ttu-id="30931-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30931-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="30931-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30931-133">Minimum supported server</span></span><br/> | <span data-ttu-id="30931-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30931-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="30931-135">Header</span><span class="sxs-lookup"><span data-stu-id="30931-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="30931-136"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30931-136"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30931-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30931-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="30931-138">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="30931-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="30931-139">**DDEInitialize**</span><span class="sxs-lookup"><span data-stu-id="30931-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="30931-140">**DDENameService**</span><span class="sxs-lookup"><span data-stu-id="30931-140">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

<span data-ttu-id="30931-141">**Licher**</span><span class="sxs-lookup"><span data-stu-id="30931-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="30931-142">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30931-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

