---
description: Gibt die bevorzugte Anzahl von Stichproben pro Frame an.
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: MFPKEY_PREFERRED_FRAMESIZE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362136"
---
# <a name="mfpkey_preferred_framesize-property"></a><span data-ttu-id="eee41-103">Von mfpkey \_ bevorzugte \_ frameSize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eee41-103">MFPKEY\_PREFERRED\_FRAMESIZE Property</span></span>

<span data-ttu-id="eee41-104">Gibt die bevorzugte Anzahl von Stichproben pro Frame an.</span><span class="sxs-lookup"><span data-stu-id="eee41-104">Specifies the preferred number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="eee41-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="eee41-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="eee41-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eee41-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="eee41-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="eee41-107">Data Type</span></span>

<span data-ttu-id="eee41-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="eee41-108">**VT\_UI4**</span></span>

## <a name="remarks"></a><span data-ttu-id="eee41-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eee41-109">Remarks</span></span>

<span data-ttu-id="eee41-110">Um eine bevorzugte Frame Größe festzulegen, legen Sie die folgenden Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="eee41-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="eee41-111">Legen Sie [**mfpkey fest, um \_ \_ einen \_ frameSize**](mfpkey-requesting-a-framesizeproperty.md) -Wert auf **Variant \_ true** anzufordern.</span><span class="sxs-lookup"><span data-stu-id="eee41-111">Set [**MFPKEY\_REQUESTING\_A\_FRAMESIZE**](mfpkey-requesting-a-framesizeproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="eee41-112">Legen Sie die **\_ gewünschte \_ frameSize von mfpkey** auf die gewünschte Anzahl von Stichproben in jedem Frame fest.</span><span class="sxs-lookup"><span data-stu-id="eee41-112">Set **MFPKEY\_PREFERRED\_FRAMESIZE** to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="eee41-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eee41-113">Requirements</span></span>



| <span data-ttu-id="eee41-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eee41-114">Requirement</span></span> | <span data-ttu-id="eee41-115">Wert</span><span class="sxs-lookup"><span data-stu-id="eee41-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eee41-116">Client</span><span class="sxs-lookup"><span data-stu-id="eee41-116">Client</span></span><br/> | <span data-ttu-id="eee41-117">Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="eee41-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="eee41-118">Header</span><span class="sxs-lookup"><span data-stu-id="eee41-118">Header</span></span><br/> | <dl> <span data-ttu-id="eee41-119"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eee41-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eee41-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eee41-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eee41-121">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eee41-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
