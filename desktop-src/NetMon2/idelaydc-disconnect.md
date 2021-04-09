---
description: Mit der Disconnect-Methode wird die Netzwerkverbindung mit dem Netzwerk getrennt.
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: Idelta-DC::D isconnect-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d192aa80f543706eea4bc197bc3dc8d57dd64aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128336"
---
# <a name="idelaydcdisconnect-method"></a><span data-ttu-id="5222a-103">Idelta-DC::D isconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="5222a-103">IDelaydC::Disconnect method</span></span>

<span data-ttu-id="5222a-104">Mit der **Disconnect** -Methode wird die Netzwerkverbindung mit dem Netzwerk getrennt.</span><span class="sxs-lookup"><span data-stu-id="5222a-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="5222a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5222a-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="5222a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5222a-106">Parameters</span></span>

<span data-ttu-id="5222a-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5222a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5222a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5222a-108">Return value</span></span>

<span data-ttu-id="5222a-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5222a-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5222a-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="5222a-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="5222a-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5222a-111">Return code</span></span>                                                                                          | <span data-ttu-id="5222a-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5222a-112">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5222a-113"><dt>**nmerr- \_ Erfassung**</dt></span><span class="sxs-lookup"><span data-stu-id="5222a-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="5222a-114">Der NPP erfasst Daten.</span><span class="sxs-lookup"><span data-stu-id="5222a-114">The NPP is capturing data.</span></span> <span data-ttu-id="5222a-115">Sie können den NPP während einer Erfassung nicht vom Netzwerk trennen.</span><span class="sxs-lookup"><span data-stu-id="5222a-115">You cannot disconnect the NPP from the network during a capture.</span></span><br/>            |
| <dl> <span data-ttu-id="5222a-116"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="5222a-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5222a-117">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="5222a-117">The NPP is not connected to the network.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="5222a-118"><dt>**nmerr \_ nicht \_ verzögert**</dt></span><span class="sxs-lookup"><span data-stu-id="5222a-118"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="5222a-119">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [idelta aydc:: Connect](idelaydc-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5222a-119">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5222a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5222a-120">Remarks</span></span>

<span data-ttu-id="5222a-121">Diese Methode kann nicht aufgerufen werden, wenn der NPP Daten erfasst.</span><span class="sxs-lookup"><span data-stu-id="5222a-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="5222a-122">Vor dem Aufrufen von **Disconnect** muss die **idelta-DC:: beenden** -Methode aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5222a-122">You must call the **IDelaydC::Stop** method before calling **Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5222a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5222a-123">Requirements</span></span>



| <span data-ttu-id="5222a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5222a-124">Requirement</span></span> | <span data-ttu-id="5222a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5222a-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5222a-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5222a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5222a-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5222a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="5222a-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5222a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5222a-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5222a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="5222a-130">Header</span><span class="sxs-lookup"><span data-stu-id="5222a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5222a-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5222a-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="5222a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5222a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5222a-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5222a-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5222a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5222a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5222a-135">Idelta-DC</span><span class="sxs-lookup"><span data-stu-id="5222a-135">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="5222a-136">Idelta aydc:: Connect</span><span class="sxs-lookup"><span data-stu-id="5222a-136">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="5222a-137">Idelta aydc:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="5222a-137">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




