---
description: Enthält den für den Stream definierten Sami-Sprachnamen (für den verfügbaren Medienaustausch).
ms.assetid: 3151c369-9d2b-4f03-9a4a-9b9267314dc1
title: MF_SD_SAMI_LANGUAGE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd476c86ddde7d369265c5302192e4a7c01295f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350924"
---
# <a name="mf_sd_sami_language-attribute"></a><span data-ttu-id="0d666-103">MF \_ SD \_ - \_ Attribut "Sami"</span><span class="sxs-lookup"><span data-stu-id="0d666-103">MF\_SD\_SAMI\_LANGUAGE attribute</span></span>

<span data-ttu-id="0d666-104">Enthält den für den Stream definierten Sami-Sprachnamen (für den verfügbaren Medienaustausch).</span><span class="sxs-lookup"><span data-stu-id="0d666-104">Contains the Synchronized Accessible Media Interchange (SAMI) language name that is defined for the stream.</span></span>

<span data-ttu-id="0d666-105">Dieses Attribut ist in den Datenstrom Deskriptoren vorhanden, die von der Sami Media-Quelle zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="0d666-105">This attribute is present in the stream descriptors returned from the SAMI media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="0d666-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0d666-106">Data type</span></span>

<span data-ttu-id="0d666-107">Breitzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0d666-107">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="0d666-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d666-108">Remarks</span></span>

<span data-ttu-id="0d666-109">Der Name der Sami-Sprache wird in der Sami-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="0d666-109">The SAMI language name is specified in the SAMI file.</span></span>

<span data-ttu-id="0d666-110">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="0d666-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d666-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d666-111">Requirements</span></span>



| <span data-ttu-id="0d666-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d666-112">Requirement</span></span> | <span data-ttu-id="0d666-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0d666-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d666-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d666-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0d666-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d666-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0d666-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d666-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0d666-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d666-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0d666-118">Header</span><span class="sxs-lookup"><span data-stu-id="0d666-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d666-119"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d666-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d666-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d666-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d666-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0d666-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0d666-122">**Imfattributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="0d666-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="0d666-123">**Imfattributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="0d666-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="0d666-124">**IMF-Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="0d666-124">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="0d666-125">Streamdeskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="0d666-125">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="0d666-126">**Imsasamistyle**</span><span class="sxs-lookup"><span data-stu-id="0d666-126">**IMFSAMIStyle**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)
</dt> </dl>

 

 




