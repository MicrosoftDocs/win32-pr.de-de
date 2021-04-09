---
title: WINBIO_UNIT_SCHEMA Struktur (winbio \_ types. h)
description: Beschreibt die Funktionen einer biometrischen Einheit.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- WINBIO_UNIT_SCHEMA Struktur Windows-Biometrieframework-API
- PWINBIO_UNIT_SCHEMA Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_UNIT_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c217be1e0c6bde740c815f5a990509a6a87ef0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957155"
---
# <a name="winbio_unit_schema-structure"></a><span data-ttu-id="c7368-105">Struktur des winbio- \_ Einheiten \_ Schemas</span><span class="sxs-lookup"><span data-stu-id="c7368-105">WINBIO\_UNIT\_SCHEMA structure</span></span>

<span data-ttu-id="c7368-106">Die Struktur der **winbio- \_ Einheiten \_ Schema** beschreibt die Funktionen einer biometrischen Einheit.</span><span class="sxs-lookup"><span data-stu-id="c7368-106">The **WINBIO\_UNIT\_SCHEMA** structure describes the capabilities of a biometric unit.</span></span> <span data-ttu-id="c7368-107">Sie wird von der [**winbioenumbiometricunits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7368-107">It is used by the [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7368-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7368-108">Syntax</span></span>


```C++
typedef struct _WINBIO_UNIT_SCHEMA {
  WINBIO_UNIT_ID                  UnitId;
  WINBIO_POOL_TYPE                PoolType;
  WINBIO_BIOMETRIC_TYPE           BiometricFactor;
  WINBIO_BIOMETRIC_SENSOR_SUBTYPE SensorSubType;
  WINBIO_CAPABILITIES             Capabilities;
  WINBIO_STRING                   DeviceInstanceId;
  WINBIO_STRING                   Description;
  WINBIO_STRING                   Manufacturer;
  WINBIO_STRING                   Model;
  WINBIO_STRING                   SerialNumber;
  WINBIO_VERSION                  FirmwareVersion;
} WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="c7368-109">Member</span><span class="sxs-lookup"><span data-stu-id="c7368-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7368-110">**Unitid**</span><span class="sxs-lookup"><span data-stu-id="c7368-110">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="c7368-111">Ein-Wert, der die biometrische Einheit identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c7368-111">A value that identifies the biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="c7368-112">**Pooltyp**</span><span class="sxs-lookup"><span data-stu-id="c7368-112">**PoolType**</span></span>
</dt> <dd>

<span data-ttu-id="c7368-113">Ein **ulong** -Wert, der den Typ der biometrischen Einheit angibt.</span><span class="sxs-lookup"><span data-stu-id="c7368-113">A **ULONG** value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="c7368-114">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="c7368-114">This can be one of the following values:</span></span>



| <span data-ttu-id="c7368-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c7368-115">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="c7368-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c7368-116">Meaning</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="c7368-117"><dt>**winbio- \_ Pool \_ unbekannt**</dt></span><span class="sxs-lookup"><span data-stu-id="c7368-117"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="c7368-118">Der Typ ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c7368-118">The type is unknown.</span></span><br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="c7368-119"><dt>**winbio- \_ Pool \_ System**</dt></span><span class="sxs-lookup"><span data-stu-id="c7368-119"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>    | <span data-ttu-id="c7368-120">Die Sitzung stellt eine Verbindung mit einer freigegebenen Sammlung von biometrischen Einheiten her, die vom Dienstanbieter verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c7368-120">The session connects to a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="c7368-121"><dt>**privater winbio- \_ Pool \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c7368-121"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="c7368-122">Die Sitzung stellt eine Verbindung mit einer Sammlung von biometrischen Einheiten her, die vom Aufrufer verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c7368-122">The session connects to a collection of biometric units that are managed by the caller.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="c7368-123">**Biometricfactor**</span><span class="sxs-lookup"><span data-stu-id="c7368-123">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="c7368-124">Ein-Wert, der den Typ der biometrischen Einheit angibt.</span><span class="sxs-lookup"><span data-stu-id="c7368-124">A value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="c7368-125">Derzeit wird nur der **winbio- \_ \_ typfingerabdruck** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7368-125">Only **WINBIO\_TYPE\_FINGERPRINT** is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="c7368-126">**Sensorsubtype**</span><span class="sxs-lookup"><span data-stu-id="c7368-126">**SensorSubType**</span></span>
</dt> <dd>

<span data-ttu-id="c7368-127">Ein Sensor Untertyp, der für den biometrischen Typ definiert ist, der vom **biometricfactor** -Member angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c7368-127">A sensor subtype defined for the biometric type specified by the **BiometricFactor** member.</span></span> <span data-ttu-id="c7368-128">Derzeit werden nur Fingerabdruck Typen (**winbio- \_ \_ typfingerabdruck**) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7368-128">Only fingerprint types (**WINBIO\_TYPE\_FINGERPRINT**) are currently supported.</span></span> <span data-ttu-id="c7368-129">Die folgenden Untertypen sind zurzeit für Fingerabdrücke definiert:</span><span class="sxs-lookup"><span data-stu-id="c7368-129">The following subtypes are currently defined for fingerprints:</span></span>

-   <span data-ttu-id="c7368-130">der winbio- \_ Sensor \_ Untertyp ist \_ unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c7368-130">WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="c7368-131">winbio- \_ FP- \_ \_ unter Typ \_ schwenken</span><span class="sxs-lookup"><span data-stu-id="c7368-131">WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE</span></span>
-   <span data-ttu-id="c7368-132">Fingereingabe von winbio \_ FP- \_ Sensor \_ unter Typ \_</span><span class="sxs-lookup"><span data-stu-id="c7368-132">WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH</span></span>

</dd> <dt>

<span data-ttu-id="c7368-133">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c7368-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="c7368-134">Eine Bitmaske der Funktionen des biometrischen Sensors.</span><span class="sxs-lookup"><span data-stu-id="c7368-134">A bitmask of the biometric sensor capabilities.</span></span> <span data-ttu-id="c7368-135">Hierbei kann es sich um einen bitweisen **oder** um die folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="c7368-135">This can be a bitwise **OR** of the following values:</span></span>

-   <span data-ttu-id="c7368-136">winbio- \_ Fähigkeits \_ Sensor</span><span class="sxs-lookup"><span data-stu-id="c7368-136">WINBIO\_CAPABILITY\_SENSOR</span></span>
-   <span data-ttu-id="c7368-137">winbio-Funktions Vergleich \_ \_</span><span class="sxs-lookup"><span data-stu-id="c7368-137">WINBIO\_CAPABILITY\_MATCHING</span></span>
-   <span data-ttu-id="c7368-138">winbio-Funktions \_ \_ Datenbank</span><span class="sxs-lookup"><span data-stu-id="c7368-138">WINBIO\_CAPABILITY\_DATABASE</span></span>
-   <span data-ttu-id="c7368-139">Verarbeitung von winbio- \_ Funktionen \_</span><span class="sxs-lookup"><span data-stu-id="c7368-139">WINBIO\_CAPABILITY\_PROCESSING</span></span>
-   <span data-ttu-id="c7368-140">Verschlüsselung von winbio- \_ Funktionen \_</span><span class="sxs-lookup"><span data-stu-id="c7368-140">WINBIO\_CAPABILITY\_ENCRYPTION</span></span>
-   <span data-ttu-id="c7368-141">Navigation in winbio- \_ Funktionen \_</span><span class="sxs-lookup"><span data-stu-id="c7368-141">WINBIO\_CAPABILITY\_NAVIGATION</span></span>
-   <span data-ttu-id="c7368-142">winbio-Funktions \_ \_ Indikator</span><span class="sxs-lookup"><span data-stu-id="c7368-142">WINBIO\_CAPABILITY\_INDICATOR</span></span>
-   <span data-ttu-id="c7368-143">virtueller winbio- \_ Fähigkeits \_ \_ Sensor</span><span class="sxs-lookup"><span data-stu-id="c7368-143">WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR</span></span>
    > [!Note]  
    > <span data-ttu-id="c7368-144">Die **\_ \_ virtuelle \_ Sensor Konstante für winbio-Funktionen** gilt nur für Windows 10 und höher.</span><span class="sxs-lookup"><span data-stu-id="c7368-144">The **WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR** constant applies only for Windows 10 and later.</span></span>

     

</dd> <dt>

<span data-ttu-id="c7368-145">**Geräte-ID**</span><span class="sxs-lookup"><span data-stu-id="c7368-145">**DeviceInstanceId**</span></span>
</dt> <dd>

<span data-ttu-id="c7368-146">Ein Zeichen folgen Wert, der die Geräte-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="c7368-146">A string value that contains the device ID.</span></span> <span data-ttu-id="c7368-147">Die Zeichenfolge kann bis zu 256 Unicode-Zeichen einschließlich eines abschließenden **null** -Zeichens enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7368-147">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="c7368-148">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c7368-148">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c7368-149">Ein Zeichen folgen Wert, der eine Beschreibung der biometrischen Einheit enthält.</span><span class="sxs-lookup"><span data-stu-id="c7368-149">A string value that contains a description of the biometric unit.</span></span> <span data-ttu-id="c7368-150">Die Zeichenfolge kann bis zu 256 Unicode-Zeichen einschließlich eines abschließenden **null** -Zeichens enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7368-150">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="c7368-151">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="c7368-151">**Manufacturer**</span></span>
</dt> <dd>

<span data-ttu-id="c7368-152">Ein Zeichen folgen Wert, der den Namen des Herstellers enthält.</span><span class="sxs-lookup"><span data-stu-id="c7368-152">A string value that contains the name of the manufacturer.</span></span> <span data-ttu-id="c7368-153">Die Zeichenfolge kann bis zu 256 Unicode-Zeichen einschließlich eines abschließenden **null** -Zeichens enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7368-153">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="c7368-154">**Modell**</span><span class="sxs-lookup"><span data-stu-id="c7368-154">**Model**</span></span>
</dt> <dd>

<span data-ttu-id="c7368-155">Ein Zeichen folgen Wert, der die Modellnummer der biometrischen Einheit enthält.</span><span class="sxs-lookup"><span data-stu-id="c7368-155">A string value that contains the model number of the biometric unit.</span></span> <span data-ttu-id="c7368-156">Die Zeichenfolge kann bis zu 256 Unicode-Zeichen einschließlich eines abschließenden **null** -Zeichens enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7368-156">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="c7368-157">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="c7368-157">**SerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="c7368-158">Eine **null**-terminierte Unicode-Zeichenfolge, die die Seriennummer der biometrischen Einheit enthält.</span><span class="sxs-lookup"><span data-stu-id="c7368-158">A **NULL**-terminated Unicode string that contains the serial number of the biometric unit.</span></span> <span data-ttu-id="c7368-159">Die Zeichenfolge kann bis zu 256 Unicode-Zeichen einschließlich eines abschließenden **null** -Zeichens enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7368-159">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="c7368-160">**Firmwareversion**</span><span class="sxs-lookup"><span data-stu-id="c7368-160">**FirmwareVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c7368-161">Eine [**winbio- \_ Versions**](winbio-version.md) Struktur, die die Haupt-und neben Versionsnummern für die biometrische Einheit enthält.</span><span class="sxs-lookup"><span data-stu-id="c7368-161">A [**WINBIO\_VERSION**](winbio-version.md) structure that contains the major and minor version numbers for the biometric unit.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7368-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7368-162">Requirements</span></span>



| <span data-ttu-id="c7368-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7368-163">Requirement</span></span> | <span data-ttu-id="c7368-164">Wert</span><span class="sxs-lookup"><span data-stu-id="c7368-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7368-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7368-165">Minimum supported client</span></span><br/> | <span data-ttu-id="c7368-166">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7368-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="c7368-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7368-167">Minimum supported server</span></span><br/> | <span data-ttu-id="c7368-168">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7368-168">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c7368-169">Header</span><span class="sxs-lookup"><span data-stu-id="c7368-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7368-170"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7368-170"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7368-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7368-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7368-172">Client Anwendungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="c7368-172">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="c7368-173">**Winbioenumbiometricunits**</span><span class="sxs-lookup"><span data-stu-id="c7368-173">**WinBioEnumBiometricUnits**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





