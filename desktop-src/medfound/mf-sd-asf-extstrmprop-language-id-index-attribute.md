---
description: Gibt die Sprache an, die von einem Datenstrom in einer ASF-Datei (Advanced Systems Format) verwendet wird.
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2afcf2388d2c0641aede4ff0eaccac9178207fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349317"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a><span data-ttu-id="0cba7-103">\_Benutzer- \_ ID- \_ \_ \_ \_ Index Attribut der MF SD-Datei</span><span class="sxs-lookup"><span data-stu-id="0cba7-103">MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX attribute</span></span>

<span data-ttu-id="0cba7-104">Gibt die Sprache an, die von einem Datenstrom in einer ASF-Datei (Advanced Systems Format) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0cba7-104">Specifies the language used by a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="0cba7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0cba7-105">Data type</span></span>

<span data-ttu-id="0cba7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0cba7-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0cba7-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cba7-107">Remarks</span></span>

<span data-ttu-id="0cba7-108">Dieses Attribut gilt für streamdeskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="0cba7-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="0cba7-109">Der Wert ist ein Index in der Sprachliste, die im [**MF PD-Attribut " \_ \_ ASF \_ langlist**](mf-pd-asf-langlist-attribute.md) " enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0cba7-109">The value is an index into the language list contained in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

<span data-ttu-id="0cba7-110">Dieses Attribut entspricht dem Feld "Stream Language ID Index" im erweiterten Stream Properties-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0cba7-110">This attribute corresponds to the Stream Language ID Index field in the Extended Stream Properties object.</span></span> <span data-ttu-id="0cba7-111">Weitere Informationen finden Sie in der ASF-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="0cba7-111">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="0cba7-112">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="0cba7-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="0cba7-113">Die Anwendung kann den Datenstrom Deskriptor für den Stream aus dem Präsentations Deskriptor erstellen, indem Sie [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0cba7-113">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="0cba7-114">Sie können das Sprachtag auch abrufen, indem Sie den Datenstrom Deskriptor für das [**MF \_ SD- \_ sprach**](mf-sd-language-attribute.md) Attribut Abfragen.</span><span class="sxs-lookup"><span data-stu-id="0cba7-114">You can also get the language tag by querying the stream descriptor for the [**MF\_SD\_LANGUAGE**](mf-sd-language-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cba7-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cba7-115">Requirements</span></span>



| <span data-ttu-id="0cba7-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0cba7-116">Requirement</span></span> | <span data-ttu-id="0cba7-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0cba7-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cba7-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0cba7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0cba7-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cba7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0cba7-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cba7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0cba7-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cba7-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0cba7-122">Header</span><span class="sxs-lookup"><span data-stu-id="0cba7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cba7-123"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cba7-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cba7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cba7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cba7-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0cba7-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0cba7-126">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0cba7-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0cba7-127">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0cba7-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0cba7-128">**IMF-Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="0cba7-128">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="0cba7-129">Streamdeskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="0cba7-129">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="0cba7-130">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="0cba7-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




