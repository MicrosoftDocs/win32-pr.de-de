---
title: WINBIO_VERSION Struktur (winbio \_ types. h)
description: Enthält die Software Versionsnummer der Komponente eines biometrischen Dienstanbieters.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- WINBIO_VERSION Struktur Windows-Biometrieframework-API
- PWINBIO_VERSION Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d9cda802e89006ed49f6ec4b4e96c88602c511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479125"
---
# <a name="winbio_version-structure"></a><span data-ttu-id="24465-105">Winbio- \_ Versions Struktur</span><span class="sxs-lookup"><span data-stu-id="24465-105">WINBIO\_VERSION structure</span></span>

<span data-ttu-id="24465-106">Die Struktur der **winbio- \_ Version** enthält die Software Versionsnummer der Komponente eines biometrischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="24465-106">The **WINBIO\_VERSION** structure contains the software version number of a biometric service provider component.</span></span>

## <a name="syntax"></a><span data-ttu-id="24465-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="24465-107">Syntax</span></span>


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a><span data-ttu-id="24465-108">Member</span><span class="sxs-lookup"><span data-stu-id="24465-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="24465-109">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="24465-109">**MajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="24465-110">Ein **DWORD** , das die Hauptversionsnummer enthält.</span><span class="sxs-lookup"><span data-stu-id="24465-110">A **DWORD** that contains the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="24465-111">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="24465-111">**MinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="24465-112">Ein **DWORD** , das die neben Versionsnummer enthält.</span><span class="sxs-lookup"><span data-stu-id="24465-112">A **DWORD** that contains the minor version number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24465-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24465-113">Requirements</span></span>



| <span data-ttu-id="24465-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24465-114">Requirement</span></span> | <span data-ttu-id="24465-115">Wert</span><span class="sxs-lookup"><span data-stu-id="24465-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24465-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24465-116">Minimum supported client</span></span><br/> | <span data-ttu-id="24465-117">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24465-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="24465-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24465-118">Minimum supported server</span></span><br/> | <span data-ttu-id="24465-119">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24465-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="24465-120">Header</span><span class="sxs-lookup"><span data-stu-id="24465-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="24465-121"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24465-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24465-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24465-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24465-123">Client Anwendungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="24465-123">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="24465-124">**winbio- \_ BSP- \_ Schema**</span><span class="sxs-lookup"><span data-stu-id="24465-124">**WINBIO\_BSP\_SCHEMA**</span></span>](winbio-bsp-schema.md)
</dt> <dt>

[<span data-ttu-id="24465-125">**winbio- \_ Einheits \_ Schema**</span><span class="sxs-lookup"><span data-stu-id="24465-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





