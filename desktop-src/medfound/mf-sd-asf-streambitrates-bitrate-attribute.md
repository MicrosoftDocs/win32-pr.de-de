---
description: Gibt die durchschnittliche Bitrate eines Streams in einer ASF-Datei (Advanced Systems Format) in Bits pro Sekunde an. Dieses Attribut entspricht dem Eigenschaften Objekt der Stream-Bitrate, das in der ASF-Spezifikation definiert ist.
ms.assetid: 7ec6004f-c71b-413f-b2fd-dc03a5bf8c57
title: MF_SD_ASF_STREAMBITRATES_BITRATE-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5132ba69f88ce3c0f62160e88d11a6b794b2f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358941"
---
# <a name="mf_sd_asf_streambitrates_bitrate-attribute"></a><span data-ttu-id="2224f-104">MF \_ SD-Attribut für die \_ Attribut- \_ \_ Bitrate</span><span class="sxs-lookup"><span data-stu-id="2224f-104">MF\_SD\_ASF\_STREAMBITRATES\_BITRATE attribute</span></span>

<span data-ttu-id="2224f-105">Gibt die durchschnittliche Bitrate eines Streams in einer ASF-Datei (Advanced Systems Format) in Bits pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="2224f-105">Specifies the average bit rate, in bits per second, of a stream in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="2224f-106">Dieses Attribut entspricht dem Eigenschaften Objekt der Stream-Bitrate, das in der ASF-Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="2224f-106">This attribute corresponds to the Stream Bitrate Properties Object defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="2224f-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2224f-107">Data type</span></span>

<span data-ttu-id="2224f-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2224f-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2224f-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2224f-109">Remarks</span></span>

<span data-ttu-id="2224f-110">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut und legt es für den Datenstrom Deskriptor fest.</span><span class="sxs-lookup"><span data-stu-id="2224f-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the stream descriptor.</span></span> <span data-ttu-id="2224f-111">Die Anwendung kann den Datenstrom Deskriptor für den Stream aus dem Präsentations Deskriptor erstellen, indem Sie [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2224f-111">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="2224f-112">Der Attribut Wert ist mit dem Feld Average Bit Rate im Eigenschaften Objekt der Stream-Bitrate.</span><span class="sxs-lookup"><span data-stu-id="2224f-112">The attribute value equals the Average Bit Rate field in the Stream Bit Rate Properties object.</span></span>

## <a name="requirements"></a><span data-ttu-id="2224f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2224f-113">Requirements</span></span>



| <span data-ttu-id="2224f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2224f-114">Requirement</span></span> | <span data-ttu-id="2224f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2224f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2224f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2224f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2224f-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2224f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2224f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2224f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2224f-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2224f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2224f-120">Header</span><span class="sxs-lookup"><span data-stu-id="2224f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2224f-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2224f-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2224f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2224f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2224f-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="2224f-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2224f-124">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2224f-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2224f-125">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2224f-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2224f-126">**IMF-Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="2224f-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="2224f-127">Streamdeskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="2224f-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="2224f-128">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="2224f-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




