---
description: Gibt an, ob die Komplexität des audiocodierungs Algorithmus eingeschränkt ist.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: MFPKEY_CONSTRAINENCOMPLEXITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345889"
---
# <a name="mfpkey_constrainencomplexity-property"></a><span data-ttu-id="c59c0-103">Mfpkey- \_ einschränitäts Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c59c0-103">MFPKEY\_CONSTRAINENCOMPLEXITY Property</span></span>

<span data-ttu-id="c59c0-104">Gibt an, ob die Komplexität des audiocodierungs Algorithmus eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="c59c0-104">Specifies whether the complexity of the audio encoding algorithm is constrained.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c59c0-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c59c0-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c59c0-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c59c0-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="c59c0-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c59c0-107">Data Type</span></span>

<span data-ttu-id="c59c0-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c59c0-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="c59c0-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="c59c0-109">Default Value</span></span>

<span data-ttu-id="c59c0-110">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="c59c0-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="c59c0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c59c0-111">Remarks</span></span>

<span data-ttu-id="c59c0-112">Wenn Sie für diese Eigenschaft den Standardwert **Variant \_ false** belassen, verwendet der Audioencoder seinen Standard Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="c59c0-112">If you leave this property at its default value of **VARIANT\_FALSE**, the audio encoder uses its default algorithm.</span></span> <span data-ttu-id="c59c0-113">Der Standard Algorithmus hängt vom Ausgabetyp und der Version von Windows ab.</span><span class="sxs-lookup"><span data-stu-id="c59c0-113">The default algorithm depends on the output type and which version of Windows is running.</span></span> <span data-ttu-id="c59c0-114">In der folgenden Tabelle wird das Standardverhalten für die verschiedenen Kombinationen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c59c0-114">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="c59c0-115">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="c59c0-115">Operating system</span></span> | <span data-ttu-id="c59c0-116">Standardverhalten</span><span class="sxs-lookup"><span data-stu-id="c59c0-116">Default behavior</span></span>                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c59c0-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c59c0-117">Windows Vista</span></span>    | <span data-ttu-id="c59c0-118">Für alle Ausgabetypen verwendet der Audioencoder standardmäßig den komplexesten Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="c59c0-118">For all output types, the audio encoder uses the most complex algorithm by default.</span></span>                                                                                                                 |
| <span data-ttu-id="c59c0-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c59c0-119">Windows 7</span></span>        | <span data-ttu-id="c59c0-120">Bei Standard-und Professional-Ausgabetypen verwendet der Audioencoder standardmäßig den komplexesten Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="c59c0-120">For Standard and Professional output types, the audio encoder uses the most complex algorithm by default.</span></span> <span data-ttu-id="c59c0-121">Für verlustfreie Ausgabetypen verwendet der Audioencoder standardmäßig den am wenigsten komplexen Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="c59c0-121">For Lossless output types, the audio encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="c59c0-122">Wenn Sie diese Eigenschaft auf **Variant \_ true** festlegen, müssen Sie auch einen Komplexitäts Wert angeben, indem Sie die Eigenschaft [**mfpkey \_ enckomplexewert**](mfpkey-enccomplexityproperty.md) festlegen.</span><span class="sxs-lookup"><span data-stu-id="c59c0-122">If you set this property to **VARIANT\_TRUE**, you must also specify a complexity value by setting the [**MFPKEY\_ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c59c0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c59c0-123">Requirements</span></span>



| <span data-ttu-id="c59c0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c59c0-124">Requirement</span></span> | <span data-ttu-id="c59c0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c59c0-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c59c0-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c59c0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c59c0-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c59c0-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c59c0-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c59c0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c59c0-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c59c0-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c59c0-130">Header</span><span class="sxs-lookup"><span data-stu-id="c59c0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c59c0-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c59c0-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c59c0-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c59c0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59c0-133">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c59c0-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
