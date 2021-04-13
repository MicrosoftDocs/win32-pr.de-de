---
description: Beginnend mit Windows 2000-Telefoniedienstanbietern, die eine Version von 3,0 oder höher aushandeln, muss ein entsprechender Medien Dienstanbieter vorhanden sein.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Kommunikation mit dem Mediendienst Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a50ec6a4fb96a86ceab3a302b138ee72d6c61b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351478"
---
# <a name="media-service-provider-communication"></a><span data-ttu-id="39aad-103">Kommunikation mit dem Mediendienst Anbieter</span><span class="sxs-lookup"><span data-stu-id="39aad-103">Media Service Provider Communication</span></span>

<span data-ttu-id="39aad-104">Beginnend mit Windows 2000-Telefoniedienstanbietern, die eine Version von 3,0 oder höher aushandeln, muss ein entsprechender Medien Dienstanbieter vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="39aad-104">Starting with Windows 2000 telephony service providers that negotiate a version of 3.0 or later must have a matching media service provider.</span></span> <span data-ttu-id="39aad-105">Die genaue Division von betrieblichen Zuständigkeiten ist implementierungsabhängig.</span><span class="sxs-lookup"><span data-stu-id="39aad-105">The precise division of operational responsibilities is implementation dependent.</span></span> <span data-ttu-id="39aad-106">Beispielsweise kann ein TSP den passenden MSP verwenden, um die Medientyp Bestimmung für eine eingehende Sitzung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="39aad-106">For example, a TSP might use the matching MSP to perform media type determination on an incoming session.</span></span> <span data-ttu-id="39aad-107">Der TSP muss jedoch dem TSPI entsprechen. Dies bedeutet, dass diese Bestimmung vom MSP erhalten und an TAPI gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="39aad-107">However, the TSP must conform to the TSPI, which means getting that determination from the MSP and reporting it to TAPI.</span></span>

<span data-ttu-id="39aad-108">TSPI bietet die folgenden Funktionen und Meldungen, um eine virtuelle Verbindung zwischen einem TSP und einem MSP zuzulassen:</span><span class="sxs-lookup"><span data-stu-id="39aad-108">TSPI provides the following functions and messages to allow a virtual connection between a TSP and an MSP:</span></span>

-   [<span data-ttu-id="39aad-109">**TSPI \_ lineclosemspinstance**</span><span class="sxs-lookup"><span data-stu-id="39aad-109">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [<span data-ttu-id="39aad-110">**TSPI \_ linecreatemspinstance**</span><span class="sxs-lookup"><span data-stu-id="39aad-110">**TSPI\_lineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [<span data-ttu-id="39aad-111">**TSPI \_ linemspidentify**</span><span class="sxs-lookup"><span data-stu-id="39aad-111">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [<span data-ttu-id="39aad-112">**TSPI \_ linereceivemspdata**</span><span class="sxs-lookup"><span data-stu-id="39aad-112">**TSPI\_lineReceiveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [<span data-ttu-id="39aad-113">**Zeilen- \_ qosinfo**</span><span class="sxs-lookup"><span data-stu-id="39aad-113">**LINE\_QOSINFO**</span></span>](line-qosinfo.md)
-   [<span data-ttu-id="39aad-114">**Zeile \_ sendmspdata**</span><span class="sxs-lookup"><span data-stu-id="39aad-114">**LINE\_SENDMSPDATA**</span></span>](line-sendmspdata.md)

 

 
