---
title: Mpsource-Enumeration (mpclient. h)
description: Mögliche Quell Kategorie.
ms.assetid: 1AD12D67-C74B-481A-AC9B-D119AABDB6E9
keywords:
- Mpsource-Enumeration Legacy Windows-Umgebungs Features
- Pmpsource-enumerationszeiger ältere Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSOURCE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9255029512499a0e2948a44701ef4482aff4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956734"
---
# <a name="mpsource-enumeration"></a><span data-ttu-id="28ffd-105">Mpsource-Enumeration</span><span class="sxs-lookup"><span data-stu-id="28ffd-105">MPSOURCE enumeration</span></span>

<span data-ttu-id="28ffd-106">Mögliche Quell Kategorie.</span><span class="sxs-lookup"><span data-stu-id="28ffd-106">Possible category of source.</span></span>

## <a name="syntax"></a><span data-ttu-id="28ffd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="28ffd-107">Syntax</span></span>


```C++
typedef enum tagMPSOURCE { 
  MPSOURCE_UNKNOWN             = 0,
  MPSOURCE_USER                = 1,
  MPSOURCE_SYSTEM              = 2,
  MPSOURCE_REALTIME            = 3,
  MPSOURCE_IOAV                = 4,
  MPSOURCE_NIS                 = 5,
  MPSOURCE_BHO                 = 6,
  MPSOURCE_IEPROTECT           = 6,
  MPSOURCE_ELAM                = 7,
  MPSOURCE_LOCAL_ATTESTATION   = 8,
  MPSOURCE_REMOTE_ATTESTATION  = 9,
  MPSOURCE_AMSI                = 10,
  MP_SOURCE_MAXVALUE           = 10
} MPSOURCE, *PMPSOURCE;
```



## <a name="constants"></a><span data-ttu-id="28ffd-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="28ffd-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="28ffd-109"><span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**mpsource \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="28ffd-109"><span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**MPSOURCE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="28ffd-110">Die Quelle ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="28ffd-110">Source unknown.</span></span>

</dd> <dt>

<span data-ttu-id="28ffd-111"><span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**mpsource- \_ Benutzer**</span><span class="sxs-lookup"><span data-stu-id="28ffd-111"><span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**MPSOURCE\_USER**</span></span>
</dt> <dd>

<span data-ttu-id="28ffd-112">Vom Benutzer initiiert.</span><span class="sxs-lookup"><span data-stu-id="28ffd-112">User initiated.</span></span>

</dd> <dt>

<span data-ttu-id="28ffd-113"><span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**mpsource- \_ System**</span><span class="sxs-lookup"><span data-stu-id="28ffd-113"><span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**MPSOURCE\_SYSTEM**</span></span>
</dt> <dd>

<span data-ttu-id="28ffd-114">System initiiert.</span><span class="sxs-lookup"><span data-stu-id="28ffd-114">system initiated.</span></span>

</dd> <dt>

<span data-ttu-id="28ffd-115"><span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**mpsource in \_ Echtzeit**</span><span class="sxs-lookup"><span data-stu-id="28ffd-115"><span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**MPSOURCE\_REALTIME**</span></span>
</dt> <dd>

<span data-ttu-id="28ffd-116">Die Echtzeit-Komponente wurde initiiert.</span><span class="sxs-lookup"><span data-stu-id="28ffd-116">Realtime component initiated.</span></span>

</dd> <dt>

<span data-ttu-id="28ffd-117"><span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**mpsource \_ ioav**</span><span class="sxs-lookup"><span data-stu-id="28ffd-117"><span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**MPSOURCE\_IOAV**</span></span>
</dt> <dd>

<span data-ttu-id="28ffd-118">Internet Explorer-Downloads und Outlook Express-Anlagen wurden initiiert.</span><span class="sxs-lookup"><span data-stu-id="28ffd-118">IE Downloads and Outlook Express Attachments initiated.</span></span>

