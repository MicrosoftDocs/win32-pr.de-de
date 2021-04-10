---
description: Gibt an, wie ein benutzerdefinierter Presenter für den erweiterten Videorenderer (EVR) erstellt wird.
ms.assetid: 40893e13-bf2e-4424-ae43-2b253fc0b622
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3681edaed39b63b0f7c13313039f1c6e72311a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042579"
---
# <a name="mf_activate_custom_video_presenter_flags-attribute"></a><span data-ttu-id="03541-103">MF \_ - \_ Attribut für benutzerdefinierte \_ Video \_ Presenter- \_ Flags aktivieren</span><span class="sxs-lookup"><span data-stu-id="03541-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_FLAGS attribute</span></span>

<span data-ttu-id="03541-104">Gibt an, wie ein benutzerdefinierter Presenter für den erweiterten Videorenderer (EVR) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="03541-104">Specifies how to create a custom presenter for the enhanced video renderer (EVR).</span></span>

## <a name="data-type"></a><span data-ttu-id="03541-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="03541-105">Data type</span></span>

<span data-ttu-id="03541-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="03541-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="03541-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03541-107">Remarks</span></span>

<span data-ttu-id="03541-108">Sie können dieses Attribut für den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festlegen, der von der MF-Funktion der [**MF**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="03541-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer obtained from the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span> <span data-ttu-id="03541-109">Der Wert dieses Attributs ist ein bitweises **or** der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="03541-109">The value of this attribute is a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="03541-110">Wert</span><span class="sxs-lookup"><span data-stu-id="03541-110">Value</span></span>                                          | <span data-ttu-id="03541-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03541-111">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03541-112">**MF \_ Aktivieren von \_ benutzerdefiniertem \_ Presenter \_ allowfail**</span><span class="sxs-lookup"><span data-stu-id="03541-112">**MF\_ACTIVATE\_CUSTOM\_PRESENTER\_ALLOWFAIL**</span></span> | <span data-ttu-id="03541-113">Wenn die [**imfactivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) -Methode den benutzerdefinierten Presenter der Anwendung nicht erstellen kann, wird stattdessen der standardmäßige "EVR Presenter" verwendet.</span><span class="sxs-lookup"><span data-stu-id="03541-113">If the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails to create the application's custom presenter, it uses the default EVR presenter instead.</span></span> <span data-ttu-id="03541-114">Wenn das [**imfactivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Objekt bei dem Versuch, den benutzerdefinierten Presenter zu erstellen, fehlschlägt, schlägt die **activateobject** -Methode standardmäßig fehl.</span><span class="sxs-lookup"><span data-stu-id="03541-114">By default, if the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object fails when it tries to create the custom presenter, the **ActivateObject** method fails.</span></span> |



 

<span data-ttu-id="03541-115">Anwendungen können das CLSID-Attribut für [**\_ \_ benutzerdefinierte \_ Video \_ \_ Presenter aktivieren**](mf-activate-custom-video-presenter-clsid-attribute.md) verwenden, um einen benutzerdefinierten Presenter für den EVR anzugeben.</span><span class="sxs-lookup"><span data-stu-id="03541-115">Applications can use the [**MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md) attribute to specify a custom presenter for the EVR.</span></span>

<span data-ttu-id="03541-116">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="03541-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="03541-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03541-117">Requirements</span></span>



| <span data-ttu-id="03541-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03541-118">Requirement</span></span> | <span data-ttu-id="03541-119">Wert</span><span class="sxs-lookup"><span data-stu-id="03541-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03541-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03541-120">Minimum supported client</span></span><br/> | <span data-ttu-id="03541-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03541-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="03541-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03541-122">Minimum supported server</span></span><br/> | <span data-ttu-id="03541-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03541-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="03541-124">Header</span><span class="sxs-lookup"><span data-stu-id="03541-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="03541-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="03541-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03541-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03541-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03541-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="03541-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="03541-128">Erweiterte Videorenderer-Attribute</span><span class="sxs-lookup"><span data-stu-id="03541-128">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="03541-129">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="03541-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="03541-130">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="03541-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="03541-131">Aktivierungs Objekte</span><span class="sxs-lookup"><span data-stu-id="03541-131">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="03541-132">Schreiben von EVR Presenter</span><span class="sxs-lookup"><span data-stu-id="03541-132">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




