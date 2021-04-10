---
description: Eigenschaften Satz für externen Geräte Transport
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Eigenschaften Satz für externen Geräte Transport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e77942157b7cf5f75b883e6953f3a115d1fa9f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125600"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="7cc58-103">Eigenschaften Satz für externen Geräte Transport</span><span class="sxs-lookup"><span data-stu-id="7cc58-103">External Device Transport Property Set</span></span>

<span data-ttu-id="7cc58-104">Dieser Eigenschaften Satz steuert den Transport von Daten zu und von einem externen Gerät.</span><span class="sxs-lookup"><span data-stu-id="7cc58-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="7cc58-105">In den meisten Fällen sollten diese Eigenschaften nicht direkt von Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cc58-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="7cc58-106">Verwenden Sie stattdessen die [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7cc58-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="7cc58-107">In der folgenden Tabelle sind die Eigenschaften aufgelistet, die für Benutzermodusanwendungen relevant sind.</span><span class="sxs-lookup"><span data-stu-id="7cc58-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="7cc58-108">Eine umfassende Beschreibung dieses Eigenschaften Satzes finden Sie im Microsoft Windows Driver Development Kit-DDK.</span><span class="sxs-lookup"><span data-stu-id="7cc58-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="7cc58-109">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="7cc58-109">Property Set GUID</span></span> | <span data-ttu-id="7cc58-110">propseetid- \_ Ext- \_ Transport</span><span class="sxs-lookup"><span data-stu-id="7cc58-110">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="7cc58-111">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="7cc58-111">Property ID</span></span>                                                                           | <span data-ttu-id="7cc58-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7cc58-112">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="7cc58-113">**ksproperty \_ extxport- \_ Atn- \_ Suche**</span><span class="sxs-lookup"><span data-stu-id="7cc58-113">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="7cc58-114">Sucht nach einer absoluten Spur Nummer (ATN).</span><span class="sxs-lookup"><span data-stu-id="7cc58-114">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="7cc58-115">**ksproperty \_ extxport- \_ \_ timecodesuche**</span><span class="sxs-lookup"><span data-stu-id="7cc58-115">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="7cc58-116">Sucht nach einem Zeit Code.</span><span class="sxs-lookup"><span data-stu-id="7cc58-116">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="7cc58-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7cc58-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cc58-118">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="7cc58-118">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



