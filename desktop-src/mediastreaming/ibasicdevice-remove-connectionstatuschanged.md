---
title: Ibasicdevice-remove_ConnectionStatusChanged-Methode
description: Hebt die Registrierung eines Ereignis Handlers für das connectionstatuschge-Ereignis auf. | Ibasicdevice-remove_ConnectionStatusChanged-Methode
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- Medien Streaming-API für remove_ConnectionStatusChanged-Methode
- remove_ConnectionStatusChanged-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, remove_ConnectionStatusChanged-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c2bfa2886774ad637e66385a057c9d4e21efe0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361813"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="d0f8f-107">Ibasicdevice:: Remove \_ connectionstatuschangimethod</span><span class="sxs-lookup"><span data-stu-id="d0f8f-107">IBasicDevice::remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="d0f8f-108">Hebt die Registrierung eines Ereignis Handlers für das [**connectionstatuschge**](connectionstatuschanged.md) -Ereignis auf.</span><span class="sxs-lookup"><span data-stu-id="d0f8f-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f8f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0f8f-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="d0f8f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0f8f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0f8f-111">*Token* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0f8f-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f8f-112">Ein Verweis auf ein Token, das von der [**Add \_ connectionstatuschangi-**](ibasicdevice-add-connectionstatuschanged.md) Methode abgerufen wurde, als der Ereignishandler registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="d0f8f-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0f8f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0f8f-113">Return value</span></span>

<span data-ttu-id="d0f8f-114">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="d0f8f-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d0f8f-115">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d0f8f-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d0f8f-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d0f8f-116">Return code</span></span>                                                                          | <span data-ttu-id="d0f8f-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0f8f-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d0f8f-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d0f8f-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d0f8f-119">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0f8f-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d0f8f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0f8f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f8f-121">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="d0f8f-121">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





