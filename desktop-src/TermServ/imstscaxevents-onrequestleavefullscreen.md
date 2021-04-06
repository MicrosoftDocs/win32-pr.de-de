---
title: Imstscaxevents onrequestleavefullscreen-Methode
description: Wird aufgerufen, wenn der Client anfordert, den Vollbildmodus zu verlassen, und die imstscadvancedsettings put \_ containerhandledfullscreen-Eigenschaft auf einen Wert ungleich 0 (null) festgelegt wurde.
ms.assetid: db6ee012-8288-4360-98b2-12858ea65baa
ms.tgt_platform: multiple
keywords:
- Onrequestleavefullscreen-Methode Remotedesktopdienste
- Onrequestleavefullscreen-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onrequestleavefullscreen-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestLeaveFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e814d6153e32fdf4fa498a6630fc9ca2908510e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742096"
---
# <a name="imstscaxeventsonrequestleavefullscreen-method"></a><span data-ttu-id="6cc92-106">Imstscaxevents:: onrequestleavefullscreen-Methode</span><span class="sxs-lookup"><span data-stu-id="6cc92-106">IMsTscAxEvents::OnRequestLeaveFullScreen method</span></span>

<span data-ttu-id="6cc92-107">Wird aufgerufen, wenn der Client den Vollbildmodus verlässt und die [**imstscadvancedsettings::p UT \_ containerhandledfullscreen**](imstscadvancedsettings-containerhandledfullscreen.md) -Eigenschaft auf einen Wert ungleich 0 (null) festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="6cc92-107">Called when the client requests to leave full-screen mode and the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) property has been set to a nonzero value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc92-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cc92-108">Syntax</span></span>


```C++
void OnRequestLeaveFullScreen();
```



## <a name="parameters"></a><span data-ttu-id="6cc92-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cc92-109">Parameters</span></span>

<span data-ttu-id="6cc92-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6cc92-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6cc92-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6cc92-111">Return value</span></span>

<span data-ttu-id="6cc92-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6cc92-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cc92-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6cc92-113">Remarks</span></span>

<span data-ttu-id="6cc92-114">Im Container behandelten Vollbildmodus sollte der Container den Standard-Vollbildmodus als Reaktion auf dieses Ereignis belassen.</span><span class="sxs-lookup"><span data-stu-id="6cc92-114">In container-handled full-screen mode, the container should leave standard full-screen mode in response to this event.</span></span>

<span data-ttu-id="6cc92-115">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6cc92-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cc92-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6cc92-116">Requirements</span></span>



| <span data-ttu-id="6cc92-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6cc92-117">Requirement</span></span> | <span data-ttu-id="6cc92-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6cc92-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc92-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6cc92-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc92-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6cc92-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6cc92-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6cc92-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc92-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cc92-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6cc92-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6cc92-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="6cc92-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cc92-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6cc92-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6cc92-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cc92-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cc92-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6cc92-127">IID</span><span class="sxs-lookup"><span data-stu-id="6cc92-127">IID</span></span><br/>                      | <span data-ttu-id="6cc92-128">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="6cc92-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="6cc92-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cc92-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc92-130">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="6cc92-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





