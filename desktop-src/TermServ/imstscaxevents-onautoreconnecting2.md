---
title: Imstscaxevents OnAutoReconnecting2-Methode
description: Wird aufgerufen, wenn ein Client gerade eine Sitzung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server automatisch erneut verbindet. | Imstscaxevents OnAutoReconnecting2-Methode
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- OnAutoReconnecting2-Methode Remotedesktopdienste
- OnAutoReconnecting2-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, OnAutoReconnecting2-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901bb196922d1772782ab7f1c911c96573c88b36
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353321"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a><span data-ttu-id="6ba3b-107">Imstscaxevents:: OnAutoReconnecting2-Methode</span><span class="sxs-lookup"><span data-stu-id="6ba3b-107">IMsTscAxEvents::OnAutoReconnecting2 method</span></span>

<span data-ttu-id="6ba3b-108">Wird aufgerufen, wenn ein Client gerade eine Sitzung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server automatisch erneut verbindet.</span><span class="sxs-lookup"><span data-stu-id="6ba3b-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="6ba3b-109">Dies ist eine erweiterte Version der [**onautoreconnecting**](-imstscaxevents--onautoreconnecting.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6ba3b-109">This is an enhanced version of the [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba3b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ba3b-110">Syntax</span></span>


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="6ba3b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ba3b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ba3b-112">*disconnecverrat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ba3b-112">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba3b-113">Code, der den Grund für das letzte Trennen der Sitzung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6ba3b-113">Code that describes the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="6ba3b-114">*NetworkAvailable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ba3b-114">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba3b-115">Gibt an, ob das Netzwerk verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6ba3b-115">Specifies if the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="6ba3b-116">*Anzahl* \[ der Versuche in\]</span><span class="sxs-lookup"><span data-stu-id="6ba3b-116">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba3b-117">Anzahl der Versuche, die im aktuellen automatischen erneuten Verbindungsvorgang durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="6ba3b-117">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="6ba3b-118">Diese Anzahl wird für jeden erfolgten Versuch um eins erhöht.</span><span class="sxs-lookup"><span data-stu-id="6ba3b-118">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="6ba3b-119">*maxder-Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ba3b-119">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba3b-120">Die maximale Anzahl der Versuche, die beim aktuellen automatischen erneuten Verbindungsvorgang durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6ba3b-120">The maximum number of attempts that will be made in the current automatic reconnection process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ba3b-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ba3b-121">Return value</span></span>

<span data-ttu-id="6ba3b-122">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6ba3b-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba3b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ba3b-123">Requirements</span></span>



| <span data-ttu-id="6ba3b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ba3b-124">Requirement</span></span> | <span data-ttu-id="6ba3b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6ba3b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba3b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ba3b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6ba3b-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6ba3b-127">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="6ba3b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ba3b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6ba3b-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ba3b-129">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="6ba3b-130">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6ba3b-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ba3b-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ba3b-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ba3b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6ba3b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ba3b-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ba3b-133"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ba3b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ba3b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba3b-135">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="6ba3b-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





