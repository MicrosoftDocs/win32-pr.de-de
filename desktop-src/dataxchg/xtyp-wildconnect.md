---
title: XTYP_WILDCONNECT Transaktion (Ddeml. h)
description: Ermöglicht einem Client, eine Konversation für alle Dienstnamen-und Themen Namen Paare des Servers einzurichten, die dem angegebenen Dienstnamen und Themen Namen entsprechen.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- XTYP_WILDCONNECT Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_WILDCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc63d6c367aebc440418beaabb0a06f05b0df967
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340788"
---
# <a name="xtyp_wildconnect-transaction"></a><span data-ttu-id="71676-104">XYP- \_ wildconnect-Transaktion</span><span class="sxs-lookup"><span data-stu-id="71676-104">XTYP\_WILDCONNECT transaction</span></span>

<span data-ttu-id="71676-105">Ermöglicht einem Client, eine Konversation für alle Dienstnamen-und Themen Namen Paare des Servers einzurichten, die dem angegebenen Dienstnamen und Themen Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="71676-105">Enables a client to establish a conversation on each of the server's service name and topic name pairs that match the specified service name and topic name.</span></span> <span data-ttu-id="71676-106">Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion [*(ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, wenn ein Client einen **null** -Dienstnamen, einen **null** -Themen Namen oder beides in einem Aufrufs der [**ddeconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) -oder [**ddeconnectlist**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="71676-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a **NULL** service name, a **NULL** topic name, or both in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) or [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="71676-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="71676-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71676-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="71676-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="71676-109">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="71676-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="71676-110">*UF*</span><span class="sxs-lookup"><span data-stu-id="71676-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="71676-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="71676-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="71676-112">*has*</span><span class="sxs-lookup"><span data-stu-id="71676-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="71676-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="71676-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="71676-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="71676-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="71676-115">Ein Handle für den Themen Namen.</span><span class="sxs-lookup"><span data-stu-id="71676-115">A handle to the topic name.</span></span> <span data-ttu-id="71676-116">Wenn dieser Parameter **null** ist, fordert der Client eine Konversation für alle Themen Namen an, die der Server unterstützt.</span><span class="sxs-lookup"><span data-stu-id="71676-116">If this parameter is **NULL**, the client is requesting a conversation on all topic names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="71676-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="71676-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="71676-118">Ein Handle für den Dienstnamen.</span><span class="sxs-lookup"><span data-stu-id="71676-118">A handle to the service name.</span></span> <span data-ttu-id="71676-119">Wenn dieser Parameter **null** ist, fordert der Client eine Konversation für alle Dienstnamen an, die der Server unterstützt.</span><span class="sxs-lookup"><span data-stu-id="71676-119">If this parameter is **NULL**, the client is requesting a conversation on all service names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="71676-120">*hdata*</span><span class="sxs-lookup"><span data-stu-id="71676-120">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="71676-121">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="71676-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="71676-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="71676-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="71676-123">Ein Zeiger auf eine [**konvcontext**](/windows/win32/api/ddeml/ns-ddeml-convcontext) -Struktur, die Kontextinformationen für die Konversation enthält.</span><span class="sxs-lookup"><span data-stu-id="71676-123">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="71676-124">Wenn der Client keine Ddeml-Anwendung ist, wird dieser Parameter auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="71676-124">If the client is not a DDEML application, this parameter is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="71676-125">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="71676-125">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="71676-126">Gibt an, ob es sich bei dem Client um dieselbe Anwendungs Instanz wie der Server handelt.</span><span class="sxs-lookup"><span data-stu-id="71676-126">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="71676-127">Wenn der-Parameter 1 ist, ist der Client dieselbe Instanz.</span><span class="sxs-lookup"><span data-stu-id="71676-127">If the parameter is 1, the client is same instance.</span></span> <span data-ttu-id="71676-128">Wenn der-Parameter 0 ist, ist der Client eine andere-Instanz.</span><span class="sxs-lookup"><span data-stu-id="71676-128">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71676-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71676-129">Return value</span></span>

<span data-ttu-id="71676-130">Der Server sollte ein Daten Handle zurückgeben, das ein Array von [**hszpair**](/windows/win32/api/ddeml/ns-ddeml-hszpair) -Strukturen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="71676-130">The server should return a data handle that identifies an array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="71676-131">Das Array sollte eine Struktur für jedes Paar aus Dienst Name und Themenname enthalten, das mit dem vom Client angeforderten Dienstnamen und Topic-Name-Paar übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="71676-131">The array should contain one structure for each service-name and topic-name pair that matches the service-name and topic-name pair requested by the client.</span></span> <span data-ttu-id="71676-132">Das Array muss von einem **null** -Zeichen folgen handle beendet werden.</span><span class="sxs-lookup"><span data-stu-id="71676-132">The array must be terminated by a **NULL** string handle.</span></span> <span data-ttu-id="71676-133">Das System sendet die [**xtipp \_ Connect- \_ Bestätigungs**](xtyp-connect-confirm.md) Transaktion an den Server, um die einzelnen Konversation zu bestätigen und die Konversations Handles an den Server zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="71676-133">The system sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server to confirm each conversation and to pass the conversation handles to the server.</span></span> <span data-ttu-id="71676-134">Der Server empfängt diese Bestätigungen nicht, wenn er das Flag **CBF \_ Skip \_ Connect \_ Bestätigungen** in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="71676-134">The server will not receive these confirmations if it specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="71676-135">Der Server sollte **null** zurückgeben, um die **XYP \_ wildconnect** -Transaktion abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="71676-135">The server should return **NULL** to refuse the **XTYP\_WILDCONNECT** transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="71676-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71676-136">Remarks</span></span>

<span data-ttu-id="71676-137">Diese Transaktion wird gefiltert, wenn von der Serveranwendung das Flag " **CBF \_ Fail \_ Connections** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="71676-137">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="71676-138">Ein Server kann diesen Transaktionstyp nicht blockieren. der Rückgabecode des CBR- \_ Blocks wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="71676-138">A server cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="71676-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71676-139">Requirements</span></span>



| <span data-ttu-id="71676-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71676-140">Requirement</span></span> | <span data-ttu-id="71676-141">Wert</span><span class="sxs-lookup"><span data-stu-id="71676-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71676-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71676-142">Minimum supported client</span></span><br/> | <span data-ttu-id="71676-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71676-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="71676-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71676-144">Minimum supported server</span></span><br/> | <span data-ttu-id="71676-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71676-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="71676-146">Header</span><span class="sxs-lookup"><span data-stu-id="71676-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="71676-147"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71676-147"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71676-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71676-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="71676-149">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="71676-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="71676-150">**Konvcontext**</span><span class="sxs-lookup"><span data-stu-id="71676-150">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="71676-151">**DDE Connect**</span><span class="sxs-lookup"><span data-stu-id="71676-151">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="71676-152">**DDEInitialize**</span><span class="sxs-lookup"><span data-stu-id="71676-152">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="71676-153">**Hszpair**</span><span class="sxs-lookup"><span data-stu-id="71676-153">**HSZPAIR**</span></span>](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

<span data-ttu-id="71676-154">**Licher**</span><span class="sxs-lookup"><span data-stu-id="71676-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="71676-155">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71676-155">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

