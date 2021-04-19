---
title: DRM_SAPLEVEL (veraltet)
description: Gibt die von der Anwendung unterstützte SAP-Ebene (Secure audiopath) an.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (veraltet) Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43711c6c394761f599271809419a46311265d8b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369357"
---
# <a name="drm_saplevel-deprecated"></a><span data-ttu-id="7e55b-104">DRM- \_ saplevel (veraltet)</span><span class="sxs-lookup"><span data-stu-id="7e55b-104">DRM\_SAPLEVEL (deprecated)</span></span>

<span data-ttu-id="7e55b-105">\[**DRM \_ Saplevel** ist nicht mehr für die Verwendung ab Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7e55b-105">\[**DRM\_SAPLEVEL** is no longer available for use as of Windows Vista.</span></span> <span data-ttu-id="7e55b-106">Verwenden Sie stattdessen "Protected User Mode" (Puma) in der Media Foundation-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="7e55b-106">Instead, use Protected User Mode Audio (PUMA) in the Media Foundation library.</span></span> <span data-ttu-id="7e55b-107">\]</span><span class="sxs-lookup"><span data-stu-id="7e55b-107">\]</span></span>

<span data-ttu-id="7e55b-108">Die DRM-Eigenschaft " **\_ saplevel** " gibt die von der Anwendung unterstützte SAP-Ebene (Secure audiopath) an.</span><span class="sxs-lookup"><span data-stu-id="7e55b-108">The **DRM\_SAPLEVEL** property specifies the secure audio path (SAP) level supported by your application.</span></span>

## <a name="global-constant"></a><span data-ttu-id="7e55b-109">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="7e55b-109">Global Constant</span></span>

<span data-ttu-id="7e55b-110">g \_ wszwmdrm ( \_ saplevel)</span><span class="sxs-lookup"><span data-stu-id="7e55b-110">g\_wszWMDRM\_SAPLEVEL</span></span>

## <a name="data-type"></a><span data-ttu-id="7e55b-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7e55b-111">Data Type</span></span>

<span data-ttu-id="7e55b-112">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e55b-112">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="7e55b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e55b-113">Remarks</span></span>

<span data-ttu-id="7e55b-114">Dies ist eine schreibgeschützte Eigenschaft, die durch den Aufruf von [**iwmdrmreader:: setdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7e55b-114">This is a write-only property that is set by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty).</span></span> <span data-ttu-id="7e55b-115">Der Wert ist eine breit Zeichen-Zeichen folgen Darstellung der SAP-Ebene, z. b. L "200".</span><span class="sxs-lookup"><span data-stu-id="7e55b-115">The value is a wide-character string representation of the SAP level, such as L"200".</span></span> <span data-ttu-id="7e55b-116">Die derzeit unterstützten Werte sind 200 und 300.</span><span class="sxs-lookup"><span data-stu-id="7e55b-116">Current supported values are 200 and 300.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e55b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e55b-117">Requirements</span></span>



| <span data-ttu-id="7e55b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e55b-118">Requirement</span></span> | <span data-ttu-id="7e55b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7e55b-119">Value</span></span> |
|----------------------------------|--------------------------------|
| <span data-ttu-id="7e55b-120">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7e55b-120">End of client support</span></span><br/> | <span data-ttu-id="7e55b-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7e55b-121">Windows XP</span></span><br/>          |
| <span data-ttu-id="7e55b-122">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="7e55b-122">End of server support</span></span><br/> | <span data-ttu-id="7e55b-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e55b-123">Windows Server 2003</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e55b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e55b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e55b-125">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="7e55b-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





