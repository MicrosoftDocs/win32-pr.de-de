---
description: Der Medientyp (oder Modus) eines Geräts beschreibt den Typ der Informationen, die ausgetauscht werden können, z. b. interaktive Stimme. Ein bestimmtes Gerät kann möglicherweise nur einen Medientyp verarbeiten, oder es kann mit einem Bereich von Typen umzugehen.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Medientyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369954a4b0d1f78e12f6ea42bcc2ec61ca425012
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354272"
---
# <a name="media-type"></a><span data-ttu-id="58b08-104">Medientyp</span><span class="sxs-lookup"><span data-stu-id="58b08-104">Media Type</span></span>

<span data-ttu-id="58b08-105">Der *Medientyp* (oder Modus) eines Geräts beschreibt den Typ der Informationen, die ausgetauscht werden können, z. b. interaktive Stimme.</span><span class="sxs-lookup"><span data-stu-id="58b08-105">The *media type* (or mode) of a device describes the type of information that can be exchanged, such as interactive voice.</span></span> <span data-ttu-id="58b08-106">Ein bestimmtes Gerät kann möglicherweise nur einen Medientyp verarbeiten, oder es kann mit einem Bereich von Typen umzugehen.</span><span class="sxs-lookup"><span data-stu-id="58b08-106">A given device might be able to handle only one media type, or it might be able to deal with a range of types.</span></span>

<span data-ttu-id="58b08-107">Dienstanbieter machen den Medientyp oder die Typen verfügbar, die von den von Ihnen kontrollierten Geräten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="58b08-107">Service providers expose the media type or types supported by the devices they control.</span></span> <span data-ttu-id="58b08-108">Anwendungen Fragen den Medientyp ab und verwenden diese Informationen dann, um eine geeignete Adresse auszuwählen, auf der eine Sitzung initiiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="58b08-108">Applications query for media type and then use this information to select an appropriate address on which to initiate a session.</span></span> <span data-ttu-id="58b08-109">Die Anwendungs Antwort auf eine angebotene Sitzung kann auch für den Medientyp als Prädikat vorgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="58b08-109">Application response to a session offered may also be predicated on media type.</span></span>

<span data-ttu-id="58b08-110">Eine bestimmte Kommunikationssitzung bzw. ein angegebener-Rückruf kann mehrere Medientypen einschließen.</span><span class="sxs-lookup"><span data-stu-id="58b08-110">A given communications session, or call, can involve several media types.</span></span> <span data-ttu-id="58b08-111">Weitere Informationen finden Sie unter Medientyp für eine Sitzung.</span><span class="sxs-lookup"><span data-stu-id="58b08-111">For further information, see Media type for a session.</span></span>

<span data-ttu-id="58b08-112">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetaddresscaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **dwavailablemediamodes** -Member der [**lineaddresscaps**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) -Struktur, auf die von *lpaddresscaps* und [linemediamode- \_ Konstanten](./linemediamode--constants.md)verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="58b08-112">**TAPI 2.x:** See [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **dwAvailableMediaModes** member of [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) structure pointed to by *lpAddressCaps*, [LINEMEDIAMODE\_ Constants](./linemediamode--constants.md).</span></span>

<span data-ttu-id="58b08-113">**TAPI 3. x:** Siehe [**itterminal:: get \_ mediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [tapimediatype \_ Konstanten](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="58b08-113">**TAPI 3.x:** See [**ITTerminal::get\_MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE\_ Constants](tapimediatype--constants.md).</span></span>
