---
description: Mit der Disconnect-Methode wird die Netzwerkverbindung mit dem Netzwerk getrennt.
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: Untc::D isconnect-Methode (Netmon. h)
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
ms.openlocfilehash: df58d6ac0e61ecc370510474c3bc067726d9824b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215472"
---
# <a name="irtcdisconnect-method"></a><span data-ttu-id="27563-103">Untc::D isconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="27563-103">IRTC::Disconnect method</span></span>

<span data-ttu-id="27563-104">Mit der **Disconnect** -Methode wird die Netzwerkverbindung mit dem Netzwerk getrennt.</span><span class="sxs-lookup"><span data-stu-id="27563-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="27563-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="27563-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="27563-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="27563-106">Parameters</span></span>

<span data-ttu-id="27563-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="27563-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27563-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27563-108">Return value</span></span>

<span data-ttu-id="27563-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="27563-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="27563-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="27563-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="27563-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="27563-111">Return code</span></span>                                                                                          | <span data-ttu-id="27563-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27563-112">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="27563-113"><dt>**nmerr- \_ Erfassung**</dt></span><span class="sxs-lookup"><span data-stu-id="27563-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="27563-114">Der NPP erfasst Daten.</span><span class="sxs-lookup"><span data-stu-id="27563-114">The NPP is capturing data.</span></span> <span data-ttu-id="27563-115">Die Verbindung mit dem Netzwerk kann während der Datenerfassung nicht getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="27563-115">You cannot disconnect from the network while the data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="27563-116"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="27563-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="27563-117">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="27563-117">The NPP is not connected to the network.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="27563-118"><dt>**nmerr \_ nicht in \_ Echtzeit**</dt></span><span class="sxs-lookup"><span data-stu-id="27563-118"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="27563-119">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".</span><span class="sxs-lookup"><span data-stu-id="27563-119">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="27563-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27563-120">Remarks</span></span>

<span data-ttu-id="27563-121">Diese Methode kann nicht aufgerufen werden, wenn der NPP Daten erfasst.</span><span class="sxs-lookup"><span data-stu-id="27563-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="27563-122">Vor dem Aufrufen von "untc::D isconnect" müssen Sie die " [untc:: Beendigung](irtc-stop.md) "-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="27563-122">You must call the [IRTC::Stop](irtc-stop.md) method before calling IRTC::Disconnect.</span></span>

## <a name="requirements"></a><span data-ttu-id="27563-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27563-123">Requirements</span></span>



| <span data-ttu-id="27563-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27563-124">Requirement</span></span> | <span data-ttu-id="27563-125">Wert</span><span class="sxs-lookup"><span data-stu-id="27563-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27563-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27563-126">Minimum supported client</span></span><br/> | <span data-ttu-id="27563-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27563-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="27563-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27563-128">Minimum supported server</span></span><br/> | <span data-ttu-id="27563-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27563-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="27563-130">Header</span><span class="sxs-lookup"><span data-stu-id="27563-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="27563-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="27563-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="27563-132">DLL</span><span class="sxs-lookup"><span data-stu-id="27563-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27563-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27563-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27563-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27563-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27563-135">"Iran"</span><span class="sxs-lookup"><span data-stu-id="27563-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="27563-136">Iran:: Connect</span><span class="sxs-lookup"><span data-stu-id="27563-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="27563-137">Iran:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="27563-137">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




