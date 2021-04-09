---
description: Mit der Disconnect-Methode wird die Netzwerkverbindung mit dem Netzwerk getrennt.
ms.assetid: 962e033d-a51c-47a2-83dc-cee1e7150ab8
title: IESP::D isconnect-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b0dac1843083d77121883b2609c32addffbae290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128328"
---
# <a name="iespdisconnect-method"></a><span data-ttu-id="74f99-103">IESP::D isconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="74f99-103">IESP::Disconnect method</span></span>

<span data-ttu-id="74f99-104">Mit der **Disconnect** -Methode wird die Netzwerkverbindung mit dem Netzwerk getrennt.</span><span class="sxs-lookup"><span data-stu-id="74f99-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f99-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="74f99-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="74f99-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="74f99-106">Parameters</span></span>

<span data-ttu-id="74f99-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="74f99-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74f99-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74f99-108">Return value</span></span>

<span data-ttu-id="74f99-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="74f99-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="74f99-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="74f99-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="74f99-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="74f99-111">Return code</span></span>                                                                                          | <span data-ttu-id="74f99-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74f99-112">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74f99-113"><dt>**nmerr- \_ Erfassung**</dt></span><span class="sxs-lookup"><span data-stu-id="74f99-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="74f99-114">Der NPP erfasst Daten.</span><span class="sxs-lookup"><span data-stu-id="74f99-114">The NPP is capturing data.</span></span> <span data-ttu-id="74f99-115">Die Verbindung mit dem Netzwerk kann während der Datenerfassung nicht getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="74f99-115">You cannot disconnect from the network while data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="74f99-116"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="74f99-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="74f99-117">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="74f99-117">The NPP is not connected to the network.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="74f99-118"><dt>**nmerr \_ nicht \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="74f99-118"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="74f99-119">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iESP:: Connect](iesp-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="74f99-119">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="74f99-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74f99-120">Remarks</span></span>

<span data-ttu-id="74f99-121">Diese Methode kann nicht aufgerufen werden, wenn der NPP Daten erfasst.</span><span class="sxs-lookup"><span data-stu-id="74f99-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="74f99-122">Sie müssen vor dem Aufrufen von **iESP::D isconnect** die **iESP:: Station** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="74f99-122">You must call the **IESP::Stop** method before calling **IESP::Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="74f99-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74f99-123">Requirements</span></span>



| <span data-ttu-id="74f99-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74f99-124">Requirement</span></span> | <span data-ttu-id="74f99-125">Wert</span><span class="sxs-lookup"><span data-stu-id="74f99-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74f99-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74f99-126">Minimum supported client</span></span><br/> | <span data-ttu-id="74f99-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74f99-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="74f99-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74f99-128">Minimum supported server</span></span><br/> | <span data-ttu-id="74f99-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74f99-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="74f99-130">Header</span><span class="sxs-lookup"><span data-stu-id="74f99-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="74f99-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="74f99-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="74f99-132">DLL</span><span class="sxs-lookup"><span data-stu-id="74f99-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74f99-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74f99-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74f99-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74f99-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f99-135">IESP</span><span class="sxs-lookup"><span data-stu-id="74f99-135">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="74f99-136">IESP:: Connect</span><span class="sxs-lookup"><span data-stu-id="74f99-136">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="74f99-137">IESP:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="74f99-137">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




