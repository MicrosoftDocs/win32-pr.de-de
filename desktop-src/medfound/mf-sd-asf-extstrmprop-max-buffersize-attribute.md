---
description: Gibt die maximale Puffergröße in Bytes an, die für einen Datenstrom in einer ASF-Datei (Advanced Systems Format) benötigt wird.
ms.assetid: 1704a70a-a52b-4e7d-8a32-d0c4e97f8cc2
title: MF_SD_ASF_EXTSTRMPROP_MAX_BUFFERSIZE-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce31dfacd1d53cadcc38b37e1cb755c330a7882f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362715"
---
# <a name="mf_sd_asf_extstrmprop_max_buffersize-attribute"></a><span data-ttu-id="e85de-103">"MF SD"- \_ \_ Attribut " \_ \_ maximal \_ bufferSize"</span><span class="sxs-lookup"><span data-stu-id="e85de-103">MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_BUFFERSIZE attribute</span></span>

<span data-ttu-id="e85de-104">Gibt die maximale Puffergröße in Bytes an, die für einen Datenstrom in einer ASF-Datei (Advanced Systems Format) benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e85de-104">Specifies the maximum buffer size, in bytes, needed for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="e85de-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e85de-105">Data type</span></span>

<span data-ttu-id="e85de-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e85de-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e85de-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e85de-107">Remarks</span></span>

<span data-ttu-id="e85de-108">Dieses Attribut gilt für streamdeskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="e85de-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="e85de-109">Dies entspricht dem Feld für die Alternative Puffergröße im erweiterten Stream Properties-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e85de-109">It corresponds to the Alternate Buffer Size field in the Extended Stream Properties object.</span></span> <span data-ttu-id="e85de-110">Weitere Informationen finden Sie in der ASF-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="e85de-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="e85de-111">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="e85de-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="e85de-112">Die Anwendung kann den Datenstrom Deskriptor für den Stream aus dem Präsentations Deskriptor erstellen, indem Sie [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e85de-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="e85de-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e85de-113">Requirements</span></span>



| <span data-ttu-id="e85de-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e85de-114">Requirement</span></span> | <span data-ttu-id="e85de-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e85de-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e85de-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e85de-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e85de-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e85de-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e85de-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e85de-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e85de-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e85de-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e85de-120">Header</span><span class="sxs-lookup"><span data-stu-id="e85de-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e85de-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="e85de-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e85de-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e85de-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e85de-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e85de-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e85de-124">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e85de-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e85de-125">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e85de-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e85de-126">**IMF-Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="e85de-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="e85de-127">Streamdeskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="e85de-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="e85de-128">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="e85de-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




