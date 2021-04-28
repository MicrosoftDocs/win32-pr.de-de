---
description: 'IESP::D isconnect-Methode: Die Disconnect-Methode trennt den NPP vom Netzwerk.'
ms.assetid: 962e033d-a51c-47a2-83dc-cee1e7150ab8
title: IESP::D isconnect-Methode (Netmon.h)
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
ms.openlocfilehash: d0a07748781a567c889e879e2e99462d8cfb876a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110758"
---
# <a name="iespdisconnect-method"></a><span data-ttu-id="2853c-103">IESP::D isconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="2853c-103">IESP::Disconnect method</span></span>

<span data-ttu-id="2853c-104">Die **Disconnect-Methode** trennt den Netzwerk-NPP vom Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2853c-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="2853c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2853c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="2853c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2853c-106">Parameters</span></span>

<span data-ttu-id="2853c-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2853c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2853c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2853c-108">Return value</span></span>

<span data-ttu-id="2853c-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="2853c-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2853c-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="2853c-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="2853c-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2853c-111">Return code</span></span>                                                                                          | <span data-ttu-id="2853c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2853c-112">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2853c-113"><dt>**NMERR-ERFASSUNG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2853c-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="2853c-114">Das NPP erfasst Daten.</span><span class="sxs-lookup"><span data-stu-id="2853c-114">The NPP is capturing data.</span></span> <span data-ttu-id="2853c-115">Sie können die Verbindung mit dem Netzwerk nicht trennen, während die Datenerfassung läuft.</span><span class="sxs-lookup"><span data-stu-id="2853c-115">You cannot disconnect from the network while data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="2853c-116"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="2853c-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2853c-117">Der NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="2853c-117">The NPP is not connected to the network.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="2853c-118"><dt>**NMERR \_ NICHT \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="2853c-118"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="2853c-119">Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IESP::Connect-Methode.](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="2853c-119">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="2853c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2853c-120">Remarks</span></span>

<span data-ttu-id="2853c-121">Diese Methode kann nicht aufgerufen werden, wenn der NPP Daten erfasst.</span><span class="sxs-lookup"><span data-stu-id="2853c-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="2853c-122">Sie müssen die **IESP::Stop-Methode aufrufen,** bevor **Sie IESP::D isconnect aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="2853c-122">You must call the **IESP::Stop** method before calling **IESP::Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2853c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2853c-123">Requirements</span></span>



| <span data-ttu-id="2853c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2853c-124">Requirement</span></span> | <span data-ttu-id="2853c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2853c-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2853c-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2853c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2853c-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2853c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2853c-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2853c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2853c-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2853c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2853c-130">Header</span><span class="sxs-lookup"><span data-stu-id="2853c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2853c-131"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="2853c-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2853c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2853c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2853c-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2853c-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2853c-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2853c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2853c-135">IESP</span><span class="sxs-lookup"><span data-stu-id="2853c-135">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="2853c-136">IESP::Connect</span><span class="sxs-lookup"><span data-stu-id="2853c-136">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="2853c-137">IESP::Stop</span><span class="sxs-lookup"><span data-stu-id="2853c-137">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




