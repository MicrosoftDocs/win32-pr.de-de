---
description: Gilt für Windows Vista und höher.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d465329c2c8de1a66f04a830d183b8cba88c0728
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910248"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="94984-103">AM \_ RATE \_ ResetOnTimeDisc-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="94984-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="94984-104">Gilt für Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="94984-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="94984-105">Diese Eigenschaft fragt ab, ob der Decoder die Ausgabezeitstempel erneut mit den Eingabezeitstempeln synchronisiert, wenn der Decoder ein Beispiel mit dem Diskontinuitätsflag empfängt.</span><span class="sxs-lookup"><span data-stu-id="94984-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="94984-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="94984-106">This property is read/write.</span></span>



| <span data-ttu-id="94984-107">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="94984-107">Label</span></span> | <span data-ttu-id="94984-108">Wert</span><span class="sxs-lookup"><span data-stu-id="94984-108">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="94984-109">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="94984-109">Property Set GUID</span></span> | <span data-ttu-id="94984-110">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="94984-110">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="94984-111">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="94984-111">Property ID</span></span>       | <span data-ttu-id="94984-112">AM \_ RATE \_ ResetOnTimeDisc</span><span class="sxs-lookup"><span data-stu-id="94984-112">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="94984-113">Datentyp</span><span class="sxs-lookup"><span data-stu-id="94984-113">Data Type</span></span>         | <span data-ttu-id="94984-114">**Dword**</span><span class="sxs-lookup"><span data-stu-id="94984-114">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="94984-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94984-115">Remarks</span></span>

<span data-ttu-id="94984-116">Diese Eigenschaft unterstützt Smooth Rate-Änderungen.</span><span class="sxs-lookup"><span data-stu-id="94984-116">This property supports smooth rate changes.</span></span> <span data-ttu-id="94984-117">Wenn der Wert dieser Eigenschaft **TRUE** ist und der Decoder ein Eingabebeispiel mit dem \_ AM SAMPLE \_ TIMEDISCONTINUITY-Flag empfängt, sollte der decodierte Frame den gleichen Zeitstempel wie der Eingaberahmen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="94984-117">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="94984-118">Um das AM \_ SAMPLE \_ TIMEDISCONTINUITY-Flag abzurufen, rufen [**Sie IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) für das Beispiel auf.</span><span class="sxs-lookup"><span data-stu-id="94984-118">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="94984-119">Das Flag wird im **dwSampleFlags-Member** der [**AM \_ SAMPLE2 \_ PROPERTIES-Struktur**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="94984-119">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="94984-120">Weitere Informationen finden Sie unter [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="94984-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94984-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94984-121">Requirements</span></span>



| <span data-ttu-id="94984-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94984-122">Requirement</span></span> | <span data-ttu-id="94984-123">Wert</span><span class="sxs-lookup"><span data-stu-id="94984-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94984-124">Header</span><span class="sxs-lookup"><span data-stu-id="94984-124">Header</span></span><br/> | <dl> <span data-ttu-id="94984-125"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="94984-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94984-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94984-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94984-127">**Ratenänderungseigenschaftensatz**</span><span class="sxs-lookup"><span data-stu-id="94984-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




