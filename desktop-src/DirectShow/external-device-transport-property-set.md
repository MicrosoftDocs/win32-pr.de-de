---
description: Eigenschaftensatz für den Transport externer Geräte
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Eigenschaftensatz für den Transport externer Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e38217af21ea1839d7c9207a4922bcff00d63a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909218"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="a6b8d-103">Eigenschaftensatz für den Transport externer Geräte</span><span class="sxs-lookup"><span data-stu-id="a6b8d-103">External Device Transport Property Set</span></span>

<span data-ttu-id="a6b8d-104">Dieser Eigenschaftensatz steuert den Transport von Daten zu und von einem externen Gerät.</span><span class="sxs-lookup"><span data-stu-id="a6b8d-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="a6b8d-105">In den meisten Fällen sollten Anwendungen diesen Eigenschaftensatz nicht direkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6b8d-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="a6b8d-106">Verwenden Sie stattdessen die [**IAMExtTransport-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)</span><span class="sxs-lookup"><span data-stu-id="a6b8d-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="a6b8d-107">In der folgenden Tabelle sind die Eigenschaften aufgeführt, die für Benutzermodusanwendungen relevant sind.</span><span class="sxs-lookup"><span data-stu-id="a6b8d-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="a6b8d-108">Eine vollständige Beschreibung dieses Eigenschaftensatzes finden Sie im Microsoft Windows Driver Development Kit DDK.</span><span class="sxs-lookup"><span data-stu-id="a6b8d-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



| <span data-ttu-id="a6b8d-109">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="a6b8d-109">Label</span></span> | <span data-ttu-id="a6b8d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="a6b8d-110">Value</span></span> |
|-------------------|---------------------------|
| <span data-ttu-id="a6b8d-111">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="a6b8d-111">Property Set GUID</span></span> | <span data-ttu-id="a6b8d-112">PROPSETID \_ EXT \_ TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="a6b8d-112">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="a6b8d-113">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="a6b8d-113">Property ID</span></span>                                                                           | <span data-ttu-id="a6b8d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6b8d-114">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="a6b8d-115">**KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH**</span><span class="sxs-lookup"><span data-stu-id="a6b8d-115">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="a6b8d-116">Sucht nach einer absoluten Tracknummer (ATN).</span><span class="sxs-lookup"><span data-stu-id="a6b8d-116">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="a6b8d-117">**KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH**</span><span class="sxs-lookup"><span data-stu-id="a6b8d-117">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="a6b8d-118">Sucht nach einem Zeitcode.</span><span class="sxs-lookup"><span data-stu-id="a6b8d-118">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="a6b8d-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6b8d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6b8d-120">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="a6b8d-120">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



