---
description: Gibt an, ob ein Algorithmus verwendet werden soll, der ein Video mit höherer Qualität oder einen schnelleren Algorithmus erzeugt.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: MFPKEY_RESIZE_QUALITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79ae1cac78b4d836261905afdacaf14fc227fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360194"
---
# <a name="mfpkey_resize_quality-property"></a><span data-ttu-id="26ebc-103">Eigenschaft "mfpkey \_ Resize \_ Quality"</span><span class="sxs-lookup"><span data-stu-id="26ebc-103">MFPKEY\_RESIZE\_QUALITY Property</span></span>

<span data-ttu-id="26ebc-104">Gibt an, ob ein Algorithmus verwendet werden soll, der ein Video mit höherer Qualität oder einen schnelleren Algorithmus erzeugt.</span><span class="sxs-lookup"><span data-stu-id="26ebc-104">Specifies whether to use an algorithm that produces higher-quality video, or a faster algorithm.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="26ebc-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="26ebc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="26ebc-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26ebc-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="26ebc-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="26ebc-107">Data Type</span></span>

<span data-ttu-id="26ebc-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="26ebc-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="26ebc-109">Gilt für</span><span class="sxs-lookup"><span data-stu-id="26ebc-109">Applies To</span></span>

-   [<span data-ttu-id="26ebc-110">Video Resizer DSP</span><span class="sxs-lookup"><span data-stu-id="26ebc-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="26ebc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26ebc-111">Remarks</span></span>

<span data-ttu-id="26ebc-112">Verwenden Sie einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="26ebc-112">Use one of the following values:</span></span>



| <span data-ttu-id="26ebc-113">Wert</span><span class="sxs-lookup"><span data-stu-id="26ebc-113">Value</span></span>     | <span data-ttu-id="26ebc-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26ebc-114">Description</span></span>          |
|-----------|----------------------|
| <span data-ttu-id="26ebc-115">VT \_ false</span><span class="sxs-lookup"><span data-stu-id="26ebc-115">VT\_FALSE</span></span> | <span data-ttu-id="26ebc-116">Schnellerer Algorithmus</span><span class="sxs-lookup"><span data-stu-id="26ebc-116">Faster algorithm</span></span>     |
| <span data-ttu-id="26ebc-117">VT \_ true</span><span class="sxs-lookup"><span data-stu-id="26ebc-117">VT\_TRUE</span></span>  | <span data-ttu-id="26ebc-118">Video mit höherer Qualität</span><span class="sxs-lookup"><span data-stu-id="26ebc-118">Higher-quality video</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="26ebc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26ebc-119">Requirements</span></span>



| <span data-ttu-id="26ebc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26ebc-120">Requirement</span></span> | <span data-ttu-id="26ebc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="26ebc-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26ebc-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26ebc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="26ebc-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26ebc-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="26ebc-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26ebc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="26ebc-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26ebc-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26ebc-126">Header</span><span class="sxs-lookup"><span data-stu-id="26ebc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="26ebc-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="26ebc-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ebc-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26ebc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ebc-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26ebc-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
