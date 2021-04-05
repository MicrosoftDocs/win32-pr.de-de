---
description: Typspezifische Daten für einen binären Stream in einer ASF-Datei (Advanced Systems Format).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: MF_MT_ARBITRARY_HEADER-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd559ede3506335378ae1d56bf5b886e1407946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041955"
---
# <a name="mf_mt_arbitrary_header-attribute"></a><span data-ttu-id="4843d-103">Beliebiges "MF MT"- \_ \_ \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="4843d-103">MF\_MT\_ARBITRARY\_HEADER attribute</span></span>

<span data-ttu-id="4843d-104">Typspezifische Daten für einen binären Stream in einer ASF-Datei (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="4843d-104">Type-specific data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="4843d-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4843d-105">Data type</span></span>

<span data-ttu-id="4843d-106">**[**MT \_ Beliebiger \_ Header**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** , gespeichert als **Byte \[ \]**</span><span class="sxs-lookup"><span data-stu-id="4843d-106">**[**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="4843d-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="4843d-107">Get/set</span></span>

<span data-ttu-id="4843d-108">Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4843d-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="4843d-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4843d-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="4843d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4843d-110">Remarks</span></span>

<span data-ttu-id="4843d-111">ASF-Dateien können Streams mit Binärdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="4843d-111">ASF files can contain streams with binary data.</span></span> <span data-ttu-id="4843d-112">Das MF \_ MT \_ - \_ Attribut beliebiges Header im Medientyp enthält [**eine \_ beliebige MT- \_ Header**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) Struktur, die den Datenstrom beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4843d-112">The MF\_MT\_ARBITRARY\_HEADER attribute in the media type contains an [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure that describes the stream.</span></span>

<span data-ttu-id="4843d-113">Zusätzlich zum "MF MT"- \_ \_ Attribut beliebiger \_ Header enthält der Medientyp für einen binären ASF-Stream die folgenden Attribute:</span><span class="sxs-lookup"><span data-stu-id="4843d-113">In addition to the MF\_MT\_ARBITRARY\_HEADER attribute, the media type for an ASF binary stream contains the following attributes:</span></span>



| <span data-ttu-id="4843d-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="4843d-114">Attribute</span></span>                                                 | <span data-ttu-id="4843d-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4843d-115">Description</span></span>                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="4843d-116">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4843d-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="4843d-117">Der Wert des-Attributs ist **MF MediaType \_ Binary**.</span><span class="sxs-lookup"><span data-stu-id="4843d-117">The value of the attribute is **MFMediaType\_Binary**.</span></span> |
| [<span data-ttu-id="4843d-118">\_ \_ beliebiges \_ Format der MF-MT</span><span class="sxs-lookup"><span data-stu-id="4843d-118">MF\_MT\_ARBITRARY\_FORMAT</span></span>](mf-mt-arbitrary-format.md)   | <span data-ttu-id="4843d-119">Enthält zusätzliche Formatierungsdaten.</span><span class="sxs-lookup"><span data-stu-id="4843d-119">Contains additional format data.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="4843d-120">Im Windows Media-Format-SDK werden binäre Streams als *beliebige Streams* oder *beliebige Datenströme* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4843d-120">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="4843d-121">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="4843d-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4843d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4843d-122">Requirements</span></span>



| <span data-ttu-id="4843d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4843d-123">Requirement</span></span> | <span data-ttu-id="4843d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4843d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4843d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4843d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4843d-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4843d-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4843d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4843d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4843d-128">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4843d-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4843d-129">Header</span><span class="sxs-lookup"><span data-stu-id="4843d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4843d-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4843d-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4843d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4843d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4843d-132">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4843d-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4843d-133">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="4843d-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




