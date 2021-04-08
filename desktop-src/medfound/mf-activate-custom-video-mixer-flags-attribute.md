---
description: Gibt an, wie ein benutzerdefinierter Mixer für den erweiterten Videorenderer (EVR) erstellt wird.
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b17a0063b7ef4b6a1cbb5993ea2fb7af2a4a678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757867"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a><span data-ttu-id="83602-103">MF \_ - \_ Attribut für benutzerdefinierte \_ Video- \_ \_ mischflags aktivieren</span><span class="sxs-lookup"><span data-stu-id="83602-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_FLAGS attribute</span></span>

<span data-ttu-id="83602-104">Gibt an, wie ein benutzerdefinierter Mixer für den erweiterten Videorenderer (EVR) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="83602-104">Specifies how to create a custom mixer for the enhanced video renderer (EVR).</span></span>

## <a name="data-type"></a><span data-ttu-id="83602-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="83602-105">Data type</span></span>

<span data-ttu-id="83602-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="83602-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="83602-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83602-107">Remarks</span></span>

<span data-ttu-id="83602-108">Sie können dieses Attribut für den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festlegen, der von der MF-Funktion der [**MF**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="83602-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer obtained from the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span> <span data-ttu-id="83602-109">Der Wert dieses Attributs ist ein bitweises **or** der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="83602-109">The value of this attribute is a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="83602-110">Wert</span><span class="sxs-lookup"><span data-stu-id="83602-110">Value</span></span>                                      | <span data-ttu-id="83602-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83602-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83602-112">**MF \_ Aktivieren von \_ benutzerdefiniertem \_ Mixer \_ allowfail**</span><span class="sxs-lookup"><span data-stu-id="83602-112">**MF\_ACTIVATE\_CUSTOM\_MIXER\_ALLOWFAIL**</span></span> | <span data-ttu-id="83602-113">Wenn die [**imfactivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) -Methode den benutzerdefinierten Mixer der Anwendung nicht erstellen kann, wird stattdessen der standardmäßige EVR-Mixer verwendet.</span><span class="sxs-lookup"><span data-stu-id="83602-113">If the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails to create the application's custom mixer, it uses the default EVR mixer instead.</span></span> <span data-ttu-id="83602-114">Wenn das [**imfactivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Objekt bei der Erstellung des benutzerdefinierten Mischers fehlschlägt, schlägt die **activateobject** -Methode standardmäßig fehl.</span><span class="sxs-lookup"><span data-stu-id="83602-114">By default, if the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object fails when it tries to create the custom mixer, the **ActivateObject** method fails.</span></span> |



 

<span data-ttu-id="83602-115">Anwendungen können das CLSID-Attribut " [**\_ \_ benutzerdefiniertes \_ Video- \_ Mixer \_ aktivieren**](mf-activate-custom-video-mixer-clsid-attribute.md) " verwenden, um einen benutzerdefinierten Mixer für den EVR anzugeben.</span><span class="sxs-lookup"><span data-stu-id="83602-115">Applications can use the [**MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md) attribute to specify a custom mixer for the EVR.</span></span>

<span data-ttu-id="83602-116">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="83602-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="83602-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83602-117">Requirements</span></span>



| <span data-ttu-id="83602-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83602-118">Requirement</span></span> | <span data-ttu-id="83602-119">Wert</span><span class="sxs-lookup"><span data-stu-id="83602-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83602-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83602-120">Minimum supported client</span></span><br/> | <span data-ttu-id="83602-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="83602-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="83602-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83602-122">Minimum supported server</span></span><br/> | <span data-ttu-id="83602-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="83602-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="83602-124">Header</span><span class="sxs-lookup"><span data-stu-id="83602-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="83602-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="83602-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83602-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83602-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83602-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="83602-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="83602-128">Erweiterte Videorenderer-Attribute</span><span class="sxs-lookup"><span data-stu-id="83602-128">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="83602-129">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="83602-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="83602-130">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="83602-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="83602-131">Aktivierungs Objekte</span><span class="sxs-lookup"><span data-stu-id="83602-131">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




