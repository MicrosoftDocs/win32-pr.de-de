---
description: Gibt die maximale Anzahl von Ausgabe Beispielen an, die eine Microsoft Media Foundation Transformation (MFT) jederzeit in der Pipeline aussteht.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf168158fd6a5f9a173d4d5d25dda3fa5b16d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214884"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a><span data-ttu-id="de416-103">VM \_ - \_ \_ mindestausgabe \_ Sample \_ count-Attribut</span><span class="sxs-lookup"><span data-stu-id="de416-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="de416-104">Gibt die maximale Anzahl von Ausgabe Beispielen an, die eine Microsoft Media Foundation Transformation (MFT) jederzeit in der Pipeline aussteht.</span><span class="sxs-lookup"><span data-stu-id="de416-104">Specifies the maximum number of output samples that a Microsoft Media Foundation transform (MFT) will have outstanding in the pipeline at any time.</span></span>

## <a name="data-type"></a><span data-ttu-id="de416-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="de416-105">Data type</span></span>

<span data-ttu-id="de416-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="de416-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="de416-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de416-107">Remarks</span></span>

<span data-ttu-id="de416-108">Dieses Attribut gilt nur für MFTs, die einen Zirkel Puffer verwenden, um eigene Ausgabe Beispiele zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="de416-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="de416-109">Andere MFTs ignorieren dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="de416-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="de416-110">So legen Sie dieses Attribut fest:</span><span class="sxs-lookup"><span data-stu-id="de416-110">To set this attribute:</span></span>

1.  <span data-ttu-id="de416-111">Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Decoder zum Abrufen eines [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeigers.</span><span class="sxs-lookup"><span data-stu-id="de416-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="de416-112">Zum Hinzufügen des Attributs wird [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="de416-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="de416-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de416-113">Requirements</span></span>



| <span data-ttu-id="de416-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de416-114">Requirement</span></span> | <span data-ttu-id="de416-115">Wert</span><span class="sxs-lookup"><span data-stu-id="de416-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de416-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de416-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de416-117">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="de416-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="de416-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de416-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de416-119">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="de416-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="de416-120">Header</span><span class="sxs-lookup"><span data-stu-id="de416-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="de416-121"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="de416-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de416-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de416-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de416-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="de416-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="de416-124">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="de416-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




