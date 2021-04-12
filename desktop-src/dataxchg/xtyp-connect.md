---
title: XTYP_CONNECT Transaktion (Ddeml. h)
description: Ein Client verwendet die xtipp \_ Connect-Transaktion zum Einrichten einer Konversation.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- XTYP_CONNECT Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2268994f1be000373691d6c25dbb7220d3e109e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104078"
---
# <a name="xtyp_connect-transaction"></a><span data-ttu-id="491af-104">XYP \_ Connect-Transaktion</span><span class="sxs-lookup"><span data-stu-id="491af-104">XTYP\_CONNECT transaction</span></span>

<span data-ttu-id="491af-105">Ein Client verwendet die **xtipp \_ Connect** -Transaktion zum Einrichten einer Konversation.</span><span class="sxs-lookup"><span data-stu-id="491af-105">A client uses the **XTYP\_CONNECT** transaction to establish a conversation.</span></span> <span data-ttu-id="491af-106">Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion ( [*ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, wenn ein Client einen Dienstnamen angibt, der vom Server unterstützt wird (und einen Themen Namen, der nicht **null** ist), wenn die [**ddeconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="491af-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a service name that the server supports (and a topic name that is not **NULL**) in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="491af-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="491af-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="491af-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="491af-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="491af-109">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="491af-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="491af-110">*UF*</span><span class="sxs-lookup"><span data-stu-id="491af-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="491af-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="491af-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="491af-112">*has*</span><span class="sxs-lookup"><span data-stu-id="491af-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="491af-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="491af-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="491af-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="491af-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="491af-115">Ein Handle für den Themen Namen.</span><span class="sxs-lookup"><span data-stu-id="491af-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="491af-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="491af-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="491af-117">Ein Handle für den Dienstnamen.</span><span class="sxs-lookup"><span data-stu-id="491af-117">A handle to the service name.</span></span>

</dd> <dt>

<span data-ttu-id="491af-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="491af-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="491af-119">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="491af-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="491af-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="491af-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="491af-121">Ein Zeiger auf eine [**konvcontext**](/windows/win32/api/ddeml/ns-ddeml-convcontext) -Struktur, die Kontextinformationen für die Konversation enthält.</span><span class="sxs-lookup"><span data-stu-id="491af-121">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="491af-122">Wenn der Client keine Ddeml-Anwendung ist, ist dieser Parameter 0.</span><span class="sxs-lookup"><span data-stu-id="491af-122">If the client is not a DDEML application, this parameter is 0.</span></span>

</dd> <dt>

<span data-ttu-id="491af-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="491af-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="491af-124">Gibt an, ob es sich bei dem Client um dieselbe Anwendungs Instanz wie der Server handelt.</span><span class="sxs-lookup"><span data-stu-id="491af-124">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="491af-125">Wenn der-Parameter 1 ist, ist der Client dieselbe Instanz.</span><span class="sxs-lookup"><span data-stu-id="491af-125">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="491af-126">Wenn der-Parameter 0 ist, ist der Client eine andere-Instanz.</span><span class="sxs-lookup"><span data-stu-id="491af-126">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="491af-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="491af-127">Return value</span></span>

<span data-ttu-id="491af-128">Eine Server Rückruffunktion sollte " **true** " zurückgeben, damit der Client eine Konversation für das angegebene Paar aus Dienst Name und Themenname einrichten kann. andernfalls sollte die Funktion " **false** " zurückgeben, um die Konversation abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="491af-128">A server callback function should return **TRUE** to allow the client to establish a conversation on the specified service name and topic name pair, or the function should return **FALSE** to deny the conversation.</span></span> <span data-ttu-id="491af-129">Wenn die Rückruffunktion " **true** " zurückgibt und eine Konversation erfolgreich eingerichtet wurde, übergibt das System das Konversations Handle an den Server, indem eine [**xtipp Connect-Transaktion zum \_ \_ bestätigen**](xtyp-connect-confirm.md) an die Rückruffunktion des Servers ausgegeben wird (es sei denn, der Server hat das Flag " **CBF \_ Skip \_ Connect \_ bestätigt** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben</span><span class="sxs-lookup"><span data-stu-id="491af-129">If the callback function returns **TRUE** and a conversation is successfully established, the system passes the conversation handle to the server by issuing an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's callback function (unless the server specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function).</span></span>

## <a name="remarks"></a><span data-ttu-id="491af-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="491af-130">Remarks</span></span>

<span data-ttu-id="491af-131">Diese Transaktion wird gefiltert, wenn von der Serveranwendung das Flag " **CBF \_ Fail \_ Connections** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="491af-131">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="491af-132">Ein Server kann diesen Transaktionstyp nicht blockieren. der Rückgabecode des **CBR- \_ Blocks** wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="491af-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="491af-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="491af-133">Requirements</span></span>



| <span data-ttu-id="491af-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="491af-134">Requirement</span></span> | <span data-ttu-id="491af-135">Wert</span><span class="sxs-lookup"><span data-stu-id="491af-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="491af-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="491af-136">Minimum supported client</span></span><br/> | <span data-ttu-id="491af-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="491af-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="491af-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="491af-138">Minimum supported server</span></span><br/> | <span data-ttu-id="491af-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="491af-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="491af-140">Header</span><span class="sxs-lookup"><span data-stu-id="491af-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="491af-141"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="491af-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="491af-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="491af-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="491af-143">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="491af-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="491af-144">**Konvcontext**</span><span class="sxs-lookup"><span data-stu-id="491af-144">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="491af-145">**DDE Connect**</span><span class="sxs-lookup"><span data-stu-id="491af-145">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="491af-146">**DDEInitialize**</span><span class="sxs-lookup"><span data-stu-id="491af-146">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="491af-147">**Licher**</span><span class="sxs-lookup"><span data-stu-id="491af-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="491af-148">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="491af-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

