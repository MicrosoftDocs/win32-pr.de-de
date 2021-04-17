---
title: WINBIO_PRESENCE_PROPERTIES Union (winbio \_ types. h)
description: Enthält biometrische Werte, die der Windows-Biometrieframework, um zu bestimmen, ob eine Person vorhanden war.
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- WINBIO_PRESENCE_PROPERTIES Union Windows-Biometrieframework-API
- PWINBIO_PRESENCE_PROPERTIES Union-Zeiger Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_PROPERTIES
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0568008b870953c34205706acc90cb22a2c0e92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475663"
---
# <a name="winbio_presence_properties-union"></a><span data-ttu-id="5b08c-105">Winbio- \_ Anwesenheits \_ Eigenschaften Union</span><span class="sxs-lookup"><span data-stu-id="5b08c-105">WINBIO\_PRESENCE\_PROPERTIES union</span></span>

<span data-ttu-id="5b08c-106">Enthält biometrische Werte, die der Windows-Biometrieframework, um zu bestimmen, ob eine Person vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="5b08c-106">Contains biometric values that the Windows Biometric Framework used to determine that an individual was present.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b08c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b08c-107">Syntax</span></span>


```C++
typedef union _WINBIO_PRESENCE_PROPERTIES {
  struct {
    RECT BoundingBox;
    LONG Distance;
  } FacialFeatures;
  struct {
    RECT  EyeBoundingBox_1;
    RECT  EyeBoundingBox_2;
    POINT PupilCenter_1;
    POINT PupilCenter_2;
    LONG  Distance;
  } Iris;
} WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES;
```



## <a name="members"></a><span data-ttu-id="5b08c-108">Member</span><span class="sxs-lookup"><span data-stu-id="5b08c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b08c-109">**Fakialfeatures**</span><span class="sxs-lookup"><span data-stu-id="5b08c-109">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="5b08c-110">Werte für den Speicherort der Gesichts Features, die der Windows-Biometrieframework, um zu bestimmen, ob eine Person vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="5b08c-110">Values for the location of facial features that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="5b08c-111">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="5b08c-111">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="5b08c-112">Die Position innerhalb des Kamera Rahmens der Vorderseite der Person in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5b08c-112">The position within the camera frame of the face of the individual, in pixels.</span></span> <span data-ttu-id="5b08c-113">Die Größe des Kamera Rahmens bestimmt die Obergrenze für die Anzahl der Pixel für diese Position.</span><span class="sxs-lookup"><span data-stu-id="5b08c-113">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="5b08c-114">Die Eigenschaft " **\_ \_ erweiterter \_ Sensor \_ Info" der winbio-Eigenschaft** zum Bestimmen der Größe des Kamera Rahmens.</span><span class="sxs-lookup"><span data-stu-id="5b08c-114">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="5b08c-115">Ein Client, der den Anwesenheits Monitor verwendet, muss den Skalierungs Vorgang ausführen, um die Position dem Kamera Rahmen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5b08c-115">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame .</span></span>

</dd> <dt>

