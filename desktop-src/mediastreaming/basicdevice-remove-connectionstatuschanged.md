---
title: BasicDevice.remove_ConnectionStatusChanged-Methode
description: Hebt die Registrierung eines Ereignis Handlers für das connectionstatuschge-Ereignis auf. | BasicDevice.remove_ConnectionStatusChanged-Methode
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- Medien Streaming-API für remove_ConnectionStatusChanged-Methode
- remove_ConnectionStatusChanged-Methode Medien Streaming-API, basicdevice-Schnittstelle
- Basicdevice-Schnittstelle Medien Streaming-API, remove_ConnectionStatusChanged-Methode
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdd39309774a61c4fd115ff09e16428101439a0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219300"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="c4865-107">Basicdevice. Remove \_ connectionstatuschangimethod</span><span class="sxs-lookup"><span data-stu-id="c4865-107">BasicDevice.remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="c4865-108">Hebt die Registrierung eines Ereignis Handlers für das [**connectionstatuschge**](connectionstatuschanged.md) -Ereignis auf.</span><span class="sxs-lookup"><span data-stu-id="c4865-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4865-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4865-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="c4865-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4865-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4865-111">*Token* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4865-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4865-112">Ein Verweis auf ein Token, das von der [**Add \_ connectionstatuschangi-**](basicdevice-add-connectionstatuschanged.md) Methode abgerufen wurde, als der Ereignishandler registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="c4865-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4865-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4865-113">Return value</span></span>

<span data-ttu-id="c4865-114">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="c4865-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c4865-115">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c4865-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c4865-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c4865-116">Return code</span></span>                                                                          | <span data-ttu-id="c4865-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4865-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c4865-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4865-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c4865-119">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4865-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c4865-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4865-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4865-121">[**Basicdevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4865-121">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

