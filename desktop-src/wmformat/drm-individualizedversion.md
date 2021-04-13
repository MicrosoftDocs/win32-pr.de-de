---
title: DRM_IndividualizedVersion
description: Das DRM \_ -Attribut "IndividualizedVersion" wird im DRM-Header gespeichert und enthält die für den Zugriff auf den Inhalt erforderliche minimale individualisierte Version.
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- DRM_IndividualizedVersion Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ecde48ef3d68e30116cdd7fc8a77179f2282c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314357"
---
# <a name="drm_individualizedversion"></a><span data-ttu-id="1ae47-104">DRM- \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="1ae47-104">DRM\_IndividualizedVersion</span></span>

<span data-ttu-id="1ae47-105">Das DRM-Attribut " **\_ IndividualizedVersion** " wird im DRM-Header gespeichert und enthält die für den Zugriff auf den Inhalt erforderliche minimale individualisierte Version.</span><span class="sxs-lookup"><span data-stu-id="1ae47-105">The **DRM\_IndividualizedVersion** attribute is stored in the DRM header and contains the minimum individualized version required to access the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1ae47-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="1ae47-106">Global Constant</span></span>

<span data-ttu-id="1ae47-107">g \_ wszwmdrm \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="1ae47-107">g\_wszWMDRM\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="1ae47-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1ae47-108">Data Type</span></span>

<span data-ttu-id="1ae47-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ae47-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="1ae47-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ae47-110">Remarks</span></span>

<span data-ttu-id="1ae47-111">Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1ae47-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="1ae47-112">Sie kann mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt werden und kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1ae47-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="1ae47-113">Das gleiche Datei Attribut kann mit [**DRM \_ drmHeader \_ Individual Version**](drm-drmheader-individualizedversion.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1ae47-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1ae47-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ae47-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae47-115">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="1ae47-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




