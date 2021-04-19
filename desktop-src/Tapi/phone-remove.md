---
description: Die TAPI-Telefon \_ Entfernungs Nachricht wird gesendet, um eine Anwendung über das Entfernen (Löschen vom System) eines Telefon Geräts zu informieren.
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: PHONE_REMOVE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab32ba8b8a8e003c5d87109dd2d0c9dbe98c236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370688"
---
# <a name="phone_remove-message"></a><span data-ttu-id="a7e8a-103">Meldung zum Entfernen des Telefons \_</span><span class="sxs-lookup"><span data-stu-id="a7e8a-103">PHONE\_REMOVE message</span></span>

<span data-ttu-id="a7e8a-104">Die TAPI- **Telefon \_ Entfernungs** Nachricht wird gesendet, um eine Anwendung über das Entfernen (Löschen vom System) eines Telefon Geräts zu informieren.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-104">The TAPI **PHONE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a phone device.</span></span> <span data-ttu-id="a7e8a-105">Dies wird im Allgemeinen nicht für temporäre Entfernungen verwendet, wie z. b. das Extrahieren von PCMCIA-Geräten, sondern nur für permanente Entfernungen, bei denen das Gerät nicht mehr vom Dienstanbieter gemeldet wird, wenn TAPI erneut initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="a7e8a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7e8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7e8a-107">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="a7e8a-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a7e8a-108">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-108">Reserved.</span></span> <span data-ttu-id="a7e8a-109">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a7e8a-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="a7e8a-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="a7e8a-111">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-111">Reserved.</span></span> <span data-ttu-id="a7e8a-112">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a7e8a-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="a7e8a-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="a7e8a-114">Der Bezeichner des entfernten Phone-Geräts.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-114">Identifier of the phone device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="a7e8a-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="a7e8a-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="a7e8a-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-116">Reserved.</span></span> <span data-ttu-id="a7e8a-117">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a7e8a-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="a7e8a-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="a7e8a-119">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-119">Reserved.</span></span> <span data-ttu-id="a7e8a-120">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7e8a-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7e8a-121">Return value</span></span>

<span data-ttu-id="a7e8a-122">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7e8a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7e8a-123">Remarks</span></span>

<span data-ttu-id="a7e8a-124">Anwendungen TAPI Version 2,0 oder höher wird eine Nachricht **zum \_ Entfernen per Telefon** gesendet.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-124">Applications TAPI version 2.0 or later are sent a **PHONE\_REMOVE** message.</span></span> <span data-ttu-id="a7e8a-125">Dadurch werden Sie darüber informiert, dass das Gerät aus dem System entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="a7e8a-126">Der **Telefon \_ Entfernungs** Meldung wird eine Telefonnachricht zum [**\_ Schließen**](phone-close.md) der Telefonnummer vorangestellt, wenn für die Anwendung das Telefon geöffnet war.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-126">The **PHONE\_REMOVE** message is preceded by a [**PHONE\_CLOSE**](phone-close.md) message on each phone handle, if the application had the phone open.</span></span> <span data-ttu-id="a7e8a-127">Diese Nachricht wird an alle Anwendungen gesendet, die TAPI-Version 2,0 oder höher unterstützen, die " [**phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)" genannt haben, einschließlich derjenigen, die keine Telefongeräte gleichzeitig geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), including those that do not have any phone devices open at the time.</span></span>

<span data-ttu-id="a7e8a-128">Älteren Anwendungen (die die TAPI-Version 1,4 oder früher ausgehandelt haben) wird eine [**Telefon \_ Zustands**](phone-state.md) Meldung gesendet \_ , in der phonestate entfernt wird, gefolgt von einer Meldung zum [**\_ Schließen des Telefons**](phone-close.md) .</span><span class="sxs-lookup"><span data-stu-id="a7e8a-128">Older applications (that negotiated TAPI version 1.4 or earlier) are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REMOVED, followed by a [**PHONE\_CLOSE**](phone-close.md) message.</span></span> <span data-ttu-id="a7e8a-129">Anders als bei der **Telefon \_ Entfernungs** Nachricht können diese älteren Anwendungen diese Nachrichten jedoch nur empfangen, wenn Sie das Telefon geöffnet haben, wenn es entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-129">Unlike the **PHONE\_REMOVE** message, however, these older applications can receive these messages only if they have the phone open when it is removed.</span></span> <span data-ttu-id="a7e8a-130">Wenn kein Telefon geöffnet ist, erhält der einzige Hinweis darauf, dass das Gerät entfernt wurde, \_ beim Versuch, auf das Gerät zuzugreifen, ein phoneerr-nodevice.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-130">If they do not have the phone open, their only indication that the device was removed would be receiving a PHONEERR\_NODEVICE when they attempt to access the device.</span></span>

<span data-ttu-id="a7e8a-131">Nachdem ein Gerät entfernt wurde, führt jeder Versuch, über seine Gerätekennung auf das Gerät zuzugreifen, zu einem phoneerr- \_ nodevice-Fehler.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-131">After a device has been removed, any attempt to access the device by its device identifier results in a PHONEERR\_NODEVICE error.</span></span> <span data-ttu-id="a7e8a-132">Nachdem alle TAPI-Anwendungen heruntergefahren wurden, sodass TAPI neu gestartet werden kann, und wenn TAPI erneut initialisiert wird, belegt das entfernte Gerät keinen Geräte Bezeichner mehr.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="a7e8a-133">Implementierung: Dies ist TAPI, die diese phoneerr \_ nodevice-Nachricht zurückgibt, nachdem eine Telefon \_ Entfernungs Nachricht von einem Dienstanbieter empfangen wurde. es werden keine weiteren Aufrufe an den Dienstanbieter über diese Telefongeräte-ID gesendet.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-133">Implementation: it is TAPI that returns this PHONEERR\_NODEVICE message after a PHONE\_REMOVE message is received from a service provider; no further calls are made to that service provider using that phone device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a7e8a-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7e8a-134">Requirements</span></span>



| <span data-ttu-id="a7e8a-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7e8a-135">Requirement</span></span> | <span data-ttu-id="a7e8a-136">Wert</span><span class="sxs-lookup"><span data-stu-id="a7e8a-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a7e8a-137">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="a7e8a-137">TAPI version</span></span><br/> | <span data-ttu-id="a7e8a-138">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="a7e8a-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a7e8a-139">Header</span><span class="sxs-lookup"><span data-stu-id="a7e8a-139">Header</span></span><br/>       | <dl> <span data-ttu-id="a7e8a-140"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7e8a-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7e8a-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7e8a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7e8a-142">**Telefon \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="a7e8a-142">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="a7e8a-143">**Telefon \_ Status**</span><span class="sxs-lookup"><span data-stu-id="a7e8a-143">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="a7e8a-144">**phoneinitialize**</span><span class="sxs-lookup"><span data-stu-id="a7e8a-144">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="a7e8a-145">**phoneinitializeex**</span><span class="sxs-lookup"><span data-stu-id="a7e8a-145">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




