---
title: WINBIO_BSP_SCHEMA Struktur (winbio \_ types. h)
description: Beschreibt die Funktionen eines biometrischen Dienstanbieters.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- WINBIO_BSP_SCHEMA Struktur Windows-Biometrieframework-API
- PWINBIO_BSP_SCHEMA Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ae63aefb64eb22f454559b76e9922242ca9530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476875"
---
# <a name="winbio_bsp_schema-structure"></a><span data-ttu-id="0a6fb-105">Winbio- \_ BSP- \_ Schema Struktur</span><span class="sxs-lookup"><span data-stu-id="0a6fb-105">WINBIO\_BSP\_SCHEMA structure</span></span>

<span data-ttu-id="0a6fb-106">Die Struktur " **winbio \_ BSP \_ Schema** " beschreibt die Funktionen eines biometrischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-106">The **WINBIO\_BSP\_SCHEMA** structure describes the capabilities of a biometric service provider.</span></span> <span data-ttu-id="0a6fb-107">Diese Struktur wird von der [**winbioenumserviceproviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-107">This structure is used by the [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a6fb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a6fb-108">Syntax</span></span>


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="0a6fb-109">Member</span><span class="sxs-lookup"><span data-stu-id="0a6fb-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="0a6fb-110">**Biometricfactor**</span><span class="sxs-lookup"><span data-stu-id="0a6fb-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="0a6fb-111">Der Typ der von diesem Gerät verwendeten biometrischen Messung.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-111">The type of biometric measurement used by this device.</span></span> <span data-ttu-id="0a6fb-112">Zurzeit muss dies ein **winbio- \_ \_ typfingerabdruck** sein.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-112">Currently this must be **WINBIO\_TYPE\_FINGERPRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="0a6fb-113">**Bspid**</span><span class="sxs-lookup"><span data-stu-id="0a6fb-113">**BspId**</span></span>
</dt> <dd>

<span data-ttu-id="0a6fb-114">Ein Wert, der die Komponente des biometrischen Dienstanbieters eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-114">A value that uniquely identifies this biometric service provider component.</span></span>

</dd> <dt>

<span data-ttu-id="0a6fb-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0a6fb-115">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0a6fb-116">Eine **null**-terminierte Unicode-Zeichenfolge, die eine Beschreibung des biometrischen Dienstanbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-116">A **NULL**-terminated Unicode string that contains a description of the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="0a6fb-117">**Hersteller**</span><span class="sxs-lookup"><span data-stu-id="0a6fb-117">**Vendor**</span></span>
</dt> <dd>

<span data-ttu-id="0a6fb-118">Eine **null**-terminierte Unicode-Zeichenfolge, die den Namen des Anbieters enthält, der den biometrischen Dienstanbieter bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-118">A **NULL**-terminated Unicode string that contains the name of the vendor supplying the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="0a6fb-119">**Version**</span><span class="sxs-lookup"><span data-stu-id="0a6fb-119">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="0a6fb-120">Eine [**winbio- \_ Versions**](winbio-version.md) Struktur, die die Softwareversion der Komponente des biometrischen Dienstanbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="0a6fb-120">A [**WINBIO\_VERSION**](winbio-version.md) structure the contains the software version of the biometric service provider component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a6fb-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a6fb-121">Requirements</span></span>



| <span data-ttu-id="0a6fb-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a6fb-122">Requirement</span></span> | <span data-ttu-id="0a6fb-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0a6fb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a6fb-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a6fb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0a6fb-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a6fb-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="0a6fb-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a6fb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0a6fb-127">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a6fb-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0a6fb-128">Header</span><span class="sxs-lookup"><span data-stu-id="0a6fb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a6fb-129"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a6fb-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a6fb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a6fb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a6fb-131">Client Anwendungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="0a6fb-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="0a6fb-132">**Winbioenumserviceproviders**</span><span class="sxs-lookup"><span data-stu-id="0a6fb-132">**WinBioEnumServiceProviders**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





