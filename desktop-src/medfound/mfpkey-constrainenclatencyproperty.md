---
description: Gibt an, ob der Encoder durch eine maximale Latenz Anforderung eingeschränkt wird.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: MFPKEY_CONSTRAINENCLATENCY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f880006bf2aba04196547a79e74f94a7210edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349782"
---
# <a name="mfpkey_constrainenclatency-property"></a><span data-ttu-id="567d4-103">Mfpkey- \_ einschrängericlatency (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="567d4-103">MFPKEY\_CONSTRAINENCLATENCY Property</span></span>

<span data-ttu-id="567d4-104">Gibt an, ob der Encoder durch eine maximale Latenz Anforderung eingeschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="567d4-104">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="567d4-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="567d4-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="567d4-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="567d4-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="567d4-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="567d4-107">Data Type</span></span>

<span data-ttu-id="567d4-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="567d4-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="567d4-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="567d4-109">Default Value</span></span>

<span data-ttu-id="567d4-110">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="567d4-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="567d4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="567d4-111">Remarks</span></span>

<span data-ttu-id="567d4-112">Wenn Sie für diese Eigenschaft den Standardwert **Variant \_ false** belassen, listet der Encoder einen Standardsatz von Modi auf, die ungefähr 2000 Millisekunden der Encoder-Latenzzeit haben.</span><span class="sxs-lookup"><span data-stu-id="567d4-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 2000 milliseconds of encoder latency.</span></span> <span data-ttu-id="567d4-113">Wenn Sie diese Eigenschaft auf **Variant \_ true** festlegen, müssen Sie auch eine maximale encoderwartezeit angeben, indem Sie die Eigenschaft " [**mfpkey \_ maxenclatencyms**](mfpkey-maxenclatencymsproperty.md) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="567d4-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum encoder latency by setting the [**MFPKEY\_MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) property.</span></span> <span data-ttu-id="567d4-114">In diesem Fall erstellt der Encoder Modi, die die Latenz Anforderung erfüllen, und listet nur diese Modi auf.</span><span class="sxs-lookup"><span data-stu-id="567d4-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="567d4-115">Der Encoder garantiert ein Ausgabe Beispiel, sobald der Encoder Eingaben für einen Zeitraum empfangen hat, der **mfpkey \_ maxenclatencyms** entspricht.</span><span class="sxs-lookup"><span data-stu-id="567d4-115">The encoder guarantees an output sample as soon as the encoder has received input for a time period equal to **MFPKEY\_MAXENCLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="567d4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="567d4-116">Requirements</span></span>



| <span data-ttu-id="567d4-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="567d4-117">Requirement</span></span> | <span data-ttu-id="567d4-118">Wert</span><span class="sxs-lookup"><span data-stu-id="567d4-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="567d4-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="567d4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="567d4-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="567d4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="567d4-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="567d4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="567d4-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="567d4-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="567d4-123">Header</span><span class="sxs-lookup"><span data-stu-id="567d4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="567d4-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="567d4-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="567d4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="567d4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="567d4-126">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="567d4-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
