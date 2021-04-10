---
title: Imstscaxevents onchannelreceiveddata-Methode
description: Wird aufgerufen, wenn der Client Daten eines Skript fähigen virtuellen Kanals empfängt.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- Onchannelreceiveddata-Methode Remotedesktopdienste
- Onchannelreceiveddata-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onchannelreceiveddata-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1cae4f35435138e219c628dd504c595939adfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103523"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a><span data-ttu-id="ded18-106">Imstscaxevents:: onchannelreceiveddata-Methode</span><span class="sxs-lookup"><span data-stu-id="ded18-106">IMsTscAxEvents::OnChannelReceivedData method</span></span>

<span data-ttu-id="ded18-107">Wird aufgerufen, wenn der Client Daten eines Skript fähigen virtuellen Kanals empfängt.</span><span class="sxs-lookup"><span data-stu-id="ded18-107">Called when the client receives data on a scriptable virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="ded18-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ded18-108">Syntax</span></span>


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a><span data-ttu-id="ded18-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ded18-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ded18-110">*channame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ded18-110">*chanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded18-111">Der Name des virtuellen Kanals, auf dem Daten empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="ded18-111">The name of the virtual channel on which data was received.</span></span> <span data-ttu-id="ded18-112">Dieser Name entspricht einem der Kanäle, die durch den Aufrufen von [**imstscax:: foratevirtualchannels**](imstscax-createvirtualchannels.md)erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ded18-112">This name matches one of the channels created by the call to [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="ded18-113">*Daten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ded18-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded18-114">Die Daten, die auf dem Skript fähigen virtuellen Kanal empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="ded18-114">The data received on the scriptable virtual channel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ded18-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ded18-115">Return value</span></span>

<span data-ttu-id="ded18-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ded18-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ded18-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ded18-117">Remarks</span></span>

<span data-ttu-id="ded18-118">Weitere Informationen zu diesem Ereignis finden Sie unter [Implementieren von Skript fähigen virtuellen Kanälen mithilfe von Remotedesktop-Webverbindung](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) .</span><span class="sxs-lookup"><span data-stu-id="ded18-118">Refer to [Implementing Scriptable Virtual Channels using Remote Desktop Web Connection](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) for more information about this event.</span></span>

<span data-ttu-id="ded18-119">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ded18-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ded18-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ded18-120">Requirements</span></span>



| <span data-ttu-id="ded18-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ded18-121">Requirement</span></span> | <span data-ttu-id="ded18-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ded18-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ded18-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ded18-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ded18-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ded18-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ded18-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ded18-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ded18-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ded18-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ded18-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ded18-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="ded18-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ded18-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ded18-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ded18-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ded18-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ded18-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ded18-131">IID</span><span class="sxs-lookup"><span data-stu-id="ded18-131">IID</span></span><br/>                      | <span data-ttu-id="ded18-132">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="ded18-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="ded18-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ded18-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ded18-134">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="ded18-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





