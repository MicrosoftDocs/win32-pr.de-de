---
title: WINBIO_EXTENDED_ENGINE_INFO Struktur (winbio \_ types. h)
description: Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit.
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- WINBIO_EXTENDED_ENGINE_INFO Struktur Windows-Biometrieframework-API
- PWINBIO_EXTENDED_ENGINE_INFO Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENGINE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829bd0423ab6add41b17f59d308aea850c5b2f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859267"
---
# <a name="winbio_extended_engine_info-structure"></a><span data-ttu-id="a71ee-105">Struktur der erweiterten winbio- \_ \_ Engine- \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="a71ee-105">WINBIO\_EXTENDED\_ENGINE\_INFO structure</span></span>

<span data-ttu-id="a71ee-106">Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit.</span><span class="sxs-lookup"><span data-stu-id="a71ee-106">Contains information about the capabilities and enrollment requirements of the engine adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="a71ee-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a71ee-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENGINE_INFO {
  WINBIO_CAPABILITIES   GenericEngineCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG GeneralSamples;
        ULONG Center;
        ULONG TopEdge;
        ULONG BottomEdge;
        ULONG LeftEdge;
        ULONG RightEdge;
      } EnrollmentRequirements;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENGINE_INFO, *PWINBIO_EXTENDED_ENGINE_INFO;
