---
title: Imstscaxevents-Methode (onidletimeoutnotification)
description: Wird aufgerufen, wenn der Benutzer während der von der imsrdpclientadvancedsettings Put minutestoidletimeout-Methode festgelegten Zeitspanne keine Maus-oder Tastatureingaben eingegeben hat \_ .
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- Onidletimeoutnotification-Methode Remotedesktopdienste
- Onidletimeoutnotification-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onidletimeoutnotification-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e305b0ed22e733053e33451aa35d3b8f8d6c138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346725"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a><span data-ttu-id="3cf5d-106">Imstscaxevents:: onidletimeoutnotification-Methode</span><span class="sxs-lookup"><span data-stu-id="3cf5d-106">IMsTscAxEvents::OnIdleTimeoutNotification method</span></span>

<span data-ttu-id="3cf5d-107">Wird aufgerufen, wenn der Benutzer während der von der [**imsrdpclientadvancedsettings::p UT \_ minutestoidletimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) -Methode festgelegten Zeitspanne keine Maus-oder Tastatureingaben hat.</span><span class="sxs-lookup"><span data-stu-id="3cf5d-107">Called when there has been no mouse or keyboard input by the user during the period of time set by the [**IMsRdpClientAdvancedSettings::put\_MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cf5d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cf5d-108">Syntax</span></span>


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a><span data-ttu-id="3cf5d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cf5d-109">Parameters</span></span>

<span data-ttu-id="3cf5d-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3cf5d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3cf5d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3cf5d-111">Return value</span></span>

<span data-ttu-id="3cf5d-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3cf5d-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cf5d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3cf5d-113">Remarks</span></span>

<span data-ttu-id="3cf5d-114">Standardmäßig ist der Wert der [**minutestoidletimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) -Eigenschaft auf 0 (null) festgelegt, und das System überwacht keine Leerlauf Timeouts.</span><span class="sxs-lookup"><span data-stu-id="3cf5d-114">By default, the value of the [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) property is set to zero and the system does not monitor for idle time-outs.</span></span> <span data-ttu-id="3cf5d-115">Dieses Ereignis tritt nur auf, wenn die-Eigenschaft auf einen Wert ungleich 0 (null) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3cf5d-115">This event occurs only if the property is set to a nonzero value.</span></span>

<span data-ttu-id="3cf5d-116">Der Wert von [**minutestoidletimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) wird automatisch zurückgesetzt, wenn das Ereignis eintritt.</span><span class="sxs-lookup"><span data-stu-id="3cf5d-116">The value of [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) is automatically reset each time the event occurs.</span></span>

<span data-ttu-id="3cf5d-117">Anwendungen können [**minutestoidletimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) in Situationen verwenden, in denen es nützlich ist, einen Benutzer zu trennen. beispielsweise in einem Kiosk oder einem anderen Szenario mit öffentlichem Terminal.</span><span class="sxs-lookup"><span data-stu-id="3cf5d-117">Applications can use [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) in situations where it is useful to disconnect a user; for example, in a kiosk or other public terminal scenario.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cf5d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cf5d-118">Requirements</span></span>



| <span data-ttu-id="3cf5d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cf5d-119">Requirement</span></span> | <span data-ttu-id="3cf5d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3cf5d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf5d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3cf5d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3cf5d-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3cf5d-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3cf5d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3cf5d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3cf5d-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cf5d-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3cf5d-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3cf5d-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="3cf5d-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cf5d-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3cf5d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3cf5d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cf5d-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cf5d-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3cf5d-129">IID</span><span class="sxs-lookup"><span data-stu-id="3cf5d-129">IID</span></span><br/>                      | <span data-ttu-id="3cf5d-130">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="3cf5d-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="3cf5d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cf5d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf5d-132">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="3cf5d-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





