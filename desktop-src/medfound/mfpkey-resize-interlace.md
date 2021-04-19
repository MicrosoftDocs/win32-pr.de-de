---
description: Gibt an, ob der Eingabedaten Strom mit Zeilen Sprung verknüpft ist.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: MFPKEY_RESIZE_INTERLACE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a27504bd6da92bc48fee04afc999568a514fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356903"
---
# <a name="mfpkey_resize_interlace-property"></a><span data-ttu-id="710e2-103">Mfpkey \_ Resize \_ Interlace-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="710e2-103">MFPKEY\_RESIZE\_INTERLACE Property</span></span>

<span data-ttu-id="710e2-104">Gibt an, ob der Eingabedaten Strom mit Zeilen Sprung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="710e2-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="710e2-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="710e2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="710e2-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="710e2-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="710e2-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="710e2-107">Data Type</span></span>

<span data-ttu-id="710e2-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="710e2-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="710e2-109">Gilt für</span><span class="sxs-lookup"><span data-stu-id="710e2-109">Applies To</span></span>

-   [<span data-ttu-id="710e2-110">Video Resizer DSP</span><span class="sxs-lookup"><span data-stu-id="710e2-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="710e2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="710e2-111">Remarks</span></span>

<span data-ttu-id="710e2-112">Verwenden Sie einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="710e2-112">Use one of the following values:</span></span>



| <span data-ttu-id="710e2-113">Wert</span><span class="sxs-lookup"><span data-stu-id="710e2-113">Value</span></span>     | <span data-ttu-id="710e2-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="710e2-114">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="710e2-115">VT \_ false</span><span class="sxs-lookup"><span data-stu-id="710e2-115">VT\_FALSE</span></span> | <span data-ttu-id="710e2-116">progressiv</span><span class="sxs-lookup"><span data-stu-id="710e2-116">Progressive</span></span> |
| <span data-ttu-id="710e2-117">VT \_ true</span><span class="sxs-lookup"><span data-stu-id="710e2-117">VT\_TRUE</span></span>  | <span data-ttu-id="710e2-118">Interlaced</span><span class="sxs-lookup"><span data-stu-id="710e2-118">Interlaced</span></span>  |



 

<span data-ttu-id="710e2-119">Wenn diese Eigenschaft nicht festgelegt ist, verwendet der DSP den Eingabe Medientyp, um zu bestimmen, ob das Video mit Zeilen Sprung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="710e2-119">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="710e2-120">Sie können diese Eigenschaft festlegen, um die Medientyp Einstellung außer Kraft zu setzen.</span><span class="sxs-lookup"><span data-stu-id="710e2-120">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="710e2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="710e2-121">Requirements</span></span>



| <span data-ttu-id="710e2-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="710e2-122">Requirement</span></span> | <span data-ttu-id="710e2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="710e2-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="710e2-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="710e2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="710e2-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="710e2-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="710e2-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="710e2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="710e2-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="710e2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="710e2-128">Header</span><span class="sxs-lookup"><span data-stu-id="710e2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="710e2-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="710e2-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="710e2-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="710e2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="710e2-131">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="710e2-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
