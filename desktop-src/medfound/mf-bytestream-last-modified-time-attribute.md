---
description: Gibt an, wann ein Bytestream zuletzt geändert wurde.
ms.assetid: dceff922-44eb-478f-842a-8ac0e73a02ee
title: MF_BYTESTREAM_LAST_MODIFIED_TIME-Attribut (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11a5069f8c3f826db9f2ec031d5674013839d97f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754281"
---
# <a name="mf_bytestream_last_modified_time-attribute"></a><span data-ttu-id="6b51b-103">MF- \_ Bytestream- \_ Attribut der letzten \_ Änderung \_</span><span class="sxs-lookup"><span data-stu-id="6b51b-103">MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="6b51b-104">Gibt an, wann ein Bytestream zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="6b51b-104">Specifies when a byte stream was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="6b51b-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6b51b-105">Data type</span></span>

<span data-ttu-id="6b51b-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="6b51b-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="6b51b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b51b-107">Remarks</span></span>

<span data-ttu-id="6b51b-108">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="6b51b-108">This attribute is optional.</span></span> <span data-ttu-id="6b51b-109">Der Wert des-Attributs ist eine [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6b51b-109">The value of the attribute is a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

<span data-ttu-id="6b51b-110">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="6b51b-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b51b-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b51b-111">Requirements</span></span>



| <span data-ttu-id="6b51b-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b51b-112">Requirement</span></span> | <span data-ttu-id="6b51b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="6b51b-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b51b-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b51b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6b51b-115">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6b51b-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="6b51b-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b51b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6b51b-117">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6b51b-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="6b51b-118">Header</span><span class="sxs-lookup"><span data-stu-id="6b51b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b51b-119"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b51b-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b51b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b51b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b51b-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="6b51b-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6b51b-122">Byte Datenstrom Attribute</span><span class="sxs-lookup"><span data-stu-id="6b51b-122">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="6b51b-123">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="6b51b-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="6b51b-124">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="6b51b-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="6b51b-125">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="6b51b-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 
