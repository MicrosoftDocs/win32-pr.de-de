---
description: Definiert den Status des Output Protection Managers (OPM).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: MF_MEDIA_ENGINE_OPM_STATUS-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 73585bf63bc559f30ce114730274e30518497b05
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361119"
---
# <a name="mf_media_engine_opm_status-enumeration"></a><span data-ttu-id="60e7a-103">\_ \_ \_ OPM- \_ Status Enumeration für MF-Medien-Engine</span><span class="sxs-lookup"><span data-stu-id="60e7a-103">MF\_MEDIA\_ENGINE\_OPM\_STATUS enumeration</span></span>

<span data-ttu-id="60e7a-104">Definiert den Status des [Output Protection Managers](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="60e7a-104">Defines the status of the [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

## <a name="syntax"></a><span data-ttu-id="60e7a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60e7a-105">Syntax</span></span>


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a><span data-ttu-id="60e7a-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="60e7a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="60e7a-107"><span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**Das MF \_ Media \_ Engine \_ OPM wurde \_ nicht \_ angefordert.**</span><span class="sxs-lookup"><span data-stu-id="60e7a-107"><span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**MF\_MEDIA\_ENGINE\_OPM\_NOT\_REQUESTED**</span></span>
</dt> <dd>

<span data-ttu-id="60e7a-108">Standardstatus.</span><span class="sxs-lookup"><span data-stu-id="60e7a-108">Default status.</span></span> <span data-ttu-id="60e7a-109">Wird verwendet, um den korrekten Status zurückzugeben, wenn der Inhalt nicht geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="60e7a-109">Used to return the correct status when the content is unprotected.</span></span>

</dd> <dt>

<span data-ttu-id="60e7a-110"><span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**OPM der MF- \_ Medien- \_ Engine \_ \_ eingerichtet**</span><span class="sxs-lookup"><span data-stu-id="60e7a-110"><span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**MF\_MEDIA\_ENGINE\_OPM\_ESTABLISHED**</span></span>
</dt> <dd>

<span data-ttu-id="60e7a-111">OPM wurde erfolgreich eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="60e7a-111">OPM successfully established.</span></span>

</dd> <dt>

<span data-ttu-id="60e7a-112"><span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**Fehler beim virtuellen Computer der MF- \_ Medien- \_ Engine \_ OPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="60e7a-112"><span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_VM**</span></span>
</dt> <dd>

<span data-ttu-id="60e7a-113">OPM ist fehlgeschlagen, weil die Ausführung in einer virtuellen Maschine (VM) ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="60e7a-113">OPM failed because running in a virtual machined (VM).</span></span>

</dd> <dt>

<span data-ttu-id="60e7a-114"><span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**Fehler \_ beim \_ \_ BM der \_ MF-Medien-Engine-Fehler \_**</span><span class="sxs-lookup"><span data-stu-id="60e7a-114"><span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_BDA**</span></span>
</dt> <dd>

<span data-ttu-id="60e7a-115">OPM ist fehlgeschlagen, da es keinen Grafiktreiber gibt und das System den Basic Display Adapter (BDA) verwendet.</span><span class="sxs-lookup"><span data-stu-id="60e7a-115">OPM failed because there is no graphics driver and the system is using Basic Display Adapter (BDA).</span></span>

</dd> <dt>

<span data-ttu-id="60e7a-116"><span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**MF-Medien-Engine-Fehler bei \_ \_ \_ \_ \_ nicht signiertem \_ Treiber**</span><span class="sxs-lookup"><span data-stu-id="60e7a-116"><span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_UNSIGNED\_DRIVER**</span></span>
</dt> <dd>

<span data-ttu-id="60e7a-117">OPM ist fehlgeschlagen, da der Grafiktreiber nicht mit PE signiert ist und auf den Warp zurückfällt.</span><span class="sxs-lookup"><span data-stu-id="60e7a-117">OPM failed because the graphics driver is not PE signed, falling back to WARP.</span></span>

</dd> <dt>

<span data-ttu-id="60e7a-118"><span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**Fehler \_ beim \_ \_ OPM der MF-Medien-Engine \_**</span><span class="sxs-lookup"><span data-stu-id="60e7a-118"><span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="60e7a-119">OPM konnte aus anderen Gründen nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="60e7a-119">OPM failed for other reasons.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60e7a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60e7a-120">Requirements</span></span>



| <span data-ttu-id="60e7a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60e7a-121">Requirement</span></span> | <span data-ttu-id="60e7a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="60e7a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e7a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60e7a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="60e7a-124">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="60e7a-124">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="60e7a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60e7a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="60e7a-126">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60e7a-126">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="60e7a-127">IDL</span><span class="sxs-lookup"><span data-stu-id="60e7a-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60e7a-128"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60e7a-128"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e7a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60e7a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e7a-130">Media Foundation Enumerationen</span><span class="sxs-lookup"><span data-stu-id="60e7a-130">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




