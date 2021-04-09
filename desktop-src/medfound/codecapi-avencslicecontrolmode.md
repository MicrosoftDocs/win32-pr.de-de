---
description: Gibt den Slice-Steuerelement Modus an. Gültige Werte sind 0, 1 und 2.
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: CODECAPI_AVEncSliceControlMode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958655"
---
# <a name="codecapi_avencslicecontrolmode-property"></a><span data-ttu-id="11e20-104">Codecapi- \_ Eigenschaft "avencslicecontrolmode"</span><span class="sxs-lookup"><span data-stu-id="11e20-104">CODECAPI\_AVEncSliceControlMode property</span></span>

<span data-ttu-id="11e20-105">Gibt den Slice-Steuerelement Modus an.</span><span class="sxs-lookup"><span data-stu-id="11e20-105">Specifies the slice control mode.</span></span> <span data-ttu-id="11e20-106">Gültige Werte sind 0, 1 und 2.</span><span class="sxs-lookup"><span data-stu-id="11e20-106">Valid values are 0, 1, and 2.</span></span>

## <a name="data-type"></a><span data-ttu-id="11e20-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="11e20-107">Data type</span></span>

<span data-ttu-id="11e20-108">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="11e20-108">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="11e20-109">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="11e20-109">Property GUID</span></span>

<span data-ttu-id="11e20-110">**Codecapi \_ avencslicecontrolmode**</span><span class="sxs-lookup"><span data-stu-id="11e20-110">**CODECAPI\_AVEncSliceControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="11e20-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="11e20-111">Property value</span></span>

<span data-ttu-id="11e20-112">Werte für Slice-Steuerelement Modus:</span><span class="sxs-lookup"><span data-stu-id="11e20-112">Slice control mode values:</span></span>



| <span data-ttu-id="11e20-113">Wert</span><span class="sxs-lookup"><span data-stu-id="11e20-113">Value</span></span>                                                                        | <span data-ttu-id="11e20-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="11e20-114">Meaning</span></span>                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11e20-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="11e20-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="11e20-116">Wenn dieser Wert auf 0 festgelegt wird, wird angegeben, dass die [codecapi-Eigenschaft " \_ avencslicecontrolsize](codecapi-avencslicecontrolsize.md) " die Slice-Größe in Einheiten von makroblöcken pro Slice angibt.</span><span class="sxs-lookup"><span data-stu-id="11e20-116">Setting this value to 0 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblocks per slice.</span></span><br/>     |
| <dl> <span data-ttu-id="11e20-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="11e20-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="11e20-118">Wenn dieser Wert auf 1 festgelegt wird, gibt die [codecapi-Eigenschaft " \_ avencslicecontrolsize](codecapi-avencslicecontrolsize.md) " die Slice-Größe in Bits-Einheiten pro Slice an.</span><span class="sxs-lookup"><span data-stu-id="11e20-118">Setting this value to 1 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of bits per slice.</span></span><br/>            |
| <dl> <span data-ttu-id="11e20-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="11e20-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="11e20-120">Wenn dieser Wert auf 2 festgelegt wird, gibt die [codecapi-Eigenschaft " \_ avencslicecontrolsize](codecapi-avencslicecontrolsize.md) " die Slice-Größe in Einheiten von Makroblock Zeilen pro Slice an.</span><span class="sxs-lookup"><span data-stu-id="11e20-120">Setting this value to 2 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblock rows per slice.</span></span><br/> |



 

<span data-ttu-id="11e20-121">Der Encoder gibt die Werte zurück, die er unterstützt.</span><span class="sxs-lookup"><span data-stu-id="11e20-121">The encoder returns the values that it supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="11e20-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11e20-122">Remarks</span></span>

<span data-ttu-id="11e20-123">**H. 264/AVC-Encoder:**</span><span class="sxs-lookup"><span data-stu-id="11e20-123">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="11e20-124">Es wird empfohlen, dass der Encoder " [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)", " [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)" und " [**getparameterrange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="11e20-124">It is recommended that the encoder supports [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="11e20-125">Wenn [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) nicht für codecapi \_ avencslicecontrolmode aufgerufen wird, kann [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) für codecapi \_ avencslicecontrolmode den **VFW \_ E \_ codecapi \_ ohne \_ aktuellen \_ Wert** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="11e20-125">If [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) is not called for CODECAPI\_AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) for CODECAPI\_AVEncSliceControlMode can return **VFW\_E\_CODECAPI\_NO\_CURRENT\_VALUE**.</span></span> <span data-ttu-id="11e20-126">" [**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) " gibt möglicherweise " **VFW \_ E \_ codecapi \_ No \_ default** " für codecapi \_ avencslicecontrolmode zurück.</span><span class="sxs-lookup"><span data-stu-id="11e20-126">[**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) may return **VFW\_E\_CODECAPI\_NO\_DEFAULT** for CODECAPI\_AVEncSliceControlMode.</span></span>

<span data-ttu-id="11e20-127">Der empfohlene Standardwert ist 2 (Größe in MB Zeile pro Slice).</span><span class="sxs-lookup"><span data-stu-id="11e20-127">Recommended default value is 2 (size in MB row per slice).</span></span>

<span data-ttu-id="11e20-128">Dabei handelt es sich um eine statische API, was bedeutet, dass sich die Anwendung bei Ausführung des Encoders nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="11e20-128">This is a static API, which means the application won t change this while the encoder is running.</span></span>

## <a name="examples"></a><span data-ttu-id="11e20-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11e20-129">Examples</span></span>


```C++
if (pCodecAPI->IsSupported(&CODECAPI_AVEncSliceControlMode) == S_OK) {                
     VARIANT var;
     var.vt = VT_UI4;
     var.ulVal =ulSliceMode;
     pCodecAPI->SetValue(&CODECAPI_AVEncSliceControlMode, &var);
}
```



## <a name="requirements"></a><span data-ttu-id="11e20-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11e20-130">Requirements</span></span>



| <span data-ttu-id="11e20-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11e20-131">Requirement</span></span> | <span data-ttu-id="11e20-132">Wert</span><span class="sxs-lookup"><span data-stu-id="11e20-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11e20-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11e20-133">Minimum supported client</span></span><br/> | <span data-ttu-id="11e20-134">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="11e20-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="11e20-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11e20-135">Minimum supported server</span></span><br/> | <span data-ttu-id="11e20-136">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="11e20-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="11e20-137">Header</span><span class="sxs-lookup"><span data-stu-id="11e20-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="11e20-138"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="11e20-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11e20-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11e20-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e20-140">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="11e20-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

