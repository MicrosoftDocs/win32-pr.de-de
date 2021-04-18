---
description: Handle für das Video Clipping-Fenster.
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: MF_ACTIVATE_VIDEO_WINDOW-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a23253c0cd1e4ae90659838acbb58056f770419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351784"
---
# <a name="mf_activate_video_window-attribute"></a><span data-ttu-id="acbc8-103">MF \_ - \_ Video \_ Fenster Attribut aktivieren</span><span class="sxs-lookup"><span data-stu-id="acbc8-103">MF\_ACTIVATE\_VIDEO\_WINDOW attribute</span></span>

<span data-ttu-id="acbc8-104">Handle für das Video Clipping-Fenster.</span><span class="sxs-lookup"><span data-stu-id="acbc8-104">Handle to the video clipping window.</span></span>

## <a name="data-type"></a><span data-ttu-id="acbc8-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="acbc8-105">Data type</span></span>

<span data-ttu-id="acbc8-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="acbc8-106">**UINT64**</span></span>

<span data-ttu-id="acbc8-107">Als **DWORD \_ ptr** (**HWND**) behandeln.</span><span class="sxs-lookup"><span data-stu-id="acbc8-107">Treat as **DWORD\_PTR** (**HWND**).</span></span>

## <a name="remarks"></a><span data-ttu-id="acbc8-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="acbc8-108">Remarks</span></span>

<span data-ttu-id="acbc8-109">Dieses Attribut gilt für das Aktivierungs Objekt für den erweiterten Videorenderer (EVR).</span><span class="sxs-lookup"><span data-stu-id="acbc8-109">This attribute applies to the activation object for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="acbc8-110">Der Wert wird automatisch festgelegt, wenn Sie [**mfkreatevideorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) aufrufen, um das EVR-Aktivierungs Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="acbc8-110">The value is set automatically when you call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the EVR activation object.</span></span>

<span data-ttu-id="acbc8-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="acbc8-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="acbc8-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acbc8-112">Requirements</span></span>



| <span data-ttu-id="acbc8-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acbc8-113">Requirement</span></span> | <span data-ttu-id="acbc8-114">Wert</span><span class="sxs-lookup"><span data-stu-id="acbc8-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="acbc8-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="acbc8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="acbc8-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acbc8-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="acbc8-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="acbc8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="acbc8-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acbc8-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="acbc8-119">Header</span><span class="sxs-lookup"><span data-stu-id="acbc8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="acbc8-120"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="acbc8-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acbc8-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acbc8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acbc8-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="acbc8-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="acbc8-123">Erweiterte Videorenderer-Attribute</span><span class="sxs-lookup"><span data-stu-id="acbc8-123">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="acbc8-124">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="acbc8-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="acbc8-125">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="acbc8-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="acbc8-126">Aktivierungs Objekte</span><span class="sxs-lookup"><span data-stu-id="acbc8-126">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




