---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: Das vom DRM-Attribut ausführbare \_ \_ copytosdmidevice-Attribut gibt an, ob der Inhalt auf ein SDMI-Gerät kopiert werden darf.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f61da53fd060bd4fb06dbbb7586d923ac17fc0f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389823"
---
# <a name="drm_actionallowed_copytosdmidevice"></a><span data-ttu-id="d5628-104">DRM-Aktions zulässiges \_ \_ copytosdmidevice</span><span class="sxs-lookup"><span data-stu-id="d5628-104">DRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

<span data-ttu-id="d5628-105">Das vom DRM-Attribut ausführbare **\_ \_ copytosdmidevice** -Attribut gibt an, ob der Inhalt auf ein SDMI-Gerät kopiert werden darf.</span><span class="sxs-lookup"><span data-stu-id="d5628-105">The **DRM\_ActionAllowed\_CopyToSDMIDevice** attribute indicates whether the content is allowed to be copied to an SDMI device.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d5628-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="d5628-106">Global Constant</span></span>

<span data-ttu-id="d5628-107">g \_ wszwmdrm- \_ Aktions zulässige \_ copytosdmidevice</span><span class="sxs-lookup"><span data-stu-id="d5628-107">g\_wszWMDRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

## <a name="data-type"></a><span data-ttu-id="d5628-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d5628-108">Data Type</span></span>

<span data-ttu-id="d5628-109">**WMT- \_ Typ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="d5628-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="d5628-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5628-110">Remarks</span></span>

<span data-ttu-id="d5628-111">Windows Media DRM 10-Lizenzen verwenden Sie die Kopier Aktion, um das Kopieren auf Geräte einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="d5628-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to devices.</span></span> <span data-ttu-id="d5628-112">Überprüfen Sie die Eigenschaft " [**DRM- \_ Aktions zulässige \_ Kopie**](drm-actionallowed-copy.md) ", um zu bestimmen, ob das Kopieren zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="d5628-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="d5628-113">Dies ist eine schreibgeschützte Eigenschaft, die mithilfe von [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d5628-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="d5628-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5628-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5628-115">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="d5628-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




