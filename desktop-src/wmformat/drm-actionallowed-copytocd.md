---
title: DRM_ActionAllowed_CopyToCD
description: Das vom DRM-Attribut ausführbare \_ \_ Attribut copyper CD gibt an, ob der Inhalt auf eine CD kopiert werden darf.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba214fb2f067ba523222f92211bf7a9412a1634
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106340684"
---
# <a name="drm_actionallowed_copytocd"></a><span data-ttu-id="f0939-104">DRM- \_ Aktions zulässige \_ CopyTo-CD</span><span class="sxs-lookup"><span data-stu-id="f0939-104">DRM\_ActionAllowed\_CopyToCD</span></span>

<span data-ttu-id="f0939-105">Das vom DRM-Attribut ausführbare Attribut **\_ \_ copyper CD** gibt an, ob der Inhalt auf eine CD kopiert werden darf.</span><span class="sxs-lookup"><span data-stu-id="f0939-105">The **DRM\_ActionAllowed\_CopyToCD** attribute indicates whether the content is allowed to be copied to a CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f0939-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="f0939-106">Global Constant</span></span>

<span data-ttu-id="f0939-107">g \_ wszwmdrm- \_ Aktions zulässige \_ copyper-CD</span><span class="sxs-lookup"><span data-stu-id="f0939-107">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>

## <a name="data-type"></a><span data-ttu-id="f0939-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f0939-108">Data Type</span></span>

<span data-ttu-id="f0939-109">**WMT- \_ Typ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="f0939-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="f0939-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0939-110">Remarks</span></span>

<span data-ttu-id="f0939-111">Windows Media DRM 10-Lizenzen verwenden Sie die Kopier Aktion, um das Kopieren auf CD einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="f0939-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to CD.</span></span> <span data-ttu-id="f0939-112">Überprüfen Sie die Eigenschaft " [**DRM- \_ Aktions zulässige \_ Kopie**](drm-actionallowed-copy.md) ", um zu bestimmen, ob das Kopieren zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="f0939-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="f0939-113">Dies ist eine schreibgeschützte Eigenschaft, die mithilfe von [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f0939-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="f0939-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0939-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0939-115">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="f0939-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




