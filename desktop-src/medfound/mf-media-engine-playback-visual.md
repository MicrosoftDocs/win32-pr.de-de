---
description: Legt eine Microsoft directcomposition-Visualisierung als Wiedergabe Bereich für die Medien-Engine fest.
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: MF_MEDIA_ENGINE_PLAYBACK_VISUAL-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e9c7366bd0fbf4bf36523cf7a68f2d6da70bc3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106351848"
---
# <a name="mf_media_engine_playback_visual-attribute"></a><span data-ttu-id="df019-103">Das \_ Visual-Attribut für die \_ \_ Wiedergabe \_ von MF</span><span class="sxs-lookup"><span data-stu-id="df019-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_VISUAL attribute</span></span>

<span data-ttu-id="df019-104">Legt eine Microsoft directcomposition-Visualisierung als Wiedergabe Bereich für die Medien-Engine fest.</span><span class="sxs-lookup"><span data-stu-id="df019-104">Sets a Microsoft DirectComposition visual as the playback region for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="df019-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="df019-105">Data type</span></span>

<span data-ttu-id="df019-106">**Idcompositionvisual \* *_ gespeichert als _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="df019-106">**IDCompositionVisual\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="df019-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="df019-107">Get/set</span></span>

<span data-ttu-id="df019-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="df019-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="df019-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="df019-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="df019-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df019-110">Remarks</span></span>

<span data-ttu-id="df019-111">Weitere Informationen zu directcomposition finden Sie unter [directcomposition](../directcomp/directcomposition-portal.md) und [**idcompositionvisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).</span><span class="sxs-lookup"><span data-stu-id="df019-111">For more information on DirectComposition, see [DirectComposition](../directcomp/directcomposition-portal.md) and [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).</span></span>

<span data-ttu-id="df019-112">Dieses Attribut wird mit der [**imfmediaengineclassfactory:: forateinstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) -Methode verwendet, um die Medien-Engine zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="df019-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="df019-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df019-113">Requirements</span></span>



| <span data-ttu-id="df019-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df019-114">Requirement</span></span> | <span data-ttu-id="df019-115">Wert</span><span class="sxs-lookup"><span data-stu-id="df019-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="df019-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df019-116">Minimum supported client</span></span><br/> | <span data-ttu-id="df019-117">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="df019-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="df019-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df019-118">Minimum supported server</span></span><br/> | <span data-ttu-id="df019-119">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="df019-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="df019-120">Header</span><span class="sxs-lookup"><span data-stu-id="df019-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="df019-121"><dt>MF mediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="df019-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df019-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df019-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df019-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="df019-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
