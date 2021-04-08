---
title: WINBIO_EXTENDED_SENSOR_INFO Struktur (winbio \_ types. h)
description: Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- WINBIO_EXTENDED_SENSOR_INFO Struktur Windows-Biometrieframework-API
- PWINBIO_EXTENDED_SENSOR_INFO Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_SENSOR_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c535ef56eeade897aac3c1d0503477da406935b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949524"
---
# <a name="winbio_extended_sensor_info-structure"></a><span data-ttu-id="1b71f-105">\_Struktur erweiterter winbio- \_ Sensor \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="1b71f-105">WINBIO\_EXTENDED\_SENSOR\_INFO structure</span></span>

<span data-ttu-id="1b71f-106">Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit.</span><span class="sxs-lookup"><span data-stu-id="1b71f-106">Contains information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b71f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b71f-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_SENSOR_INFO {
  WINBIO_CAPABILITIES   GenericSensorCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } FacialFeatures;
    struct {
      ULONG32 Reserved;
    } Fingerprint;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO;
```



## <a name="members"></a><span data-ttu-id="1b71f-108">Member</span><span class="sxs-lookup"><span data-stu-id="1b71f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b71f-109">**Genericsensor-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="1b71f-109">**GenericSensorCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-110">Die generischen Funktionen der sensorkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="1b71f-110">The generic capabilities of the sensor component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="1b71f-111">**Aspekt**</span><span class="sxs-lookup"><span data-stu-id="1b71f-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-112">Der Typ der biometrischen Einheit, für die diese Strukturinformationen zu Funktionen und Registrierungsanforderungen des Sensor Adapters enthält.</span><span class="sxs-lookup"><span data-stu-id="1b71f-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the sensor adapter.</span></span> <span data-ttu-id="1b71f-113">Wenn z. b. der Wert des  **\_ faktermembers winbio- \_ Fingerabdruck** ist, gilt die Struktur **Erweiterter winbio- \_ \_ Sensor \_** für einen Fingerabdruckleser und enthält die relevanten Informationen in der **specifc. Fingerabdruck** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1b71f-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_SENSOR\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="1b71f-114">**Zugeschnitten**</span><span class="sxs-lookup"><span data-stu-id="1b71f-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-115">Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit im Zusammenhang mit einem bestimmten biometrischen Faktor.</span><span class="sxs-lookup"><span data-stu-id="1b71f-115">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="1b71f-116">**NULL**</span><span class="sxs-lookup"><span data-stu-id="1b71f-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-117">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="1b71f-117">Reserved.</span></span> <span data-ttu-id="1b71f-118">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1b71f-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1b71f-119">**Fakialfeatures**</span><span class="sxs-lookup"><span data-stu-id="1b71f-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-120">Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit im Zusammenhang mit Gesichtsmerkmalen.</span><span class="sxs-lookup"><span data-stu-id="1b71f-120">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="1b71f-121">**FrameSize**</span><span class="sxs-lookup"><span data-stu-id="1b71f-121">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-122">Die Größe des Kamera Rahmens, angegeben als Länge und Breite in Pixel des **rechten** und **unteren** Members der [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1b71f-122">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="1b71f-123">Der Punkt (0,0) stellt die obere linke Ecke des Frames dar.</span><span class="sxs-lookup"><span data-stu-id="1b71f-123">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="1b71f-124">**Frameoffset**</span><span class="sxs-lookup"><span data-stu-id="1b71f-124">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-125">Der Offset des Kamera Rahmens für das Gesicht von der Videokamera in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1b71f-125">The offset of the camera frame for the face from the video camera, in pixels.</span></span> <span data-ttu-id="1b71f-126">Der Wert (0,0) gibt an, dass sich der Kamera Rahmen für das Gesicht und die Videokamera vollständig überlappt.</span><span class="sxs-lookup"><span data-stu-id="1b71f-126">A value of (0, 0) indicates that the camera frame for the face and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="1b71f-127">**Mandatoryorientation**</span><span class="sxs-lookup"><span data-stu-id="1b71f-127">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-128">Die bevorzugte Ausrichtung für die Kamera.</span><span class="sxs-lookup"><span data-stu-id="1b71f-128">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1b71f-129">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="1b71f-129">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-130">Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit im Zusammenhang mit Fingerabdruck Mustern.</span><span class="sxs-lookup"><span data-stu-id="1b71f-130">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="1b71f-131">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="1b71f-131">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-132">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="1b71f-132">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1b71f-133">**Augen**</span><span class="sxs-lookup"><span data-stu-id="1b71f-133">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-134">Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit im Zusammenhang mit Iris-Mustern.</span><span class="sxs-lookup"><span data-stu-id="1b71f-134">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="1b71f-135">**FrameSize**</span><span class="sxs-lookup"><span data-stu-id="1b71f-135">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-136">Die Größe des Kamera Rahmens, angegeben als Länge und Breite in Pixel des **rechten** und **unteren** Members der [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1b71f-136">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="1b71f-137">Der Punkt (0,0) stellt die obere linke Ecke des Frames dar.</span><span class="sxs-lookup"><span data-stu-id="1b71f-137">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="1b71f-138">**Frameoffset**</span><span class="sxs-lookup"><span data-stu-id="1b71f-138">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-139">Der Offset des Kamera Rahmens für die Iris von der Videokamera in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1b71f-139">The offset of the camera frame for the iris from the video camera, in pixels.</span></span> <span data-ttu-id="1b71f-140">Der Wert (0,0) gibt an, dass sich der Kamera Rahmen für die Iris und die Videokamera vollständig überlappt.</span><span class="sxs-lookup"><span data-stu-id="1b71f-140">A value of (0, 0) indicates that the camera frame for the iris and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="1b71f-141">**Mandatoryorientation**</span><span class="sxs-lookup"><span data-stu-id="1b71f-141">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-142">Die bevorzugte Ausrichtung für die Kamera.</span><span class="sxs-lookup"><span data-stu-id="1b71f-142">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1b71f-143">**Voice**</span><span class="sxs-lookup"><span data-stu-id="1b71f-143">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-144">Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit im Zusammenhang mit Sprachmustern.</span><span class="sxs-lookup"><span data-stu-id="1b71f-144">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="1b71f-145">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="1b71f-145">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="1b71f-146">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="1b71f-146">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b71f-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b71f-147">Requirements</span></span>



| <span data-ttu-id="1b71f-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b71f-148">Requirement</span></span> | <span data-ttu-id="1b71f-149">Wert</span><span class="sxs-lookup"><span data-stu-id="1b71f-149">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b71f-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b71f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="1b71f-151">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b71f-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="1b71f-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b71f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="1b71f-153">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b71f-153">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="1b71f-154">Header</span><span class="sxs-lookup"><span data-stu-id="1b71f-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b71f-155"><dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="1b71f-155"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b71f-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b71f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b71f-157">**Winbio-Funktions \_ Konstanten**</span><span class="sxs-lookup"><span data-stu-id="1b71f-157">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="1b71f-158">**Winbio- \_ biometrische \_ Typkonstanten**</span><span class="sxs-lookup"><span data-stu-id="1b71f-158">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="1b71f-159">**Winbio- \_ Orientierungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="1b71f-159">**WINBIO\_ORIENTATION Constants**</span></span>](winbio-orientation-constants.md)
</dt> </dl>

 

