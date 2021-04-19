---
description: Gilt für Windows Vista und höher.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc-Eigenschaft (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c26763d32513652a08d38b52bf6fb745d3d321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371651"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="3175a-103">\_Ate \_ rementontimedisc (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3175a-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="3175a-104">Gilt für Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="3175a-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="3175a-105">Diese Eigenschaft fragt ab, ob der Decoder die Ausgabezeit Stempel erneut mit den Eingabe Zeitstempeln synchronisiert, wenn der Decoder ein Beispiel mit dem Diskontinuität-Flag empfängt.</span><span class="sxs-lookup"><span data-stu-id="3175a-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="3175a-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3175a-106">This property is read/write.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="3175a-107">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="3175a-107">Property Set GUID</span></span> | <span data-ttu-id="3175a-108">AM \_ kspropltid \_</span><span class="sxs-lookup"><span data-stu-id="3175a-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="3175a-109">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="3175a-109">Property ID</span></span>       | <span data-ttu-id="3175a-110">\_Rate \_ rementimedisc</span><span class="sxs-lookup"><span data-stu-id="3175a-110">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="3175a-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3175a-111">Data Type</span></span>         | <span data-ttu-id="3175a-112">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="3175a-112">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="3175a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3175a-113">Remarks</span></span>

<span data-ttu-id="3175a-114">Diese Eigenschaft unterstützt Smooth-Rate-Änderungen.</span><span class="sxs-lookup"><span data-stu-id="3175a-114">This property supports smooth rate changes.</span></span> <span data-ttu-id="3175a-115">Wenn der Wert dieser Eigenschaft " **true** " ist und der Decoder ein Eingabe Beispiel mit dem "am \_ Sample \_ timediscontinuity"-Flag erhält, sollte der decodierte Frame denselben Zeitstempel wie der Eingabe Rahmen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3175a-115">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="3175a-116">Rufen Sie zum Abrufen des am \_ Sample Sample \_ timediscontinuity-Flags [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) für das Beispiel auf.</span><span class="sxs-lookup"><span data-stu-id="3175a-116">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="3175a-117">Das-Flag wird im **dwsampleflags** -Member der [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) -Struktur festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3175a-117">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="3175a-118">Weitere Informationen finden Sie unter [Verbesserungen der DVD-Wiedergabe in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="3175a-118">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3175a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3175a-119">Requirements</span></span>



| <span data-ttu-id="3175a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3175a-120">Requirement</span></span> | <span data-ttu-id="3175a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3175a-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3175a-122">Header</span><span class="sxs-lookup"><span data-stu-id="3175a-122">Header</span></span><br/> | <dl> <span data-ttu-id="3175a-123"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="3175a-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3175a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3175a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3175a-125">**Eigenschaften Satz für Raten Änderung**</span><span class="sxs-lookup"><span data-stu-id="3175a-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




