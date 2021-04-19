---
description: TAPI sendet die Phone \_ DevSpecific-Nachricht an eine Anwendung, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die auf dem Telefon auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind Implementierungs definiert.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: PHONE_DEVSPECIFIC Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c817f273a49fdcda36995cec335811fb06c8a917
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373569"
---
# <a name="phone_devspecific-message"></a><span data-ttu-id="918e2-104">\_DevSpecific-Telefonnachricht</span><span class="sxs-lookup"><span data-stu-id="918e2-104">PHONE\_DEVSPECIFIC message</span></span>

<span data-ttu-id="918e2-105">TAPI sendet die **Phone \_ DevSpecific** -Nachricht an eine Anwendung, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die auf dem Telefon auftreten.</span><span class="sxs-lookup"><span data-stu-id="918e2-105">TAPI sends the **PHONE\_DEVSPECIFIC** message to an application to notify the application about device-specific events occurring at the phone.</span></span> <span data-ttu-id="918e2-106">Die Bedeutung der Nachricht und die Interpretation der Parameter sind Implementierungs definiert.</span><span class="sxs-lookup"><span data-stu-id="918e2-106">The meaning of the message and the interpretation of the parameters is implementation-defined.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="918e2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="918e2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="918e2-108">*hphone*</span><span class="sxs-lookup"><span data-stu-id="918e2-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="918e2-109">Ein Handle für das Telefongerät.</span><span class="sxs-lookup"><span data-stu-id="918e2-109">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="918e2-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="918e2-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="918e2-111">Die Rückruf Instanz der Anwendung, die beim Öffnen des Telefon Geräts bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="918e2-111">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="918e2-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="918e2-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="918e2-113">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="918e2-113">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="918e2-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="918e2-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="918e2-115">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="918e2-115">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="918e2-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="918e2-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="918e2-117">Gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="918e2-117">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="918e2-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="918e2-118">Return value</span></span>

<span data-ttu-id="918e2-119">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="918e2-119">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="918e2-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="918e2-120">Requirements</span></span>



| <span data-ttu-id="918e2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="918e2-121">Requirement</span></span> | <span data-ttu-id="918e2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="918e2-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="918e2-123">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="918e2-123">TAPI version</span></span><br/> | <span data-ttu-id="918e2-124">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="918e2-124">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="918e2-125">Header</span><span class="sxs-lookup"><span data-stu-id="918e2-125">Header</span></span><br/>       | <dl> <span data-ttu-id="918e2-126"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="918e2-126"><dt>Tapi.h</dt></span></span> </dl> |



 

 




