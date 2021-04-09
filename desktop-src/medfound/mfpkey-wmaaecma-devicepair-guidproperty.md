---
description: Gibt die Kombination der Audiogeräte an, die von der Anwendung zurzeit mit dem sprach Erfassungs-DSP verwendet werden.
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: MFPKEY_WMAAECMA_DEVICEPAIR_GUID-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a586d7d31f29b20eb7ca39320d5fa57b9943715a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130545"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a><span data-ttu-id="76101-103">Mfpkey \_ wmaaecma \_ devicepair \_ GUID-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="76101-103">MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID Property</span></span>

<span data-ttu-id="76101-104">Gibt die Kombination der Audiogeräte an, die von der Anwendung zurzeit mit dem sprach Erfassungs-DSP verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76101-104">Identifies the combination of audio devices that the application is currently using with the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="76101-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="76101-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="76101-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76101-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="76101-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="76101-107">Data Type</span></span>

<span data-ttu-id="76101-108">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="76101-108">VT\_CLSID</span></span>

## <a name="applies-to"></a><span data-ttu-id="76101-109">Gilt für</span><span class="sxs-lookup"><span data-stu-id="76101-109">Applies To</span></span>

-   [<span data-ttu-id="76101-110">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="76101-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="76101-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76101-111">Remarks</span></span>

<span data-ttu-id="76101-112">Legen Sie diese Eigenschaft fest, wenn Sie den DSP im Filter Modus verwenden und der Wert der Eigenschaft [mfpkey \_ wmaaecma \_ Abruf \_ TS \_ Stats](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) auf Variant true festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="76101-112">Set this property if you are using the DSP in filter mode and the value of the [MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE.</span></span>

<span data-ttu-id="76101-113">Wenn die Eigenschaft " [**mfpkey \_ wmaaecma \_ Abruf von \_ TS \_ Stats**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) " Variant \_ true ist, sammelt der DSP Statistiken zu den Zeitstempeln von den Audiogeräten und speichert diese Informationen in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="76101-113">When the [**MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE, the DSP collects statistics about the time stamps from the audio devices and stores this information in the registry.</span></span> <span data-ttu-id="76101-114">Diese Statistiken können für jede Kombination aus audioerfassungs-und audiorendering-Gerät geändert werden.</span><span class="sxs-lookup"><span data-stu-id="76101-114">These statistics can change for each combination of audio capture device and audio rendering device.</span></span> <span data-ttu-id="76101-115">Daher muss die Anwendung eine GUID zuweisen, um die jeweilige Kombination von verwendeten Geräten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="76101-115">Therefore, the application must assign a GUID to identify the particular combination of devices in use.</span></span> <span data-ttu-id="76101-116">Die Anwendung sollte diese GUID nachverfolgen, sodass Sie dieselbe GUID zuweisen kann, wenn Sie dasselbe paar von Audiogeräten verwendet.</span><span class="sxs-lookup"><span data-stu-id="76101-116">The application should keep track of this GUID, so that it can assign the same GUID whenever it uses the same pair of audio devices.</span></span>

<span data-ttu-id="76101-117">Wenn Sie den DSP im Quell Modus verwenden, müssen Sie diese Eigenschaft nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="76101-117">If you are using the DSP in source mode, you do not need to set this property.</span></span> <span data-ttu-id="76101-118">Der DSP generiert automatisch eine GUID basierend auf dem Wert der Eigenschaft [mfpkey \_ wmaaecma- \_ Geräte \_ Indizes](mfpkey-wmaaecma-device-indexesproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="76101-118">The DSP automatically generates a GUID based on the value of the [MFPKEY\_WMAAECMA\_DEVICE\_INDEXES](mfpkey-wmaaecma-device-indexesproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="76101-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76101-119">Requirements</span></span>



| <span data-ttu-id="76101-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76101-120">Requirement</span></span> | <span data-ttu-id="76101-121">Wert</span><span class="sxs-lookup"><span data-stu-id="76101-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76101-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76101-122">Minimum supported client</span></span><br/> | <span data-ttu-id="76101-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76101-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="76101-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76101-124">Minimum supported server</span></span><br/> | <span data-ttu-id="76101-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76101-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76101-126">Header</span><span class="sxs-lookup"><span data-stu-id="76101-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="76101-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="76101-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76101-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76101-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76101-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76101-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="76101-130">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="76101-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
