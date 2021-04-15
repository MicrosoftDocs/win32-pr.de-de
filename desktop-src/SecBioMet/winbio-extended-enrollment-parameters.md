---
title: WINBIO_EXTENDED_ENROLLMENT_PARAMETERS Struktur (winbio \_ Adapter. h)
description: Enthält zusätzliche Informationen, die ein Engine-Adapter zum Erstellen einer Registrierungs Vorlage benötigt.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS Struktur Windows-Biometrieframework-API
- PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475666"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a><span data-ttu-id="332d0-105">Struktur der erweiterten winbio-Registrierungs \_ \_ \_ Parameter</span><span class="sxs-lookup"><span data-stu-id="332d0-105">WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS structure</span></span>

<span data-ttu-id="332d0-106">Die Struktur der **erweiterten winbio-Registrierungs \_ \_ \_ Parameter** enthält zusätzliche Informationen, die ein Engine-Adapter zum Erstellen einer Registrierungs Vorlage benötigt.</span><span class="sxs-lookup"><span data-stu-id="332d0-106">The **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure contains additional information that an engine adapter needs to create an enrollment template.</span></span>

## <a name="syntax"></a><span data-ttu-id="332d0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="332d0-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="332d0-108">Member</span><span class="sxs-lookup"><span data-stu-id="332d0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="332d0-109">**Größe**</span><span class="sxs-lookup"><span data-stu-id="332d0-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="332d0-110">Die Größe (in Bytes) der Struktur der **erweiterten winbio-Registrierungs \_ \_ \_ Parameter** .</span><span class="sxs-lookup"><span data-stu-id="332d0-110">The size (in bytes) of the **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="332d0-111">**Teilfaktor**</span><span class="sxs-lookup"><span data-stu-id="332d0-111">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="332d0-112">Einer der Werte für den [**Subtyp "winbio \_ biometrische \_ SubType**](winbio-biometric-subtype-constants.md) ", der zusätzliche Informationen über die Registrierung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="332d0-112">One of the [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md) values that provides additional information about the enrollment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="332d0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="332d0-113">Remarks</span></span>

<span data-ttu-id="332d0-114">Das Windows-Biometrieframework übergibt diese Struktur während eines Registrierungsvorgangs an die [**engineadaptersetenrollmentparameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) -Methode.</span><span class="sxs-lookup"><span data-stu-id="332d0-114">The Windows Biometric Framework passes this structure to the [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) method during an enrollment operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="332d0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="332d0-115">Requirements</span></span>



| <span data-ttu-id="332d0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="332d0-116">Requirement</span></span> | <span data-ttu-id="332d0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="332d0-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332d0-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="332d0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="332d0-119">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="332d0-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="332d0-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="332d0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="332d0-121">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="332d0-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="332d0-122">Header</span><span class="sxs-lookup"><span data-stu-id="332d0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="332d0-123"><dt>Winbio \_ Adapter. h (Include winbio \_ Adapter. h)</dt></span><span class="sxs-lookup"><span data-stu-id="332d0-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





