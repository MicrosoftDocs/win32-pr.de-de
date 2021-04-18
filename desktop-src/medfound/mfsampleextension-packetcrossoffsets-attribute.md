---
description: Gibt die Offsets zu den Nutz Last Grenzen in einem Frame für geschützte Beispiele an.
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: MFSampleExtension_PacketCrossOffsets-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d416f41fef9caab3d73c2bdd015d345452ccbd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347861"
---
# <a name="mfsampleextension_packetcrossoffsets-attribute"></a><span data-ttu-id="4c3f1-103">MF Sample Extension \_ packetcrossoffsets-Attribut</span><span class="sxs-lookup"><span data-stu-id="4c3f1-103">MFSampleExtension\_PacketCrossOffsets attribute</span></span>

<span data-ttu-id="4c3f1-104">Gibt die Offsets zu den Nutz Last Grenzen in einem Frame für geschützte Beispiele an.</span><span class="sxs-lookup"><span data-stu-id="4c3f1-104">Specifies the offsets to the payload boundaries in a frame for protected samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="4c3f1-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4c3f1-105">Data type</span></span>

<span data-ttu-id="4c3f1-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="4c3f1-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="4c3f1-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="4c3f1-107">Get/set</span></span>

<span data-ttu-id="4c3f1-108">Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4c3f1-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="4c3f1-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4c3f1-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4c3f1-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="4c3f1-110">Applies to</span></span>

[<span data-ttu-id="4c3f1-111">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="4c3f1-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="4c3f1-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c3f1-112">Remarks</span></span>

<span data-ttu-id="4c3f1-113">Dieses Attribut gilt für Medien Beispiele, die von Windows Media Digital Rights Management (DRM) geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="4c3f1-113">This attribute applies to media samples protected by Windows Media Digital Rights Management (DRM).</span></span> <span data-ttu-id="4c3f1-114">Der Wert des-Attributs ist ein Array von **DWORD** s.</span><span class="sxs-lookup"><span data-stu-id="4c3f1-114">The value of the attribute is an array of **DWORD** s.</span></span> <span data-ttu-id="4c3f1-115">Jeder Eintrag im Array ist der Offset einer Nutz Last Grenze relativ zum Anfang des Frames.</span><span class="sxs-lookup"><span data-stu-id="4c3f1-115">Each entry in the array is the offset of a payload boundary, relative to the start of the frame.</span></span> <span data-ttu-id="4c3f1-116">Diese Werte können von einer Anwendung beim Entschlüsseln und erneuten Erstellen der Frames verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c3f1-116">An application can use these values when decrypting and reconstructing the frames.</span></span>

<span data-ttu-id="4c3f1-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="4c3f1-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c3f1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c3f1-118">Requirements</span></span>



| <span data-ttu-id="4c3f1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c3f1-119">Requirement</span></span> | <span data-ttu-id="4c3f1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4c3f1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c3f1-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c3f1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4c3f1-122">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4c3f1-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="4c3f1-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c3f1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4c3f1-124">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4c3f1-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="4c3f1-125">Header</span><span class="sxs-lookup"><span data-stu-id="4c3f1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c3f1-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c3f1-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c3f1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c3f1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c3f1-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4c3f1-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4c3f1-129">ASF-Splitter</span><span class="sxs-lookup"><span data-stu-id="4c3f1-129">ASF Splitter</span></span>](asf-splitter.md)
</dt> <dt>

[<span data-ttu-id="4c3f1-130">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="4c3f1-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="4c3f1-131">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c3f1-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




