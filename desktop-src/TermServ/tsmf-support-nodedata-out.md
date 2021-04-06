---
title: TSMF_SUPPORT_NODEDATA_OUT Struktur
description: Wird innerhalb der tsmf- \_ Unterstützung der \_ Datenausgabe Struktur verwendet \_ , um Informationen zu unterstützten Medienformaten zu enthalten.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_OUT Struktur Remotedesktopdienste
- PTSMF_SUPPORT_NODEDATA_OUT Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 517170e9d6580f69b59f71e0994351ebe0484ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859028"
---
# <a name="tsmf_support_nodedata_out-structure"></a><span data-ttu-id="b4c9a-105">Tsmf \_ unterstützt \_ nodedata- \_ out-Struktur</span><span class="sxs-lookup"><span data-stu-id="b4c9a-105">TSMF\_SUPPORT\_NODEDATA\_OUT structure</span></span>

<span data-ttu-id="b4c9a-106">Wird innerhalb der [**tsmf- \_ Unterstützung der \_ Daten \_**](tsmf-support-data-out.md) Ausgabestruktur verwendet, um Informationen zu unterstützten Medienformaten zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="b4c9a-106">Used inside the [**TSMF\_SUPPORT\_DATA\_OUT**](tsmf-support-data-out.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c9a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4c9a-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a><span data-ttu-id="b4c9a-108">Member</span><span class="sxs-lookup"><span data-stu-id="b4c9a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4c9a-109">**NodeId**</span><span class="sxs-lookup"><span data-stu-id="b4c9a-109">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="b4c9a-110">Der Knoten.</span><span class="sxs-lookup"><span data-stu-id="b4c9a-110">The node.</span></span>

</dd> <dt>

<span data-ttu-id="b4c9a-111">**hrsupportstatus**</span><span class="sxs-lookup"><span data-stu-id="b4c9a-111">**hrSupportStatus**</span></span>
</dt> <dd>

<span data-ttu-id="b4c9a-112">Gibt an, ob die durch den *clsidnewsink* -Parameter identifizierte Senke unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b4c9a-112">Whether the sink identified by the *clsidNewSink* parameter is supported.</span></span>

<span data-ttu-id="b4c9a-113">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="b4c9a-113">The possible values are.</span></span>

<dt>

<span data-ttu-id="b4c9a-114">0</span><span class="sxs-lookup"><span data-stu-id="b4c9a-114">0</span></span>
</dt> <dd>

<span data-ttu-id="b4c9a-115">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b4c9a-115">Not supported</span></span>

</dd> <dt>

<span data-ttu-id="b4c9a-116">1</span><span class="sxs-lookup"><span data-stu-id="b4c9a-116">1</span></span>
</dt> <dd>

<span data-ttu-id="b4c9a-117">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="b4c9a-117">Supported</span></span>

</dd> </dl>

<span data-ttu-id="b4c9a-118">Andere Werte sind nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="b4c9a-118">Other values are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="b4c9a-119">**clsidnewsink**</span><span class="sxs-lookup"><span data-stu-id="b4c9a-119">**clsidNewSink**</span></span>
</dt> <dd>

<span data-ttu-id="b4c9a-120">Die Senke, die dem Medientyp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b4c9a-120">The sink associated with the media type.</span></span>

</dd> <dt>

<span data-ttu-id="b4c9a-121">**supportedmediatypeingedex**</span><span class="sxs-lookup"><span data-stu-id="b4c9a-121">**supportedMediaTypeIndex**</span></span>
</dt> <dd>

<span data-ttu-id="b4c9a-122">Der null basierte Index des Medientyps, der von der Senke unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b4c9a-122">The zero-based index of the media type supported by the sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4c9a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4c9a-123">Requirements</span></span>



| <span data-ttu-id="b4c9a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4c9a-124">Requirement</span></span> | <span data-ttu-id="b4c9a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b4c9a-125">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="b4c9a-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4c9a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b4c9a-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b4c9a-127">None supported</span></span><br/>         |
| <span data-ttu-id="b4c9a-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4c9a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b4c9a-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4c9a-129">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4c9a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4c9a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c9a-131">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="b4c9a-131">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="b4c9a-132">**tsmf- \_ Unterstützung \_ \_ von Daten**</span><span class="sxs-lookup"><span data-stu-id="b4c9a-132">**TSMF\_SUPPORT\_DATA\_OUT**</span></span>](tsmf-support-data-out.md)
</dt> </dl>

 

 





