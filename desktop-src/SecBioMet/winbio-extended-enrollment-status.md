---
title: WINBIO_EXTENDED_ENROLLMENT_STATUS Struktur (winbio \_ types. h)
description: Enthält weitere Informationen zum Status einer aktuell ausgeführten Registrierung.
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- WINBIO_EXTENDED_ENROLLMENT_STATUS Struktur Windows-Biometrieframework-API
- PWINBIO_EXTENDED_ENROLLMENT_STATUS Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_STATUS
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 937e56e438feadc646329c673af4454cb39eaddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103114"
---
# <a name="winbio_extended_enrollment_status-structure"></a><span data-ttu-id="c1ba4-105">Struktur der erweiterten winbio-Registrierungs \_ \_ \_ Status</span><span class="sxs-lookup"><span data-stu-id="c1ba4-105">WINBIO\_EXTENDED\_ENROLLMENT\_STATUS structure</span></span>

<span data-ttu-id="c1ba4-106">Enthält weitere Informationen zum Status einer aktuell ausgeführten Registrierung.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-106">Contains additional information about the status of an enrollment that is in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1ba4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1ba4-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_STATUS {
  HRESULT                  TemplateStatus;
  WINBIO_REJECT_DETAIL     RejectDetail;
  ULONG                    PercentComplete;
  WINBIO_BIOMETRIC_TYPE    Factor;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
  union {
    ULONG32 Null;
    struct {
      RECT BoundingBox;
      LONG Distance;
    } FacialFeatures;
    struct {
      ULONG GeneralSamples;
      ULONG Center;
      ULONG TopEdge;
      ULONG BottomEdge;
      ULONG LeftEdge;
      ULONG RightEdge;
    } Fingerprint;
    struct {
      RECT  EyeBoundingBox_1;
      RECT  EyeBoundingBox_2;
      POINT PupilCenter_1;
      POINT PupilCenter_2;
      LONG  Distance;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS;
```



## <a name="members"></a><span data-ttu-id="c1ba4-108">Member</span><span class="sxs-lookup"><span data-stu-id="c1ba4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1ba4-109">**TemplateStatus**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-109">**TemplateStatus**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-110">Der Status der Beispiel Auflistung für die Registrierungs Vorlage.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-110">The status of sample collection for the enrollment template.</span></span> <span data-ttu-id="c1ba4-111">Die folgenden Werte sind für diesen Member möglich.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-111">The following values are possible for this member.</span></span>



| <span data-ttu-id="c1ba4-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c1ba4-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="c1ba4-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c1ba4-113">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="c1ba4-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c1ba4-114"><dt>**S\_OK**</dt></span></span> </dl>                                                                     | <span data-ttu-id="c1ba4-115">Die Registrierung kann jetzt gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-115">The enrollment is ready to be saved.</span></span><br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <span data-ttu-id="c1ba4-116"><dt>**\_Ungültiger winbio E- \_ \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="c1ba4-116"><dt>**WINBIO\_E\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c1ba4-117">Es wird keine Registrierung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-117">No enrollment is in progress.</span></span><br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <span data-ttu-id="c1ba4-118"><dt>**winbio \_ I \_ more \_ Data**</dt></span><span class="sxs-lookup"><span data-stu-id="c1ba4-118"><dt>**WINBIO\_I\_MORE\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="c1ba4-119">Weitere Beispiele sind erforderlich, um die Vorlage abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-119">More samples are required to complete the template.</span></span><br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <span data-ttu-id="c1ba4-120"><dt>**winbio \_ E ungültige \_ \_ Erfassung**</dt></span><span class="sxs-lookup"><span data-stu-id="c1ba4-120"><dt>**WINBIO\_E\_BAD\_CAPTURE**</dt></span></span> </dl>                   | <span data-ttu-id="c1ba4-121">Das aktuelle Beispiel kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-121">The most recent sample is not usable.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="c1ba4-122">**Rejectdetail**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-123">Der Grund, warum das aktuellste Beispiel nicht verwendbar ist, wenn der Wert des **templatestatus** -Members **winbio E ungültige \_ \_ \_ Erfassung** ist.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-123">The reason that the most recent sample is unusable, if the value of the **TemplateStatus** member is **WINBIO\_E\_BAD\_CAPTURE**.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-124">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-124">**PercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-125">Die beste Schätzung vom Modul Adapter für den Prozentsatz der abgeschlossenen Vorlage als Wert zwischen 0 und 100.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-125">The best estimate from the engine adapter for the percentage of the template that is complete, as a value from 0 to 100.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-126">**Aspekt**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-126">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-127">Der Typ der biometrischen Einheit, für die diese Strukturinformationen zu Funktionen und Registrierungsanforderungen des Engine-Adapters enthält.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-127">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="c1ba4-128">Wenn z. b. der Wert des  **\_ faktermembers winbio- \_ Fingerabdruck** ist, gilt die Struktur der [**\_ erweiterten \_ Engine \_**](winbio-extended-engine-info.md) -Informationen von winbio für einen Fingerabdruckleser und enthält die relevanten Informationen in der **specifc. Fingerabdruck** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-128">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-129">**Teilfaktor**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-129">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-130">Ein Wert des **\_ \_ Subtyps "winbio biometrische** ", der zusätzliche Informationen über die Registrierung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-130">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that provides additional information about the enrollment.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-131">**Zugeschnitten**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-131">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-132">Informationen zum Status einer Registrierung, die für einen bestimmten biometrischen Faktor ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-132">Information about the status of an enrollment that is in progress for a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="c1ba4-133">**NULL**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-133">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-134">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-134">Reserved.</span></span> <span data-ttu-id="c1ba4-135">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-135">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-136">**Fakialfeatures**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-136">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-137">Informationen zum Status einer Registrierung, die für Gesichts Features ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-137">Information about the status of an enrollment that is in progress for facial features.</span></span>

<dl> <dt>

<span data-ttu-id="c1ba4-138">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-138">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-139">Die Position innerhalb des Kamera Rahmens der Vorderseite der zu registrierenden Person in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-139">The position within the camera frame of the face of the individual to enroll, in pixels.</span></span> <span data-ttu-id="c1ba4-140">Die Größe des Kamera Rahmens bestimmt die Obergrenze für die Anzahl der Pixel für diese Position.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-140">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="c1ba4-141">Die Eigenschaft " **\_ \_ erweiterter \_ Sensor \_ Info" der winbio-Eigenschaft** zum Bestimmen der Größe des Kamera Rahmens.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-141">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="c1ba4-142">Ein Client, der den Anwesenheits Monitor verwendet, muss den Skalierungs Vorgang ausführen, um die Position dem Kamera Rahmen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-142">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-143">**Entfernung**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-143">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-144">Der Abstand zwischen dem tatsächlichen Speicherort der Vorderseite und dem idealen Fokusabstand für das Gesicht.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-144">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="c1ba4-145">Dieser Wert liegt zwischen-100 und 100.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-145">This value ranges from -100 to 100.</span></span> <span data-ttu-id="c1ba4-146">0 gibt die ideale Entfernung an, positive Werte geben an, dass der tatsächliche Speicherort der Fläche zu weit entfernt ist, und negative Werte geben an, dass der tatsächliche Speicherort zu nah ist.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-146">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c1ba4-147">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-147">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-148">Informationen zum Status einer Registrierung, die für Fingerabdruck Muster in Bearbeitung ist.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-148">Information about the status of an enrollment that is in progress for fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="c1ba4-149">**Generalsamples**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-149">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-150">Die Gesamtanzahl der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlichen Stichproben.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-150">The total number of samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-151">**Tagesstätte**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-151">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-152">Die Anzahl der Abtastungen für die Mitte des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-152">The number of samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-153">**Topedge**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-153">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-154">Die Anzahl der Abtastungen für den oberen Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-154">The number of samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-155">**Bottomedge**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-155">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-156">Die Anzahl der Abtastungen für den unteren Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-156">The number of samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-157">**Leftedge**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-157">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-158">Die Anzahl der Abtastungen für den linken Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-158">The number of samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-159">**Rechtschaffdge**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-159">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-160">Die Anzahl der Abtastungen für den rechten Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-160">The number of samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c1ba4-161">**Augen**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-161">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-162">Informationen zum Status einer Registrierung, die für Iris-Muster ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-162">Information about the status of an enrollment that is in progress for iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="c1ba4-163">**Eyeboundingbox \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-163">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-164">Die Position innerhalb des Kamera Rahmens einer der Irises der zu registrierenden Person in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-164">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="c1ba4-165">Wenn das Schwert Erkennungssystem nur ein Auge überwacht, liegt diese Position in der Schwert Position.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-165">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="c1ba4-166">Wenn das Schwert Erkennungssystem beide Augen überwacht, aber nur ein Auge im Kamera Rahmen ist, ist diese Position der Schwert im Kamera-Frame.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-166">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="c1ba4-167">Wenn das Schwert Erkennungssystem beide Augen überwacht und beide Augen im Kamera Rahmen sind, ist diese Position wahrscheinlich die Schwert Ecke der Person.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-167">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="c1ba4-168">Die Größe des Kamera Rahmens bestimmt die Obergrenze für die Anzahl der Pixel für diese Position.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-168">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="c1ba4-169">Die Eigenschaft " **\_ \_ erweiterter \_ Sensor \_ Info" der winbio-Eigenschaft** zum Bestimmen der Größe des Kamera Rahmens.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-169">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="c1ba4-170">Ein Client, der den Anwesenheits Monitor verwendet, muss den Skalierungs Vorgang ausführen, um die Position dem Kamera Rahmen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-170">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-171">**Eyeboundingbox \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-171">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-172">Die Position innerhalb des Kamera Rahmens einer der Irises der zu registrierenden Person in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-172">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="c1ba4-173">Wenn das Schwert Erkennungssystem nur ein Auge überwacht oder sich nur ein Auge im Kamera Rahmen befindet, ist dieser Wert leer.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-173">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="c1ba4-174">Wenn das Schwert Erkennungssystem beide Augen überwacht und beide Augen im Kamera Rahmen sind, ist diese Position wahrscheinlich die Schwert Ecke der Person.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-174">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="c1ba4-175">Die Größe des Kamera Rahmens bestimmt die Obergrenze für die Anzahl der Pixel für diese Position.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-175">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="c1ba4-176">Die Eigenschaft " **\_ \_ erweiterter \_ Sensor \_ Info" der winbio-Eigenschaft** zum Bestimmen der Größe des Kamera Rahmens.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-176">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="c1ba4-177">Ein Client, der den Anwesenheits Monitor verwendet, muss den Skalierungs Vorgang ausführen, um die Position dem Kamera Rahmen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-177">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-178">**Pupilcenter \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-178">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-179">Die Position der Mitte eines der zu registrierenden Schüler und/oder der zu registrierenden Person.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-179">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="c1ba4-180">Wenn das Schwert Erkennungssystem nur ein Auge überwacht, liegt diese Position in der Mitte der Schülerin dieses Auges.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-180">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="c1ba4-181">Wenn das Schwert Erkennungssystem beide Augen überwacht, sich aber nur ein Auge im Kamera Rahmen befindet, liegt diese Position in der Mitte der Schülerin des Augen Bilds.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-181">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="c1ba4-182">Wenn das Schwert Erkennungssystem beide Augen überwacht und beide Augen sich im Kamera Rahmen befinden, liegt diese Position wahrscheinlich in der Mitte des Schülers der Person.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-182">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-183">**Pupilcenter \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-183">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-184">Die Position der Mitte eines der zu registrierenden Schüler und/oder der zu registrierenden Person.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-184">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="c1ba4-185">Wenn das Schwert Erkennungssystem nur ein Auge überwacht oder sich nur ein Auge im Kamera Rahmen befindet, ist dieser Wert leer.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-185">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="c1ba4-186">Wenn das Schwert Erkennungssystem beide Augen überwacht und beide Augen sich im Kamera Rahmen befinden, liegt diese Position wahrscheinlich in der Mitte der Schülerin des linken Auges der Person.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-186">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="c1ba4-187">**Entfernung**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-187">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-188">Der Abstand zwischen dem tatsächlichen Speicherort der Iris und dem idealen Fokusabstand für die Iris.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-188">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="c1ba4-189">Dieser Wert liegt zwischen-100 und 100.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-189">This value ranges from -100 to 100.</span></span> <span data-ttu-id="c1ba4-190">0 gibt die ideale Entfernung an, positive Werte geben an, dass der tatsächliche Speicherort der IRIS zu weit entfernt ist, und negative Werte geben an, dass der tatsächliche Speicherort zu nah ist.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-190">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c1ba4-191">**Voice**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-191">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-192">Informationen zum Status einer Registrierung, die für Sprachmuster in Bearbeitung ist.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-192">Information about the status of an enrollment that is in progress for voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="c1ba4-193">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="c1ba4-193">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="c1ba4-194">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="c1ba4-194">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1ba4-195">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1ba4-195">Requirements</span></span>



| <span data-ttu-id="c1ba4-196">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1ba4-196">Requirement</span></span> | <span data-ttu-id="c1ba4-197">Wert</span><span class="sxs-lookup"><span data-stu-id="c1ba4-197">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1ba4-198">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1ba4-198">Minimum supported client</span></span><br/> | <span data-ttu-id="c1ba4-199">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1ba4-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="c1ba4-200">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1ba4-200">Minimum supported server</span></span><br/> | <span data-ttu-id="c1ba4-201">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1ba4-201">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="c1ba4-202">Header</span><span class="sxs-lookup"><span data-stu-id="c1ba4-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1ba4-203"><dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="c1ba4-203"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





