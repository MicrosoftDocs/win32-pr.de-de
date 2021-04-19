---
description: Die linemediacontrol \_ -bitflagkonstanten beschreiben einen Satz generischer Vorgänge für Mediendaten Ströme.
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: LINEMEDIACONTROL_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3241a3b5f4f8a0363f30ce7aefaded0c63fc4189
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362030"
---
# <a name="linemediacontrol_-constants"></a><span data-ttu-id="4ed7f-103">Linemediacontrol- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="4ed7f-103">LINEMEDIACONTROL\_ Constants</span></span>

<span data-ttu-id="4ed7f-104">Die **linemediacontrol \_** -bitflagkonstanten beschreiben einen Satz generischer Vorgänge für Mediendaten Ströme.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-104">The **LINEMEDIACONTROL\_** bit-flag constants describe a set of generic operations on media streams.</span></span> <span data-ttu-id="4ed7f-105">Die Interpretationen werden durch den Mediendaten Strom bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-105">The interpretations are determined by the media stream.</span></span> <span data-ttu-id="4ed7f-106">Das liniengerät muss über die Medien Steuerungsfunktion verfügen, damit jeder Medien Steuerungs Vorgang effektiv ist.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-106">The line device must have the media-control capability for any media-control operation to be effective.</span></span>

<dl> <dt>

<span data-ttu-id="4ed7f-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**linemediacontrol \_ None**</span><span class="sxs-lookup"><span data-stu-id="4ed7f-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4ed7f-108">Es muss keine Änderung am Medienstrom vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-108">No change is to be made to the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ed7f-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**linemediacontrol \_ Anhalten**</span><span class="sxs-lookup"><span data-stu-id="4ed7f-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL\_PAUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4ed7f-110">Halten Sie den Mediendaten Strom vorübergehend an.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-110">Temporarily pause the media stream.</span></span>

<span data-ttu-id="4ed7f-111">Die Geschwindigkeit des Medien Stroms wird normal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-111">The speed of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ed7f-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**linemediacontrol- \_ Raten nach unten**</span><span class="sxs-lookup"><span data-stu-id="4ed7f-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL\_RATEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4ed7f-113">Die Geschwindigkeit des Mediendaten Stroms wird durch eine streamdefinierte Menge verringert.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-113">The speed of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ed7f-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**linemediacontrol \_ ratenormal**</span><span class="sxs-lookup"><span data-stu-id="4ed7f-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL\_RATENORMAL**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ed7f-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**linemediacontrol- \_ rateup**</span><span class="sxs-lookup"><span data-stu-id="4ed7f-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL\_RATEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4ed7f-116">Die Geschwindigkeit des Mediendaten Stroms wird durch eine streamdefinierte Menge gesteigert.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-116">The speed of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ed7f-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**linemediacontrol \_ Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="4ed7f-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**LINEMEDIACONTROL\_RESET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4ed7f-118">Setzt den Mediendaten Strom zurück.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-118">Reset the media stream.</span></span> <span data-ttu-id="4ed7f-119">Äquivalent zu einem Eingangs Ende.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-119">Equivalent to an end-of-input.</span></span> <span data-ttu-id="4ed7f-120">Alle Puffer werden freigegeben.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-120">All buffers are released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ed7f-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**linemediacontrol \_ fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="4ed7f-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**LINEMEDIACONTROL\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4ed7f-122">Fortsetzen eines angehaltenen Mediendaten Stroms</span><span class="sxs-lookup"><span data-stu-id="4ed7f-122">Resume a paused media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ed7f-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**linemediacontrol \_ starten**</span><span class="sxs-lookup"><span data-stu-id="4ed7f-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4ed7f-124">Starten Sie den Mediendaten Strom.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-124">Start the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ed7f-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**linemediacontrol- \_ volumedown**</span><span class="sxs-lookup"><span data-stu-id="4ed7f-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL\_VOLUMEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4ed7f-126">Die Amplitude des Mediendaten Stroms wird durch eine streamdefinierte Menge verringert.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-126">The amplitude of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ed7f-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**linemediacontrol \_ volumenormal**</span><span class="sxs-lookup"><span data-stu-id="4ed7f-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL\_VOLUMENORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4ed7f-128">Die Amplitude des Mediendaten Stroms wird normal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-128">The amplitude of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ed7f-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**linemediacontrol- \_ volumeup**</span><span class="sxs-lookup"><span data-stu-id="4ed7f-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL\_VOLUMEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4ed7f-130">Die Amplitude des Mediendaten Stroms wird durch eine streamdefinierte Menge erweitert.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-130">The amplitude of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ed7f-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ed7f-131">Remarks</span></span>

<span data-ttu-id="4ed7f-132">Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="4ed7f-133">Die nieder wertigen 16 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="4ed7f-134">Mediensteuerung wird bereitgestellt, um die Leistung von Aktionen in Mediendaten strömen als Reaktion auf telefoniebezogene Ereignisse zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-134">Media control is provided to improve performance of actions on media streams in response to telephony-related events.</span></span> <span data-ttu-id="4ed7f-135">Die Anwendung sollte normalerweise einen Mediendaten Strom über die medienspezifische API verwalten.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-135">The application should normally manage a media stream through the media-specific API.</span></span> <span data-ttu-id="4ed7f-136">Die hier bereitgestellte Medien Steuerungsfunktion ist nicht zum Ersetzen der APIs für Native Medien vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-136">The media-control functionality provided here is not intended to replace the native media APIs.</span></span>

<span data-ttu-id="4ed7f-137">Medien Steuerungs Aktionen können mit der Erkennung von Ziffern, der Erkennung von Tönen, dem Übergang in einen aufrufzustand und der Erkennung eines Medientyps verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-137">Media-control actions can be associated with the detection of digits, the detection of tones, the transition into a call state, and the detection of a media type.</span></span> <span data-ttu-id="4ed7f-138">Überprüfen Sie die Gerätefunktionen einer Zeile, um zu bestimmen, ob die Mediensteuerung in der Zeile verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-138">Consult a line's device capabilities to determine whether media control is available on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ed7f-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ed7f-139">Requirements</span></span>



| <span data-ttu-id="4ed7f-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ed7f-140">Requirement</span></span> | <span data-ttu-id="4ed7f-141">Wert</span><span class="sxs-lookup"><span data-stu-id="4ed7f-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4ed7f-142">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4ed7f-142">TAPI version</span></span><br/> | <span data-ttu-id="4ed7f-143">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4ed7f-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="4ed7f-144">Header</span><span class="sxs-lookup"><span data-stu-id="4ed7f-144">Header</span></span><br/>       | <dl> <span data-ttu-id="4ed7f-145"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ed7f-145"><dt>Tapi.h</dt></span></span> </dl> |



 

 




