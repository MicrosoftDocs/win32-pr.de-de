---
description: Die TAPI-Telefon \_ Erstellungs Nachricht wird gesendet, um Anwendungen über das Erstellen eines neuen Telefon Geräts zu informieren.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: PHONE_CREATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92dfaad5d4007279f18890021f5cb39c22c4da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370979"
---
# <a name="phone_create-message"></a><span data-ttu-id="3152f-103">Meldung zum Erstellen des Telefons \_</span><span class="sxs-lookup"><span data-stu-id="3152f-103">PHONE\_CREATE message</span></span>

<span data-ttu-id="3152f-104">Die TAPI **- \_ Telefon** Erstellungs Nachricht wird gesendet, um Anwendungen über das Erstellen eines neuen Telefon Geräts zu informieren.</span><span class="sxs-lookup"><span data-stu-id="3152f-104">The TAPI **PHONE\_CREATE** message is sent to inform applications of the creation of a new phone device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="3152f-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="3152f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3152f-106">*hphone*</span><span class="sxs-lookup"><span data-stu-id="3152f-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="3152f-107">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3152f-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="3152f-108">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="3152f-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="3152f-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3152f-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="3152f-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="3152f-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="3152f-111">Die *HDE viceid* des neu erstellten Geräts.</span><span class="sxs-lookup"><span data-stu-id="3152f-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="3152f-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="3152f-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="3152f-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3152f-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="3152f-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="3152f-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="3152f-115">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3152f-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3152f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3152f-116">Return value</span></span>

<span data-ttu-id="3152f-117">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="3152f-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3152f-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3152f-118">Remarks</span></span>

<span data-ttu-id="3152f-119">Anwendungen, die die API-Version 1,3 ausgehandelt haben, erhalten eine [**Telefon \_ Zustands**](phone-state.md) Meldung, die phonestate \_ REIT angibt. Dies erfordert, dass Sie Ihre Verwendung der API Herunterfahren und [**phoneinitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) erneut aufrufen, um die neue Anzahl von Geräten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3152f-119">Applications that negotiated API version 1.3 are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REINIT, which requires them to shut down their use of the API and call [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="3152f-120">Die TAPI-Version 1,4 und höher erfordert jedoch nicht, dass alle Anwendungen heruntergefahren werden, bevor die erneute Initialisierung von Anwendungen zugelassen wird. die erneute Initialisierung kann sofort erfolgen, wenn ein neues Gerät erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3152f-120">However, TAPI version 1.4 and above do not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created.</span></span>

<span data-ttu-id="3152f-121">Anwendungen, die TAPI-Version 1,4 oder höher unterstützen, erhalten eine Meldung zum **\_ Erstellen eines Telefons** .</span><span class="sxs-lookup"><span data-stu-id="3152f-121">Applications supporting TAPI version 1.4 or later are sent a **PHONE\_CREATE** message.</span></span> <span data-ttu-id="3152f-122">Dadurch werden Sie darüber informiert, dass das neue Gerät und die neue Gerätekennung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3152f-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="3152f-123">Die Anwendung kann dann auswählen, ob versucht werden soll, mit dem neuen Gerät zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3152f-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3152f-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3152f-124">Requirements</span></span>



| <span data-ttu-id="3152f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3152f-125">Requirement</span></span> | <span data-ttu-id="3152f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="3152f-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3152f-127">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="3152f-127">TAPI version</span></span><br/> | <span data-ttu-id="3152f-128">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="3152f-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3152f-129">Header</span><span class="sxs-lookup"><span data-stu-id="3152f-129">Header</span></span><br/>       | <dl> <span data-ttu-id="3152f-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3152f-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3152f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3152f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3152f-132">**Telefon \_ Status**</span><span class="sxs-lookup"><span data-stu-id="3152f-132">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="3152f-133">**phoneinitialize**</span><span class="sxs-lookup"><span data-stu-id="3152f-133">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="3152f-134">**phoneinitializeex**</span><span class="sxs-lookup"><span data-stu-id="3152f-134">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




