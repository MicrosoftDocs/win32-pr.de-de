---
description: Gibt an, ob eine Hardware Geräte Quelle die Systemzeit für Zeitstempel verwendet.
ms.assetid: 54cdfa13-955a-4e92-b337-f645d526a1b8
title: MFT_HW_TIMESTAMP_WITH_QPC_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f6f7d50db89e99e76e7b7ea509f444c3998bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348905"
---
# <a name="mft_hw_timestamp_with_qpc_attribute-attribute"></a><span data-ttu-id="8eb6b-103">MFT- \_ HW- \_ Zeitstempel \_ mit \_ QPC- \_ Attribut Attribut</span><span class="sxs-lookup"><span data-stu-id="8eb6b-103">MFT\_HW\_TIMESTAMP\_WITH\_QPC\_Attribute attribute</span></span>

<span data-ttu-id="8eb6b-104">Gibt an, ob eine Hardware Geräte Quelle die Systemzeit für Zeitstempel verwendet.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-104">Specifies whether a hardware device source uses the system time for time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="8eb6b-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8eb6b-105">Data type</span></span>

<span data-ttu-id="8eb6b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8eb6b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="8eb6b-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="8eb6b-107">Get/set</span></span>

<span data-ttu-id="8eb6b-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="8eb6b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="8eb6b-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="8eb6b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="8eb6b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8eb6b-110">Remarks</span></span>

<span data-ttu-id="8eb6b-111">Wenn dieses Attribut auf **true** festgelegt ist, verwendet die Geräte Quelle die von **QueryPerformanceCounter** zurückgegebene Systemzeit für Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-111">If this attribute is **TRUE**, the device source uses the system time, as returned by the **QueryPerformanceCounter**, for time stamps.</span></span> <span data-ttu-id="8eb6b-112">Andernfalls verwendet die Geräte Quelle die Uhr des Geräts.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-112">Otherwise, the device source uses the device's clock.</span></span> <span data-ttu-id="8eb6b-113">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="8eb6b-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eb6b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8eb6b-115">Requirements</span></span>



| <span data-ttu-id="8eb6b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8eb6b-116">Requirement</span></span> | <span data-ttu-id="8eb6b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8eb6b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb6b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8eb6b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8eb6b-119">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8eb6b-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="8eb6b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8eb6b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8eb6b-121">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8eb6b-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8eb6b-122">Header</span><span class="sxs-lookup"><span data-stu-id="8eb6b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eb6b-123"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="8eb6b-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eb6b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8eb6b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb6b-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="8eb6b-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8eb6b-126">Geräte Attribute erfassen</span><span class="sxs-lookup"><span data-stu-id="8eb6b-126">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




