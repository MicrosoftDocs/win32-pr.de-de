---
description: Enthält Konfigurations Eigenschaften für den Quell Reader.
ms.assetid: f7e5ef6a-5fc3-4f39-acc0-61ce79030211
title: MF_SOURCE_READER_MEDIASOURCE_CONFIG-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f36b2a09810dd1c2563033ea65643f1dabcb3f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106370349"
---
# <a name="mf_source_reader_mediasource_config-attribute"></a><span data-ttu-id="abd1d-103">MF- \_ Quell \_ Leser \_ MediaSource \_ config-Attribut</span><span class="sxs-lookup"><span data-stu-id="abd1d-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CONFIG attribute</span></span>

<span data-ttu-id="abd1d-104">Enthält Konfigurations Eigenschaften für den [Quell Reader](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="abd1d-104">Contains configuration properties for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="abd1d-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="abd1d-105">Data type</span></span>

<span data-ttu-id="abd1d-106">**IPropertyStore \* *_ gespeichert als _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="abd1d-106">**IPropertyStore\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="abd1d-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="abd1d-107">Get/set</span></span>

<span data-ttu-id="abd1d-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="abd1d-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="abd1d-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="abd1d-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="abd1d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abd1d-110">Remarks</span></span>

<span data-ttu-id="abd1d-111">Der Wert dieses Attributs ist ein Zeiger auf die **IPropertyStore** -Schnittstelle eines Eigenschaften Stores.</span><span class="sxs-lookup"><span data-stu-id="abd1d-111">The value of this attribute is a pointer to the **IPropertyStore** interface of a property store.</span></span> <span data-ttu-id="abd1d-112">Sie können dieses Attribut verwenden, um Konfigurations Eigenschaften an die Medienquelle zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="abd1d-112">You can use this attribute to pass configuration properties to the media source.</span></span>

<span data-ttu-id="abd1d-113">Verwenden Sie dieses Attribut mit den folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="abd1d-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="abd1d-114">**MF | atesourcereaderfromb-testream**</span><span class="sxs-lookup"><span data-stu-id="abd1d-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="abd1d-115">**MF | atesourcereaderfromurl**</span><span class="sxs-lookup"><span data-stu-id="abd1d-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="abd1d-116">Intern übergibt der Quell Reader den **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="abd1d-116">Internally, the source reader passes the **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="abd1d-117">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="abd1d-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abd1d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abd1d-118">Requirements</span></span>



| <span data-ttu-id="abd1d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abd1d-119">Requirement</span></span> | <span data-ttu-id="abd1d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="abd1d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="abd1d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abd1d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="abd1d-122">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="abd1d-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="abd1d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abd1d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="abd1d-124">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="abd1d-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="abd1d-125">Header</span><span class="sxs-lookup"><span data-stu-id="abd1d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="abd1d-126"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="abd1d-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abd1d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abd1d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd1d-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="abd1d-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="abd1d-129">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="abd1d-129">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="abd1d-130">Attribute des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="abd1d-130">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




