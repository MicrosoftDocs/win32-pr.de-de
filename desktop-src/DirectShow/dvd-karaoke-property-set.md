---
description: Wenn der FILTER DVD Navigator in den Modus "Dvdoke" wechselt, wird der Audiodecoder über die EIGENSCHAFT AM \_ PROPERTY \_ DVDKARAOKE \_ ENABLE informiert.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: DVD-Dvd–Dvd-Eigenschaftssatz (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2918513de06a657436ed99e67f672fe74a113b78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909068"
---
# <a name="dvd-karaoke-property-set"></a><span data-ttu-id="d67db-103">DVD-Eigenschaftssatz "Dvd- UndOke"</span><span class="sxs-lookup"><span data-stu-id="d67db-103">DVD Karaoke Property Set</span></span>

<span data-ttu-id="d67db-104">Wenn der [FILTER DVD Navigator](dvd-navigator-filter.md) in den Modus "Dvdoke" wechselt, wird der Audiodecoder über die EIGENSCHAFT AM PROPERTY **\_ \_ DVDKARAOKE \_ ENABLE informiert.**</span><span class="sxs-lookup"><span data-stu-id="d67db-104">When the [DVD Navigator](dvd-navigator-filter.md) filter goes into karaoke mode, it informs the audio decoder through the **AM\_PROPERTY\_DVDKARAOKE\_ENABLE** property.</span></span> <span data-ttu-id="d67db-105">Der Decoder sollte dann audio channels 2 bis 5 stummschalten, bis er vom DVD-Navigator eine **AM \_ PROPERTY \_ DVDKARAOKE \_ DATA-Eigenschaft** mit einem Zeiger auf eine [**AM \_ DvdKaraokeData-Datenstruktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) empfängt, die angibt, wie die Hilfskanäle gemischt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d67db-105">The decoder should then mute audio channels 2 through 5 until it receives from the DVD Navigator an **AM\_PROPERTY\_DVDKARAOKE\_DATA** property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) data structure indicating how the auxiliary channels are to be mixed.</span></span>



| <span data-ttu-id="d67db-106">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="d67db-106">Label</span></span> | <span data-ttu-id="d67db-107">Wert</span><span class="sxs-lookup"><span data-stu-id="d67db-107">Value</span></span> |
|-------------------|-----------------------------|
| <span data-ttu-id="d67db-108">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="d67db-108">Property Set GUID</span></span> | <span data-ttu-id="d67db-109">AM \_ KSPROPSETID \_ DvdKaraoke</span><span class="sxs-lookup"><span data-stu-id="d67db-109">AM\_KSPROPSETID\_DvdKaraoke</span></span> |



 



| <span data-ttu-id="d67db-110">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="d67db-110">Property ID</span></span>                      | <span data-ttu-id="d67db-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d67db-111">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d67db-112">AM \_ PROPERTY \_ DVDKARAOKE \_ ENABLE</span><span class="sxs-lookup"><span data-stu-id="d67db-112">AM\_PROPERTY\_DVDKARAOKE\_ENABLE</span></span> | <span data-ttu-id="d67db-113">BOOLESCHER WERT.</span><span class="sxs-lookup"><span data-stu-id="d67db-113">BOOLEAN value.</span></span> <span data-ttu-id="d67db-114">Der DVD-Navigator sendet dem Decoder eine AM \_ PROPERTY \_ DVDKARAOKE \_ ENABLE-Eigenschaft mit dem Wert **TRUE,** um die Downmixing-Funktion zu aktivieren, oder **FALSE,** um sie zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d67db-114">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_ENABLE with a value of **TRUE** to enable karaoke downmixing or **FALSE** to disable it.</span></span>                                                                                                                                    |
| <span data-ttu-id="d67db-115">\_AM-EIGENSCHAFT \_ DVDKARAOKE-DATEN \_</span><span class="sxs-lookup"><span data-stu-id="d67db-115">AM\_PROPERTY\_DVDKARAOKE\_DATA</span></span>   | <span data-ttu-id="d67db-116">Der DVD-Navigator sendet dem Decoder eine AM \_ PROPERTY \_ DVDKARAOKE \_ DATA-Eigenschaft mit einem Zeiger auf eine [**AM \_ DvdKaraokeData-Struktur,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) um die Downmixkonfiguration zu ändern, d. h., um bestimmteLaufkanäle ein- oder auszuschalten und an den rechten oder linken Ausgabekanal weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="d67db-116">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_DATA property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) structure to change the downmix configuration; that is, to turn certain karaoke channels on or off and direct them to the right or left output channel.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d67db-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d67db-117">Requirements</span></span>



| <span data-ttu-id="d67db-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d67db-118">Requirement</span></span> | <span data-ttu-id="d67db-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d67db-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d67db-120">Header</span><span class="sxs-lookup"><span data-stu-id="d67db-120">Header</span></span><br/> | <dl> <span data-ttu-id="d67db-121"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="d67db-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d67db-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d67db-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d67db-123">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="d67db-123">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




