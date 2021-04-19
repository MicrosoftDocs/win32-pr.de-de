---
description: Gibt an, dass Nalu-Längen Informationen als BLOB mit jedem komprimierten H. 264-Beispiel gesendet werden.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: MF_NALU_LENGTH_SET-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a01034cf62758787747882da40ac703d205fa55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350144"
---
# <a name="mf_nalu_length_set-attribute"></a><span data-ttu-id="5105c-103">Attribut "MF \_ Nalu \_ length \_ Set"</span><span class="sxs-lookup"><span data-stu-id="5105c-103">MF\_NALU\_LENGTH\_SET attribute</span></span>

<span data-ttu-id="5105c-104">Gibt an, dass Nalu-Längen Informationen als **BLOB** mit jedem komprimierten H. 264-Beispiel gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="5105c-104">Indicates that NALU length information will be sent as a **BLOB** with each compressed H.264 sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="5105c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5105c-105">Data type</span></span>

<span data-ttu-id="5105c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5105c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5105c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5105c-107">Remarks</span></span>

<span data-ttu-id="5105c-108">Legen Sie dieses Attribut für den Eingabe Medientyp mediasubtype \_ H264 fest.</span><span class="sxs-lookup"><span data-stu-id="5105c-108">Set this attribute on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="5105c-109">Legen Sie \_ \_ \_ die für den Eingabe Medientyp des H. 264-Decoders festgelegte MF-Nalu-Länge fest, und geben Sie an, dass für jedes Eingabe Beispiel eine Nalu-Länge verfügbar ist und jede Eingabe Stichprobe ein ganzes</span><span class="sxs-lookup"><span data-stu-id="5105c-109">Set MF\_NALU\_LENGTH\_SET on input media type of H.264 decoder, indicating each input sample will have a NALU length available and each input sample contains one complete primary picture.</span></span>

<span data-ttu-id="5105c-110">Das **BLOB** , das die Nalu-Längen Informationen enthält, kann aus dem [MF- \_ Nalu- \_ Längen \_ Informations](mf-nalu-length-information.md) Attribut für das Eingabe Beispiel abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5105c-110">The **BLOB** containing the NALU length information can be retrieved from [MF\_NALU\_LENGTH\_INFORMATION](mf-nalu-length-information.md) attribute on the input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="5105c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5105c-111">Requirements</span></span>



| <span data-ttu-id="5105c-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5105c-112">Requirement</span></span> | <span data-ttu-id="5105c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="5105c-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5105c-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5105c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5105c-115">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5105c-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="5105c-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5105c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5105c-117">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5105c-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5105c-118">Header</span><span class="sxs-lookup"><span data-stu-id="5105c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5105c-119"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5105c-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5105c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5105c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5105c-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="5105c-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5105c-122">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="5105c-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




