---
description: Gibt die Dauer eines Bytestreams in 100-Nanosecond-Einheiten an.
ms.assetid: afa4930c-544b-4d66-94fe-9795bb526e0a
title: MF_BYTESTREAM_DURATION-Attribut (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df264416b8a805e6d239cfcc457f4a6db2a8e4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344588"
---
# <a name="mf_bytestream_duration-attribute"></a><span data-ttu-id="71c90-103">MF- \_ Bytestream- \_ Duration-Attribut</span><span class="sxs-lookup"><span data-stu-id="71c90-103">MF\_BYTESTREAM\_DURATION attribute</span></span>

<span data-ttu-id="71c90-104">Gibt die Dauer eines Bytestreams in 100-Nanosecond-Einheiten an.</span><span class="sxs-lookup"><span data-stu-id="71c90-104">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="71c90-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="71c90-105">Data type</span></span>

<span data-ttu-id="71c90-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="71c90-106">**UINT64**</span></span>

<span data-ttu-id="71c90-107">Als **Longlong** -Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="71c90-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71c90-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71c90-108">Remarks</span></span>

<span data-ttu-id="71c90-109">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="71c90-109">This attribute is optional.</span></span> <span data-ttu-id="71c90-110">Wenn das Objekt, das den Bytestream erstellt, die Dauer bestimmen kann, kann dieses Attribut festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="71c90-110">If the object that creates the byte stream can determine the duration, it can set this attribute.</span></span> <span data-ttu-id="71c90-111">(In einem Netzwerkstream kann die Dauer z. b. Teil der Sitzungs Beschreibung sein.)</span><span class="sxs-lookup"><span data-stu-id="71c90-111">(For example, in a network stream, the duration might be part of the session description.)</span></span>

<span data-ttu-id="71c90-112">Zum Abrufen des Attribut Werts können Sie **QueryInterface** für den Bytestream abrufen, um einen Zeiger auf die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="71c90-112">To get the attribute value, call **QueryInterface** on the byte stream to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="71c90-113">Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="71c90-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="71c90-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="71c90-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="71c90-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71c90-115">Requirements</span></span>



| <span data-ttu-id="71c90-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71c90-116">Requirement</span></span> | <span data-ttu-id="71c90-117">Wert</span><span class="sxs-lookup"><span data-stu-id="71c90-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71c90-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71c90-118">Minimum supported client</span></span><br/> | <span data-ttu-id="71c90-119">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="71c90-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="71c90-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71c90-120">Minimum supported server</span></span><br/> | <span data-ttu-id="71c90-121">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="71c90-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="71c90-122">Header</span><span class="sxs-lookup"><span data-stu-id="71c90-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="71c90-123"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71c90-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71c90-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71c90-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71c90-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="71c90-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="71c90-126">Byte Datenstrom Attribute</span><span class="sxs-lookup"><span data-stu-id="71c90-126">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="71c90-127">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="71c90-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="71c90-128">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="71c90-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="71c90-129">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="71c90-129">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




