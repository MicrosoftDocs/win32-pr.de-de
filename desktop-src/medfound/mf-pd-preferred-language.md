---
description: Enthält die bevorzugte RFC 1766-Sprache der Medienquelle.
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: MF_PD_PREFERRED_LANGUAGE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bb121c7181724ef06b3e8fe9239342a140104a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218242"
---
# <a name="mf_pd_preferred_language-attribute"></a><span data-ttu-id="c6401-103">Bevorzugte Programmiersprache für MF \_ PD \_ \_</span><span class="sxs-lookup"><span data-stu-id="c6401-103">MF\_PD\_PREFERRED\_LANGUAGE attribute</span></span>

<span data-ttu-id="c6401-104">Enthält die bevorzugte RFC 1766-Sprache der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="c6401-104">Contains the preferred RFC 1766 language of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="c6401-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c6401-105">Data type</span></span>

<span data-ttu-id="c6401-106">**WCHAR**</span><span class="sxs-lookup"><span data-stu-id="c6401-106">**WCHAR**</span></span>

## <a name="getset"></a><span data-ttu-id="c6401-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="c6401-107">Get/set</span></span>

<span data-ttu-id="c6401-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="c6401-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="c6401-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c6401-109">To set this attribute, call [**IMFAttributes::Settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c6401-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="c6401-110">Applies to</span></span>

[<span data-ttu-id="c6401-111">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="c6401-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="c6401-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6401-112">Remarks</span></span>

<span data-ttu-id="c6401-113">Das \_ bevorzugte Programmiersprachen Attribut von MF PD \_ \_ ist optional.</span><span class="sxs-lookup"><span data-stu-id="c6401-113">The MF\_PD\_PREFERRED\_LANGUAGE attribute is optional.</span></span> <span data-ttu-id="c6401-114">Eine Anwendung kann dieses Attribut für eine Medienquelle (z. b. eine Netzwerkquelle) festlegen, um Ihre bevorzugte Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c6401-114">An application can set this attribute on a media source (such as a network source) to specify its preferred language.</span></span>

<span data-ttu-id="c6401-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="c6401-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6401-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6401-116">Requirements</span></span>



| <span data-ttu-id="c6401-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6401-117">Requirement</span></span> | <span data-ttu-id="c6401-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c6401-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c6401-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6401-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c6401-120">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c6401-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c6401-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6401-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c6401-122">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c6401-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c6401-123">Header</span><span class="sxs-lookup"><span data-stu-id="c6401-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6401-124"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6401-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6401-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6401-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6401-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c6401-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6401-127">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="c6401-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




