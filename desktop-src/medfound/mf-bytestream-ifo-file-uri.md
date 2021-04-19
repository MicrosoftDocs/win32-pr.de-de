---
description: 'Enthält die URL der vom HTTP-Server im HTTP-Header angegebenen Datei vom HTTP-Server (DVD-Informationen), &\# 0034; Pragma: ifoFileURI.DLNA.org&\# 0034;.'
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: MF_BYTESTREAM_IFO_FILE_URI-Attribut (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c80e015b68272b073c442b4064c80a6787b811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349106"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a><span data-ttu-id="c9b23-103">\_Datenstrom- \_ URI- \_ \_ Attribut für MF-Bytestream</span><span class="sxs-lookup"><span data-stu-id="c9b23-103">MF\_BYTESTREAM\_IFO\_FILE\_URI attribute</span></span>

<span data-ttu-id="c9b23-104">Enthält die URL der vom HTTP-Server im HTTP-Header angegebenen-Datei ("Pragma: ifoFileURI.DLNA.org").</span><span class="sxs-lookup"><span data-stu-id="c9b23-104">Contains the URL of the IFO (DVD Information) file specified by the HTTP server in the HTTP header, "Pragma: ifoFileURI.dlna.org".</span></span>

## <a name="data-type"></a><span data-ttu-id="c9b23-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c9b23-105">Data type</span></span>

<span data-ttu-id="c9b23-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c9b23-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="c9b23-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="c9b23-107">Get/set</span></span>

<span data-ttu-id="c9b23-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="c9b23-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="c9b23-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c9b23-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c9b23-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="c9b23-110">Applies to</span></span>

[<span data-ttu-id="c9b23-111">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="c9b23-111">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="c9b23-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9b23-112">Remarks</span></span>

<span data-ttu-id="c9b23-113">Der http-Bytestream durchsucht den HTTP-Header nach der Zeichenfolge "ifoFileURI.DLNA.org".</span><span class="sxs-lookup"><span data-stu-id="c9b23-113">The HTTP byte stream searches the HTTP header for the "ifoFileURI.dlna.org" string.</span></span> <span data-ttu-id="c9b23-114">Wenn die Zeichenfolge gefunden wird, wird Sie in dieses Attribut im Bytestream kopiert.</span><span class="sxs-lookup"><span data-stu-id="c9b23-114">If the string is found, it is copied to this attribute on the byte stream.</span></span>

<span data-ttu-id="c9b23-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="c9b23-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b23-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9b23-116">Requirements</span></span>



| <span data-ttu-id="c9b23-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9b23-117">Requirement</span></span> | <span data-ttu-id="c9b23-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c9b23-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b23-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9b23-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c9b23-120">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c9b23-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                                        |
| <span data-ttu-id="c9b23-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9b23-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c9b23-122">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c9b23-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="c9b23-123">Header</span><span class="sxs-lookup"><span data-stu-id="c9b23-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9b23-124"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9b23-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9b23-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9b23-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9b23-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c9b23-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c9b23-127">Byte Datenstrom Attribute</span><span class="sxs-lookup"><span data-stu-id="c9b23-127">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="c9b23-128">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="c9b23-128">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




