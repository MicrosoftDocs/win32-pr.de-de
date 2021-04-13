---
title: IKE/AuthIP-Funktionen
description: (WFP)-Funktionen, die für die Interaktion mit Schlüssel für die Schlüssel Erstellung (8212 Internetschlüsselaustausch; IKE), Internetschlüsselaustausch v2 (IKEv2) und authentifiziertes Internetprotokoll (AuthIP) verwendet werden.
ms.assetid: df36b6cc-a304-4426-8f16-1bf92fd721e1
keywords:
- API-Internetschlüsselaustausch Funktionen der Windows-Filter Plattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cce5d3e2393bb1a83ebf816375f537318bb4b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310555"
---
# <a name="ikeauthip-functions"></a><span data-ttu-id="1c8c5-104">IKE/AuthIP-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1c8c5-104">IKE/AuthIP Functions</span></span>

<span data-ttu-id="1c8c5-105">Die Funktionen der Windows-Filter Plattform (Windows Filtering Platform, WFP), die für die Interaktion mit den – Internetschlüsselaustausch (IKE), Internetschlüsselaustausch v2 (IKEv2) und authentifiziertes Internetprotokoll (AuthIP) – verwendet werden, lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="1c8c5-105">The Windows Filtering Platform (WFP) functions used to interact with keying modules—Internet Key Exchange (IKE), Internet Key Exchange v2 (IKEv2), and Authenticated Internet Protocol (AuthIP)—are as follows.</span></span>

-   <span data-ttu-id="1c8c5-106">Ikeextgetstatistics:</span><span class="sxs-lookup"><span data-stu-id="1c8c5-106">IkeextGetStatistics:</span></span>
    -   <span data-ttu-id="1c8c5-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="1c8c5-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista)</span></span>
    -   <span data-ttu-id="1c8c5-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 und höher)</span><span class="sxs-lookup"><span data-stu-id="1c8c5-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="1c8c5-109">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="1c8c5-109">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)
-   [<span data-ttu-id="1c8c5-110">**IkeextSaDbGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="1c8c5-110">**IkeextSaDbGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbgetsecurityinfo0)
-   [<span data-ttu-id="1c8c5-111">**IkeextSaDbSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="1c8c5-111">**IkeextSaDbSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbsetsecurityinfo0)
-   [<span data-ttu-id="1c8c5-112">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="1c8c5-112">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)
-   [<span data-ttu-id="1c8c5-113">**IkeextSaDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="1c8c5-113">**IkeextSaDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadestroyenumhandle0)
-   <span data-ttu-id="1c8c5-114">Ikeextsaerum:</span><span class="sxs-lookup"><span data-stu-id="1c8c5-114">IkeextSaEnum:</span></span>
    -   <span data-ttu-id="1c8c5-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="1c8c5-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="1c8c5-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="1c8c5-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7)</span></span>
    -   <span data-ttu-id="1c8c5-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="1c8c5-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8)</span></span>
-   <span data-ttu-id="1c8c5-118">Ikeextsagetbyid:</span><span class="sxs-lookup"><span data-stu-id="1c8c5-118">IkeextSaGetById:</span></span>
    -   <span data-ttu-id="1c8c5-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="1c8c5-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista)</span></span>
    -   <span data-ttu-id="1c8c5-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="1c8c5-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7)</span></span>
    -   <span data-ttu-id="1c8c5-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="1c8c5-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8)</span></span>

 

 




