---
description: CLSID eines benutzerdefinierten Video Präsentators für die EVR-Medien Senke (Enhanced Video Renderer).
ms.assetid: f035ee56-7582-45d3-bafe-dd9c821b6326
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0eb913a56671d5d2ac8d27c785e1cc1fbfc51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343719"
---
# <a name="mf_activate_custom_video_presenter_clsid-attribute"></a><span data-ttu-id="4e322-103">MF \_ \_ benutzerdefiniertes \_ \_ CLSID-Attribut für Video Presenter \_ aktivieren</span><span class="sxs-lookup"><span data-stu-id="4e322-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID attribute</span></span>

<span data-ttu-id="4e322-104">CLSID eines benutzerdefinierten Video Präsentators für die EVR-Medien Senke (Enhanced Video Renderer).</span><span class="sxs-lookup"><span data-stu-id="4e322-104">CLSID of a custom video presenter for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="4e322-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4e322-105">Data type</span></span>

<span data-ttu-id="4e322-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="4e322-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="4e322-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e322-107">Remarks</span></span>

<span data-ttu-id="4e322-108">Wenn Sie den EVR mithilfe eines Aktivierungs Objekts erstellen, können Sie dieses Attribut verwenden, um eine benutzerdefinierte Videopräsentation für den EVR festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4e322-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video presenter on the EVR.</span></span> <span data-ttu-id="4e322-109">Verwenden Sie dieses Attribut wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4e322-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="4e322-110">Rufen Sie die [**mfkreatevideorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion auf, um ein Aktivierungs Objekt für den EVR zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e322-110">Call the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="4e322-111">Die-Funktion gibt einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="4e322-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>

2.  <span data-ttu-id="4e322-112">Legen Sie diese Attribut für den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger fest, indem Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4e322-112">Set this attribue on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span> <span data-ttu-id="4e322-113">Der Wert des-Attributs ist die CLSID des benutzerdefinierten Video Presenter der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4e322-113">The value of the attribute is the CLSID of the application's custom video presenter.</span></span>

<span data-ttu-id="4e322-114">Wenn dieses Attribut festgelegt ist, ruft der EVR **cokreateinstance** mit der angegebenen CLSID auf, um den benutzerdefinierten Video Presenter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e322-114">If this attribute is set, the EVR calls **CoCreateInstance** with the specified CLSID to create the custom video presenter.</span></span> <span data-ttu-id="4e322-115">Die Videopräsentation muss die Schnittstelle [**IMF videopresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="4e322-115">The video presenter must expose the [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface.</span></span> <span data-ttu-id="4e322-116">Der Presenter wird als Prozess interner com-Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e322-116">The presenter is created as an in-process COM server.</span></span>

<span data-ttu-id="4e322-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="4e322-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e322-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e322-118">Requirements</span></span>



| <span data-ttu-id="4e322-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e322-119">Requirement</span></span> | <span data-ttu-id="4e322-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4e322-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e322-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e322-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4e322-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e322-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4e322-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e322-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4e322-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e322-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4e322-125">Header</span><span class="sxs-lookup"><span data-stu-id="4e322-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e322-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e322-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e322-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e322-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e322-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4e322-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4e322-129">Erweiterte Videorenderer-Attribute</span><span class="sxs-lookup"><span data-stu-id="4e322-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="4e322-130">**Imfattributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="4e322-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="4e322-131">**Imfattributes:: SetGuid**</span><span class="sxs-lookup"><span data-stu-id="4e322-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="4e322-132">**Imfaktivate**</span><span class="sxs-lookup"><span data-stu-id="4e322-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="4e322-133">Aktivierungs Objekte</span><span class="sxs-lookup"><span data-stu-id="4e322-133">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="4e322-134">Schreiben von EVR Presenter</span><span class="sxs-lookup"><span data-stu-id="4e322-134">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