</dd> <dt>

<span data-ttu-id="28ffd-119"><span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**mpsource \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="28ffd-119"><span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**MPSOURCE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="28ffd-120">Netzwerk Inspektionssystem.</span><span class="sxs-lookup"><span data-stu-id="28ffd-120">Network inspection system.</span></span>

</dd> <dt>

<span data-ttu-id="28ffd-121"><span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**mpsource- \_ BHO**</span><span class="sxs-lookup"><span data-stu-id="28ffd-121"><span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**MPSOURCE\_BHO**</span></span>
</dt> <dd>

<span data-ttu-id="28ffd-122">BHO-Webskript (veraltet).</span><span class="sxs-lookup"><span data-stu-id="28ffd-122">BHO - web script (deprecated).</span></span>

</dd> <dt>

<span data-ttu-id="28ffd-123"><span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**mpsource- \_ ieprotect**</span><span class="sxs-lookup"><span data-stu-id="28ffd-123"><span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**MPSOURCE\_IEPROTECT**</span></span>
</dt> <dd>

<span data-ttu-id="28ffd-124">IE-iextensionvalidation.</span><span class="sxs-lookup"><span data-stu-id="28ffd-124">IE - IExtensionValidation.</span></span>

</dd> <dt>

<span data-ttu-id="28ffd-125"><span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**mpsource \_ Elam**</span><span class="sxs-lookup"><span data-stu-id="28ffd-125"><span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**MPSOURCE\_ELAM**</span></span>
</dt> <dd>

<span data-ttu-id="28ffd-126">ELAM</span><span class="sxs-lookup"><span data-stu-id="28ffd-126">ELAM</span></span>

</dd> <dt>

<span data-ttu-id="28ffd-127"><span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**lokaler mpsource-Nachweis \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28ffd-127"><span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**MPSOURCE\_LOCAL\_ATTESTATION**</span></span>
</dt> <dd>

<span data-ttu-id="28ffd-128">Lokaler Nachweis.</span><span class="sxs-lookup"><span data-stu-id="28ffd-128">Local attestation.</span></span>

</dd> <dt>

<span data-ttu-id="28ffd-129"><span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**mpsource- \_ Remote Nachweis \_**</span><span class="sxs-lookup"><span data-stu-id="28ffd-129"><span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**MPSOURCE\_REMOTE\_ATTESTATION**</span></span>
</dt> <dd>

<span data-ttu-id="28ffd-130">Remote Nachweis.</span><span class="sxs-lookup"><span data-stu-id="28ffd-130">Remote attestation.</span></span>

</dd> <dt>

<span data-ttu-id="28ffd-131"><span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**mpsource- \_ AMSI**</span><span class="sxs-lookup"><span data-stu-id="28ffd-131"><span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**MPSOURCE\_AMSI**</span></span>
</dt> <dd>

<span data-ttu-id="28ffd-132">AMSI</span><span class="sxs-lookup"><span data-stu-id="28ffd-132">AMSI</span></span>

</dd> <dt>

<span data-ttu-id="28ffd-133"><span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**MP- \_ Quelle \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="28ffd-133"><span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**MP\_SOURCE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="28ffd-134">Maximal möglicher Wert.</span><span class="sxs-lookup"><span data-stu-id="28ffd-134">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28ffd-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28ffd-135">Requirements</span></span>



| <span data-ttu-id="28ffd-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28ffd-136">Requirement</span></span> | <span data-ttu-id="28ffd-137">Wert</span><span class="sxs-lookup"><span data-stu-id="28ffd-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28ffd-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28ffd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="28ffd-139">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28ffd-139">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="28ffd-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28ffd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="28ffd-141">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28ffd-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28ffd-142">Header</span><span class="sxs-lookup"><span data-stu-id="28ffd-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="28ffd-143"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="28ffd-143"><dt>MpClient.h</dt></span></span> </dl> |



 

 





