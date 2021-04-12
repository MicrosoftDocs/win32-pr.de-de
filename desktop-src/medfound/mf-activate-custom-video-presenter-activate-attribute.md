---
description: Gibt ein Aktivierungs Objekt an, das eine benutzerdefinierte Videopräsentation für die EVR-Medien Senke (Enhanced Video Renderer) erstellt.
ms.assetid: 65d88832-0969-4d85-bee2-fd0aa68e9f3b
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75855c18faba8568547f9efcfb19e04574c4885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344608"
---
# <a name="mf_activate_custom_video_presenter_activate-attribute"></a><span data-ttu-id="4e9a0-103">MF Aktivieren des \_ \_ benutzerdefinierten \_ Video \_ Presenter- \_ Aktivierungs Attributs</span><span class="sxs-lookup"><span data-stu-id="4e9a0-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_ACTIVATE attribute</span></span>

<span data-ttu-id="4e9a0-104">Gibt ein Aktivierungs Objekt an, das eine benutzerdefinierte Videopräsentation für die EVR-Medien Senke (Enhanced Video Renderer) erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e9a0-104">Specifies an activation object that creates a custom video presenter for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="4e9a0-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4e9a0-105">Data type</span></span>

<span data-ttu-id="4e9a0-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="4e9a0-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="4e9a0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e9a0-107">Remarks</span></span>

<span data-ttu-id="4e9a0-108">Wenn Sie den EVR mithilfe eines Aktivierungs Objekts erstellen, können Sie dieses Attribut verwenden, um eine benutzerdefinierte Videopräsentation für den EVR festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4e9a0-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video presenter on the EVR.</span></span> <span data-ttu-id="4e9a0-109">Verwenden Sie dieses Attribut wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4e9a0-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="4e9a0-110">Rufen Sie die [_ *mfkreatevideorendereractivation* \*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion auf, um ein Aktivierungs Objekt für den EVR zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e9a0-110">Call the [_ *MFCreateVideoRendererActivate*\*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="4e9a0-111">Die-Funktion gibt einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="4e9a0-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="4e9a0-112">Legen Sie dieses Attribut für den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger fest, indem Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4e9a0-112">Set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span> <span data-ttu-id="4e9a0-113">Der Wert des-Attributs ist ein Zeiger auf ein vom Aufrufer implementiertes Aktivierungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="4e9a0-113">The value of the attribute is a pointer to an activation object implemented by the caller.</span></span> <span data-ttu-id="4e9a0-114">Das Aktivierungs Objekt des Aufrufers muss die **imfaktivate** -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="4e9a0-114">The caller's activation object must expose the **IMFActivate** interface.</span></span>

<span data-ttu-id="4e9a0-115">Wenn Sie dieses Attribut festlegen, ruft der EVR [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) auf, um den benutzerdefinierten Video Presenter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e9a0-115">If you set this attribute, the EVR calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the custom video presenter.</span></span> <span data-ttu-id="4e9a0-116">Die Videopräsentation muss die Schnittstelle [**IMF videopresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="4e9a0-116">The video presenter must expose the [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface.</span></span>

<span data-ttu-id="4e9a0-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="4e9a0-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e9a0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e9a0-118">Requirements</span></span>



| <span data-ttu-id="4e9a0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e9a0-119">Requirement</span></span> | <span data-ttu-id="4e9a0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4e9a0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e9a0-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e9a0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4e9a0-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e9a0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4e9a0-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e9a0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4e9a0-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e9a0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4e9a0-125">Header</span><span class="sxs-lookup"><span data-stu-id="4e9a0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e9a0-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e9a0-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e9a0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e9a0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e9a0-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4e9a0-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4e9a0-129">Erweiterte Videorenderer-Attribute</span><span class="sxs-lookup"><span data-stu-id="4e9a0-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="4e9a0-130">**Imfattributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="4e9a0-130">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="4e9a0-131">\**Imfattributes:: *-Known**</span><span class="sxs-lookup"><span data-stu-id="4e9a0-131">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="4e9a0-132">**Imfaktivate**</span><span class="sxs-lookup"><span data-stu-id="4e9a0-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="4e9a0-133">Aktivierungs Objekte</span><span class="sxs-lookup"><span data-stu-id="4e9a0-133">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="4e9a0-134">Schreiben von EVR Presenter</span><span class="sxs-lookup"><span data-stu-id="4e9a0-134">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




