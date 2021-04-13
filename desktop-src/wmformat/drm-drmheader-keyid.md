---
title: DRM_DRMHeader_KeyID
description: Das Attribut "DRM \_ drmHeader \_ keyid" enthält die Schlüssel-ID für die Datei.
ms.assetid: cf9fe829-8473-4dd5-9a99-48b709fec0d8
keywords:
- DRM_DRMHeader_KeyID Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebbf2f548725309717993bf29e48de2bf78ed17
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314285"
---
# <a name="drm_drmheader_keyid"></a><span data-ttu-id="46151-104">DRM- \_ drmHeader- \_ keyid</span><span class="sxs-lookup"><span data-stu-id="46151-104">DRM\_DRMHeader\_KeyID</span></span>

<span data-ttu-id="46151-105">Das Attribut " **DRM \_ drmHeader \_ keyid** " enthält die Schlüssel-ID für die Datei.</span><span class="sxs-lookup"><span data-stu-id="46151-105">The **DRM\_DRMHeader\_KeyID** attribute contains the key ID for the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="46151-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="46151-106">Global Constant</span></span>

<span data-ttu-id="46151-107">g \_ wszwmdrm \_ drmHeader- \_ keyid</span><span class="sxs-lookup"><span data-stu-id="46151-107">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="46151-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="46151-108">Data Type</span></span>

<span data-ttu-id="46151-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46151-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="46151-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46151-110">Remarks</span></span>

<span data-ttu-id="46151-111">Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="46151-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="46151-112">Sie kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="46151-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="46151-113">Wenn Sie die Schlüssel-ID für die Datei mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festlegen möchten, müssen Sie die [**DRM- \_ keyid**](drm-keyid.md) -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="46151-113">To set the key ID on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_KeyID**](drm-keyid.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="46151-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46151-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46151-115">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="46151-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




