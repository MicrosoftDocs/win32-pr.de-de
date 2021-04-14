---
title: Imstscaxevents onconnecting-Methode
description: Wird aufgerufen, wenn das Client Steuerelement mit dem Herstellen einer Verbindung mit einem Server als Reaktion auf einen Aufruf von imstscax Connect beginnt.
ms.assetid: c5e367a8-126a-48bb-bc94-1063f77e8239
ms.tgt_platform: multiple
keywords:
- Onconnecting-Methode Remotedesktopdienste
- Onconnecting-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onconnecting-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2004fde83b79aff7b7c5082562de94f943eacb25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391520"
---
# <a name="imstscaxeventsonconnecting-method"></a><span data-ttu-id="0cb7d-106">Imstscaxevents:: onconnecting-Methode</span><span class="sxs-lookup"><span data-stu-id="0cb7d-106">IMsTscAxEvents::OnConnecting method</span></span>

<span data-ttu-id="0cb7d-107">Wird aufgerufen, wenn das Client Steuerelement mit dem Herstellen einer Verbindung mit einem Server als Reaktion auf einen Aufruf von [**imstscax:: Connect**](imstscax-connect.md)beginnt.</span><span class="sxs-lookup"><span data-stu-id="0cb7d-107">Called when the client control begins connecting to a server in response to a call to [**IMsTscAx::Connect**](imstscax-connect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb7d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cb7d-108">Syntax</span></span>


```C++
void OnConnecting();
```



## <a name="parameters"></a><span data-ttu-id="0cb7d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cb7d-109">Parameters</span></span>

<span data-ttu-id="0cb7d-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0cb7d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0cb7d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0cb7d-111">Return value</span></span>

<span data-ttu-id="0cb7d-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0cb7d-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cb7d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cb7d-113">Remarks</span></span>

<span data-ttu-id="0cb7d-114">Implementieren Sie diese Methode in der Ereignis Senke, um die Benachrichtigung zu erhalten, dass das Steuerelement mit dem verbinden begonnen</span><span class="sxs-lookup"><span data-stu-id="0cb7d-114">Implement this method in your event sink to receive notification that the control has begun connecting.</span></span>

## <a name="examples"></a><span data-ttu-id="0cb7d-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0cb7d-115">Examples</span></span>

<span data-ttu-id="0cb7d-116">Im folgenden Beispiel wird gezeigt, wie dieses Ereignis mit Visual Basic Skriptcode behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="0cb7d-116">The following example shows how to handle this event with Visual Basic Scripting code.</span></span> <span data-ttu-id="0cb7d-117">In diesem Beispiel wird davon ausgegangen, dass das Steuerelement Objekt den Namen "MsRdpClient" hat.</span><span class="sxs-lookup"><span data-stu-id="0cb7d-117">The assumption in this example is that your control object is named "MsRdpClient".</span></span>

<span data-ttu-id="0cb7d-118">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0cb7d-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>


```VB
Sub MsRdpClient.OnConnecting()
    Msgbox("Connecting")
End sub
```



## <a name="requirements"></a><span data-ttu-id="0cb7d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cb7d-119">Requirements</span></span>



| <span data-ttu-id="0cb7d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0cb7d-120">Requirement</span></span> | <span data-ttu-id="0cb7d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0cb7d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb7d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0cb7d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb7d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cb7d-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0cb7d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cb7d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb7d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cb7d-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0cb7d-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0cb7d-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="0cb7d-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cb7d-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0cb7d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0cb7d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cb7d-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cb7d-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0cb7d-130">IID</span><span class="sxs-lookup"><span data-stu-id="0cb7d-130">IID</span></span><br/>                      | <span data-ttu-id="0cb7d-131">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="0cb7d-131">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="0cb7d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cb7d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb7d-133">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="0cb7d-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





