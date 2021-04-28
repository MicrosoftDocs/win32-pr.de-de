---
description: 'IRTC::Stop-Methode: Die Stop-Methode beendet die aktuelle Erfassung.'
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: IRTC::Stop-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 10bf0886032c93288435ade05fec46077d53753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113518"
---
# <a name="irtcstop-method"></a><span data-ttu-id="ac0c8-103">IRTC::Stop-Methode</span><span class="sxs-lookup"><span data-stu-id="ac0c8-103">IRTC::Stop method</span></span>

<span data-ttu-id="ac0c8-104">Die **Stop-Methode** beendet die aktuelle Erfassung.</span><span class="sxs-lookup"><span data-stu-id="ac0c8-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac0c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac0c8-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="ac0c8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac0c8-106">Parameters</span></span>

<span data-ttu-id="ac0c8-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ac0c8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac0c8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac0c8-108">Return value</span></span>

<span data-ttu-id="ac0c8-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="ac0c8-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ac0c8-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="ac0c8-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="ac0c8-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ac0c8-111">Return code</span></span>                                                                                          | <span data-ttu-id="ac0c8-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac0c8-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac0c8-113"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="ac0c8-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ac0c8-114">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="ac0c8-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="ac0c8-115">Rufen [Sie IRTC::Connect auf,](irtc-connect.md) um das NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="ac0c8-115">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="ac0c8-116"><dt>**NMERR \_ WIRD NICHT \_ ERFASST**</dt></span><span class="sxs-lookup"><span data-stu-id="ac0c8-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="ac0c8-117">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="ac0c8-117">The NPP is not capturing data.</span></span> <span data-ttu-id="ac0c8-118">Rufen Sie [IRTC::Start auf,](irtc-start.md) um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="ac0c8-118">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="ac0c8-119"><dt>**NMERR \_ NOT \_ REALTIME**</dt></span><span class="sxs-lookup"><span data-stu-id="ac0c8-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="ac0c8-120">Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IRTC::Connect-Methode.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="ac0c8-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="ac0c8-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac0c8-121">Remarks</span></span>

<span data-ttu-id="ac0c8-122">Wenn Sie die Erfassung nach dem Aufruf der **IRTC::Stop-Methode** neu starten, müssen Sie jedes Mal [IRTC::Configure](irtc-configure.md) aufrufen, wenn Sie [IRTC::Start](irtc-start.md) aufrufen, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="ac0c8-122">When you restart the capture after calling the **IRTC::Stop** method, make sure to call [IRTC::Configure](irtc-configure.md) each time you call [IRTC::Start](irtc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac0c8-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac0c8-123">Requirements</span></span>



| <span data-ttu-id="ac0c8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac0c8-124">Requirement</span></span> | <span data-ttu-id="ac0c8-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ac0c8-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac0c8-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac0c8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ac0c8-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac0c8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ac0c8-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac0c8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ac0c8-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac0c8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ac0c8-130">Header</span><span class="sxs-lookup"><span data-stu-id="ac0c8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac0c8-131"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="ac0c8-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ac0c8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ac0c8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac0c8-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac0c8-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac0c8-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ac0c8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac0c8-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="ac0c8-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="ac0c8-136">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="ac0c8-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="ac0c8-137">IRTC::Configure</span><span class="sxs-lookup"><span data-stu-id="ac0c8-137">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="ac0c8-138">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="ac0c8-138">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




