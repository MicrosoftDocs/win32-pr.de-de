---
title: DRM_LicenseID
description: Die DRM \_ licenseid-Eigenschaft enthält eine Zeichenfolge, die aus der Lizenz abgerufen wird, die der aktuell geöffneten Datei zugeordnet ist, die diese Lizenz eindeutig identifiziert.
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314345"
---
# <a name="drm_licenseid"></a><span data-ttu-id="35d7c-104">DRM- \_ Lizenz seid</span><span class="sxs-lookup"><span data-stu-id="35d7c-104">DRM\_LicenseID</span></span>

<span data-ttu-id="35d7c-105">Die **DRM \_ licenseid** -Eigenschaft enthält eine Zeichenfolge, die aus der Lizenz abgerufen wird, die der aktuell geöffneten Datei zugeordnet ist, die diese Lizenz eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="35d7c-105">The **DRM\_LicenseID** property contains a string retrieved from the license associated with the currently open file that uniquely identifies that license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="35d7c-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="35d7c-106">Global Constant</span></span>

<span data-ttu-id="35d7c-107">g \_ wszwmdrm \_ licenseid</span><span class="sxs-lookup"><span data-stu-id="35d7c-107">g\_wszWMDRM\_LicenseID</span></span>

## <a name="data-type"></a><span data-ttu-id="35d7c-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="35d7c-108">Data Type</span></span>

<span data-ttu-id="35d7c-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="35d7c-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="35d7c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35d7c-110">Remarks</span></span>

<span data-ttu-id="35d7c-111">Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="35d7c-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="35d7c-112">Sie kann mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt werden und kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="35d7c-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

<span data-ttu-id="35d7c-113">Die Lizenz-ID wird in einer Lizenz gespeichert, nicht in einer ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="35d7c-113">The license ID is stored in a license, not in an ASF file.</span></span> <span data-ttu-id="35d7c-114">Jede einzelne Lizenz verfügt über eine eindeutige ID, die dem Lizenz-Generator zum Zeitpunkt der Erstellung der Lizenz zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="35d7c-114">Each individual license has a unique ID which is assigned by the license generator at the time the license is created.</span></span> <span data-ttu-id="35d7c-115">Wenn Sie z. b. zwei Lizenzen für denselben Inhalt erhalten, verfügt jedes über ein anderes licenseid-Attribut.</span><span class="sxs-lookup"><span data-stu-id="35d7c-115">For example, if you obtain two licenses for the same content, each one will have a different LicenseID attribute.</span></span> <span data-ttu-id="35d7c-116">In der Regel müssen Anwendungen diesen Wert nicht abrufen.</span><span class="sxs-lookup"><span data-stu-id="35d7c-116">Typically, applications have no need to retrieve this value.</span></span>

## <a name="see-also"></a><span data-ttu-id="35d7c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35d7c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d7c-118">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="35d7c-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