<span data-ttu-id="5b08c-116">**Entfernung**</span><span class="sxs-lookup"><span data-stu-id="5b08c-116">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="5b08c-117">Der Abstand zwischen dem tatsächlichen Speicherort der Vorderseite und dem idealen Fokusabstand für das Gesicht.</span><span class="sxs-lookup"><span data-stu-id="5b08c-117">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="5b08c-118">Dieser Wert liegt zwischen-100 und 100.</span><span class="sxs-lookup"><span data-stu-id="5b08c-118">This value ranges from -100 to 100.</span></span> <span data-ttu-id="5b08c-119">0 gibt die ideale Entfernung an, positive Werte geben an, dass der tatsächliche Speicherort der Fläche zu weit entfernt ist, und negative Werte geben an, dass der tatsächliche Speicherort zu nah ist.</span><span class="sxs-lookup"><span data-stu-id="5b08c-119">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5b08c-120">**Augen**</span><span class="sxs-lookup"><span data-stu-id="5b08c-120">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="5b08c-121">Werte für Iris-Speicherort, die der Windows-Biometrieframework, um zu bestimmen, ob eine Person vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="5b08c-121">Values for iris location that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="5b08c-122">**Eyeboundingbox \_ 1**</span><span class="sxs-lookup"><span data-stu-id="5b08c-122">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="5b08c-123">Die Position innerhalb des Kamera Rahmens einer der Irises der zu registrierenden Person in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5b08c-123">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="5b08c-124">Wenn das Schwert Erkennungssystem nur ein Auge überwacht, liegt diese Position in der Schwert Position.</span><span class="sxs-lookup"><span data-stu-id="5b08c-124">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="5b08c-125">Wenn das Schwert Erkennungssystem beide Augen überwacht, aber nur ein Auge im Kamera Rahmen ist, ist diese Position der Schwert im Kamera-Frame.</span><span class="sxs-lookup"><span data-stu-id="5b08c-125">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="5b08c-126">Wenn das Schwert Erkennungssystem beide Augen überwacht und beide Augen im Kamera Rahmen sind, ist diese Position wahrscheinlich die Schwert Ecke der Person.</span><span class="sxs-lookup"><span data-stu-id="5b08c-126">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="5b08c-127">Die Größe des Kamera Rahmens bestimmt die Obergrenze für die Anzahl der Pixel für diese Position.</span><span class="sxs-lookup"><span data-stu-id="5b08c-127">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="5b08c-128">Die Eigenschaft " **\_ \_ erweiterter \_ Sensor \_ Info" der winbio-Eigenschaft** zum Bestimmen der Größe des Kamera Rahmens.</span><span class="sxs-lookup"><span data-stu-id="5b08c-128">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="5b08c-129">Ein Client, der den Anwesenheits Monitor verwendet, muss den Skalierungs Vorgang ausführen, um die Position dem Kamera Rahmen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5b08c-129">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="5b08c-130">**Eyeboundingbox \_ 2**</span><span class="sxs-lookup"><span data-stu-id="5b08c-130">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="5b08c-131">Die Position innerhalb des Kamera Rahmens einer der Irises der zu registrierenden Person in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5b08c-131">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="5b08c-132">Wenn das Schwert Erkennungssystem nur ein Auge überwacht oder sich nur ein Auge im Kamera Rahmen befindet, ist dieser Wert leer.</span><span class="sxs-lookup"><span data-stu-id="5b08c-132">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="5b08c-133">Wenn das Schwert Erkennungssystem beide Augen überwacht und beide Augen im Kamera Rahmen sind, ist diese Position wahrscheinlich die Schwert Ecke der Person.</span><span class="sxs-lookup"><span data-stu-id="5b08c-133">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="5b08c-134">Die Größe des Kamera Rahmens bestimmt die Obergrenze für die Anzahl der Pixel für diese Position.</span><span class="sxs-lookup"><span data-stu-id="5b08c-134">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="5b08c-135">Die Eigenschaft " **\_ \_ erweiterter \_ Sensor \_ Info" der winbio-Eigenschaft** zum Bestimmen der Größe des Kamera Rahmens.</span><span class="sxs-lookup"><span data-stu-id="5b08c-135">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="5b08c-136">Ein Client, der den Anwesenheits Monitor verwendet, muss den Skalierungs Vorgang ausführen, um die Position dem Kamera Rahmen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5b08c-136">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="5b08c-137">**Pupilcenter \_ 1**</span><span class="sxs-lookup"><span data-stu-id="5b08c-137">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="5b08c-138">Die Position der Mitte eines der zu registrierenden Schüler und/oder der zu registrierenden Person.</span><span class="sxs-lookup"><span data-stu-id="5b08c-138">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="5b08c-139">Wenn das Schwert Erkennungssystem nur ein Auge überwacht, liegt diese Position in der Mitte der Schülerin dieses Auges.</span><span class="sxs-lookup"><span data-stu-id="5b08c-139">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="5b08c-140">Wenn das Schwert Erkennungssystem beide Augen überwacht, sich aber nur ein Auge im Kamera Rahmen befindet, liegt diese Position in der Mitte der Schülerin des Augen Bilds.</span><span class="sxs-lookup"><span data-stu-id="5b08c-140">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="5b08c-141">Wenn das Schwert Erkennungssystem beide Augen überwacht und beide Augen sich im Kamera Rahmen befinden, liegt diese Position wahrscheinlich in der Mitte des Schülers der Person.</span><span class="sxs-lookup"><span data-stu-id="5b08c-141">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="5b08c-142">**Pupilcenter \_ 2**</span><span class="sxs-lookup"><span data-stu-id="5b08c-142">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="5b08c-143">Die Position der Mitte eines der zu registrierenden Schüler und/oder der zu registrierenden Person.</span><span class="sxs-lookup"><span data-stu-id="5b08c-143">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="5b08c-144">Wenn das Schwert Erkennungssystem nur ein Auge überwacht oder sich nur ein Auge im Kamera Rahmen befindet, ist dieser Wert leer.</span><span class="sxs-lookup"><span data-stu-id="5b08c-144">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="5b08c-145">Wenn das Schwert Erkennungssystem beide Augen überwacht und beide Augen sich im Kamera Rahmen befinden, liegt diese Position wahrscheinlich in der Mitte der Schülerin des linken Auges der Person.</span><span class="sxs-lookup"><span data-stu-id="5b08c-145">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="5b08c-146">**Entfernung**</span><span class="sxs-lookup"><span data-stu-id="5b08c-146">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="5b08c-147">Der Abstand zwischen dem tatsächlichen Speicherort der Iris und dem idealen Fokusabstand für die Iris.</span><span class="sxs-lookup"><span data-stu-id="5b08c-147">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="5b08c-148">Dieser Wert liegt zwischen-100 und 100.</span><span class="sxs-lookup"><span data-stu-id="5b08c-148">This value ranges from -100 to 100.</span></span> <span data-ttu-id="5b08c-149">0 gibt die ideale Entfernung an, positive Werte geben an, dass der tatsächliche Speicherort der IRIS zu weit entfernt ist, und negative Werte geben an, dass der tatsächliche Speicherort zu nah ist.</span><span class="sxs-lookup"><span data-stu-id="5b08c-149">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b08c-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b08c-150">Requirements</span></span>



| <span data-ttu-id="5b08c-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b08c-151">Requirement</span></span> | <span data-ttu-id="5b08c-152">Wert</span><span class="sxs-lookup"><span data-stu-id="5b08c-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b08c-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b08c-153">Minimum supported client</span></span><br/> | <span data-ttu-id="5b08c-154">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b08c-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="5b08c-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b08c-155">Minimum supported server</span></span><br/> | <span data-ttu-id="5b08c-156">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b08c-156">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="5b08c-157">Header</span><span class="sxs-lookup"><span data-stu-id="5b08c-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b08c-158"><dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="5b08c-158"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





