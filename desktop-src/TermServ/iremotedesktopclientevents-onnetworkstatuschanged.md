---
title: Iremotedesktopclientevents onnetworkstatuschangi-Methode
description: Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat. | Iremotedesktopclientevents onnetworkstatuschangi-Methode
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- Onnetworkstatuschangi-Methode Remotedesktopdienste
- Onnetworkstatuschangi-Methode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, onnetworkstatuschangi-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de64d8b16ea9acf9defc976d4baa91afd64f8fa7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530662"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a><span data-ttu-id="c802d-107">Iremotedesktopclientevents:: onnetworkstatuschangi-Methode</span><span class="sxs-lookup"><span data-stu-id="c802d-107">IRemoteDesktopClientEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="c802d-108">Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="c802d-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c802d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c802d-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] unsigned long qualityLevel,
  [in] long          bandwidth,
  [in] long          rtt
);
```



## <a name="parameters"></a><span data-ttu-id="c802d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c802d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c802d-111">*qualitylevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c802d-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c802d-112">Die neue Qualitätsstufe der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c802d-112">The new quality level of the connection.</span></span> <span data-ttu-id="c802d-113">Die Qualitätsstufe wird von den Werten für Bandbreite und Roundtrip-Zeit (RTT) bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c802d-113">The quality level is determined from the bandwidth and round-trip time (rtt) values.</span></span>

<span data-ttu-id="c802d-114">Einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="c802d-114">One of the following values.</span></span>



| <span data-ttu-id="c802d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c802d-115">Value</span></span>                                                                        | <span data-ttu-id="c802d-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c802d-116">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="c802d-117"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c802d-117"><dt>0</dt></span></span> </dl> | <span data-ttu-id="c802d-118">Die Qualitätsstufe konnte nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="c802d-118">The quality level could not be determined.</span></span><br/>       |
| <dl> <span data-ttu-id="c802d-119"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c802d-119"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c802d-120">Die Verbindungsqualität ist "schlecht" (ein Balken).</span><span class="sxs-lookup"><span data-stu-id="c802d-120">The connection quality is poor (one bar).</span></span><br/>        |
| <dl> <span data-ttu-id="c802d-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c802d-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c802d-122">Die Verbindungsqualität ist fair (zwei Balken).</span><span class="sxs-lookup"><span data-stu-id="c802d-122">The connection quality is fair (two bars).</span></span><br/>       |
| <dl> <span data-ttu-id="c802d-123"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c802d-123"><dt>3</dt></span></span> </dl> | <span data-ttu-id="c802d-124">Die Verbindungsqualität ist gut (drei Balken).</span><span class="sxs-lookup"><span data-stu-id="c802d-124">The connection quality is good (three bars).</span></span><br/>     |
| <dl> <span data-ttu-id="c802d-125"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c802d-125"><dt>4</dt></span></span> </dl> | <span data-ttu-id="c802d-126">Die Verbindungsqualität ist hervorragend (vier Balken).</span><span class="sxs-lookup"><span data-stu-id="c802d-126">The connection quality is excellent (four bars).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c802d-127">*Bandbreite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c802d-127">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c802d-128">Gibt die neue Verbindungs Bandbreite in Kbit pro Sekunde (Kbit/s) an.</span><span class="sxs-lookup"><span data-stu-id="c802d-128">Specifies the new connection bandwidth, in kilobits per second (Kbps).</span></span>

</dd> <dt>

<span data-ttu-id="c802d-129">*RTT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c802d-129">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c802d-130">Gibt die neue Roundtripzeit der Verbindung (Latenzzeit) in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="c802d-130">Specifies the new connection roundtrip time (latency), in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c802d-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c802d-131">Return value</span></span>

<span data-ttu-id="c802d-132">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c802d-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c802d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c802d-133">Requirements</span></span>



| <span data-ttu-id="c802d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c802d-134">Requirement</span></span> | <span data-ttu-id="c802d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="c802d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c802d-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c802d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c802d-137">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c802d-137">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="c802d-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c802d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c802d-139">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c802d-139">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="c802d-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c802d-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="c802d-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c802d-141"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="c802d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c802d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c802d-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c802d-143"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="c802d-144">IID</span><span class="sxs-lookup"><span data-stu-id="c802d-144">IID</span></span><br/>                      | <span data-ttu-id="c802d-145">Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.</span><span class="sxs-lookup"><span data-stu-id="c802d-145">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c802d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c802d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c802d-147">**Iremotedesktopclientevents**</span><span class="sxs-lookup"><span data-stu-id="c802d-147">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





