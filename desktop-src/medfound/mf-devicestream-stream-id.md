---
description: Gibt den kernelstreamingbezeichner für einen Datenstrom auf einem Video Erfassungsgerät an.
ms.assetid: 03C48CBA-FAD0-4127-89E5-3F1874BF32DB
title: MF_DEVICESTREAM_STREAM_ID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f7143487af1125da9334fc39c152aee9363b97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041961"
---
# <a name="mf_devicestream_stream_id-attribute"></a><span data-ttu-id="16f6a-103">Das MF- \_ Attribut "devicestream \_ Stream \_ ID"</span><span class="sxs-lookup"><span data-stu-id="16f6a-103">MF\_DEVICESTREAM\_STREAM\_ID attribute</span></span>

<span data-ttu-id="16f6a-104">Gibt den kernelstreamingbezeichner für einen Datenstrom auf einem Video Erfassungsgerät an.</span><span class="sxs-lookup"><span data-stu-id="16f6a-104">Specifies the kernel streaming (KS) identifier for a stream on a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="16f6a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="16f6a-105">Data type</span></span>

<span data-ttu-id="16f6a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="16f6a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="16f6a-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16f6a-107">Remarks</span></span>

<span data-ttu-id="16f6a-108">Gehen Sie folgendermaßen vor, um dieses Attribut zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="16f6a-108">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="16f6a-109">Fragen Sie die Medienquelle für die [**imfmediasourceex**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="16f6a-109">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="16f6a-110">Aufrufen von [**imfmediasourceex:: getstreamattributs**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , um einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger für den Stream zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="16f6a-110">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="16f6a-111">Zum Abrufen des Attributs muss [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="16f6a-111">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="16f6a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16f6a-112">Requirements</span></span>



| <span data-ttu-id="16f6a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16f6a-113">Requirement</span></span> | <span data-ttu-id="16f6a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="16f6a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16f6a-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16f6a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="16f6a-116">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16f6a-116">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="16f6a-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16f6a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="16f6a-118">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16f6a-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="16f6a-119">Header</span><span class="sxs-lookup"><span data-stu-id="16f6a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="16f6a-120"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="16f6a-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16f6a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16f6a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16f6a-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="16f6a-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




