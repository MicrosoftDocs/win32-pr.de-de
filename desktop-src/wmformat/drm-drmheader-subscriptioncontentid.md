---
title: DRM_DRMHeader_SubscriptionContentID
description: Das \_ Attribut DRM drmHeader \_ abonnementcontentid enthält die Abonnement Inhalts-ID.
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- DRM_DRMHeader_SubscriptionContentID Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151665777aa6b68078361eb6e063e374a52f30bf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948430"
---
# <a name="drm_drmheader_subscriptioncontentid"></a><span data-ttu-id="4ec7d-104">DRM- \_ drmHeader- \_ abonnemencontentid</span><span class="sxs-lookup"><span data-stu-id="4ec7d-104">DRM\_DRMHeader\_SubscriptionContentID</span></span>

<span data-ttu-id="4ec7d-105">Das Attribut **DRM \_ drmHeader \_ abonnementcontentid** enthält die Abonnement Inhalts-ID.</span><span class="sxs-lookup"><span data-stu-id="4ec7d-105">The **DRM\_DRMHeader\_SubscriptionContentID** attribute contains the subscription content ID.</span></span>

## <a name="global-constant"></a><span data-ttu-id="4ec7d-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="4ec7d-106">Global Constant</span></span>

<span data-ttu-id="4ec7d-107">g \_ wszwmdrm \_ drmHeader \_ abonnemencontentid</span><span class="sxs-lookup"><span data-stu-id="4ec7d-107">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span>

## <a name="data-type"></a><span data-ttu-id="4ec7d-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4ec7d-108">Data Type</span></span>

<span data-ttu-id="4ec7d-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ec7d-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="4ec7d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ec7d-110">Remarks</span></span>

<span data-ttu-id="4ec7d-111">Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4ec7d-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="4ec7d-112">Die Abonnement Inhalts-ID ist optional und wird nur vom Ersteller des Inhalts bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4ec7d-112">The subscription content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="4ec7d-113">Das Writer-Objekt hat nichts mit diesem Attribut.</span><span class="sxs-lookup"><span data-stu-id="4ec7d-113">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="4ec7d-114">Sie kann mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt werden und kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4ec7d-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="4ec7d-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ec7d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec7d-116">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="4ec7d-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




