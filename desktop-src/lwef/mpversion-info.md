---
title: MPVERSION_INFO Struktur (mpclient. h)
description: Versionsinformationen für die Komponenten von Malware Protection Manager.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- MPVERSION_INFO Struktur Funktionen der Legacy-Windows-Umgebung
- PMPVERSION_INFO Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30153c427b880600a3d8aeb3c411a8679cd64b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341047"
---
# <a name="mpversion_info-structure"></a><span data-ttu-id="c1f8e-105">Mpversion- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="c1f8e-105">MPVERSION\_INFO structure</span></span>

<span data-ttu-id="c1f8e-106">Versionsinformationen für die Komponenten von Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="c1f8e-106">Version information for the malware protection manager's components.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1f8e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1f8e-107">Syntax</span></span>


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a><span data-ttu-id="c1f8e-108">Member</span><span class="sxs-lookup"><span data-stu-id="c1f8e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1f8e-109">**Produkt**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-109">**Product**</span></span>
</dt> <dd>

<span data-ttu-id="c1f8e-110">Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-110">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1f8e-111">Die Produktversion.</span><span class="sxs-lookup"><span data-stu-id="c1f8e-111">Product version.</span></span>

</dd> <dt>

<span data-ttu-id="c1f8e-112">**Service**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-112">**Service**</span></span>
</dt> <dd>

<span data-ttu-id="c1f8e-113">Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-113">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1f8e-114">Die Dienst Komponenten Version.</span><span class="sxs-lookup"><span data-stu-id="c1f8e-114">Service component version.</span></span>

</dd> <dt>

<span data-ttu-id="c1f8e-115">**File System Filter**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-115">**FileSystemFilter**</span></span>
</dt> <dd>

<span data-ttu-id="c1f8e-116">Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-116">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1f8e-117">Version der Dateisystem Filter-Komponente.</span><span class="sxs-lookup"><span data-stu-id="c1f8e-117">File system filter component version.</span></span>

</dd> <dt>

<span data-ttu-id="c1f8e-118">**Engine**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-118">**Engine**</span></span>
</dt> <dd>

<span data-ttu-id="c1f8e-119">Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-119">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1f8e-120">Engine-Komponenten Version.</span><span class="sxs-lookup"><span data-stu-id="c1f8e-120">Engine component version.</span></span>

</dd> <dt>

<span data-ttu-id="c1f8e-121">**Assignature**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-121">**ASSignature**</span></span>
</dt> <dd>

<span data-ttu-id="c1f8e-122">Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-122">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1f8e-123">Version der AntiSpyware-Signatur Komponente.</span><span class="sxs-lookup"><span data-stu-id="c1f8e-123">Antispyware signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="c1f8e-124">**Avsignature**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-124">**AVSignature**</span></span>
</dt> <dd>

<span data-ttu-id="c1f8e-125">Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-125">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1f8e-126">Version der Antivirus-Signatur Komponente.</span><span class="sxs-lookup"><span data-stu-id="c1f8e-126">Antivirus signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="c1f8e-127">**Nisengine**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-127">**NISEngine**</span></span>
</dt> <dd>

<span data-ttu-id="c1f8e-128">Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-128">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1f8e-129">Die NIS-Engine-Version.</span><span class="sxs-lookup"><span data-stu-id="c1f8e-129">NIS engine version.</span></span>

</dd> <dt>

<span data-ttu-id="c1f8e-130">**Nissignature**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-130">**NISSignature**</span></span>
</dt> <dd>

<span data-ttu-id="c1f8e-131">Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-131">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1f8e-132">Die Komponenten Version der NIS-Signatur Signatur.</span><span class="sxs-lookup"><span data-stu-id="c1f8e-132">NIS Signature signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="c1f8e-133">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-133">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="c1f8e-134">Typ: **[**mpcomponent \_ Version**](mpcomponent-version.md) \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-134">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="c1f8e-135">Reservierte Felder.</span><span class="sxs-lookup"><span data-stu-id="c1f8e-135">Reserved fields.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1f8e-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1f8e-136">Requirements</span></span>



| <span data-ttu-id="c1f8e-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1f8e-137">Requirement</span></span> | <span data-ttu-id="c1f8e-138">Wert</span><span class="sxs-lookup"><span data-stu-id="c1f8e-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f8e-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1f8e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c1f8e-140">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1f8e-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c1f8e-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1f8e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c1f8e-142">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1f8e-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1f8e-143">Header</span><span class="sxs-lookup"><span data-stu-id="c1f8e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1f8e-144"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1f8e-144"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1f8e-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1f8e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1f8e-146">**mpcomponent- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="c1f8e-146">**MPCOMPONENT\_VERSION**</span></span>](mpcomponent-version.md)
</dt> </dl>

 

 





