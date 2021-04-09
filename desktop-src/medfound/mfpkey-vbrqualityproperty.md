---
description: Gibt die tatsächliche Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (Variable-Bitrate) an.
ms.assetid: e45d583a-323b-4394-9df3-949a3f713708
title: MFPKEY_VBRQUALITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dff57fc27b952780737d63fa8f04faf722ed8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959410"
---
# <a name="mfpkey_vbrquality-property"></a><span data-ttu-id="4c7db-103">Mfpkey \_ vbrquality (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4c7db-103">MFPKEY\_VBRQUALITY Property</span></span>

<span data-ttu-id="4c7db-104">Gibt die tatsächliche Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (Variable-Bitrate) an.</span><span class="sxs-lookup"><span data-stu-id="4c7db-104">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4c7db-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="4c7db-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4c7db-106">g \_ wszwmvcvbrquality, g \_ wszwmcpaudiovbrquality</span><span class="sxs-lookup"><span data-stu-id="4c7db-106">g\_wszWMVCVBRQuality, g\_wszWMCPAudioVBRQuality</span></span>

## <a name="data-type"></a><span data-ttu-id="4c7db-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4c7db-107">Data Type</span></span>

<span data-ttu-id="4c7db-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="4c7db-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="4c7db-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c7db-109">Remarks</span></span>

<span data-ttu-id="4c7db-110">Nicht alle Werte im Bereich haben eine eindeutige Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="4c7db-110">Not all of the values in the range have a unique meaning.</span></span> <span data-ttu-id="4c7db-111">Die Werte, die einen Schritt in der Qualität der vorherigen Ebene darstellen, sind: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97 und 100.</span><span class="sxs-lookup"><span data-stu-id="4c7db-111">The values that represent a step up in quality from the previous level are: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, and 100.</span></span>

<span data-ttu-id="4c7db-112">Für audioencoderobjekte werden die Qualitäts Modi in der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur der Ausgabetypen bereitgestellt, die Sie mithilfe von [**imediaobject:: getoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)abrufen.</span><span class="sxs-lookup"><span data-stu-id="4c7db-112">For audio encoder objects, the quality modes are provided in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the output types that you retrieve using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c7db-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c7db-113">Requirements</span></span>



| <span data-ttu-id="4c7db-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c7db-114">Requirement</span></span> | <span data-ttu-id="4c7db-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4c7db-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c7db-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c7db-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4c7db-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c7db-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4c7db-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c7db-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4c7db-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c7db-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4c7db-120">Header</span><span class="sxs-lookup"><span data-stu-id="4c7db-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c7db-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c7db-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c7db-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c7db-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c7db-123">Auflisten von Audiotypen für bestimmte Codierungs Modi</span><span class="sxs-lookup"><span data-stu-id="4c7db-123">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> <dt>

[<span data-ttu-id="4c7db-124">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4c7db-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
