---
description: Gibt die maximale Zeit (in Millisekunden) zwischen Keyframes in der Codec-Ausgabe an.
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: MFPKEY_KEYDIST-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55925811db71f24cf360113aa6d03a325bcdc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864152"
---
# <a name="mfpkey_keydist-property"></a><span data-ttu-id="f5bfa-103">Mfpkey \_ keydist (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f5bfa-103">MFPKEY\_KEYDIST Property</span></span>

<span data-ttu-id="f5bfa-104">Gibt die maximale Zeit (in Millisekunden) zwischen Keyframes in der Codec-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-104">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f5bfa-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f5bfa-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f5bfa-106">g \_ wszwmvckeyframedistance</span><span class="sxs-lookup"><span data-stu-id="f5bfa-106">g\_wszWMVCKeyframeDistance</span></span>

## <a name="data-type"></a><span data-ttu-id="f5bfa-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f5bfa-107">Data Type</span></span>

<span data-ttu-id="f5bfa-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f5bfa-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="f5bfa-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="f5bfa-109">Default Value</span></span>

<span data-ttu-id="f5bfa-110">Der Standardwert hängt davon ab, welche Version von Windows ausgeführt wird, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-110">The default value depends on which version of Windows is running, as shown in the following table.</span></span>



| <span data-ttu-id="f5bfa-111">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="f5bfa-111">Operating system</span></span> | <span data-ttu-id="f5bfa-112">Standardwert</span><span class="sxs-lookup"><span data-stu-id="f5bfa-112">Default value</span></span> |
|------------------|---------------|
| <span data-ttu-id="f5bfa-113">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5bfa-113">Windows XP</span></span>       | <span data-ttu-id="f5bfa-114">8.000</span><span class="sxs-lookup"><span data-stu-id="f5bfa-114">8000</span></span>          |
| <span data-ttu-id="f5bfa-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5bfa-115">Windows Vista</span></span>    | <span data-ttu-id="f5bfa-116">8.000</span><span class="sxs-lookup"><span data-stu-id="f5bfa-116">8000</span></span>          |
| <span data-ttu-id="f5bfa-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f5bfa-117">Windows 7</span></span>        | <span data-ttu-id="f5bfa-118">2000</span><span class="sxs-lookup"><span data-stu-id="f5bfa-118">2000</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="f5bfa-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5bfa-119">Remarks</span></span>

<span data-ttu-id="f5bfa-120">Die interne Logik des Codecs bestimmt den tatsächlichen Speicherort der einzelnen Keyframes.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-120">The internal logic of the codec determines the actual location of each key frame.</span></span> <span data-ttu-id="f5bfa-121">Der Abstand zwischen zwei Keyframes kann kleiner sein als der Wert dieser Eigenschaft, er ist jedoch nie größer.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-121">The distance between any two key frames may be less than the value of this property, however, it will never be greater.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5bfa-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5bfa-122">Requirements</span></span>



| <span data-ttu-id="f5bfa-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5bfa-123">Requirement</span></span> | <span data-ttu-id="f5bfa-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f5bfa-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5bfa-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5bfa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f5bfa-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5bfa-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f5bfa-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5bfa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f5bfa-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5bfa-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5bfa-129">Header</span><span class="sxs-lookup"><span data-stu-id="f5bfa-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5bfa-130"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5bfa-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5bfa-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5bfa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5bfa-132">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5bfa-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




