---
description: 'IDelaydC::D isconnect-Methode: Die Disconnect-Methode trennt das NPP vom Netzwerk.'
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: IDelaydC::D isconnect-Methode (Netmon.h)
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
ms.openlocfilehash: 967bd9674cb28363804b8c8af12c541bcb8675ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110808"
---
# <a name="idelaydcdisconnect-method"></a><span data-ttu-id="f86ce-103">IDelaydC::D isconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="f86ce-103">IDelaydC::Disconnect method</span></span>

<span data-ttu-id="f86ce-104">Die **Disconnect-Methode** trennt den Netzwerk-NPP vom Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f86ce-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="f86ce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f86ce-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="f86ce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f86ce-106">Parameters</span></span>

<span data-ttu-id="f86ce-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f86ce-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f86ce-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f86ce-108">Return value</span></span>

<span data-ttu-id="f86ce-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="f86ce-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f86ce-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="f86ce-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="f86ce-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f86ce-111">Return code</span></span>                                                                                          | <span data-ttu-id="f86ce-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f86ce-112">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f86ce-113"><dt>**NMERR-ERFASSUNG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f86ce-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="f86ce-114">Das NPP erfasst Daten.</span><span class="sxs-lookup"><span data-stu-id="f86ce-114">The NPP is capturing data.</span></span> <span data-ttu-id="f86ce-115">Sie können das Netzwerksicherheits-Netzwerk während einer Erfassung nicht vom Netzwerk trennen.</span><span class="sxs-lookup"><span data-stu-id="f86ce-115">You cannot disconnect the NPP from the network during a capture.</span></span><br/>            |
| <dl> <span data-ttu-id="f86ce-116"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="f86ce-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="f86ce-117">Der NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="f86ce-117">The NPP is not connected to the network.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="f86ce-118"><dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt></span><span class="sxs-lookup"><span data-stu-id="f86ce-118"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="f86ce-119">Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IDelaydC::Connect-Methode.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="f86ce-119">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f86ce-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f86ce-120">Remarks</span></span>

<span data-ttu-id="f86ce-121">Diese Methode kann nicht aufgerufen werden, wenn der NPP Daten erfasst.</span><span class="sxs-lookup"><span data-stu-id="f86ce-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="f86ce-122">Sie müssen die **IDelaydC::Stop-Methode aufrufen,** bevor Sie **Disconnect aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="f86ce-122">You must call the **IDelaydC::Stop** method before calling **Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f86ce-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f86ce-123">Requirements</span></span>



| <span data-ttu-id="f86ce-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f86ce-124">Requirement</span></span> | <span data-ttu-id="f86ce-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f86ce-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f86ce-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f86ce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f86ce-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f86ce-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="f86ce-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f86ce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f86ce-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f86ce-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="f86ce-130">Header</span><span class="sxs-lookup"><span data-stu-id="f86ce-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f86ce-131"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="f86ce-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="f86ce-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f86ce-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f86ce-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f86ce-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f86ce-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f86ce-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f86ce-135">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="f86ce-135">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="f86ce-136">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="f86ce-136">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="f86ce-137">IDelaydC::Stop</span><span class="sxs-lookup"><span data-stu-id="f86ce-137">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




