---
description: Die TAPI Line \_ Create-Meldung wird gesendet, um die Anwendung über die Erstellung eines neuen Zeilen Geräts zu informieren.
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: LINE_CREATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9973849c3942b5427dfb6b3fe7c47bc4d2a716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357679"
---
# <a name="line_create-message"></a><span data-ttu-id="27b82-103">Nachricht zum Erstellen von Zeilen \_</span><span class="sxs-lookup"><span data-stu-id="27b82-103">LINE\_CREATE message</span></span>

<span data-ttu-id="27b82-104">Die TAPI **line \_ Create** -Meldung wird gesendet, um die Anwendung über die Erstellung eines neuen Zeilen Geräts zu informieren.</span><span class="sxs-lookup"><span data-stu-id="27b82-104">The TAPI **LINE\_CREATE** message is sent to inform the application of the creation of a new line device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="27b82-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="27b82-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27b82-106">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="27b82-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="27b82-107">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27b82-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="27b82-108">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="27b82-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="27b82-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27b82-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="27b82-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="27b82-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="27b82-111">Die *HDE viceid* des neu erstellten Geräts.</span><span class="sxs-lookup"><span data-stu-id="27b82-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="27b82-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="27b82-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="27b82-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27b82-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="27b82-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="27b82-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="27b82-115">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27b82-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27b82-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27b82-116">Return value</span></span>

<span data-ttu-id="27b82-117">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="27b82-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="27b82-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27b82-118">Remarks</span></span>

<span data-ttu-id="27b82-119">Ältere Anwendungen (die die TAPI-Version 1,3 aushandeln) werden an eine [**line- \_ linedevstate**](line-linedevstate.md) -Nachricht gesendet, die linedevstate \_ REIT angibt. Dies erfordert, dass Sie Ihre Verwendung der API Herunterfahren und [**lineinitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) erneut aufrufen, um die neue Anzahl von Geräten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="27b82-119">Older applications (that negotiated TAPI version 1.3) are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REINIT, which requires them to shut down their use of the API and call [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="27b82-120">Im Gegensatz zu früheren Versionen von TAPI erfordert diese Version jedoch nicht, dass alle Anwendungen heruntergefahren werden, bevor Anwendungen erneut initialisiert werden können. die erneute Initialisierung kann sofort durchgeführt werden, wenn ein neues Gerät erstellt wird (das Herunterfahren ist nach wie vor erforderlich, wenn ein Dienstanbieter aus dem System entfernt wird).</span><span class="sxs-lookup"><span data-stu-id="27b82-120">Unlike previous versions of TAPI, however, this version does not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created (complete shutdown is still required when a service provider is removed from the system).</span></span>

<span data-ttu-id="27b82-121">Anwendungen, die TAPI-Version 1,4 oder höher unterstützen, werden als Nachricht zum **\_ Erstellen von Zeilen** gesendet</span><span class="sxs-lookup"><span data-stu-id="27b82-121">Applications supporting TAPI version 1.4 or later are sent a **LINE\_CREATE** message.</span></span> <span data-ttu-id="27b82-122">Dadurch werden Sie darüber informiert, dass das neue Gerät und die neue Gerätekennung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="27b82-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="27b82-123">Die Anwendung kann dann auswählen, ob versucht werden soll, mit dem neuen Gerät zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="27b82-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span> <span data-ttu-id="27b82-124">Diese Nachricht wird an alle Anwendungen gesendet, die diese oder nachfolgende Versionen der API unterstützen, die [**lineinitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) oder [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)aufgerufen haben, einschließlich derjenigen, die zu diesem Zeitpunkt keine Zeilen Geräte geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="27b82-124">This message is sent to all applications supporting this or subsequent versions of the API that have called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

## <a name="requirements"></a><span data-ttu-id="27b82-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27b82-125">Requirements</span></span>



| <span data-ttu-id="27b82-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27b82-126">Requirement</span></span> | <span data-ttu-id="27b82-127">Wert</span><span class="sxs-lookup"><span data-stu-id="27b82-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="27b82-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="27b82-128">TAPI version</span></span><br/> | <span data-ttu-id="27b82-129">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="27b82-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="27b82-130">Header</span><span class="sxs-lookup"><span data-stu-id="27b82-130">Header</span></span><br/>       | <dl> <span data-ttu-id="27b82-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="27b82-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27b82-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27b82-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27b82-133">**\_linienlinedevstate**</span><span class="sxs-lookup"><span data-stu-id="27b82-133">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="27b82-134">**lineinitialize**</span><span class="sxs-lookup"><span data-stu-id="27b82-134">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="27b82-135">**lineinitializeex**</span><span class="sxs-lookup"><span data-stu-id="27b82-135">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




