---
title: WMDRMNET_POLICY Struktur (wmdrmsdk. h)
description: Die wmdrmnet- \_ Richtlinien Struktur enthält die Richtlinie, die für Windows Media DRM für Netzwerkgeräte Vorgänge verwendet werden soll.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- WMDRMNET_POLICY Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373611"
---
# <a name="wmdrmnet_policy-structure"></a><span data-ttu-id="26194-105">Wmdrmnet- \_ Richtlinien Struktur</span><span class="sxs-lookup"><span data-stu-id="26194-105">WMDRMNET\_POLICY structure</span></span>

<span data-ttu-id="26194-106">Die **wmdrmnet- \_ Richtlinien** Struktur enthält die Richtlinie, die für Windows Media DRM für Netzwerkgeräte Vorgänge verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="26194-106">The **WMDRMNET\_POLICY** structure contains the policy to be used for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="26194-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="26194-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a><span data-ttu-id="26194-108">Member</span><span class="sxs-lookup"><span data-stu-id="26194-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="26194-109">**epolicytype**</span><span class="sxs-lookup"><span data-stu-id="26194-109">**ePolicyType**</span></span>
</dt> <dd>

<span data-ttu-id="26194-110">Member der [**wmdrmnet- \_ \_ Richtlinientyp**](wmdrmnet-policy-type.md) -Enumeration, die den Richtlinientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="26194-110">Member of the [**WMDRMNET\_POLICY\_TYPE**](wmdrmnet-policy-type.md) enumeration that specifies the type of policy.</span></span>

</dd> <dt>

<span data-ttu-id="26194-111">**pbpolicy**</span><span class="sxs-lookup"><span data-stu-id="26194-111">**pbPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="26194-112">Puffer, der die Richtlinie enthält.</span><span class="sxs-lookup"><span data-stu-id="26194-112">Buffer containing the policy.</span></span> <span data-ttu-id="26194-113">Der einzige derzeit unterstützte Richtlinientyp ist der **wmdrmnet- \_ Richtlinientyp \_ \_ transryptplay**.</span><span class="sxs-lookup"><span data-stu-id="26194-113">The only type of policy currently supported is **WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**.</span></span> <span data-ttu-id="26194-114">Dieser Member ist ein Zeiger auf die **\_ \_ transryptplay-Struktur der wmdrmnet-Richtlinie** .</span><span class="sxs-lookup"><span data-stu-id="26194-114">This member is a pointer to a **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26194-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26194-115">Remarks</span></span>

<span data-ttu-id="26194-116">Diese Struktur wird als Parameter für die [**iwmdrmnettransmitter:: getleaflicenseresponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="26194-116">This structure is used as a parameter for the [**IWMDRMNetTransmitter::GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="26194-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26194-117">Requirements</span></span>



| <span data-ttu-id="26194-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26194-118">Requirement</span></span> | <span data-ttu-id="26194-119">Wert</span><span class="sxs-lookup"><span data-stu-id="26194-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26194-120">Header</span><span class="sxs-lookup"><span data-stu-id="26194-120">Header</span></span><br/> | <dl> <span data-ttu-id="26194-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="26194-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26194-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26194-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26194-123">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="26194-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="26194-124">**globale Anforderungen für wmdrmnet- \_ Richtlinien \_ \_**</span><span class="sxs-lookup"><span data-stu-id="26194-124">**WMDRMNET\_POLICY\_GLOBAL\_REQUIREMENTS**</span></span>](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[<span data-ttu-id="26194-125">**minimale Umgebung der wmdrmnet- \_ Richtlinie \_ \_**</span><span class="sxs-lookup"><span data-stu-id="26194-125">**WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT**</span></span>](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[<span data-ttu-id="26194-126">**wmdrmnet- \_ Richtlinie \_ transryptplay**</span><span class="sxs-lookup"><span data-stu-id="26194-126">**WMDRMNET\_POLICY\_TRANSCRYPTPLAY**</span></span>](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[<span data-ttu-id="26194-127">**wmdrmnet \_ - \_ Richtlinientyp**</span><span class="sxs-lookup"><span data-stu-id="26194-127">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





