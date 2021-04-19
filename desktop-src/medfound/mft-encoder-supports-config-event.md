---
description: Gibt an, dass der MFT-Encoder beim Streaming das Empfangen von meencodingparameter-Ereignissen unterstützt.
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: MFT_ENCODER_SUPPORTS_CONFIG_EVENT-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49c688abc4d372a463115c369e4616babe3bcaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356640"
---
# <a name="mft_encoder_supports_config_event-attribute"></a><span data-ttu-id="4f419-103">Der MFT- \_ Encoder \_ unterstützt das \_ config- \_ Ereignis Attribut</span><span class="sxs-lookup"><span data-stu-id="4f419-103">MFT\_ENCODER\_SUPPORTS\_CONFIG\_EVENT attribute</span></span>

<span data-ttu-id="4f419-104">Gibt an, dass der MFT-Encoder beim Streaming das Empfangen von [meencodingparameter](meencodingparameters.md) -Ereignissen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f419-104">Specifies that the MFT encoder supports receiving [MEEncodingParameter](meencodingparameters.md) events while streaming.</span></span>

## <a name="data-type"></a><span data-ttu-id="4f419-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4f419-105">Data type</span></span>

<span data-ttu-id="4f419-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f419-106">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4f419-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f419-107">Remarks</span></span>

<span data-ttu-id="4f419-108">Gesendet vom MFT-Encoder durch [**imftransform::P rocesabvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span><span class="sxs-lookup"><span data-stu-id="4f419-108">Sent by the MFT encoder through [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f419-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f419-109">Requirements</span></span>



| <span data-ttu-id="4f419-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f419-110">Requirement</span></span> | <span data-ttu-id="4f419-111">Wert</span><span class="sxs-lookup"><span data-stu-id="4f419-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f419-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f419-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4f419-113">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4f419-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="4f419-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f419-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4f419-115">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4f419-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="4f419-116">Header</span><span class="sxs-lookup"><span data-stu-id="4f419-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f419-117"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4f419-117"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f419-118">IDL</span><span class="sxs-lookup"><span data-stu-id="4f419-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4f419-119"><dt>"MF Transform. idl"</dt></span><span class="sxs-lookup"><span data-stu-id="4f419-119"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f419-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f419-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f419-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4f419-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4f419-122">**IMF Transform::P rocesabvent**</span><span class="sxs-lookup"><span data-stu-id="4f419-122">**IMFTransform::ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




