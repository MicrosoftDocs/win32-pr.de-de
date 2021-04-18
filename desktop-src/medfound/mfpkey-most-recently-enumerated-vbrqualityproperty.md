---
description: Gibt die VBR-Qualitätsstufe des zuletzt aufgezählten Ausgabe Typs an.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd3b5f3aae6dc5347672cf6697c3431163dcbd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352122"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a><span data-ttu-id="5eacc-103">\_ \_ Aktuell \_ aufgelistete \_ vbrquality-Eigenschaft für mfpkey</span><span class="sxs-lookup"><span data-stu-id="5eacc-103">MFPKEY\_MOST\_RECENT\_ENUMERATED\_VBRQUALITY Property</span></span>

<span data-ttu-id="5eacc-104">Gibt die VBR-Qualitätsstufe des zuletzt aufgezählten Ausgabe Typs an.</span><span class="sxs-lookup"><span data-stu-id="5eacc-104">Specifies the VBR quality level of the most recently enumerated output type.</span></span> <span data-ttu-id="5eacc-105">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5eacc-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5eacc-106">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5eacc-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="5eacc-107">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5eacc-107">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="5eacc-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5eacc-108">Data Type</span></span>

<span data-ttu-id="5eacc-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="5eacc-109">**VT\_UI4**</span></span>

## <a name="remarks"></a><span data-ttu-id="5eacc-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5eacc-110">Remarks</span></span>

<span data-ttu-id="5eacc-111">Wenn der Encoder als Media Foundation Transformation (MFT) fungiert und einen Ausgabetyp für einen [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)-Befehl auflistet, können Sie die MFT für die zuletzt **\_ \_ \_ aufgezählte \_ vbrquality-Eigenschaft von mfpkey** Abfragen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-111">When the encoder is acting as an Media Foundation Transform (MFT) and it enumerates an output type on a call to [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), you can query the MFT for the **MFPKEY\_MOST\_RECENTLY\_ENUMERATED\_VBRQUALITY** property.</span></span> <span data-ttu-id="5eacc-112">Der zurückgegebene Wert gibt die VBR-Qualität des zuletzt zurückgegebenen Ausgabemedien Typs an.</span><span class="sxs-lookup"><span data-stu-id="5eacc-112">The value returned indicates the VBR quality of the most recently returned output media type.</span></span> <span data-ttu-id="5eacc-113">Anschließend können Sie diesen Wert verwenden, um die [**\_ gewünschte \_ Eigenschaft "mfpkey**](mfpkey-desired-vbrqualityproperty.md) " des Encoders festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-113">Then you can use that value to set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property of the encoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eacc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5eacc-114">Requirements</span></span>



| <span data-ttu-id="5eacc-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5eacc-115">Requirement</span></span> | <span data-ttu-id="5eacc-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5eacc-116">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5eacc-117">Client</span><span class="sxs-lookup"><span data-stu-id="5eacc-117">Client</span></span><br/> | <span data-ttu-id="5eacc-118">Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="5eacc-118">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="5eacc-119">Header</span><span class="sxs-lookup"><span data-stu-id="5eacc-119">Header</span></span><br/> | <dl> <span data-ttu-id="5eacc-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eacc-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eacc-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5eacc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eacc-122">**mfpkey \_ vbrenabled**</span><span class="sxs-lookup"><span data-stu-id="5eacc-122">**MFPKEY\_VBRENABLED**</span></span>](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[<span data-ttu-id="5eacc-123">**mfpkey \_ schränkt die \_ Enumeration von \_ vbrquality ein**</span><span class="sxs-lookup"><span data-stu-id="5eacc-123">**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**</span></span>](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="5eacc-124">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5eacc-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
