---
title: BasicDevice.add_ConnectionStatusChanged-Methode
description: Registriert einen Ereignishandler für das connectionstatuschangi-Ereignis. | BasicDevice.add_ConnectionStatusChanged-Methode
ms.assetid: FFAA0981-508C-4300-9CA9-24C6AFC1183D
keywords:
- Medien Streaming-API für add_ConnectionStatusChanged-Methode
- add_ConnectionStatusChanged-Methode Medien Streaming-API, basicdevice-Schnittstelle
- Basicdevice-Schnittstelle Medien Streaming-API, add_ConnectionStatusChanged-Methode
topic_type:
- apiref
api_name:
- BasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61a36e46d554a953ecd061ccf2396d33b0578d8f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353659"
---
# <a name="basicdeviceadd_connectionstatuschanged-method"></a><span data-ttu-id="cf2aa-107">Basicdevice. Add \_ connectionstatuschangimethod</span><span class="sxs-lookup"><span data-stu-id="cf2aa-107">BasicDevice.add\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="cf2aa-108">Registriert einen Ereignishandler für das [**connectionstatuschangi-Ereignis**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="cf2aa-108">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf2aa-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf2aa-109">Syntax</span></span>


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a><span data-ttu-id="cf2aa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf2aa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf2aa-111">*Handler* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf2aa-111">*handler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf2aa-112">Eine [**connectionstatushandler-Ereignishandlerfunktion**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cf2aa-112">A [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function.</span></span>

</dd> <dt>

<span data-ttu-id="cf2aa-113">*Token* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cf2aa-113">*token* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cf2aa-114">Verweis auf ein Token, das verwendet werden kann, um die Registrierung des Ereignis Handlers aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="cf2aa-114">Reference to a token that can be used to unregister the event handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf2aa-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf2aa-115">Return value</span></span>

<span data-ttu-id="cf2aa-116">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="cf2aa-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cf2aa-117">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cf2aa-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cf2aa-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cf2aa-118">Return code</span></span>                                                                          | <span data-ttu-id="cf2aa-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf2aa-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cf2aa-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf2aa-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cf2aa-121">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf2aa-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf2aa-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf2aa-122">Remarks</span></span>

<span data-ttu-id="cf2aa-123">Um die Registrierung des Ereignis Handlers aufzuheben, der durch diese Methode registriert wurde, übergeben Sie den *Tokenwert* an die [**Remove \_ connectionstatuschangi-**](basicdevice-remove-connectionstatuschanged.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="cf2aa-123">To unregister the event handler that was registered by this method, pass the *token* value to the [**remove\_ConnectionStatusChanged**](basicdevice-remove-connectionstatuschanged.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf2aa-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf2aa-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf2aa-125">[**Basicdevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf2aa-125">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

