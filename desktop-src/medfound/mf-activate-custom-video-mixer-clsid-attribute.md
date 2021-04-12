---
description: CLSID eines benutzerdefinierten Video Mischers für die EVR-Medien Senke (Enhanced Video Renderer).
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc1049fb3bc77b65fb48fe9a4c10a059b2a4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343948"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a><span data-ttu-id="bfceb-103">\_ \_ Benutzerdefiniertes \_ \_ \_ CLSID-Attribut für benutzerdefiniertes Video</span><span class="sxs-lookup"><span data-stu-id="bfceb-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID attribute</span></span>

<span data-ttu-id="bfceb-104">CLSID eines benutzerdefinierten Video Mischers für die EVR-Medien Senke (Enhanced Video Renderer).</span><span class="sxs-lookup"><span data-stu-id="bfceb-104">CLSID of a custom video mixer for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="bfceb-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bfceb-105">Data type</span></span>

<span data-ttu-id="bfceb-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="bfceb-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="bfceb-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfceb-107">Remarks</span></span>

<span data-ttu-id="bfceb-108">Wenn Sie den EVR mithilfe eines Aktivierungs Objekts erstellen, können Sie dieses Attribut verwenden, um einen benutzerdefinierten Videomixer auf dem EVR festzulegen.</span><span class="sxs-lookup"><span data-stu-id="bfceb-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video mixer on the EVR.</span></span> <span data-ttu-id="bfceb-109">Verwenden Sie dieses Attribut wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bfceb-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="bfceb-110">Rufen Sie die [**mfkreatevideorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion auf, um ein Aktivierungs Objekt für den EVR zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bfceb-110">Call the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="bfceb-111">Die-Funktion gibt einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="bfceb-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>

2.  <span data-ttu-id="bfceb-112">Legen Sie diese Attribut für den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger fest, indem Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bfceb-112">Set this attribue on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span> <span data-ttu-id="bfceb-113">Der Wert des-Attributs ist die CLSID des benutzerdefinierten Video Mischers der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bfceb-113">The value of the attribute is the CLSID of the application's custom video mixer.</span></span>

<span data-ttu-id="bfceb-114">Wenn dieses Attribut festgelegt ist, ruft der EVR **cokreateinstance** mit der angegebenen CLSID auf, um den benutzerdefinierten Video Mischungs Wert zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bfceb-114">If this attribute is set, the EVR calls **CoCreateInstance** with the specified CLSID to create the custom video mixer.</span></span> <span data-ttu-id="bfceb-115">Der Video-Mixer muss die [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="bfceb-115">The video mixer must expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="bfceb-116">Der Mixer wird als Prozess interner com-Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="bfceb-116">The mixer is created as an in-process COM server.</span></span>

<span data-ttu-id="bfceb-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="bfceb-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfceb-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfceb-118">Requirements</span></span>



| <span data-ttu-id="bfceb-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfceb-119">Requirement</span></span> | <span data-ttu-id="bfceb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="bfceb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bfceb-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfceb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bfceb-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfceb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bfceb-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfceb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bfceb-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfceb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bfceb-125">Header</span><span class="sxs-lookup"><span data-stu-id="bfceb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfceb-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfceb-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfceb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfceb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfceb-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="bfceb-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bfceb-129">Erweiterte Videorenderer-Attribute</span><span class="sxs-lookup"><span data-stu-id="bfceb-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="bfceb-130">**Imfattributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="bfceb-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="bfceb-131">**Imfattributes:: SetGuid**</span><span class="sxs-lookup"><span data-stu-id="bfceb-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="bfceb-132">**Imfaktivate**</span><span class="sxs-lookup"><span data-stu-id="bfceb-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="bfceb-133">Aktivierungs Objekte</span><span class="sxs-lookup"><span data-stu-id="bfceb-133">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




