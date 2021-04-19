---
description: Gibt an, ob der Encoder eine bevorzugte Frame Größe in der Anzahl von Stichproben pro Frame verwenden soll.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: MFPKEY_REQUESTING_A_FRAMESIZE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370946"
---
# <a name="mfpkey_requesting_a_framesize-property"></a><span data-ttu-id="4eb5d-103">Mfpkey- \_ Anforderung \_ einer \_ frameSize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4eb5d-103">MFPKEY\_REQUESTING\_A\_FRAMESIZE Property</span></span>

<span data-ttu-id="4eb5d-104">Gibt an, ob der Encoder eine bevorzugte Frame Größe in der Anzahl von Stichproben pro Frame verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="4eb5d-104">Specifies whether the encoder should use a preferred frame size given in number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4eb5d-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="4eb5d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4eb5d-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4eb5d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="4eb5d-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4eb5d-107">Data Type</span></span>

<span data-ttu-id="4eb5d-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="4eb5d-108">**VT\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb5d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4eb5d-109">Remarks</span></span>

<span data-ttu-id="4eb5d-110">Um eine bevorzugte Frame Größe festzulegen, legen Sie die folgenden Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="4eb5d-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="4eb5d-111">Legen Sie **mfpkey fest, um \_ \_ einen \_ frameSize** -Wert auf Variant \_ true anzufordern.</span><span class="sxs-lookup"><span data-stu-id="4eb5d-111">Set **MFPKEY\_REQUESTING\_A\_FRAMESIZE** to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="4eb5d-112">Legen Sie die [**\_ gewünschte \_ frameSize von mfpkey**](mfpkey-preferred-framesizeproperty.md) auf die gewünschte Anzahl von Stichproben in jedem Frame fest.</span><span class="sxs-lookup"><span data-stu-id="4eb5d-112">Set [**MFPKEY\_PREFERRED\_FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb5d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4eb5d-113">Requirements</span></span>



| <span data-ttu-id="4eb5d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4eb5d-114">Requirement</span></span> | <span data-ttu-id="4eb5d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4eb5d-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb5d-116">Client</span><span class="sxs-lookup"><span data-stu-id="4eb5d-116">Client</span></span><br/> | <span data-ttu-id="4eb5d-117">Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="4eb5d-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="4eb5d-118">Header</span><span class="sxs-lookup"><span data-stu-id="4eb5d-118">Header</span></span><br/> | <dl> <span data-ttu-id="4eb5d-119"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eb5d-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eb5d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4eb5d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb5d-121">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4eb5d-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
