---
description: Gibt die ursprüngliche URL für einen Byte Datenstrom an.
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: MF_BYTESTREAM_ORIGIN_NAME-Attribut (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe32602501b3750f709135cf7ca458b6eb6a572f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353120"
---
# <a name="mf_bytestream_origin_name-attribute"></a><span data-ttu-id="7696d-103">MF- \_ Bytestream- \_ Ursprungs \_ Namensattribut</span><span class="sxs-lookup"><span data-stu-id="7696d-103">MF\_BYTESTREAM\_ORIGIN\_NAME attribute</span></span>

<span data-ttu-id="7696d-104">Gibt die ursprüngliche URL für einen Byte Datenstrom an.</span><span class="sxs-lookup"><span data-stu-id="7696d-104">Specifies the original URL for a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="7696d-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7696d-105">Data type</span></span>

<span data-ttu-id="7696d-106">Breitzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7696d-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="7696d-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7696d-107">Remarks</span></span>

<span data-ttu-id="7696d-108">Dateibasierte Byte Datenströme können dieses Attribut unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7696d-108">File-based byte streams can support this attribute.</span></span> <span data-ttu-id="7696d-109">Der Attribut Wert wird festgelegt, wenn der Byte Datenstrom erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7696d-109">The attribute value is set when the byte stream is created.</span></span> <span data-ttu-id="7696d-110">Um den Attribut Wert zu erhalten, Fragen Sie das Byte Datenstrom Objekt für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="7696d-110">To get the attribute value, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="7696d-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="7696d-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7696d-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7696d-112">Requirements</span></span>



| <span data-ttu-id="7696d-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7696d-113">Requirement</span></span> | <span data-ttu-id="7696d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7696d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7696d-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7696d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7696d-116">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7696d-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="7696d-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7696d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7696d-118">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7696d-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="7696d-119">Header</span><span class="sxs-lookup"><span data-stu-id="7696d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7696d-120"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7696d-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7696d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7696d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7696d-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7696d-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7696d-123">Byte Datenstrom Attribute</span><span class="sxs-lookup"><span data-stu-id="7696d-123">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="7696d-124">**Imfattributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="7696d-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="7696d-125">**Imfattributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="7696d-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="7696d-126">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="7696d-126">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




