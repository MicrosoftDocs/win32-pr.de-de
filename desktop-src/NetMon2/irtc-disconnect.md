---
description: 'IRTC::D isconnect-Methode: Die Disconnect-Methode trennt den NPP vom Netzwerk.'
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: IRTC::D isconnect-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 43acb88e2c7b6108a162c4715de02375121021f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110718"
---
# <a name="irtcdisconnect-method"></a><span data-ttu-id="385a2-103">IRTC::D isconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="385a2-103">IRTC::Disconnect method</span></span>

<span data-ttu-id="385a2-104">Die **Disconnect-Methode** trennt den Netzwerk-NPP vom Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="385a2-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="385a2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="385a2-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="385a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="385a2-106">Parameters</span></span>

<span data-ttu-id="385a2-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="385a2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="385a2-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="385a2-108">Return value</span></span>

<span data-ttu-id="385a2-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="385a2-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="385a2-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="385a2-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="385a2-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="385a2-111">Return code</span></span>                                                                                          | <span data-ttu-id="385a2-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="385a2-112">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="385a2-113"><dt>**NMERR-ERFASSUNG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="385a2-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="385a2-114">Das NPP erfasst Daten.</span><span class="sxs-lookup"><span data-stu-id="385a2-114">The NPP is capturing data.</span></span> <span data-ttu-id="385a2-115">Sie können die Verbindung mit dem Netzwerk nicht trennen, während die Datenerfassung läuft.</span><span class="sxs-lookup"><span data-stu-id="385a2-115">You cannot disconnect from the network while the data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="385a2-116"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="385a2-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="385a2-117">Der NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="385a2-117">The NPP is not connected to the network.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="385a2-118"><dt>**NMERR \_ NOT \_ REALTIME**</dt></span><span class="sxs-lookup"><span data-stu-id="385a2-118"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="385a2-119">Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IRTC::Connect-Methode.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="385a2-119">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="385a2-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="385a2-120">Remarks</span></span>

<span data-ttu-id="385a2-121">Diese Methode kann nicht aufgerufen werden, wenn der NPP Daten erfasst.</span><span class="sxs-lookup"><span data-stu-id="385a2-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="385a2-122">Sie müssen die [IRTC::Stop-Methode aufrufen,](irtc-stop.md) bevor Sie IRTC::D isconnect aufrufen.</span><span class="sxs-lookup"><span data-stu-id="385a2-122">You must call the [IRTC::Stop](irtc-stop.md) method before calling IRTC::Disconnect.</span></span>

## <a name="requirements"></a><span data-ttu-id="385a2-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="385a2-123">Requirements</span></span>



| <span data-ttu-id="385a2-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="385a2-124">Requirement</span></span> | <span data-ttu-id="385a2-125">Wert</span><span class="sxs-lookup"><span data-stu-id="385a2-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="385a2-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="385a2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="385a2-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="385a2-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="385a2-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="385a2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="385a2-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="385a2-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="385a2-130">Header</span><span class="sxs-lookup"><span data-stu-id="385a2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="385a2-131"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="385a2-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="385a2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="385a2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="385a2-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="385a2-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="385a2-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="385a2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="385a2-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="385a2-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="385a2-136">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="385a2-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="385a2-137">IRTC::Stop</span><span class="sxs-lookup"><span data-stu-id="385a2-137">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




