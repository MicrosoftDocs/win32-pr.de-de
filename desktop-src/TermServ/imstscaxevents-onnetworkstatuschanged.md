---
title: Imstscaxevents onnetworkstatuschangi-Methode
description: Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat. | Imstscaxevents onnetworkstatuschangi-Methode
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- Onnetworkstatuschangi-Methode Remotedesktopdienste
- Onnetworkstatuschangi-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onnetworkstatuschangi-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363909"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a><span data-ttu-id="378ac-107">Imstscaxevents:: onnetworkstatuschangi-Methode</span><span class="sxs-lookup"><span data-stu-id="378ac-107">IMsTscAxEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="378ac-108">Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="378ac-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="378ac-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="378ac-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a><span data-ttu-id="378ac-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="378ac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="378ac-111">*qualitylevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="378ac-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378ac-112">Gibt die neue Verbindungsgeschwindigkeit an.</span><span class="sxs-lookup"><span data-stu-id="378ac-112">Specifies the new connection speed.</span></span> <span data-ttu-id="378ac-113">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="378ac-113">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="378ac-114">1</span><span class="sxs-lookup"><span data-stu-id="378ac-114">1</span></span>
</dt> <dd>

<span data-ttu-id="378ac-115">Weniger als 512 Kilobyte pro Sekunde (Kbit/s).</span><span class="sxs-lookup"><span data-stu-id="378ac-115">Less than 512 kilobytes per second (KBps).</span></span>

</dd> <dt>

<span data-ttu-id="378ac-116">2</span><span class="sxs-lookup"><span data-stu-id="378ac-116">2</span></span>
</dt> <dd>

<span data-ttu-id="378ac-117">512 bis 1.999 Kbit/s.</span><span class="sxs-lookup"><span data-stu-id="378ac-117">512 to 1,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="378ac-118">3</span><span class="sxs-lookup"><span data-stu-id="378ac-118">3</span></span>
</dt> <dd>

<span data-ttu-id="378ac-119">2.000 bis 9.999 Kbit/s.</span><span class="sxs-lookup"><span data-stu-id="378ac-119">2,000 to 9,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="378ac-120">4</span><span class="sxs-lookup"><span data-stu-id="378ac-120">4</span></span>
</dt> <dd>

<span data-ttu-id="378ac-121">Größer oder gleich 10.000 Kbit/s.</span><span class="sxs-lookup"><span data-stu-id="378ac-121">Greater than or equal to 10,000 KBps.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="378ac-122">*Bandbreite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="378ac-122">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378ac-123">Gibt die Verbindungs Bandbreite an.</span><span class="sxs-lookup"><span data-stu-id="378ac-123">Specifies the connection bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="378ac-124">*RTT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="378ac-124">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378ac-125">Gibt die Verbindungs Latenz an.</span><span class="sxs-lookup"><span data-stu-id="378ac-125">Specifies the connection latency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="378ac-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="378ac-126">Return value</span></span>

<span data-ttu-id="378ac-127">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="378ac-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="378ac-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="378ac-128">Requirements</span></span>



| <span data-ttu-id="378ac-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="378ac-129">Requirement</span></span> | <span data-ttu-id="378ac-130">Wert</span><span class="sxs-lookup"><span data-stu-id="378ac-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="378ac-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="378ac-131">Minimum supported client</span></span><br/> | <span data-ttu-id="378ac-132">Windows 8</span><span class="sxs-lookup"><span data-stu-id="378ac-132">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="378ac-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="378ac-133">Minimum supported server</span></span><br/> | <span data-ttu-id="378ac-134">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="378ac-134">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="378ac-135">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="378ac-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="378ac-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="378ac-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="378ac-137">DLL</span><span class="sxs-lookup"><span data-stu-id="378ac-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="378ac-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="378ac-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="378ac-139">IID</span><span class="sxs-lookup"><span data-stu-id="378ac-139">IID</span></span><br/>                      | <span data-ttu-id="378ac-140">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="378ac-140">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="378ac-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="378ac-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="378ac-142">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="378ac-142">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





