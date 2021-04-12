---
title: Referenz zu Unterstützungsfunktionen
description: Die folgenden Funktionen werden für das Routing von Protokollen durch den routermanager bereitgestellt.
ms.assetid: 4e88c9fe-f6ec-4f9c-88b1-8726e10d0f6d
keywords:
- Routing Protokoll Schnittstelle RRAS, Supportfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbaba49c5f7e4130491a50176d560ee565b0046
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473813"
---
# <a name="support-functions-reference"></a><span data-ttu-id="ea47d-104">Referenz zu Unterstützungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ea47d-104">Support Functions Reference</span></span>

<span data-ttu-id="ea47d-105">Die folgenden Funktionen werden für das Routing von Protokollen durch den routermanager bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ea47d-105">The following functions are provided to routing protocols by the router manager.</span></span> <span data-ttu-id="ea47d-106">Wenn der routermanager die [**startprotocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) -Funktion aufruft (implementiert durch das Routing Protokoll), übergibt der routermanager das Routing Protokoll einer [**Unterstützungs \_ Funktions**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) Struktur, die Zeiger auf diese Funktionen enthält:</span><span class="sxs-lookup"><span data-stu-id="ea47d-106">When the router manager calls the [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) function (implemented by the routing protocol), the router manager passes the routing protocol a [**SUPPORT\_FUNCTIONS**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) structure containing pointers to these functions:</span></span>

<span data-ttu-id="ea47d-107">[**Demanddialrequest**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea47d-107">[**DemandDialRequest**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))</span></span>

<span data-ttu-id="ea47d-108">[**Mibentrycreate**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea47d-108">[**MIBEntryCreate**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))</span></span>

<span data-ttu-id="ea47d-109">[**Mibentrydelete**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea47d-109">[**MIBEntryDelete**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))</span></span>

<span data-ttu-id="ea47d-110">[**Mibentryget**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea47d-110">[**MIBEntryGet**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))</span></span>

<span data-ttu-id="ea47d-111">[**Mibentrygetfirst**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea47d-111">[**MIBEntryGetFirst**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))</span></span>

<span data-ttu-id="ea47d-112">[**Mibentrygetnext**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea47d-112">[**MIBEntryGetNext**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))</span></span>

<span data-ttu-id="ea47d-113">[**Mibentryset**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea47d-113">[**MIBEntrySet**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))</span></span>

<span data-ttu-id="ea47d-114">[**Setinterfakereceivetype**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea47d-114">[**SetInterfaceReceiveType**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))</span></span>

<span data-ttu-id="ea47d-115">[**Validateroute**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea47d-115">[**ValidateRoute**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))</span></span>

 

 