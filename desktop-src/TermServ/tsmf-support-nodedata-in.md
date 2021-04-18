---
title: TSMF_SUPPORT_NODEDATA_IN Struktur
description: Wird innerhalb der tsmf- \_ Unterstützungs \_ Daten in der Struktur verwendet \_ , um Informationen zu den unterstützten Medienformaten zu enthalten.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_IN Struktur Remotedesktopdienste
- PTSMF_SUPPORT_NODEDATA_IN Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c36d18ea0e97da8df60475855c93755727fa87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338554"
---
# <a name="tsmf_support_nodedata_in-structure"></a><span data-ttu-id="5d60c-105">Tsmf \_ unterstützt \_ nodedata \_ in der Struktur</span><span class="sxs-lookup"><span data-stu-id="5d60c-105">TSMF\_SUPPORT\_NODEDATA\_IN structure</span></span>

<span data-ttu-id="5d60c-106">Wird innerhalb der [**tsmf- \_ Unterstützungs \_ Daten \_ in**](tsmf-support-data-in.md) der Struktur verwendet, um Informationen zu den unterstützten Medienformaten zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="5d60c-106">Used inside the [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d60c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d60c-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a><span data-ttu-id="5d60c-108">Member</span><span class="sxs-lookup"><span data-stu-id="5d60c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d60c-109">**byteCount**</span><span class="sxs-lookup"><span data-stu-id="5d60c-109">**byteCount**</span></span>
</dt> <dd>

<span data-ttu-id="5d60c-110">Die Größe der Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5d60c-110">The size of the structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5d60c-111">**NodeId**</span><span class="sxs-lookup"><span data-stu-id="5d60c-111">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="5d60c-112">Der Knoten.</span><span class="sxs-lookup"><span data-stu-id="5d60c-112">The node.</span></span>

</dd> <dt>

<span data-ttu-id="5d60c-113">**nummediatypes**</span><span class="sxs-lookup"><span data-stu-id="5d60c-113">**numMediaTypes**</span></span>
</dt> <dd>

<span data-ttu-id="5d60c-114">Die Anzahl der Medienformat Strukturen.</span><span class="sxs-lookup"><span data-stu-id="5d60c-114">The number of media format structures.</span></span>

</dd> <dt>

<span data-ttu-id="5d60c-115">**...**</span><span class="sxs-lookup"><span data-stu-id="5d60c-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="5d60c-116">Eine Variable Anzahl von Strukturen, die Audioformate oder Video Medienformate definieren.</span><span class="sxs-lookup"><span data-stu-id="5d60c-116">A variable number of structures defining audio or video media formats.</span></span> <span data-ttu-id="5d60c-117">Der **formatType** ist entweder **Format \_ WaveFormatEx** for Audiodatei oder **Format \_ MF Videoformat** for Video.</span><span class="sxs-lookup"><span data-stu-id="5d60c-117">The **FormatType** is either **FORMAT\_WaveFormatEx** for audio or **FORMAT\_MFVideoFormat** for video.</span></span>

<span data-ttu-id="5d60c-118">Details zu dieser Struktur finden Sie unter [TS \_ am \_ \_ Medientyp Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).</span><span class="sxs-lookup"><span data-stu-id="5d60c-118">For details of this structure, see [TS\_AM\_MEDIA\_TYPE Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d60c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d60c-119">Requirements</span></span>



| <span data-ttu-id="5d60c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d60c-120">Requirement</span></span> | <span data-ttu-id="5d60c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5d60c-121">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="5d60c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d60c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5d60c-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5d60c-123">None supported</span></span><br/>         |
| <span data-ttu-id="5d60c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d60c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5d60c-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5d60c-125">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5d60c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d60c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d60c-127">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="5d60c-127">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="5d60c-128">**tsmf- \_ Unterstützungs \_ Daten \_ in**</span><span class="sxs-lookup"><span data-stu-id="5d60c-128">**TSMF\_SUPPORT\_DATA\_IN**</span></span>](tsmf-support-data-in.md)
</dt> </dl>

 

