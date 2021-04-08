---
description: Gibt die Komplexität des Codierungs Algorithmus an.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: MFPKEY_ENCCOMPLEXITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f50e7966a05affe8ae75869b670cf75f088b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864164"
---
# <a name="mfpkey_enccomplexity-property"></a><span data-ttu-id="bcbdc-103">Mfpkey \_ enckomplexität (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bcbdc-103">MFPKEY\_ENCCOMPLEXITY Property</span></span>

<span data-ttu-id="bcbdc-104">Gibt die Komplexität des Codierungs Algorithmus an.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-104">Specifies the complexity of the encoding algorithm.</span></span> <span data-ttu-id="bcbdc-105">Der Wert ist eine ganze Zahl zwischen 0 und 100, wobei 0 den am wenigsten komplexen Algorithmus und 100 den komplexesten Algorithmus angibt.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-105">The value is an integer between 0 and 100, where 0 specifies the least complex algorithm, and 100 specifies the most complex algorithm.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="bcbdc-106">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="bcbdc-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="bcbdc-107">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-107">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="bcbdc-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bcbdc-108">Data Type</span></span>

<span data-ttu-id="bcbdc-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="bcbdc-109">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="bcbdc-110">Standardwert</span><span class="sxs-lookup"><span data-stu-id="bcbdc-110">Default Value</span></span>

<span data-ttu-id="bcbdc-111">100 für Windows Media Audio 10 und Windows Media Audio 10 Professional</span><span class="sxs-lookup"><span data-stu-id="bcbdc-111">100 for Windows Media Audio 10 and Windows Media Audio 10 Professional</span></span>

<span data-ttu-id="bcbdc-112">100 für die Windows Vista-Version von Windows Media Audio 10 verlustfrei</span><span class="sxs-lookup"><span data-stu-id="bcbdc-112">100 for the Windows Vista release of Windows Media Audio 10 Lossless</span></span>

<span data-ttu-id="bcbdc-113">0 für Windows 7 Release Windows Media Audio 10 verlustfreie Version</span><span class="sxs-lookup"><span data-stu-id="bcbdc-113">0 for the Windows 7 release Windows Media Audio 10 Lossless</span></span>

## <a name="remarks"></a><span data-ttu-id="bcbdc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcbdc-114">Remarks</span></span>

<span data-ttu-id="bcbdc-115">Wenn die Eigenschaft [**mfpkey \_ einschränationskomplexität**](mfpkey-constrainenccomplexityproperty.md) den Wert **Variant \_ true** hat, passt der Encoder die Komplexität seines Algorithmus entsprechend dem Wert dieser Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-115">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_TRUE**, the encoder adjusts the complexity of its algorithm according to the value of this property.</span></span>

<span data-ttu-id="bcbdc-116">Für den Windows Media Audio 10-Encoder und den Windows Media Audio 10 Professional-Encoder, wenn der Wert dieser Eigenschaft 100 ist, stellt der Encoder einen hohen Bedarf an der CPU her und erzeugt die höchst wertige Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-116">For the Windows Media Audio 10 encoder and the Windows Media Audio 10 Professional encoder, if the value of this property is 100, the encoder places a high demand on the CPU and produces the highest quality output.</span></span> <span data-ttu-id="bcbdc-117">Wenn der Wert dieser Eigenschaft abnimmt, sinkt die Nachfrage nach der CPU, aber die Qualität der Ausgabe wird ebenfalls verringert.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-117">As the value of this property decreases, the demand on the CPU decreases, but the quality of the output also decreases.</span></span>

<span data-ttu-id="bcbdc-118">Wenn der Wert dieser Eigenschaft auf 0 (null) gesetzt ist und der Wert dieser Eigenschaft auf 0 (null) gesetzt ist, stellt der Encoder für den Windows Media Audio 10-Encoder ohne Verlust</span><span class="sxs-lookup"><span data-stu-id="bcbdc-118">For the Windows Media Audio 10 Lossless encoder, if the value of this property is 0, the encoder places a low demand on the CPU.</span></span> <span data-ttu-id="bcbdc-119">Wenn der Wert dieser Eigenschaft zunimmt, steigt der Bedarf an der CPU, und die Größe der Encoder-Ausgabe nimmt geringfügig ab.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-119">As the value of this property increases, the demand on the CPU increases, and the size of the encoder output decreases slightly.</span></span> <span data-ttu-id="bcbdc-120">Die Ausgabe ist unabhängig vom Wert dieser Eigenschaft verlustfrei.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-120">The output is lossless regardless of the value of this property.</span></span>

<span data-ttu-id="bcbdc-121">Wenn Sie für diese Eigenschaft den Standardwert **Variant \_ false** belassen, verwendet der Encoder seinen Standard Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-121">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder uses its default algorithm.</span></span> <span data-ttu-id="bcbdc-122">Der Standard Algorithmus hängt davon ab, welchen Encoder Sie verwenden und welche Version von Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-122">The default algorithm depends on which encoder you are using and which version of Windows is running.</span></span> <span data-ttu-id="bcbdc-123">In der folgenden Tabelle wird das Standardverhalten für die verschiedenen Kombinationen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-123">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="bcbdc-124">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="bcbdc-124">Operating system</span></span> | <span data-ttu-id="bcbdc-125">Standardverhalten</span><span class="sxs-lookup"><span data-stu-id="bcbdc-125">Default behavior</span></span>                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbdc-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcbdc-126">Windows Vista</span></span>    | <span data-ttu-id="bcbdc-127">Die Windows Media Audio 10, Windows Media Audio 10 Professional und die Windows Media Audio 10 Verlust lose Encoder verwenden standardmäßig den komplexesten Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-127">The Windows Media Audio 10, Windows Media Audio 10 Professional, and Windows Media Audio 10 Lossless encoders all use the most complex algorithm by default.</span></span>                                                    |
| <span data-ttu-id="bcbdc-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bcbdc-128">Windows 7</span></span>        | <span data-ttu-id="bcbdc-129">Die Windows Media Audio 10-und Windows Media Audio 10 Professional Encoder verwenden standardmäßig den komplexesten Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-129">The Windows Media Audio 10 and Windows Media Audio 10 Professional encoders use the most complex algorithm by default.</span></span> <span data-ttu-id="bcbdc-130">Der Windows Media Audio 10-Encoder ohne Verlust verwendet standardmäßig den am wenigsten komplexen Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-130">The Windows Media Audio 10 Lossless encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="bcbdc-131">Wenn die Eigenschaft [**mfpkey \_ einschränationskomplexität**](mfpkey-constrainenccomplexityproperty.md) den Wert **Variant \_ false** aufweist, ignoriert der Encoder diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bcbdc-131">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_FALSE**, the encoder ignores this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcbdc-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bcbdc-132">Requirements</span></span>



| <span data-ttu-id="bcbdc-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bcbdc-133">Requirement</span></span> | <span data-ttu-id="bcbdc-134">Wert</span><span class="sxs-lookup"><span data-stu-id="bcbdc-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbdc-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bcbdc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bcbdc-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bcbdc-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bcbdc-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bcbdc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bcbdc-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bcbdc-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bcbdc-139">Header</span><span class="sxs-lookup"><span data-stu-id="bcbdc-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcbdc-140"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcbdc-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcbdc-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcbdc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbdc-142">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bcbdc-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
