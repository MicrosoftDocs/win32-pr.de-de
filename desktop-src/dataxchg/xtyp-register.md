---
title: XTYP_REGISTER Transaktion (Ddeml. h)
description: Eine dynamischer Datenaustausch (DDE)-Rückruffunktion (ddecallback) empfängt den xtyp- \_ Register Transaktionstyp, wenn eine Ddeml-Serveranwendung (dynamischer Datenaustausch Management Library) die Funktion "DDENameService" zum Registrieren eines Dienst namens verwendet, oder wenn eine nicht-Ddeml-Anwendung gestartet wird, die das System Thema unterstützt.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- XTYP_REGISTER Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_REGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd56bf4f5ac2b4eb0f714e5348174942f685c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476179"
---
# <a name="xtyp_register-transaction"></a><span data-ttu-id="51aa8-104">XYP- \_ Register Transaktion</span><span class="sxs-lookup"><span data-stu-id="51aa8-104">XTYP\_REGISTER transaction</span></span>

<span data-ttu-id="51aa8-105">Eine dynamischer Datenaustausch (DDE)-Rückruffunktion ( [*ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt den **xtyp- \_ Register** Transaktionstyp, wenn eine Ddeml-Serveranwendung (dynamischer Datenaustausch Management Library) die Funktion " [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) " zum Registrieren eines Dienst namens verwendet, oder wenn eine nicht-Ddeml-Anwendung gestartet wird, die das System Thema unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51aa8-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_REGISTER** transaction type whenever a Dynamic Data Exchange Management Library (DDEML) server application uses the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function to register a service name, or whenever a non-DDEML application that supports the System topic is started.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_REGISTER           (0x00A0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="51aa8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51aa8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51aa8-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="51aa8-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="51aa8-108">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="51aa8-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="51aa8-109">*UF*</span><span class="sxs-lookup"><span data-stu-id="51aa8-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="51aa8-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51aa8-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="51aa8-111">*has*</span><span class="sxs-lookup"><span data-stu-id="51aa8-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="51aa8-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51aa8-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="51aa8-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="51aa8-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="51aa8-114">Ein Handle für den Basis Dienstnamen, der registriert wird.</span><span class="sxs-lookup"><span data-stu-id="51aa8-114">A handle to the base service name being registered.</span></span>

</dd> <dt>

<span data-ttu-id="51aa8-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="51aa8-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="51aa8-116">Ein Handle für den instanzspezifischen Dienstnamen, der registriert wird.</span><span class="sxs-lookup"><span data-stu-id="51aa8-116">A handle to the instance-specific service name being registered.</span></span>

</dd> <dt>

<span data-ttu-id="51aa8-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="51aa8-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="51aa8-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51aa8-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="51aa8-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="51aa8-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="51aa8-120">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51aa8-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="51aa8-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="51aa8-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="51aa8-122">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51aa8-122">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51aa8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51aa8-123">Remarks</span></span>

<span data-ttu-id="51aa8-124">Diese Transaktion wird gefiltert, wenn die Anwendung das Flag " **CBF \_ Skip \_ Registrierungen** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="51aa8-124">This transaction is filtered if the application specified the **CBF\_SKIP\_REGISTRATIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="51aa8-125">Eine-Anwendung kann diesen Transaktionstyp nicht blockieren; der Rückgabecode des **CBR- \_ Blocks** wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="51aa8-125">A application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

<span data-ttu-id="51aa8-126">Eine Anwendung sollte den *hsz1* -Parameter verwenden, um den Dienstnamen zur Liste der Server hinzuzufügen, die dem Benutzer zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="51aa8-126">An application should use the *hsz1* parameter to add the service name to the list of servers available to the user.</span></span> <span data-ttu-id="51aa8-127">Eine Anwendung sollte den *hsz2* -Parameter verwenden, um die gestartete Anwendungs Instanz zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="51aa8-127">An application should use the *hsz2* parameter to identify which application instance has started.</span></span>

## <a name="requirements"></a><span data-ttu-id="51aa8-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51aa8-128">Requirements</span></span>



| <span data-ttu-id="51aa8-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51aa8-129">Requirement</span></span> | <span data-ttu-id="51aa8-130">Wert</span><span class="sxs-lookup"><span data-stu-id="51aa8-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51aa8-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51aa8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="51aa8-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51aa8-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="51aa8-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51aa8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="51aa8-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51aa8-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="51aa8-135">Header</span><span class="sxs-lookup"><span data-stu-id="51aa8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="51aa8-136"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51aa8-136"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51aa8-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51aa8-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="51aa8-138">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="51aa8-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="51aa8-139">**DDEInitialize**</span><span class="sxs-lookup"><span data-stu-id="51aa8-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="51aa8-140">**DDENameService**</span><span class="sxs-lookup"><span data-stu-id="51aa8-140">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

<span data-ttu-id="51aa8-141">**Licher**</span><span class="sxs-lookup"><span data-stu-id="51aa8-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="51aa8-142">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="51aa8-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

