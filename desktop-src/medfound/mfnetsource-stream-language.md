---
description: Speichert die Zeichenfolge, die im Accept-Language-Header gesendet wird.
ms.assetid: b6ac613c-099b-4415-84ad-c0f8ad5f667b
title: MFNETSOURCE_STREAM_LANGUAGE-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200c49d4a14146277c66fbb3389cf1ba6ab13fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393254"
---
# <a name="mfnetsource_stream_language-property"></a><span data-ttu-id="66eec-103">MF-Quelldaten \_ Strom ( \_ sprach Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="66eec-103">MFNETSOURCE\_STREAM\_LANGUAGE property</span></span>

<span data-ttu-id="66eec-104">Speichert die Zeichenfolge, die im Accept-Language-Header gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="66eec-104">Stores the string sent in the Accept-Language header.</span></span>



<span data-ttu-id="66eec-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="66eec-105">Data type</span></span>

<span data-ttu-id="66eec-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="66eec-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="66eec-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="66eec-107">PROPVARIANT member</span></span>

<span data-ttu-id="66eec-108">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="66eec-108">\**WCHAR\** _</span></span>

<span data-ttu-id="66eec-109">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="66eec-109">VT\_LPWSTR</span></span>

<span data-ttu-id="66eec-110">_ *pwszval*\*</span><span class="sxs-lookup"><span data-stu-id="66eec-110">_ *pwszVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="66eec-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66eec-111">Remarks</span></span>

<span data-ttu-id="66eec-112">Die MF-Quell \_ Datenstrom- \_ sprach Konstante definiert die GUID für den Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="66eec-112">The MFNETSOURCE\_STREAM\_LANGUAGE constant defines the GUID for the property key.</span></span> <span data-ttu-id="66eec-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="66eec-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="66eec-114">Um diese Eigenschaft für die Netzwerkquelle festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="66eec-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="66eec-115">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="66eec-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66eec-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66eec-116">Requirements</span></span>



| <span data-ttu-id="66eec-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66eec-117">Requirement</span></span> | <span data-ttu-id="66eec-118">Wert</span><span class="sxs-lookup"><span data-stu-id="66eec-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66eec-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66eec-119">Minimum supported client</span></span><br/> | <span data-ttu-id="66eec-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66eec-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="66eec-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66eec-121">Minimum supported server</span></span><br/> | <span data-ttu-id="66eec-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66eec-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="66eec-123">Header</span><span class="sxs-lookup"><span data-stu-id="66eec-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="66eec-124"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66eec-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66eec-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66eec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66eec-126">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66eec-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="66eec-127">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66eec-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




