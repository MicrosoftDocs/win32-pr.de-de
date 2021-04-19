---
description: Gibt die Grenzen des relevanten Bereichs an, der den Bereich des Frames angibt, der unterschiedliche Qualität erfordert.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: MFSampleExtension_ROIRectangle-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d84d2054caa96feaf7bfb4ccc7a91ecf4ac9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356891"
---
# <a name="mfsampleextension_roirectangle-attribute"></a><span data-ttu-id="9aaa5-103">MF Sample Extension- \_ Attribut (roirechteck)</span><span class="sxs-lookup"><span data-stu-id="9aaa5-103">MFSampleExtension\_ROIRectangle attribute</span></span>

<span data-ttu-id="9aaa5-104">Gibt die Grenzen des relevanten Bereichs an, der den Bereich des Frames angibt, der unterschiedliche Qualität erfordert.</span><span class="sxs-lookup"><span data-stu-id="9aaa5-104">Specifies the bounds of the region of interest which indicates the region of the frame that requires different quality.</span></span>

## <a name="data-type"></a><span data-ttu-id="9aaa5-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9aaa5-105">Data type</span></span>

<span data-ttu-id="9aaa5-106">**[**ROI \_**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** Als **BLOB** gespeicherter Bereich</span><span class="sxs-lookup"><span data-stu-id="9aaa5-106">**[**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** stored as **BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="9aaa5-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9aaa5-107">Remarks</span></span>

<span data-ttu-id="9aaa5-108">Nach der erfolgreichen Festlegung von [codecapi \_ avencvideoroiaktiviertem](codecapi-avencvideoroienabled.md) Wert ungleich 0 (null) auf einem Encoder-MFT kann die Anwendung dieses Attribut für Eingabe Beispiele festlegen und erwarten, dass Sie berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="9aaa5-108">After successfully setting [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) to a non-zero value on an encoder MFT, the application can set this attribute on input samples and expect it to be honored.</span></span>

<span data-ttu-id="9aaa5-109">Wenn [codecapi \_ avencvideoroiaktivinicht](codecapi-avencvideoroienabled.md) auf einen Wert ungleich 0 (null) festgelegt ist, wird das Attribut "mfsampleextension \_ roirechteck" bei Eingabe Beispielen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9aaa5-109">If [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) is not set to a non-zero value, the MFSampleExtension\_ROIRectangle attribute is ignored on input samples.</span></span>

<span data-ttu-id="9aaa5-110">Das mfsampleextension \_ -roirechteck ist für ein Eingabe Beispiel festgelegt und wird nur auf das aktuelle Eingabe Beispiel angewendet.</span><span class="sxs-lookup"><span data-stu-id="9aaa5-110">MFSampleExtension\_ROIRectangle is set on an input sample and is only applied to the current input sample.</span></span>

<span data-ttu-id="9aaa5-111">Das Feld **qpdelta** in der [**ROI- \_ Bereichs**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) Struktur gibt den quantisierungsparameterdelta für den angegebenen Bereich vom Rest des Frames an.</span><span class="sxs-lookup"><span data-stu-id="9aaa5-111">The **QPDelta** field on the [**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) structure specifies the quantization parameter delta for the specified region from the rest of the frame.</span></span> <span data-ttu-id="9aaa5-112">Wenn **qpdelta** positiv ist, bedeutet dies, dass die Anwendung für das Rechteck eine niedrigere Qualität als für den Rest des Frames hat.</span><span class="sxs-lookup"><span data-stu-id="9aaa5-112">If **QPDelta** is positive, this indicates the application wants the rectangle to have lower quality than the rest of the frame.</span></span>

<span data-ttu-id="9aaa5-113">**H. 264/AVC-Encoder:** **qpdelta** muss zwischen \[ -25 und + 25 liegen \] .</span><span class="sxs-lookup"><span data-stu-id="9aaa5-113">**H.264/AVC encoders:** **QPDelta** shall be between \[-25, +25\].</span></span> <span data-ttu-id="9aaa5-114">Der Encoder muss sicherstellen, dass das endgültige QP in einem gültigen Bereich für den Videostandard liegt.</span><span class="sxs-lookup"><span data-stu-id="9aaa5-114">The encoder shall ensure that the final QP is in a valid range for the video standard.</span></span>

<span data-ttu-id="9aaa5-115">Der angegebene Bereich muss nicht auf MB ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="9aaa5-115">The specified region is not required to be MB aligned.</span></span> <span data-ttu-id="9aaa5-116">Encoder können die tatsächliche Grenze flexibel festlegen.</span><span class="sxs-lookup"><span data-stu-id="9aaa5-116">Encoders have flexibility to decide the actual boundary.</span></span> <span data-ttu-id="9aaa5-117">Es wird empfohlen, den gesamten angegebenen Bereich abzudecken.</span><span class="sxs-lookup"><span data-stu-id="9aaa5-117">It is recommended to cover the entire specified region.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aaa5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9aaa5-118">Requirements</span></span>



| <span data-ttu-id="9aaa5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9aaa5-119">Requirement</span></span> | <span data-ttu-id="9aaa5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9aaa5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9aaa5-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9aaa5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9aaa5-122">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9aaa5-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="9aaa5-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9aaa5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9aaa5-124">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9aaa5-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9aaa5-125">Header</span><span class="sxs-lookup"><span data-stu-id="9aaa5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aaa5-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aaa5-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aaa5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9aaa5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aaa5-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9aaa5-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




