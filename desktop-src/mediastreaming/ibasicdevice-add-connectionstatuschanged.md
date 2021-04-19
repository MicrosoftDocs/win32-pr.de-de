---
title: Ibasicdevice-add_ConnectionStatusChanged-Methode
description: Registriert einen Ereignishandler für das connectionstatuschangi-Ereignis. | Ibasicdevice-add_ConnectionStatusChanged-Methode
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- Medien Streaming-API für add_ConnectionStatusChanged-Methode
- add_ConnectionStatusChanged-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, add_ConnectionStatusChanged-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0028e6f3dad1670974178b0f07a59f74dffdc06f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366602"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a><span data-ttu-id="a6b0e-107">Ibasicdevice:: Add \_ connectionstatuschangi-Methode</span><span class="sxs-lookup"><span data-stu-id="a6b0e-107">IBasicDevice::add\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="a6b0e-108">Registriert einen Ereignishandler für das [**connectionstatuschangi-Ereignis**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="a6b0e-108">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6b0e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6b0e-109">Syntax</span></span>


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a><span data-ttu-id="a6b0e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6b0e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6b0e-111">*Handler* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6b0e-111">*handler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6b0e-112">Eine [**connectionstatushandler-Ereignishandlerfunktion**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a6b0e-112">A [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function.</span></span>

</dd> <dt>

<span data-ttu-id="a6b0e-113">*Token* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a6b0e-113">*token* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a6b0e-114">Verweis auf ein Token, das verwendet werden kann, um die Registrierung des Ereignis Handlers aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="a6b0e-114">Reference to a token that can be used to unregister the event handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6b0e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6b0e-115">Return value</span></span>

<span data-ttu-id="a6b0e-116">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="a6b0e-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a6b0e-117">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a6b0e-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a6b0e-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a6b0e-118">Return code</span></span>                                                                          | <span data-ttu-id="a6b0e-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6b0e-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a6b0e-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a6b0e-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a6b0e-121">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6b0e-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6b0e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6b0e-122">Remarks</span></span>

<span data-ttu-id="a6b0e-123">Um die Registrierung des Ereignis Handlers aufzuheben, der durch diese Methode registriert wurde, übergeben Sie den *Tokenwert* an die [**Remove \_ connectionstatuschangi-**](ibasicdevice-remove-connectionstatuschanged.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="a6b0e-123">To unregister the event handler that was registered by this method, pass the *token* value to the [**remove\_ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6b0e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6b0e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6b0e-125">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="a6b0e-125">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

