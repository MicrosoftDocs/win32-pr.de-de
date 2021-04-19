---
description: Die iinstallationprogress-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: f16c682f-3e9f-4767-8f26-d7af0a14d720
title: Iinstallationprogress-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbcdb162c544c81b96326ec7b2b7657d81538a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353108"
---
# <a name="iinstallationprogress-properties"></a><span data-ttu-id="bb993-103">Iinstallationprogress-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb993-103">IInstallationProgress Properties</span></span>

<span data-ttu-id="bb993-104">Die [**iinstallationprogress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bb993-104">The [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="bb993-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bb993-105">Property</span></span>                                                                                   | <span data-ttu-id="bb993-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb993-106">Description</span></span>                                                                                                                                        |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb993-107">**Currentupdateingedex**</span><span class="sxs-lookup"><span data-stu-id="bb993-107">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdateindex)                     | <span data-ttu-id="bb993-108">Ruft einen NULL basierten Indexwert ab, der das Update angibt, das zurzeit installiert oder deinstalliert wird, wenn mehrere Updates ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="bb993-108">Gets a zero-based index value that specifies the update that is currently being installed or uninstalled when multiple updates have been selected.</span></span> |
| [<span data-ttu-id="bb993-109">**Currentupdateprozentucomplete**</span><span class="sxs-lookup"><span data-stu-id="bb993-109">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="bb993-110">Ruft ab, wie weit der Installations-oder der deinstalstallvorgang für das aktuelle Update in Prozent erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="bb993-110">Gets how far the installation or uninstallation process for the current update has progressed, as a percentage.</span></span>                                    |
| [<span data-ttu-id="bb993-111">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="bb993-111">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_percentcomplete)                           | <span data-ttu-id="bb993-112">Ruft ab, wie weit der gesamte Installations-oder Deinstallationsprozess als Prozentsatz fortgeschritten ist.</span><span class="sxs-lookup"><span data-stu-id="bb993-112">Gets how far the overall installation or uninstallation process has progressed, as a percentage.</span></span>                                                   |



 

 

 



