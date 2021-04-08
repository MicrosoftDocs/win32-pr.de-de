---
title: Imstscaxevents (onconnected-Methode)
description: Wird aufgerufen, wenn das Client Steuerelement gerade eine Verbindung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server herstellt.
ms.assetid: 9c26d112-c070-4870-93d5-2fcc84a1331f
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der onconnected-Methode
- Onconnected-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onconnected-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d83a6a14f58a0704f0a3110532ad8cf8c0d7dc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741321"
---
# <a name="imstscaxeventsonconnected-method"></a><span data-ttu-id="695d1-106">Imstscaxevents:: onconnected-Methode</span><span class="sxs-lookup"><span data-stu-id="695d1-106">IMsTscAxEvents::OnConnected method</span></span>

<span data-ttu-id="695d1-107">Wird aufgerufen, wenn das Client Steuerelement gerade eine Verbindung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server herstellt.</span><span class="sxs-lookup"><span data-stu-id="695d1-107">Called when the client control is in the process of establishing a connection with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="695d1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="695d1-108">Syntax</span></span>


```C++
void OnConnected();
```



## <a name="parameters"></a><span data-ttu-id="695d1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="695d1-109">Parameters</span></span>

<span data-ttu-id="695d1-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="695d1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="695d1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="695d1-111">Return value</span></span>

<span data-ttu-id="695d1-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="695d1-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="695d1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="695d1-113">Remarks</span></span>

<span data-ttu-id="695d1-114">Implementieren Sie diese Methode in der Ereignis Senke, um eine Benachrichtigung zu erhalten, dass das Steuerelement eine Verbindung mit einem RD-Sitzungshost Server hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="695d1-114">Implement this method in your event sink to receive notification that the control has established a connection with an RD Session Host server.</span></span>

<span data-ttu-id="695d1-115">Weitere Informationen zum Aufrufen dieser Methode finden Sie im [**imstscaxevents:: onlogincomplete**](imstscaxevents-onlogincomplete.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="695d1-115">Refer to the [**IMsTscAxEvents::OnLoginComplete**](imstscaxevents-onlogincomplete.md) event for more information on calling this method.</span></span>

<span data-ttu-id="695d1-116">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="695d1-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="695d1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="695d1-117">Requirements</span></span>



| <span data-ttu-id="695d1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="695d1-118">Requirement</span></span> | <span data-ttu-id="695d1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="695d1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="695d1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="695d1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="695d1-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="695d1-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="695d1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="695d1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="695d1-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="695d1-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="695d1-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="695d1-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="695d1-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="695d1-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="695d1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="695d1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="695d1-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="695d1-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="695d1-128">IID</span><span class="sxs-lookup"><span data-stu-id="695d1-128">IID</span></span><br/>                      | <span data-ttu-id="695d1-129">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="695d1-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="695d1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="695d1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="695d1-131">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="695d1-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





