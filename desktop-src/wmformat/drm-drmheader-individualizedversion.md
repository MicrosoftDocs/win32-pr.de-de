---
title: DRM_DRMHeader_IndividualizedVersion
description: Das DRM- \_ Attribut "drmheaderindividualizedversion" enthält die mindestens erforderliche individualisierte Version, die für die Wiedergabe der Datei erforderlich ist.
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- DRM_DRMHeader_IndividualizedVersion Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167065f99a72245c6d7cc677ce24fa1ff96dec84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338438"
---
# <a name="drm_drmheader_individualizedversion"></a><span data-ttu-id="1312f-104">DRM \_ drmHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="1312f-104">DRM\_DRMHeader\_IndividualizedVersion</span></span>

<span data-ttu-id="1312f-105">Das DRM-Attribut " **\_ drmheaderindividualizedversion** " enthält die mindestens erforderliche individualisierte Version, die für die Wiedergabe der Datei erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1312f-105">The **DRM\_DRMHeaderIndividualizedVersion** attribute contains the minimum individualized version required to play back the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1312f-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="1312f-106">Global Constant</span></span>

<span data-ttu-id="1312f-107">g \_ wszwmdrm \_ drmHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="1312f-107">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="1312f-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1312f-108">Data Type</span></span>

<span data-ttu-id="1312f-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1312f-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="1312f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1312f-110">Remarks</span></span>

<span data-ttu-id="1312f-111">Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1312f-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="1312f-112">Sie kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1312f-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="1312f-113">Zum Festlegen der individualisierten Version (auch als Sicherheitsversion bezeichnet) für die Datei mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) müssen Sie die [**DRM \_ Individual Version**](drm-individualizedversion.md) -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="1312f-113">To set the individualized version (also called the security version) on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_IndividualizedVersion**](drm-individualizedversion.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="1312f-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1312f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1312f-115">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="1312f-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




