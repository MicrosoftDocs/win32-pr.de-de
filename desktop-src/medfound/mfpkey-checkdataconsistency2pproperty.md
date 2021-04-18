---
description: Gibt an, ob der Encoder bei der Durchführung einer zweistufigen VBR-Codierung eine übergreifende Datenkonsistenz überprüfen soll. Lese-/Schreibzugriff.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: MFPKEY_CHECKDATACONSISTENCY2P-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc706712ef1e8bff36a118031fde155bb9bda31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371983"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a><span data-ttu-id="33353-104">Mfpkey \_ CHECKDATACONSISTENCY2P-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="33353-104">MFPKEY\_CHECKDATACONSISTENCY2P Property</span></span>

<span data-ttu-id="33353-105">Gibt an, ob der Encoder bei der Durchführung einer zweistufigen VBR-Codierung eine übergreifende Datenkonsistenz überprüfen soll.</span><span class="sxs-lookup"><span data-stu-id="33353-105">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <span data-ttu-id="33353-106">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="33353-106">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="33353-107">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="33353-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="33353-108">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="33353-108">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="33353-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="33353-109">Data Type</span></span>

<span data-ttu-id="33353-110">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="33353-110">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="33353-111">Standardwert</span><span class="sxs-lookup"><span data-stu-id="33353-111">Default Value</span></span>

<span data-ttu-id="33353-112">**Variant \_ true**</span><span class="sxs-lookup"><span data-stu-id="33353-112">**VARIANT\_TRUE**</span></span>

## <a name="remarks"></a><span data-ttu-id="33353-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33353-113">Remarks</span></span>

<span data-ttu-id="33353-114">Wenn Sie für diese Eigenschaft den Standardwert **Variant \_ true** belassen, überprüft der Encoder, ob die Eingabe Beispiele zwischen den beiden Durchläufen Stimmen, und schlägt fehl, wenn eine Abweichung erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="33353-114">If you leave this property at its default value of **VARIANT\_TRUE**, the encoder verifies that the input samples match between the two passes, and fails if it detects a discrepancy.</span></span> <span data-ttu-id="33353-115">Das wichtigste Szenario, das zu einer Abweichung führt, besteht darin, dass die Eingabe von einem Gerät stammt.</span><span class="sxs-lookup"><span data-stu-id="33353-115">The main scenario that leads to a discrepancy is when the input comes from a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="33353-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33353-116">Requirements</span></span>



| <span data-ttu-id="33353-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33353-117">Requirement</span></span> | <span data-ttu-id="33353-118">Wert</span><span class="sxs-lookup"><span data-stu-id="33353-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33353-119">Client</span><span class="sxs-lookup"><span data-stu-id="33353-119">Client</span></span><br/> | <span data-ttu-id="33353-120">Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="33353-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="33353-121">Header</span><span class="sxs-lookup"><span data-stu-id="33353-121">Header</span></span><br/> | <dl> <span data-ttu-id="33353-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="33353-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33353-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33353-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33353-124">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33353-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
