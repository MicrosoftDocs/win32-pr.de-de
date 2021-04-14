---
title: XTYP_CONNECT_CONFIRM Transaktion (Ddeml. h)
description: Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion (DDE Callback) empfängt die xtipp \_ Connect \_ -Bestätigungs Transaktion, um zu bestätigen, dass eine Konversation mit einem Client hergestellt wurde, und um dem Server das Konversations handle bereitzustellen.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- XTYP_CONNECT_CONFIRM Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e880dfffc7f7825c99ab9e4e3bf980baa978b786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391972"
---
# <a name="xtyp_connect_confirm-transaction"></a><span data-ttu-id="078bb-104">Xtipp \_ Connect- \_ Transaktion bestätigen</span><span class="sxs-lookup"><span data-stu-id="078bb-104">XTYP\_CONNECT\_CONFIRM transaction</span></span>

<span data-ttu-id="078bb-105">Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt die **xtipp \_ Connect- \_ Bestätigungs** Transaktion, um zu bestätigen, dass eine Konversation mit einem Client hergestellt wurde, und um dem Server das Konversations handle bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="078bb-105">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_CONNECT\_CONFIRM** transaction to confirm that a conversation has been established with a client and to provide the server with the conversation handle.</span></span> <span data-ttu-id="078bb-106">Das System sendet diese Transaktion als Ergebnis einer vorherigen [**xtipp \_ Connect**](xtyp-connect.md) -oder [**XYP \_ wildconnect**](xtyp-wildconnect.md) -Transaktion.</span><span class="sxs-lookup"><span data-stu-id="078bb-106">The system sends this transaction as a result of a previous [**XTYP\_CONNECT**](xtyp-connect.md) or [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="078bb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="078bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="078bb-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="078bb-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="078bb-109">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="078bb-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="078bb-110">*UF*</span><span class="sxs-lookup"><span data-stu-id="078bb-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="078bb-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="078bb-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="078bb-112">*has*</span><span class="sxs-lookup"><span data-stu-id="078bb-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="078bb-113">Ein Handle für die neue Konversation.</span><span class="sxs-lookup"><span data-stu-id="078bb-113">A handle to the new conversation.</span></span>

</dd> <dt>

<span data-ttu-id="078bb-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="078bb-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="078bb-115">Ein Handle für den Themen Namen, für den die Konversation eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="078bb-115">A handle to the topic name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="078bb-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="078bb-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="078bb-117">Ein Handle für den Dienstnamen, für den die Konversation eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="078bb-117">A handle to the service name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="078bb-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="078bb-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="078bb-119">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="078bb-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="078bb-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="078bb-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="078bb-121">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="078bb-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="078bb-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="078bb-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="078bb-123">Gibt an, ob es sich bei dem Client um dieselbe Anwendungs Instanz wie der Server handelt.</span><span class="sxs-lookup"><span data-stu-id="078bb-123">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="078bb-124">Wenn der-Parameter 1 ist, ist der Client dieselbe Instanz.</span><span class="sxs-lookup"><span data-stu-id="078bb-124">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="078bb-125">Wenn der-Parameter 0 ist, ist der Client eine andere-Instanz.</span><span class="sxs-lookup"><span data-stu-id="078bb-125">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="078bb-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="078bb-126">Remarks</span></span>

<span data-ttu-id="078bb-127">Diese Transaktion wird gefiltert, wenn von der Serveranwendung das Flag **CBF \_ Skip \_ Connect \_ bestätigt** in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="078bb-127">This transaction is filtered if the server application specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="078bb-128">Ein Server kann diesen Transaktionstyp nicht blockieren. der Rückgabecode des **CBR- \_ Blocks** wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="078bb-128">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="078bb-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="078bb-129">Requirements</span></span>



| <span data-ttu-id="078bb-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="078bb-130">Requirement</span></span> | <span data-ttu-id="078bb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="078bb-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="078bb-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="078bb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="078bb-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="078bb-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="078bb-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="078bb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="078bb-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="078bb-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="078bb-136">Header</span><span class="sxs-lookup"><span data-stu-id="078bb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="078bb-137"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="078bb-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="078bb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="078bb-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="078bb-139">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="078bb-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="078bb-140">**DDE Connect**</span><span class="sxs-lookup"><span data-stu-id="078bb-140">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="078bb-141">**DDE ConnectList**</span><span class="sxs-lookup"><span data-stu-id="078bb-141">**DdeConnectList**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[<span data-ttu-id="078bb-142">**DDEInitialize**</span><span class="sxs-lookup"><span data-stu-id="078bb-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="078bb-143">**Licher**</span><span class="sxs-lookup"><span data-stu-id="078bb-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="078bb-144">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="078bb-144">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

