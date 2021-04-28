---
description: 'MFPKEY_RESIZE_INTERLACE-Eigenschaft: Gibt an, ob der Eingabestream interlaced ist.'
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: MFPKEY_RESIZE_INTERLACE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d0efe93901a08322a05dbed2515f76b04a214b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092878"
---
# <a name="mfpkey_resize_interlace-property"></a><span data-ttu-id="f041f-103">MFPKEY \_ RESIZE \_ INTERLACE-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f041f-103">MFPKEY\_RESIZE\_INTERLACE Property</span></span>

<span data-ttu-id="f041f-104">Gibt an, ob der Eingabestream als Interlacing verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f041f-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f041f-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f041f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f041f-106">Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)</span><span class="sxs-lookup"><span data-stu-id="f041f-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f041f-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f041f-107">Data Type</span></span>

<span data-ttu-id="f041f-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="f041f-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="f041f-109">Gilt für</span><span class="sxs-lookup"><span data-stu-id="f041f-109">Applies To</span></span>

-   [<span data-ttu-id="f041f-110">Video Resizer DSP</span><span class="sxs-lookup"><span data-stu-id="f041f-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="f041f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f041f-111">Remarks</span></span>

<span data-ttu-id="f041f-112">Verwenden Sie einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="f041f-112">Use one of the following values:</span></span>



| <span data-ttu-id="f041f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f041f-113">Value</span></span>     | <span data-ttu-id="f041f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f041f-114">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="f041f-115">VT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="f041f-115">VT\_FALSE</span></span> | <span data-ttu-id="f041f-116">progressiv</span><span class="sxs-lookup"><span data-stu-id="f041f-116">Progressive</span></span> |
| <span data-ttu-id="f041f-117">VT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="f041f-117">VT\_TRUE</span></span>  | <span data-ttu-id="f041f-118">Interlaced</span><span class="sxs-lookup"><span data-stu-id="f041f-118">Interlaced</span></span>  |



 

<span data-ttu-id="f041f-119">Wenn diese Eigenschaft nicht festgelegt ist, verwendet der DSP den Eingabemedientyp, um zu bestimmen, ob das Video interlaced ist.</span><span class="sxs-lookup"><span data-stu-id="f041f-119">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="f041f-120">Sie können diese Eigenschaft festlegen, um die Medientypeinstellung zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="f041f-120">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="f041f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f041f-121">Requirements</span></span>



| <span data-ttu-id="f041f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f041f-122">Requirement</span></span> | <span data-ttu-id="f041f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f041f-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f041f-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f041f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f041f-125">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f041f-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f041f-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f041f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f041f-127">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f041f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f041f-128">Header</span><span class="sxs-lookup"><span data-stu-id="f041f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f041f-129"><dt>Wmcodecdsp.h</dt></span><span class="sxs-lookup"><span data-stu-id="f041f-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f041f-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f041f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f041f-131">Media Foundation Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f041f-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
