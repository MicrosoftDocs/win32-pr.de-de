---
description: Aktiviert statische Optimierungen in der Video Pipeline.
ms.assetid: 62fb3f0f-ab1f-4c61-8e7f-62908b947788
title: MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f9f7d884c49078ca02571f8ba141f9a1e13589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350907"
---
# <a name="mf_topology_static_playback_optimizations-attribute"></a><span data-ttu-id="e4190-103">\_ \_ Optimierungs Attribut für statische \_ Wiedergabe \_ der MF-Topologie</span><span class="sxs-lookup"><span data-stu-id="e4190-103">MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS attribute</span></span>

<span data-ttu-id="e4190-104">Aktiviert statische Optimierungen in der Video Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e4190-104">Enables static optimizations in the video pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="e4190-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e4190-105">Data type</span></span>

<span data-ttu-id="e4190-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e4190-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e4190-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="e4190-107">Get/set</span></span>

<span data-ttu-id="e4190-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e4190-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e4190-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e4190-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e4190-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="e4190-110">Applies to</span></span>

[<span data-ttu-id="e4190-111">**Imftopology**</span><span class="sxs-lookup"><span data-stu-id="e4190-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="e4190-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4190-112">Remarks</span></span>

<span data-ttu-id="e4190-113">Legen Sie dieses Attribut fest, bevor Sie eine Topologie laden.</span><span class="sxs-lookup"><span data-stu-id="e4190-113">Set this attribute before loading a topology.</span></span> <span data-ttu-id="e4190-114">Wenn das Attribut " **true**" ist, versucht das topologielader die Pipeline zu optimieren, bevor die Wiedergabe gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e4190-114">If the attribute is **TRUE**, the topology loader attempts to optimize the pipeline before playback starts.</span></span>

<span data-ttu-id="e4190-115">Wenn Sie dieses Attribut festlegen, sollten Sie auch die folgenden Attribute festlegen:</span><span class="sxs-lookup"><span data-stu-id="e4190-115">If you set this attribute, you should also set the following attributes:</span></span>

-   [<span data-ttu-id="e4190-116">MF- \_ \_ topologiewiedergabe \_ Framerate</span><span class="sxs-lookup"><span data-stu-id="e4190-116">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span>](mf-topology-playback-framerate.md)
-   [<span data-ttu-id="e4190-117">maximal zulässige Anzahl von MF- \_ \_ topologiewiedergabe \_ \_</span><span class="sxs-lookup"><span data-stu-id="e4190-117">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span>](mf-topology-playback-max-dims.md)

<span data-ttu-id="e4190-118">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="e4190-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="e4190-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4190-119">Examples</span></span>


```C++
HRESULT SetPlaybackOptimizations(IMFTopology *pTopology, HWND hwnd)
{
    HRESULT hr = pTopology->SetUINT32(
        MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS, TRUE);

    if (FAILED(hr))
    {
        return hr;
    }

    HMONITOR hCurrentMon = MonitorFromWindow(hwnd, MONITOR_DEFAULTTOPRIMARY);

    if (hCurrentMon)
    {
        MONITORINFO MonitorInfo = {0};
        MonitorInfo.cbSize = sizeof(MONITORINFO);

        BOOL fSucceeded = GetMonitorInfo(hCurrentMon, &MonitorInfo);

        if (fSucceeded )
        {
            const RECT& rcMonitor = MonitorInfo.rcMonitor;

            LONG width = rcMonitor.right - rcMonitor.left;
            LONG height = rcMonitor.bottom - rcMonitor.top;

            hr = MFSetAttributeSize(
                pTopology, 
                MF_TOPOLOGY_PLAYBACK_MAX_DIMS, 
                (UINT32)width, (UINT32)height
                );

            if (FAILED(hr))
            {
                goto done;
            }

            HDC hdc = GetDC(hwnd);

            hr = MFSetAttributeRatio(
                pTopology,
                MF_TOPOLOGY_PLAYBACK_FRAMERATE,
                GetDeviceCaps(hdc, VREFRESH), 1
                );

            ReleaseDC(hwnd, hdc);
        }
    }
done:
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="e4190-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4190-120">Requirements</span></span>



| <span data-ttu-id="e4190-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4190-121">Requirement</span></span> | <span data-ttu-id="e4190-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e4190-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4190-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4190-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e4190-124">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4190-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e4190-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4190-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e4190-126">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4190-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e4190-127">Header</span><span class="sxs-lookup"><span data-stu-id="e4190-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4190-128"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4190-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4190-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4190-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4190-130">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e4190-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e4190-131">Topologieattribute</span><span class="sxs-lookup"><span data-stu-id="e4190-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="e4190-132">Video Qualitäts Verwaltung</span><span class="sxs-lookup"><span data-stu-id="e4190-132">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




