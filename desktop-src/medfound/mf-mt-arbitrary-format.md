---
description: Zusätzliche Formatierungsdaten für einen binären Stream in einer ASF-Datei (Advanced Systems Format).
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: MF_MT_ARBITRARY_FORMAT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf98da23fbc4631ca67462dfc58f870abe73885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348099"
---
# <a name="mf_mt_arbitrary_format-attribute"></a><span data-ttu-id="9467f-103">\_ \_ Beliebiges Format von MF MT \_</span><span class="sxs-lookup"><span data-stu-id="9467f-103">MF\_MT\_ARBITRARY\_FORMAT attribute</span></span>

<span data-ttu-id="9467f-104">Zusätzliche Formatierungsdaten für einen binären Stream in einer ASF-Datei (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="9467f-104">Additional format data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="9467f-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9467f-105">Data type</span></span>

<span data-ttu-id="9467f-106">**Hobby\[\]**</span><span class="sxs-lookup"><span data-stu-id="9467f-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="9467f-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="9467f-107">Get/set</span></span>

<span data-ttu-id="9467f-108">Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9467f-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="9467f-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9467f-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="9467f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9467f-110">Remarks</span></span>

<span data-ttu-id="9467f-111">Anwendungen können binäre Datenströme verwenden, um benutzerdefinierte Datentypen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9467f-111">Applications can use binary streams to hold custom data types.</span></span> <span data-ttu-id="9467f-112">Der Wert dieses Attributs wird von der ASF-Medienquelle als undurchsichtiges BLOB behandelt.</span><span class="sxs-lookup"><span data-stu-id="9467f-112">The ASF media source treats the value of this attribute as an opaque blob.</span></span> <span data-ttu-id="9467f-113">Der **Format Type** -Member der [**willkürlichen MT- \_ \_ Header**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) Struktur definiert das Layout der Formatierungsdaten.</span><span class="sxs-lookup"><span data-stu-id="9467f-113">The **formattype** member of the [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure defines the layout of the format data.</span></span>

<span data-ttu-id="9467f-114">Diese Struktur entspricht dem Format Daten Feld der typspezifischen Daten im Stream Properties-Objekt in Dateien, bei denen der Streamtyp ein ASF- **\_ Binär \_ Medium** ist.</span><span class="sxs-lookup"><span data-stu-id="9467f-114">This structure corresponds to the Format Data field of the type-specific data in the Stream Properties Object, in files where the stream type is **ASF\_Binary\_Media**.</span></span> <span data-ttu-id="9467f-115">Weitere Informationen finden Sie in der ASF-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="9467f-115">For more information, see the ASF specification.</span></span>

> [!Note]  
> <span data-ttu-id="9467f-116">Im Windows Media-Format-SDK werden binäre Streams als *beliebige Streams* oder *beliebige Datenströme* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9467f-116">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="9467f-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="9467f-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9467f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9467f-118">Requirements</span></span>



| <span data-ttu-id="9467f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9467f-119">Requirement</span></span> | <span data-ttu-id="9467f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9467f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9467f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9467f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9467f-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9467f-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9467f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9467f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9467f-124">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9467f-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9467f-125">Header</span><span class="sxs-lookup"><span data-stu-id="9467f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9467f-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9467f-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9467f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9467f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9467f-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9467f-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9467f-129">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="9467f-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="9467f-130">\_ \_ beliebiger Header von MF MT \_</span><span class="sxs-lookup"><span data-stu-id="9467f-130">MF\_MT\_ARBITRARY\_HEADER</span></span>](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




