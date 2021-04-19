---
description: Ruft Qualitätsmetriken für den akustische Echo Abbruch (AEC) aus dem sprach Erfassungs-DSP ab.
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: MFPKEY_WMAAECMA_QUALITY_METRICS-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3740630bc23c4e3e0e824e55b4e34bcd8b1347f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356583"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a><span data-ttu-id="18fe1-103">Mfpkey \_ wmaaecma \_ Quality- \_ Metriken (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="18fe1-103">MFPKEY\_WMAAECMA\_QUALITY\_METRICS Property</span></span>

<span data-ttu-id="18fe1-104">Ruft Qualitätsmetriken für den akustische Echo Abbruch (AEC) aus dem sprach Erfassungs-DSP ab.</span><span class="sxs-lookup"><span data-stu-id="18fe1-104">Retrieves quality metrics on acoustic echo cancellation (AEC) from the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="18fe1-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="18fe1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="18fe1-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="18fe1-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="18fe1-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="18fe1-107">Data Type</span></span>

<span data-ttu-id="18fe1-108">VT- \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="18fe1-108">VT\_BLOB</span></span>

## <a name="remarks"></a><span data-ttu-id="18fe1-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18fe1-109">Remarks</span></span>

<span data-ttu-id="18fe1-110">Der Wert dieser Eigenschaft ist eine [aecqualitymetrics- \_ ](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) Struktur Struktur.</span><span class="sxs-lookup"><span data-stu-id="18fe1-110">The value of this property is an [AecQualityMetrics\_Struct](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) structure.</span></span> <span data-ttu-id="18fe1-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="18fe1-111">This property is read-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="18fe1-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18fe1-112">Requirements</span></span>



| <span data-ttu-id="18fe1-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18fe1-113">Requirement</span></span> | <span data-ttu-id="18fe1-114">Wert</span><span class="sxs-lookup"><span data-stu-id="18fe1-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18fe1-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18fe1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="18fe1-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18fe1-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="18fe1-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18fe1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="18fe1-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18fe1-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="18fe1-119">Header</span><span class="sxs-lookup"><span data-stu-id="18fe1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="18fe1-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="18fe1-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18fe1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18fe1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18fe1-122">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18fe1-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="18fe1-123">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="18fe1-123">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
