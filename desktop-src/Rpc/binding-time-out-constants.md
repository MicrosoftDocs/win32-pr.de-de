---
title: Bindungs Timeout Konstanten (rpcdce. h)
description: Die RPC-Bibliothek verwendet die Bindungs Timeout Konstanten, um die relative Zeitspanne anzugeben, die für das Herstellen einer Bindung an den Server aufgewendet werden soll, bevor ein Timeout auftritt.
ms.assetid: bf5f3f08-ab29-4732-9ce3-d6d7ad699369
topic_type:
- apiref
api_name:
- RPC_C_BINDING_INFINITE_TIMEOUT
- RPC_C_BINDING_MIN_TIMEOUT
- RPC_C_BINDING_DEFAULT_TIMEOUT
- RPC_C_BINDING_MAX_TIMEOUT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096fd320e1341f9affc35ae6ff1d355fcf12d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337727"
---
# <a name="binding-time-out-constants"></a><span data-ttu-id="23703-103">Binden von Timeout Konstanten</span><span class="sxs-lookup"><span data-stu-id="23703-103">Binding Time-out Constants</span></span>

<span data-ttu-id="23703-104">Die RPC-Bibliothek verwendet die Bindungs Timeout Konstanten, um die relative Zeitspanne anzugeben, die für das Herstellen einer Bindung an den Server aufgewendet werden soll, bevor ein Timeout auftritt.</span><span class="sxs-lookup"><span data-stu-id="23703-104">The RPC library uses the binding time-out constants to specify the relative amount of time that should be spent to establish a binding to the server before giving up.</span></span> <span data-ttu-id="23703-105">Das Timeout kann durch einen Aufrufder [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) -Funktion aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="23703-105">The timeout can be enabled with a call to the [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) function.</span></span> <span data-ttu-id="23703-106">In der folgenden Liste sind die gültigen Timeout Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="23703-106">The following list contains the valid time-out values.</span></span>



| <span data-ttu-id="23703-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="23703-107">Constant/value</span></span>                                                                                                                                                                                                                                                                | <span data-ttu-id="23703-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23703-108">Description</span></span>                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <span data-ttu-id="23703-109"><dt>**RPC \_ C- \_ Bindung \_ unendlich \_ Timeout**</dt> <dt> 10</dt></span><span class="sxs-lookup"><span data-stu-id="23703-109"><dt>**RPC\_C\_BINDING\_INFINITE\_TIMEOUT**</dt> <dt> 10 </dt></span></span> </dl> | <span data-ttu-id="23703-110">Versucht immer, die Kommunikation immer wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="23703-110">Keeps trying to establish communications forever.</span></span><br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <span data-ttu-id="23703-111"><dt>**RPC \_ C- \_ Bindung \_ Min. \_ Timeout**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="23703-111"><dt>**RPC\_C\_BINDING\_MIN\_TIMEOUT**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="23703-112">Versucht, die minimale Zeitspanne für das verwendete Netzwerkprotokoll zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="23703-112">Tries the minimum amount of time for the network protocol being used.</span></span> <span data-ttu-id="23703-113">Dieser Wert begünstigt die Reaktionszeit gegenüber der Richtigkeit bei der Bestimmung, ob der Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23703-113">This value favors response time over correctness in determining whether the server is running.</span></span><br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <span data-ttu-id="23703-114"><dt>**RPC \_ C- \_ Bindungs \_ Standard \_ Timeout**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="23703-114"><dt>**RPC\_C\_BINDING\_DEFAULT\_TIMEOUT**</dt> <dt>5</dt></span></span> </dl>       | <span data-ttu-id="23703-115">Versucht eine durchschnittliche Zeitspanne für das verwendete Netzwerkprotokoll.</span><span class="sxs-lookup"><span data-stu-id="23703-115">Tries an average amount of time for the network protocol being used.</span></span> <span data-ttu-id="23703-116">Mit diesem Wert wird festgelegt, ob ein Server ausgeführt wird und wie die Antwortzeit Gleichgewicht ist.</span><span class="sxs-lookup"><span data-stu-id="23703-116">This value gives correctness in determining whether a server is running and gives response time equal weight.</span></span> <span data-ttu-id="23703-117">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="23703-117">This is the default value.</span></span><br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <span data-ttu-id="23703-118"><dt>**RPC \_ C- \_ Bindung \_ Max. \_ Timeout**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="23703-118"><dt>**RPC\_C\_BINDING\_MAX\_TIMEOUT**</dt> <dt>9</dt></span></span> </dl>                   | <span data-ttu-id="23703-119">Versucht den längsten Zeitraum für das verwendete Netzwerkprotokoll.</span><span class="sxs-lookup"><span data-stu-id="23703-119">Tries the longest amount of time for the network protocol being used.</span></span> <span data-ttu-id="23703-120">Dieser Wert begünstigt die Richtigkeit bei der Bestimmung, ob ein Server mit der Antwortzeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23703-120">This value favors correctness in determining whether a server is running over response time.</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="23703-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23703-121">Remarks</span></span>

<span data-ttu-id="23703-122">Die Werte in der vorangehenden Tabelle liegen nicht in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="23703-122">The values in the preceding table are not in seconds.</span></span> <span data-ttu-id="23703-123">Diese Werte stellen eine relative Zeitspanne auf einer Skala von 0 bis 10 dar.</span><span class="sxs-lookup"><span data-stu-id="23703-123">These values represent a relative amount of time on a scale of zero to 10.</span></span> <span data-ttu-id="23703-124">Weitere Informationen zum Vermeiden von Kommunikations Verzögerungen finden Sie unter verhindern von Client seitigen warte Vorhängen.</span><span class="sxs-lookup"><span data-stu-id="23703-124">For more information on avoiding communication delays, refer to Preventing Client-side Hangs.</span></span>

## <a name="requirements"></a><span data-ttu-id="23703-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23703-125">Requirements</span></span>



| <span data-ttu-id="23703-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23703-126">Requirement</span></span> | <span data-ttu-id="23703-127">Wert</span><span class="sxs-lookup"><span data-stu-id="23703-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="23703-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23703-128">Minimum supported client</span></span><br/> | <span data-ttu-id="23703-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23703-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="23703-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23703-130">Minimum supported server</span></span><br/> | <span data-ttu-id="23703-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23703-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="23703-132">Header</span><span class="sxs-lookup"><span data-stu-id="23703-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="23703-133"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="23703-133"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





