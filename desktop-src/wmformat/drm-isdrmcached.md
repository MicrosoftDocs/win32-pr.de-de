---
title: DRM_IsDRMCached
description: Die DRM- \_ Eigenschaft "isdrmcsend" gibt an, ob die Lizenzinformationen der DRM-Version 1 auf dem lokalen Computer gespeichert wurden.
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- DRM_IsDRMCached Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 185a8b2c94ca5ec517eb1a781262e3f988001a01
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341289"
---
# <a name="drm_isdrmcached"></a><span data-ttu-id="f79a3-104">DRM- \_ isdrmcme</span><span class="sxs-lookup"><span data-stu-id="f79a3-104">DRM\_IsDRMCached</span></span>

<span data-ttu-id="f79a3-105">Die DRM-Eigenschaft " **\_ isdrmcsend** " gibt an, ob die Lizenzinformationen der DRM-Version 1 auf dem lokalen Computer gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="f79a3-105">The **DRM\_IsDRMCached** property indicates whether DRM version 1 license information has been stored on the local machine.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f79a3-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="f79a3-106">Global Constant</span></span>

<span data-ttu-id="f79a3-107">g \_ wszwmdrm \_ isdrmcme</span><span class="sxs-lookup"><span data-stu-id="f79a3-107">g\_wszWMDRM\_IsDRMCached</span></span>

## <a name="data-type"></a><span data-ttu-id="f79a3-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f79a3-108">Data Type</span></span>

<span data-ttu-id="f79a3-109">**WMT- \_ Typ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="f79a3-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="f79a3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f79a3-110">Remarks</span></span>

<span data-ttu-id="f79a3-111">Dies ist eine schreibgeschützte Eigenschaft, die mithilfe von [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f79a3-111">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="f79a3-112">Dies **trifft** zu, wenn die Lizenz Erwerbs-URL mit einer von zwei bekannten URLs übereinstimmt, die für die lokale Lizenz Beschaffung in DRM-Version 1 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f79a3-112">It is **TRUE** when the license acquisition URL matches one of two know URLs used for local license acquisition in DRM version 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="f79a3-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f79a3-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f79a3-114">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="f79a3-114">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




