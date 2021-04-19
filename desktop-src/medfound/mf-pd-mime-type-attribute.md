---
description: Gibt den MIME-Typ des Inhalts an.
ms.assetid: bbcfb3e6-a86a-4621-b8d9-92ace60e8c10
title: MF_PD_MIME_TYPE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce1893253af139a73555d3a4fd483e9f59c5ae1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350328"
---
# <a name="mf_pd_mime_type-attribute"></a><span data-ttu-id="fd961-103">MF \_ PD- \_ MIME- \_ Typattribut</span><span class="sxs-lookup"><span data-stu-id="fd961-103">MF\_PD\_MIME\_TYPE attribute</span></span>

<span data-ttu-id="fd961-104">Gibt den MIME-Typ des Inhalts an.</span><span class="sxs-lookup"><span data-stu-id="fd961-104">Specifies the MIME type of the content.</span></span>

## <a name="data-type"></a><span data-ttu-id="fd961-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fd961-105">Data type</span></span>

<span data-ttu-id="fd961-106">Breitzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fd961-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="fd961-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd961-107">Remarks</span></span>

<span data-ttu-id="fd961-108">Dieses Attribut gilt für Präsentations Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="fd961-108">This attribute applies to presentation descriptors.</span></span>

<span data-ttu-id="fd961-109">Der MIME-Typ, der über [System. MimeType](../properties/props-system-mimetype.md) für Mediendateien verfügbar gemacht wird, hat möglicherweise eine Abweichung hinsichtlich der Auswahl von MIME-Typen, die für die Digital Living Network Alliance (DLNA)</span><span class="sxs-lookup"><span data-stu-id="fd961-109">The MIME type exposed through [System.MIMEType](../properties/props-system-mimetype.md) for media files may have a bias towards choosing MIME types suitable for Digital Living Network Alliance (DLNA).</span></span>

<span data-ttu-id="fd961-110">Der \_ MF \_ PD \_ -MIME-Typ und der [System. MimeType](../properties/props-system-mimetype.md) stimmen möglicherweise nicht immer ab.</span><span class="sxs-lookup"><span data-stu-id="fd961-110">MF\_PD\_MIME\_TYPE and [System.MIMEType](../properties/props-system-mimetype.md) may not always match.</span></span>

<span data-ttu-id="fd961-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="fd961-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd961-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd961-112">Requirements</span></span>



| <span data-ttu-id="fd961-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd961-113">Requirement</span></span> | <span data-ttu-id="fd961-114">Wert</span><span class="sxs-lookup"><span data-stu-id="fd961-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd961-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd961-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fd961-116">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="fd961-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="fd961-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd961-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fd961-118">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="fd961-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="fd961-119">Header</span><span class="sxs-lookup"><span data-stu-id="fd961-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd961-120"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd961-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd961-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd961-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd961-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="fd961-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fd961-123">**Imfattributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="fd961-123">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="fd961-124">**Imfattributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="fd961-124">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="fd961-125">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="fd961-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="fd961-126">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="fd961-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
