---
description: Die TAPI-Zeilen \_ Entfernungs Nachricht wird gesendet, um eine Anwendung über das Entfernen (Löschen vom System) eines Zeilen Geräts zu informieren.
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: LINE_REMOVE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567ead3ad2941845dd22405f0d8706eca74bfbd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361958"
---
# <a name="line_remove-message"></a><span data-ttu-id="fbfc4-103">Zeilen \_ Entfernungs Meldung</span><span class="sxs-lookup"><span data-stu-id="fbfc4-103">LINE\_REMOVE message</span></span>

<span data-ttu-id="fbfc4-104">Die TAPI- **Zeilen \_ Entfernungs** Nachricht wird gesendet, um eine Anwendung über das Entfernen (Löschen vom System) eines Zeilen Geräts zu informieren.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-104">The TAPI **LINE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a line device.</span></span> <span data-ttu-id="fbfc4-105">Dies wird im Allgemeinen nicht für temporäre Entfernungen verwendet, wie z. b. das Extrahieren von PCMCIA-Geräten, sondern nur für permanente Entfernungen, bei denen das Gerät nicht mehr vom Dienstanbieter gemeldet wird, wenn TAPI erneut initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="fbfc4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbfc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbfc4-107">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="fbfc4-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="fbfc4-108">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-108">Reserved.</span></span> <span data-ttu-id="fbfc4-109">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fbfc4-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="fbfc4-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="fbfc4-111">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-111">Reserved.</span></span> <span data-ttu-id="fbfc4-112">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fbfc4-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="fbfc4-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="fbfc4-114">Der Bezeichner des entfernten Zeilen Geräts.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-114">Identifier of the line device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="fbfc4-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="fbfc4-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="fbfc4-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-116">Reserved.</span></span> <span data-ttu-id="fbfc4-117">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fbfc4-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="fbfc4-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="fbfc4-119">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-119">Reserved.</span></span> <span data-ttu-id="fbfc4-120">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbfc4-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbfc4-121">Return value</span></span>

<span data-ttu-id="fbfc4-122">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbfc4-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbfc4-123">Remarks</span></span>

<span data-ttu-id="fbfc4-124">Anwendungen, die TAPI-Version 2,0 oder höher unterstützen, werden als **Zeilen \_ Entfernungs** Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-124">Applications supporting TAPI version 2.0 or later are sent a **LINE\_REMOVE** message.</span></span> <span data-ttu-id="fbfc4-125">Dadurch werden Sie darüber informiert, dass das Gerät aus dem System entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="fbfc4-126">Der **Zeilen \_ Entfernungs** Nachricht wird eine [**Zeilen Schluss \_**](line-close.md) Nachricht für jedes Zeilen handle vorangestellt, wenn die Zeile in der Anwendung geöffnet war.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-126">The **LINE\_REMOVE** message is preceded by a [**LINE\_CLOSE**](line-close.md) message on each line handle, if the application had the line open.</span></span> <span data-ttu-id="fbfc4-127">Diese Nachricht wird an alle Anwendungen gesendet, die TAPI-Version 2,0 oder höher unterstützen, die [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)aufgerufen haben, einschließlich derjenigen, die zu diesem Zeitpunkt keine Zeilen Geräte geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

<span data-ttu-id="fbfc4-128">Älteren Anwendungen wird eine [**\_ linienlinedevstate**](line-linedevstate.md) -Nachricht gesendet, in der linedevstate \_ entfernt wird, gefolgt von einer Zeilen Schluss \_ Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-128">Older applications are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REMOVED, followed by a LINE\_CLOSE message.</span></span> <span data-ttu-id="fbfc4-129">Anders als bei der **Zeilen \_ Entfernungs** Nachricht können diese älteren Anwendungen diese Nachrichten jedoch nur empfangen, wenn die Zeile beim Entfernen geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-129">Unlike the **LINE\_REMOVE** message, however, these older applications can receive these messages only if they have the line open when it is removed.</span></span> <span data-ttu-id="fbfc4-130">Wenn die Zeile nicht geöffnet ist, erhalten Sie lediglich den Hinweis, dass das Gerät entfernt wurde, \_ Wenn Sie versuchen, auf das Gerät zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-130">If they do not have the line open, their only indication that the device was removed would be receiving a LINEERR\_NODEVICE error when they attempt to access the device.</span></span>

<span data-ttu-id="fbfc4-131">Nachdem ein Gerät entfernt wurde, führt jeder Versuch, über seine Gerätekennung auf das Gerät zuzugreifen, zu einem lineerr- \_ nodevice-Fehler.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-131">After a device has been removed, any attempt to access the device by its device identifier results in a LINEERR\_NODEVICE error.</span></span> <span data-ttu-id="fbfc4-132">Nachdem alle TAPI-Anwendungen heruntergefahren wurden, sodass TAPI neu gestartet werden kann, und wenn TAPI erneut initialisiert wird, belegt das entfernte Gerät keinen Geräte Bezeichner mehr.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="fbfc4-133">Implementierung: Es ist TAPI, die dieses lineerr- \_ nodevice zurückgibt, nachdem eine **Zeile zum \_ Entfernen von Zeilen** von einem Dienstanbieter empfangen wurde. es werden keine weiteren Aufrufe an den Dienstanbieter über diese Geräte-Geräte-ID gesendet.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-133">Implementation: it is TAPI that returns this LINEERR\_NODEVICE; after a **LINE\_REMOVE** message is received from a service provider; no further calls are made to that service provider using that line device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fbfc4-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbfc4-134">Requirements</span></span>



| <span data-ttu-id="fbfc4-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbfc4-135">Requirement</span></span> | <span data-ttu-id="fbfc4-136">Wert</span><span class="sxs-lookup"><span data-stu-id="fbfc4-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fbfc4-137">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="fbfc4-137">TAPI version</span></span><br/> | <span data-ttu-id="fbfc4-138">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fbfc4-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fbfc4-139">Header</span><span class="sxs-lookup"><span data-stu-id="fbfc4-139">Header</span></span><br/>       | <dl> <span data-ttu-id="fbfc4-140"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbfc4-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbfc4-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbfc4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbfc4-142">**Zeilen \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="fbfc4-142">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="fbfc4-143">**\_linienlinedevstate**</span><span class="sxs-lookup"><span data-stu-id="fbfc4-143">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="fbfc4-144">**lineinitializeex**</span><span class="sxs-lookup"><span data-stu-id="fbfc4-144">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




