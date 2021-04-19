---
title: DRM_DRMHeader_ContentDistributor
description: Das Attribut "DRM \_ drmHeader \_ contentdistributor" enthält eine Zeichenfolge, die den Inhalts Verteiler Bezeichner.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2494f80e612e03f9d25372d38e875c1df814fd7d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106342112"
---
# <a name="drm_drmheader_contentdistributor"></a><span data-ttu-id="d90af-104">DRM- \_ drmHeader- \_ contentdistributor</span><span class="sxs-lookup"><span data-stu-id="d90af-104">DRM\_DRMHeader\_ContentDistributor</span></span>

<span data-ttu-id="d90af-105">Das Attribut " **DRM \_ drmHeader \_ contentdistributor** " enthält eine Zeichenfolge, die den Inhalts Verteiler Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d90af-105">The **DRM\_DRMHeader\_ContentDistributor** attribute contains a string identifiying the content distributor.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d90af-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="d90af-106">Global Constant</span></span>

<span data-ttu-id="d90af-107">g \_ wszwmdrm \_ drmHeader- \_ contentdistributor</span><span class="sxs-lookup"><span data-stu-id="d90af-107">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>

## <a name="data-type"></a><span data-ttu-id="d90af-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d90af-108">Data Type</span></span>

<span data-ttu-id="d90af-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d90af-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="d90af-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d90af-110">Remarks</span></span>

<span data-ttu-id="d90af-111">Die Inhalts-ID ist optional und wird nur vom Ersteller des Inhalts bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d90af-111">The content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="d90af-112">Das Writer-Objekt hat nichts mit diesem Attribut.</span><span class="sxs-lookup"><span data-stu-id="d90af-112">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="d90af-113">Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d90af-113">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="d90af-114">Sie kann mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt werden und kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d90af-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="d90af-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d90af-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d90af-116">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="d90af-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




