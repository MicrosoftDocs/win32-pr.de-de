---
description: Trennt die NPP vom Netzwerk.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: IStats::D isconnect-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a5fa56c05036380b5dba42089979b43d776a4b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347720"
---
# <a name="istatsdisconnect-method"></a><span data-ttu-id="725a7-103">IStats::D isconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="725a7-103">IStats::Disconnect method</span></span>

<span data-ttu-id="725a7-104">Mit der **Disconnect** -Methode wird die Netzwerkverbindung mit dem Netzwerk getrennt.</span><span class="sxs-lookup"><span data-stu-id="725a7-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="725a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="725a7-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="725a7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="725a7-106">Parameters</span></span>

<span data-ttu-id="725a7-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="725a7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="725a7-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="725a7-108">Return value</span></span>

<span data-ttu-id="725a7-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="725a7-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="725a7-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="725a7-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="725a7-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="725a7-111">Return code</span></span>                                                                                            | <span data-ttu-id="725a7-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="725a7-112">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="725a7-113"><dt>**nmerr- \_ Erfassung**</dt></span><span class="sxs-lookup"><span data-stu-id="725a7-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="725a7-114">Der NPP erfasst derzeit Daten.</span><span class="sxs-lookup"><span data-stu-id="725a7-114">The NPP is currently capturing data.</span></span> <span data-ttu-id="725a7-115">Die Verbindung mit dem Netzwerk kann während der Datenerfassung nicht getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="725a7-115">You cannot disconnect from the network while a data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="725a7-116"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="725a7-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="725a7-117">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="725a7-117">The NPP is not connected to the network.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="725a7-118"><dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt></span><span class="sxs-lookup"><span data-stu-id="725a7-118"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="725a7-119">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [**iStats:: Connect**](istats-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="725a7-119">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="725a7-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="725a7-120">Remarks</span></span>

<span data-ttu-id="725a7-121">Diese Methode kann nicht aufgerufen werden, wenn der NPP Daten erfasst.</span><span class="sxs-lookup"><span data-stu-id="725a7-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="725a7-122">Nennen Sie zuerst die **iStats::D isconnect** -Methode, und klicken Sie dann auf [**iStats:: Beendigung**](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="725a7-122">Call the **IStats::Disconnect** method first and then call [**IStats::Stop**](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="725a7-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="725a7-123">Requirements</span></span>



| <span data-ttu-id="725a7-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="725a7-124">Requirement</span></span> | <span data-ttu-id="725a7-125">Wert</span><span class="sxs-lookup"><span data-stu-id="725a7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="725a7-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="725a7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="725a7-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="725a7-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="725a7-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="725a7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="725a7-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="725a7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="725a7-130">Header</span><span class="sxs-lookup"><span data-stu-id="725a7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="725a7-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="725a7-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="725a7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="725a7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="725a7-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="725a7-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="725a7-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="725a7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="725a7-135">**IStats**</span><span class="sxs-lookup"><span data-stu-id="725a7-135">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="725a7-136">**IStats:: Connect**</span><span class="sxs-lookup"><span data-stu-id="725a7-136">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="725a7-137">**IStats:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="725a7-137">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 




