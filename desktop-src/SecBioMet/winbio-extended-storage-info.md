---
title: WINBIO_EXTENDED_STORAGE_INFO Struktur (winbio \_ types. h)
description: Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- WINBIO_EXTENDED_STORAGE_INFO Struktur Windows-Biometrieframework-API
- PWINBIO_EXTENDED_STORAGE_INFO Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_STORAGE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2559717a2040cfb617e85e0a51495be1b5987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949523"
---
# <a name="winbio_extended_storage_info-structure"></a><span data-ttu-id="dbf2d-105">\_Struktur erweiterter winbio- \_ Speicher \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="dbf2d-105">WINBIO\_EXTENDED\_STORAGE\_INFO structure</span></span>

<span data-ttu-id="dbf2d-106">Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit.</span><span class="sxs-lookup"><span data-stu-id="dbf2d-106">Contains information about the capabilities and enrollment requirements of the storage adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf2d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbf2d-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_STORAGE_INFO {
  WINBIO_CAPABILITIES   GenericStorageCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_STORAGE_INFO, *PWINBIO_EXTENDED_STORAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="dbf2d-108">Member</span><span class="sxs-lookup"><span data-stu-id="dbf2d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dbf2d-109">**Genericstorage-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-109">**GenericStorageCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="dbf2d-110">Die generischen Funktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="dbf2d-110">The generic capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="dbf2d-111">**Aspekt**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="dbf2d-112">Der Typ der biometrischen Einheit, für die diese Strukturinformationen zu Funktionen und Registrierungsanforderungen des Speicher Adapters enthält.</span><span class="sxs-lookup"><span data-stu-id="dbf2d-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the storage adapter.</span></span> <span data-ttu-id="dbf2d-113">Wenn z. b. der Wert des **Factor** -Members **winbio \_ - \_ typfingerabdruck** ist, gilt die **Erweiterte winbio- \_ \_ Speicher \_ Informations** Struktur für einen Fingerabdruckleser und enthält die relevanten Informationen in der **specifc. Fingerabdruck** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="dbf2d-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_STORAGE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="dbf2d-114">**Zugeschnitten**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="dbf2d-115">Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit im Zusammenhang mit einem bestimmten biometrischen Faktor.</span><span class="sxs-lookup"><span data-stu-id="dbf2d-115">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="dbf2d-116">**NULL**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="dbf2d-117">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="dbf2d-117">Reserved.</span></span> <span data-ttu-id="dbf2d-118">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="dbf2d-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dbf2d-119">**Fakialfeatures**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="dbf2d-120">Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit im Zusammenhang mit Gesichtsmerkmalen.</span><span class="sxs-lookup"><span data-stu-id="dbf2d-120">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="dbf2d-121">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="dbf2d-122">Die Gesichts Erkennungsfunktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="dbf2d-122">The facial recognition capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="dbf2d-123">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-123">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="dbf2d-124">Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit im Zusammenhang mit Fingerabdruck Mustern.</span><span class="sxs-lookup"><span data-stu-id="dbf2d-124">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="dbf2d-125">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-125">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="dbf2d-126">Die Fingerabdruck Erkennungsfunktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist</span><span class="sxs-lookup"><span data-stu-id="dbf2d-126">The fingerprint recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="dbf2d-127">**Augen**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-127">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="dbf2d-128">Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit im Zusammenhang mit Iris-Mustern.</span><span class="sxs-lookup"><span data-stu-id="dbf2d-128">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="dbf2d-129">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-129">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="dbf2d-130">Die Iris-Erkennungsfunktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist</span><span class="sxs-lookup"><span data-stu-id="dbf2d-130">The iris recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="dbf2d-131">**Voice**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-131">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="dbf2d-132">Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit im Zusammenhang mit Sprachmustern.</span><span class="sxs-lookup"><span data-stu-id="dbf2d-132">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="dbf2d-133">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="dbf2d-134">Die Spracherkennungsfunktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist</span><span class="sxs-lookup"><span data-stu-id="dbf2d-134">The voice recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbf2d-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbf2d-135">Requirements</span></span>



| <span data-ttu-id="dbf2d-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbf2d-136">Requirement</span></span> | <span data-ttu-id="dbf2d-137">Wert</span><span class="sxs-lookup"><span data-stu-id="dbf2d-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf2d-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbf2d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf2d-139">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbf2d-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="dbf2d-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbf2d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf2d-141">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbf2d-141">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="dbf2d-142">Header</span><span class="sxs-lookup"><span data-stu-id="dbf2d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbf2d-143"><dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="dbf2d-143"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbf2d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbf2d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf2d-145">**Winbio- \_ biometrische \_ Typkonstanten**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-145">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="dbf2d-146">**Winbio-Funktions \_ Konstanten**</span><span class="sxs-lookup"><span data-stu-id="dbf2d-146">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> </dl>

 

 





