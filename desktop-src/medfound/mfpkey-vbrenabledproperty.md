---
description: Gibt an, ob der Encoder die VBR-Codierung (Variable Bitrate) verwendet.
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: MFPKEY_VBRENABLED-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864128"
---
# <a name="mfpkey_vbrenabled-property"></a><span data-ttu-id="7182c-103">Mfpkey \_ vbrenabled (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7182c-103">MFPKEY\_VBRENABLED Property</span></span>

<span data-ttu-id="7182c-104">Gibt an, ob der Encoder die VBR-Codierung (Variable Bitrate) verwendet.</span><span class="sxs-lookup"><span data-stu-id="7182c-104">Specifies whether the encoder uses variable-bit-rate (VBR) encoding.</span></span> <span data-ttu-id="7182c-105">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7182c-105">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7182c-106">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7182c-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="7182c-107">**g \_ wszwmvcvbrenabled**, **g \_ wszwmcpaudiovbrsupported**</span><span class="sxs-lookup"><span data-stu-id="7182c-107">**g\_wszWMVCVBREnabled**, **g\_wszWMCPAudioVBRSupported**</span></span>

## <a name="data-type"></a><span data-ttu-id="7182c-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7182c-108">Data Type</span></span>

<span data-ttu-id="7182c-109">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="7182c-109">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="7182c-110">Standardwert</span><span class="sxs-lookup"><span data-stu-id="7182c-110">Default Value</span></span>

<span data-ttu-id="7182c-111">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="7182c-111">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="7182c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7182c-112">Remarks</span></span>

<span data-ttu-id="7182c-113">Dieser Wert muss für alle anderen VBR-Eigenschaften, die vom Codec verwendet werden sollen, auf **Variant \_ true** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7182c-113">This value must be set to **VARIANT\_TRUE** for any of the other VBR properties to be used by the codec.</span></span>

<span data-ttu-id="7182c-114">Nachdem Sie diesen Wert für den Audioencoder auf **Variant \_ true** festgelegt haben, sind die mithilfe der [**imediaobject:: getoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) -Methode abgerufenen Ausgabetypen VBR-Typen.</span><span class="sxs-lookup"><span data-stu-id="7182c-114">After you set this value to **VARIANT\_TRUE** on the audio encoder, the output types retrieved by using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) method are VBR types.</span></span>

## <a name="requirements"></a><span data-ttu-id="7182c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7182c-115">Requirements</span></span>



| <span data-ttu-id="7182c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7182c-116">Requirement</span></span> | <span data-ttu-id="7182c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7182c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7182c-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7182c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7182c-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7182c-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7182c-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7182c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7182c-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7182c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7182c-122">Header</span><span class="sxs-lookup"><span data-stu-id="7182c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7182c-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7182c-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7182c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7182c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7182c-125">**mfpkey \_ schränkt die \_ Enumeration von \_ vbrquality ein**</span><span class="sxs-lookup"><span data-stu-id="7182c-125">**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**</span></span>](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="7182c-126">**mfpkey \_ gewünschte \_ vbrquality**</span><span class="sxs-lookup"><span data-stu-id="7182c-126">**MFPKEY\_DESIRED\_VBRQUALITY**</span></span>](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="7182c-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7182c-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
