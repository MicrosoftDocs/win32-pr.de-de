---
description: Wenn der DVD-Navigator-Filter in den Karaoke-Modus wechselt, wird der Audiodecoder über die Eigenschaft "am \_ Eigenschaft \_ dvdkaraoke enable" informiert \_ .
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: DVD-Karaoke-Eigenschaften Satz (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e9fe53ad35dac0c3c0f54a8e04a6fbe698fc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371002"
---
# <a name="dvd-karaoke-property-set"></a><span data-ttu-id="cc8bf-103">DVD-Karaoke-Eigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="cc8bf-103">DVD Karaoke Property Set</span></span>

<span data-ttu-id="cc8bf-104">Wenn der [DVD-Navigator](dvd-navigator-filter.md) -Filter in den Karaoke-Modus wechselt, wird der Audiodecoder über die Eigenschaft " **am \_ Eigenschaft \_ dvdkaraoke \_ enable** " informiert.</span><span class="sxs-lookup"><span data-stu-id="cc8bf-104">When the [DVD Navigator](dvd-navigator-filter.md) filter goes into karaoke mode, it informs the audio decoder through the **AM\_PROPERTY\_DVDKARAOKE\_ENABLE** property.</span></span> <span data-ttu-id="cc8bf-105">Der Decoder sollte dann die Audiokanäle 2 bis 5 stumm schalten, bis er vom DVD-Navigator eine **am \_ Eigenschaft \_ dvdkaraoke- \_ Daten** Eigenschaft mit einem Zeiger auf eine [**am \_ dvdkaraokedata**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) -Datenstruktur empfängt, die angibt, wie die zusätzlichen Kanäle gemischt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc8bf-105">The decoder should then mute audio channels 2 through 5 until it receives from the DVD Navigator an **AM\_PROPERTY\_DVDKARAOKE\_DATA** property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) data structure indicating how the auxiliary channels are to be mixed.</span></span>



|                   |                             |
|-------------------|-----------------------------|
| <span data-ttu-id="cc8bf-106">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="cc8bf-106">Property Set GUID</span></span> | <span data-ttu-id="cc8bf-107">AM \_ kspropabtid \_ dvdkaraoke</span><span class="sxs-lookup"><span data-stu-id="cc8bf-107">AM\_KSPROPSETID\_DvdKaraoke</span></span> |



 



| <span data-ttu-id="cc8bf-108">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="cc8bf-108">Property ID</span></span>                      | <span data-ttu-id="cc8bf-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc8bf-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8bf-110">AM- \_ Eigenschaft \_ dvdkaraoke \_ enable</span><span class="sxs-lookup"><span data-stu-id="cc8bf-110">AM\_PROPERTY\_DVDKARAOKE\_ENABLE</span></span> | <span data-ttu-id="cc8bf-111">Boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="cc8bf-111">BOOLEAN value.</span></span> <span data-ttu-id="cc8bf-112">Der DVD-Navigator sendet dem Decoder eine "am- \_ Eigenschaft \_ dvdkaraoke \_ enable" mit dem Wert " **true** ", um das Karaoke-downmischungs-und " **false** " zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cc8bf-112">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_ENABLE with a value of **TRUE** to enable karaoke downmixing or **FALSE** to disable it.</span></span>                                                                                                                                    |
| <span data-ttu-id="cc8bf-113">AM- \_ Eigenschaft \_ dvdkaraoke- \_ Daten</span><span class="sxs-lookup"><span data-stu-id="cc8bf-113">AM\_PROPERTY\_DVDKARAOKE\_DATA</span></span>   | <span data-ttu-id="cc8bf-114">Der DVD-Navigator sendet dem Decoder eine "am \_ Eigenschaft \_ dvdkaraoke"- \_ Dateneigenschaft mit einem Zeiger auf eine " [**am \_ dvdkaraokedata**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) "-Struktur, um die downmischungs Konfiguration zu ändern, d. h. um bestimmte Karaoke-Kanäle ein-oder auszuschalten und Sie an den rechten oder linken Ausgabekanal weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="cc8bf-114">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_DATA property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) structure to change the downmix configuration; that is, to turn certain karaoke channels on or off and direct them to the right or left output channel.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="cc8bf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc8bf-115">Requirements</span></span>



| <span data-ttu-id="cc8bf-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc8bf-116">Requirement</span></span> | <span data-ttu-id="cc8bf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cc8bf-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8bf-118">Header</span><span class="sxs-lookup"><span data-stu-id="cc8bf-118">Header</span></span><br/> | <dl> <span data-ttu-id="cc8bf-119"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc8bf-119"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc8bf-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc8bf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc8bf-121">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="cc8bf-121">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




