---
title: DRM_DRMHeader_LicenseAcqURL
description: Das \_ Attribut DRM drmHeader \_ licen* AcqURL enthält die Lizenz Erwerbs-URL für eine DRM-Lizenz der Version 7.
ms.assetid: 00c788b4-b291-4df5-9926-0badc7357faf
keywords:
- DRM_DRMHeader_LicenseAcqURL Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c394df01703befbb17c61b340b8ea4239740ac3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038552"
---
# <a name="drm_drmheader_licenseacqurl"></a><span data-ttu-id="2e665-104">DRM \_ drmHeader \_ licenanacqurl</span><span class="sxs-lookup"><span data-stu-id="2e665-104">DRM\_DRMHeader\_LicenseAcqURL</span></span>

<span data-ttu-id="2e665-105">Das Attribut **DRM \_ drmHeader \_ licen* AcqURL*\* enthält die Lizenz Erwerbs-URL für eine DRM-Lizenz der Version 7.</span><span class="sxs-lookup"><span data-stu-id="2e665-105">The **DRM\_DRMHeader\_LicenseAcqURL** attribute contains the license acquisition URL for a DRM version 7 license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="2e665-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="2e665-106">Global Constant</span></span>

<span data-ttu-id="2e665-107">g \_ wszwmdrm \_ drmHeader \_ licengacqurl</span><span class="sxs-lookup"><span data-stu-id="2e665-107">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="2e665-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2e665-108">Data Type</span></span>

<span data-ttu-id="2e665-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e665-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="2e665-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e665-110">Remarks</span></span>

<span data-ttu-id="2e665-111">Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2e665-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="2e665-112">Sie kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2e665-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="2e665-113">Wenn Sie die Lizenz Erwerbs-URL für die Datei mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festlegen möchten, müssen Sie die Eigenschaft [**DRM \_ licenseacqurl**](drm-licenseacqurl.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="2e665-113">To set the license acquisition URL on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_LicenseAcqURL**](drm-licenseacqurl.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e665-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e665-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e665-115">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="2e665-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




