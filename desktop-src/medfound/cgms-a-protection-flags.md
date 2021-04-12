---
description: Geben Sie die Schutz Ebenen für das Verwaltungs System für die Kopier Generierung an&\# 8212; Analog (CGMS-A).
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: CGMS-A-Schutzflags (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329ae13741490f2783d548baeead65ba59bc5ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393306"
---
# <a name="cgms-a-protection-flags"></a><span data-ttu-id="17d80-103">CGMS-A-Schutzflags</span><span class="sxs-lookup"><span data-stu-id="17d80-103">CGMS-A Protection Flags</span></span>

<span data-ttu-id="17d80-104">In den Konstanten in der folgenden Tabelle sind die Schutz Ebenen für die analog zum Management System für Kopier Generierung (CGMS-A) angegeben.</span><span class="sxs-lookup"><span data-stu-id="17d80-104">The constants in the following table specify the protection levels for Copy Generation Management System Analog (CGMS-A).</span></span>



| <span data-ttu-id="17d80-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="17d80-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="17d80-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17d80-106">Description</span></span>                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <span data-ttu-id="17d80-107"><dt>**OPM \_ Cgmsa \_ außerhalb von**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="17d80-107"><dt>**OPM\_CGMSA\_OFF**</dt> <dt>0x00</dt></span></span> </dl>                                                                                       | <span data-ttu-id="17d80-108">CGMS-A ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="17d80-108">CGMS-A is disabled.</span></span> <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <span data-ttu-id="17d80-109"><dt>**OPM \_ Cgmsa- \_ Kopie \_ frei**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="17d80-109"><dt>**OPM\_CGMSA\_COPY\_FREELY**</dt> <dt>0x01</dt></span></span> </dl>                                                              | <span data-ttu-id="17d80-110">Die Schutz Ebene ist kostenlos kopieren.</span><span class="sxs-lookup"><span data-stu-id="17d80-110">The protection level is Copy Freely.</span></span><br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <span data-ttu-id="17d80-111"><dt>**OPM \_ Cgmsa- \_ Kopie \_ nicht \_ mehr**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="17d80-111"><dt>**OPM\_CGMSA\_COPY\_NO\_MORE**</dt> <dt>0x02</dt></span></span> </dl>                                                          | <span data-ttu-id="17d80-112">Die Schutz Ebene ist "Kopieren".</span><span class="sxs-lookup"><span data-stu-id="17d80-112">The protection level is Copy No More.</span></span> <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <span data-ttu-id="17d80-113"><dt>**OPM \_ Cgmsa \_ Kopie \_ 1 \_ Generation**</dt> <dt>0x03</dt></span><span class="sxs-lookup"><span data-stu-id="17d80-113"><dt>**OPM\_CGMSA\_COPY\_ONE\_GENERATION**</dt> <dt>0x03</dt></span></span> </dl>                                     | <span data-ttu-id="17d80-114">Die Schutz Ebene ist Kopie einer Generation.</span><span class="sxs-lookup"><span data-stu-id="17d80-114">The protection level is Copy One Generation.</span></span> <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <span data-ttu-id="17d80-115"><dt>**OPM \_ Cgmsa- \_ Kopie \_ nie**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="17d80-115"><dt>**OPM\_CGMSA\_COPY\_NEVER**</dt> <dt>0x04</dt></span></span> </dl>                                                                 | <span data-ttu-id="17d80-116">Die Schutz Ebene ist nie kopieren.</span><span class="sxs-lookup"><span data-stu-id="17d80-116">The protection level is Copy Never.</span></span><br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <span data-ttu-id="17d80-117"><dt>**OPM \_ Cgmsa \_ - \_ weitergabesteuerelement \_ erforderlich**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="17d80-117"><dt>**OPM\_CGMSA\_REDISTRIBUTION\_CONTROL\_REQUIRED**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="17d80-118">Ein weitergabesteuerelement (auch als *Broadcast-Flag* bezeichnet) ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="17d80-118">Redistribution control (also called the *broadcast flag*) is required.</span></span> <span data-ttu-id="17d80-119">Dieses Flag kann mit den anderen Flags kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="17d80-119">This flag can be combined with the other flags.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="17d80-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17d80-120">Remarks</span></span>

<span data-ttu-id="17d80-121">Diese Flags entsprechen den Enumerationskonstanten der **COPP \_ cgmsa- \_ Schutz \_ Ebene** , die im Certified Output Protection Protocol (COPP) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17d80-121">These flags are equivalent to the **COPP\_CGMSA\_Protection\_Level** enumeration constants used in the Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="17d80-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17d80-122">Requirements</span></span>



| <span data-ttu-id="17d80-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17d80-123">Requirement</span></span> | <span data-ttu-id="17d80-124">Wert</span><span class="sxs-lookup"><span data-stu-id="17d80-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="17d80-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17d80-125">Minimum supported client</span></span><br/> | <span data-ttu-id="17d80-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17d80-126">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="17d80-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17d80-127">Minimum supported server</span></span><br/> | <span data-ttu-id="17d80-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17d80-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="17d80-129">Header</span><span class="sxs-lookup"><span data-stu-id="17d80-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="17d80-130"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="17d80-130"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17d80-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17d80-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d80-132">Media Foundation Konstanten</span><span class="sxs-lookup"><span data-stu-id="17d80-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