```



## <a name="members"></a><span data-ttu-id="a71ee-108">Member</span><span class="sxs-lookup"><span data-stu-id="a71ee-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a71ee-109">**Genericenginecapabilitäten**</span><span class="sxs-lookup"><span data-stu-id="a71ee-109">**GenericEngineCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-110">Die generischen Funktionen der Engine-Komponente, die mit einer bestimmten biometrischen Einheit verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="a71ee-110">The generic capabilities of the engine component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="a71ee-111">**Aspekt**</span><span class="sxs-lookup"><span data-stu-id="a71ee-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-112">Der Typ der biometrischen Einheit, für die diese Strukturinformationen zu Funktionen und Registrierungsanforderungen des Engine-Adapters enthält.</span><span class="sxs-lookup"><span data-stu-id="a71ee-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="a71ee-113">Wenn z. b. der Wert des  **\_ faktermembers winbio- \_ Fingerabdruck** ist, gilt die Struktur der **\_ erweiterten \_ Engine \_** -Informationen von winbio für einen Fingerabdruckleser und enthält die relevanten Informationen in der **specifc. Fingerabdruck** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a71ee-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_ENGINE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="a71ee-114">**Zugeschnitten**</span><span class="sxs-lookup"><span data-stu-id="a71ee-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-115">Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit einem bestimmten biometrischen Faktor.</span><span class="sxs-lookup"><span data-stu-id="a71ee-115">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="a71ee-116">**NULL**</span><span class="sxs-lookup"><span data-stu-id="a71ee-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-117">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a71ee-117">Reserved.</span></span> <span data-ttu-id="a71ee-118">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a71ee-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a71ee-119">**Fakialfeatures**</span><span class="sxs-lookup"><span data-stu-id="a71ee-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-120">Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit Gesichtsmerkmalen.</span><span class="sxs-lookup"><span data-stu-id="a71ee-120">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="a71ee-121">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="a71ee-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-122">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a71ee-122">Reserved.</span></span> <span data-ttu-id="a71ee-123">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a71ee-123">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a71ee-124">**Registrierungsanforderungen**</span><span class="sxs-lookup"><span data-stu-id="a71ee-124">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a71ee-125">**NULL**</span><span class="sxs-lookup"><span data-stu-id="a71ee-125">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-126">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a71ee-126">Reserved.</span></span> <span data-ttu-id="a71ee-127">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a71ee-127">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="a71ee-128">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="a71ee-128">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-129">Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit Fingerabdruck Mustern.</span><span class="sxs-lookup"><span data-stu-id="a71ee-129">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="a71ee-130">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="a71ee-130">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-131">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a71ee-131">Reserved.</span></span> <span data-ttu-id="a71ee-132">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a71ee-132">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a71ee-133">**Registrierungsanforderungen**</span><span class="sxs-lookup"><span data-stu-id="a71ee-133">**EnrollmentRequirements**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-134">Die Anzahl von guten Beispielen, die zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a71ee-134">The number of good samples required to create a new fingerprint template.</span></span>

<dl> <dt>

<span data-ttu-id="a71ee-135">**Generalsamples**</span><span class="sxs-lookup"><span data-stu-id="a71ee-135">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-136">Die Gesamtanzahl der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlichen guten Stichproben.</span><span class="sxs-lookup"><span data-stu-id="a71ee-136">The total number of good samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="a71ee-137">**Tagesstätte**</span><span class="sxs-lookup"><span data-stu-id="a71ee-137">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-138">Die Anzahl von guten Beispielen für den Mittelpunkt des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a71ee-138">The number of good samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="a71ee-139">**Topedge**</span><span class="sxs-lookup"><span data-stu-id="a71ee-139">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-140">Die Anzahl von guten Beispielen für den oberen Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a71ee-140">The number of good samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="a71ee-141">**Bottomedge**</span><span class="sxs-lookup"><span data-stu-id="a71ee-141">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-142">Die Anzahl von guten Beispielen für den unteren Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a71ee-142">The number of good samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="a71ee-143">**Leftedge**</span><span class="sxs-lookup"><span data-stu-id="a71ee-143">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-144">Die Anzahl von guten Beispielen für den linken Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a71ee-144">The number of good samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="a71ee-145">**Rechtschaffdge**</span><span class="sxs-lookup"><span data-stu-id="a71ee-145">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-146">Die Anzahl von guten Beispielen für den rechten Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a71ee-146">The number of good samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="a71ee-147">**Augen**</span><span class="sxs-lookup"><span data-stu-id="a71ee-147">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-148">Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit Iris-Mustern.</span><span class="sxs-lookup"><span data-stu-id="a71ee-148">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="a71ee-149">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="a71ee-149">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-150">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a71ee-150">Reserved.</span></span> <span data-ttu-id="a71ee-151">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a71ee-151">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a71ee-152">**Registrierungsanforderungen**</span><span class="sxs-lookup"><span data-stu-id="a71ee-152">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a71ee-153">**NULL**</span><span class="sxs-lookup"><span data-stu-id="a71ee-153">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-154">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a71ee-154">Reserved.</span></span> <span data-ttu-id="a71ee-155">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a71ee-155">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="a71ee-156">**Voice**</span><span class="sxs-lookup"><span data-stu-id="a71ee-156">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-157">Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit Sprachmustern.</span><span class="sxs-lookup"><span data-stu-id="a71ee-157">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="a71ee-158">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="a71ee-158">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-159">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a71ee-159">Reserved.</span></span> <span data-ttu-id="a71ee-160">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a71ee-160">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a71ee-161">**Registrierungsanforderungen**</span><span class="sxs-lookup"><span data-stu-id="a71ee-161">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a71ee-162">**NULL**</span><span class="sxs-lookup"><span data-stu-id="a71ee-162">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="a71ee-163">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a71ee-163">Reserved.</span></span> <span data-ttu-id="a71ee-164">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a71ee-164">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a71ee-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a71ee-165">Requirements</span></span>



| <span data-ttu-id="a71ee-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a71ee-166">Requirement</span></span> | <span data-ttu-id="a71ee-167">Wert</span><span class="sxs-lookup"><span data-stu-id="a71ee-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a71ee-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a71ee-168">Minimum supported client</span></span><br/> | <span data-ttu-id="a71ee-169">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a71ee-169">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="a71ee-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a71ee-170">Minimum supported server</span></span><br/> | <span data-ttu-id="a71ee-171">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a71ee-171">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="a71ee-172">Header</span><span class="sxs-lookup"><span data-stu-id="a71ee-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="a71ee-173"><dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="a71ee-173"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a71ee-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a71ee-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a71ee-175">**Winbio-Funktions \_ Konstanten**</span><span class="sxs-lookup"><span data-stu-id="a71ee-175">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="a71ee-176">**Winbio- \_ biometrische \_ Typkonstanten**</span><span class="sxs-lookup"><span data-stu-id="a71ee-176">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> </dl>

 

 





