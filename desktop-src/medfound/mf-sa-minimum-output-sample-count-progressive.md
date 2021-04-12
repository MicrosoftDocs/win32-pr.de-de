---
description: Gibt die Mindestanzahl von progressiven Stichproben an, die die Microsoft Media Foundation Transform (MFT) zulassen soll, dass Sie zu einem beliebigen Zeitpunkt überstehen.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b452f9fa4016705ed90a7f5b07abcaa6ff11983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216877"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a><span data-ttu-id="bbbbc-103">\_ \_ \_ \_ \_ Anzahl \_ progressives Attribute der MF SA-Ausgabe Stichprobe</span><span class="sxs-lookup"><span data-stu-id="bbbbc-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT\_PROGRESSIVE attribute</span></span>

<span data-ttu-id="bbbbc-104">Gibt die Mindestanzahl von progressiven Stichproben an, die die Microsoft Media Foundation Transform (MFT) zulassen soll, dass Sie zu einem beliebigen Zeitpunkt überstehen.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-104">Indicates the minimum number of progressive samples that the Microsoft Media Foundation transform (MFT) should allow to be oustanding at any given time.</span></span>

## <a name="data-type"></a><span data-ttu-id="bbbbc-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bbbbc-105">Data type</span></span>

<span data-ttu-id="bbbbc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bbbbc-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bbbbc-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbbbc-107">Remarks</span></span>

<span data-ttu-id="bbbbc-108">Dieses Attribut gilt nur für MFTs, die einen Zirkel Puffer verwenden, um eigene Ausgabe Beispiele zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="bbbbc-109">Andere MFTs ignorieren dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="bbbbc-110">So legen Sie dieses Attribut fest:</span><span class="sxs-lookup"><span data-stu-id="bbbbc-110">To set this attribute:</span></span>

1.  <span data-ttu-id="bbbbc-111">Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Decoder zum Abrufen eines [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeigers.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="bbbbc-112">Zum Hinzufügen des Attributs wird [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbbbc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbbbc-113">Requirements</span></span>



| <span data-ttu-id="bbbbc-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbbbc-114">Requirement</span></span> | <span data-ttu-id="bbbbc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bbbbc-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbbbc-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bbbbc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bbbbc-117">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bbbbc-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="bbbbc-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bbbbc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bbbbc-119">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bbbbc-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="bbbbc-120">Header</span><span class="sxs-lookup"><span data-stu-id="bbbbc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbbbc-121"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="bbbbc-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbbbc-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbbbc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbbbc-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="bbbbc-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




