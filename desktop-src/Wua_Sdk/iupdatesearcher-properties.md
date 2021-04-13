---
description: Die iupdatesearcher-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Iupdatesearcher-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777c2489afe10f73c41badfb346053aefad7022
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/11/2021
ms.locfileid: "104354018"
---
# <a name="iupdatesearcher-properties"></a><span data-ttu-id="3a2af-103">Iupdatesearcher-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a2af-103">IUpdateSearcher Properties</span></span>

<span data-ttu-id="3a2af-104">Die [**iupdatesearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a2af-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following properties.</span></span>



| <span data-ttu-id="3a2af-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3a2af-105">Property</span></span>                                                                                           | <span data-ttu-id="3a2af-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a2af-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a2af-107">**Canautomaticallyupgradeservice**</span><span class="sxs-lookup"><span data-stu-id="3a2af-107">**CanAutomaticallyUpgradeService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | <span data-ttu-id="3a2af-108">Ruft einen booleschen Wert ab, der angibt, ob zukünftige Aufrufe der [**beginsearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) -Methode und der [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) -Methode zu einem automatischen Upgrade auf Windows Update-Agent (WUA) führen, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="3a2af-108">Gets and sets a Boolean value that indicates whether future calls to the [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) and [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) methods result in an automatic upgrade to Windows Update Agent (WUA).</span></span> |
| [<span data-ttu-id="3a2af-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="3a2af-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | <span data-ttu-id="3a2af-110">Identifiziert die aktuelle Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3a2af-110">Identifies the current client application.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="3a2af-111">**Incluabpotenziallyablösung dedupdates**</span><span class="sxs-lookup"><span data-stu-id="3a2af-111">**IncludePotentiallySupersededUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | <span data-ttu-id="3a2af-112">Ruft einen booleschen Wert ab, der angibt, ob die Suchergebnisse Updates enthalten, die durch andere Updates in den Suchergebnissen abgelöst werden, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="3a2af-112">Gets and sets a Boolean value that indicates whether the search results include updates that are superseded by other updates in the search results.</span></span>                                                                                          |
| [<span data-ttu-id="3a2af-113">**Online**</span><span class="sxs-lookup"><span data-stu-id="3a2af-113">**Online**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | <span data-ttu-id="3a2af-114">Ruft einen booleschen Wert ab, der angibt, ob [**updatesearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) online geschaltet wird, um nach Updates zu suchen, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="3a2af-114">Gets and sets a Boolean value that indicates whether the [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) goes online to search for updates.</span></span>                                                                                                        |
| [<span data-ttu-id="3a2af-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="3a2af-115">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | <span data-ttu-id="3a2af-116">Dient zum Abrufen und Festlegen einer Site, die durchsucht werden soll, wenn es sich bei der zu suchenden Site nicht um Windows Update</span><span class="sxs-lookup"><span data-stu-id="3a2af-116">Gets and sets a site to search when the site to search is not a Windows Update site.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="3a2af-117">**ServerSelection**</span><span class="sxs-lookup"><span data-stu-id="3a2af-117">**ServerSelection**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | <span data-ttu-id="3a2af-118">Dient zum Abrufen und Festlegen eines Server [**Auswahl**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) Werts, der den Server angibt, auf dem nach Updates gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a2af-118">Gets and sets a [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) value that indicates the server to search for updates.</span></span>                                                                                                                            |




 

 

 



