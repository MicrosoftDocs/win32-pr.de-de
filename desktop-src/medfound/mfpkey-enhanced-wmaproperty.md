---
description: Gibt an, ob der Kern Encoder den &\# 0034; Plus&\# 0034; Feature.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: MFPKEY_ENHANCED_WMA-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369290"
---
# <a name="mfpkey_enhanced_wma-property"></a><span data-ttu-id="60992-103">Mfpkey \_ Enhanced \_ WMA-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="60992-103">MFPKEY\_ENHANCED\_WMA Property</span></span>

<span data-ttu-id="60992-104">Gibt an, ob der Kern Encoder die Funktion "Plus" verwendet.</span><span class="sxs-lookup"><span data-stu-id="60992-104">Specifies whether the core encoder uses the "Plus" feature.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="60992-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="60992-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="60992-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60992-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="60992-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="60992-107">Data Type</span></span>

<span data-ttu-id="60992-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="60992-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="60992-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="60992-109">Default Value</span></span>

<span data-ttu-id="60992-110">0</span><span class="sxs-lookup"><span data-stu-id="60992-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="60992-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60992-111">Remarks</span></span>

<span data-ttu-id="60992-112">Diese Eigenschaft ist nur für Windows Media Audio Verlust lose verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60992-112">This property is available only for Windows Media Audio Lossless.</span></span>

<span data-ttu-id="60992-113">Wenn Sie für diese Eigenschaft den Standardwert 0 (null) belassen, oder wenn Sie den Wert auf 1 festlegen, entscheidet der Kern Encoder, ob der "Plus"-Teil verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="60992-113">If you leave this property at its default value of 0, or if you set it to 1, the core encoder decides whether the "Plus" portion should be used.</span></span> <span data-ttu-id="60992-114">Wenn Sie diese Eigenschaft auf 2 festlegen, wird das Feature "Plus" vom Kern Encoder nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60992-114">If you set this property to 2, the core encoder does not use the "Plus" feature.</span></span>

<span data-ttu-id="60992-115">Diese Eigenschaft ändert die aufgelisteten Medientypen. Wenn Sie Sie also festlegen, müssen Sie dies tun, bevor Sie den Ausgabetyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="60992-115">This property alters the enumerated media types, so if you set it, you must do so before you set the output type.</span></span>

## <a name="requirements"></a><span data-ttu-id="60992-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60992-116">Requirements</span></span>



| <span data-ttu-id="60992-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60992-117">Requirement</span></span> | <span data-ttu-id="60992-118">Wert</span><span class="sxs-lookup"><span data-stu-id="60992-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60992-119">Client</span><span class="sxs-lookup"><span data-stu-id="60992-119">Client</span></span><br/> | <span data-ttu-id="60992-120">Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="60992-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="60992-121">Header</span><span class="sxs-lookup"><span data-stu-id="60992-121">Header</span></span><br/> | <dl> <span data-ttu-id="60992-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="60992-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60992-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60992-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60992-124">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="60992-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
