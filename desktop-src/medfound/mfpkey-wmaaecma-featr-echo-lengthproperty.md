---
description: Gibt die Dauer von Echo an, die der AEC-Algorithmus (Akustik Echo Abbruch) in Millisekunden verarbeiten kann.
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d66f7dcc4764447495e0f3ae55d2d038c2a8d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348855"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a><span data-ttu-id="dfb02-103">Mfpkey \_ wmaaecma \_ featr- \_ Echo \_ Länge (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dfb02-103">MFPKEY\_WMAAECMA\_FEATR\_ECHO\_LENGTH Property</span></span>

<span data-ttu-id="dfb02-104">Gibt die Dauer von Echo an, die der AEC-Algorithmus (Akustik Echo Abbruch) in Millisekunden verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="dfb02-104">Specifies the duration of echo that the acoustic echo cancellation (AEC) algorithm can handle, in milliseconds.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="dfb02-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="dfb02-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="dfb02-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dfb02-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="dfb02-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="dfb02-107">Data Type</span></span>

<span data-ttu-id="dfb02-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="dfb02-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="dfb02-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="dfb02-109">Default Value</span></span>

<span data-ttu-id="dfb02-110">256</span><span class="sxs-lookup"><span data-stu-id="dfb02-110">256</span></span>

## <a name="applies-to"></a><span data-ttu-id="dfb02-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="dfb02-111">Applies To</span></span>

-   [<span data-ttu-id="dfb02-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="dfb02-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="dfb02-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfb02-113">Remarks</span></span>

<span data-ttu-id="dfb02-114">Der AEC-Algorithmus verwendet einen adaptiven Filter, dessen Länge durch die Dauer des Echo bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="dfb02-114">The AEC algorithm uses an adaptive filter whose length is determined by the duration of the echo.</span></span> <span data-ttu-id="dfb02-115">Es wird empfohlen, dass Anwendungen einen der folgenden Werte verwenden:</span><span class="sxs-lookup"><span data-stu-id="dfb02-115">It is recommended that applications use one of the following values:</span></span>

-   <span data-ttu-id="dfb02-116">128</span><span class="sxs-lookup"><span data-stu-id="dfb02-116">128</span></span>
-   <span data-ttu-id="dfb02-117">256</span><span class="sxs-lookup"><span data-stu-id="dfb02-117">256</span></span>
-   <span data-ttu-id="dfb02-118">512</span><span class="sxs-lookup"><span data-stu-id="dfb02-118">512</span></span>
-   <span data-ttu-id="dfb02-119">1024</span><span class="sxs-lookup"><span data-stu-id="dfb02-119">1024</span></span>

<span data-ttu-id="dfb02-120">Der Standardwert beträgt 256 Millisekunden. dieser Wert ist für die meisten Office-und Heim Umgebungen ausreichend.</span><span class="sxs-lookup"><span data-stu-id="dfb02-120">The default value is 256 milliseconds, which is sufficient for most office and home environments.</span></span> <span data-ttu-id="dfb02-121">Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="dfb02-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="dfb02-122">Der DSP verwendet diese Eigenschaft nur, wenn die AEC-Verarbeitung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dfb02-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb02-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfb02-123">Requirements</span></span>



| <span data-ttu-id="dfb02-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfb02-124">Requirement</span></span> | <span data-ttu-id="dfb02-125">Wert</span><span class="sxs-lookup"><span data-stu-id="dfb02-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb02-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dfb02-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dfb02-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfb02-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dfb02-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dfb02-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dfb02-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfb02-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dfb02-130">Header</span><span class="sxs-lookup"><span data-stu-id="dfb02-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfb02-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfb02-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfb02-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfb02-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb02-133">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dfb02-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="dfb02-134">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="dfb02-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
