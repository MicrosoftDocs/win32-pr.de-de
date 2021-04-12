---
description: Die folgenden Abschnitte enthalten eine alphabetische Liste der Funktionen, die nach Bereich gruppiert sind. Die Informationen für jede Funktion enthalten eine Liste der gültigen Ansichts Zustände für den Eintrag der Funktion und typische Aufrufe des Zustands von anrufen, wenn die Anforderung beendet ist.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: TAPI-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38532fa1c0b978e3e59e54b08fbc43152fa0bd64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529213"
---
# <a name="tapi-functions"></a><span data-ttu-id="d963f-104">TAPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d963f-104">TAPI Functions</span></span>

<span data-ttu-id="d963f-105">Die folgenden Abschnitte enthalten eine alphabetische Liste der Funktionen, die nach Bereich gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="d963f-105">The following sections contain an alphabetic list of functions grouped by area.</span></span> <span data-ttu-id="d963f-106">Die Informationen für jede Funktion enthalten eine Liste der gültigen Ansichts Zustände für den Eintrag der Funktion und typische Aufrufe des Zustands von anrufen, wenn die Anforderung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="d963f-106">The information for each function includes a list of the valid call states on entry of the function and typical call state transitions when the request is complete.</span></span>

-   [<span data-ttu-id="d963f-107">Unterstützte Telefoniefunktionen</span><span class="sxs-lookup"><span data-stu-id="d963f-107">Assisted Telephony Functions</span></span>](assisted-telephony-functions.md)
-   [<span data-ttu-id="d963f-108">Callcenter-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d963f-108">Call Center Functions</span></span>](call-center-functions.md)
-   [<span data-ttu-id="d963f-109">Zeilen Gerätefunktionen</span><span class="sxs-lookup"><span data-stu-id="d963f-109">Line Device Functions</span></span>](line-device-functions.md)
-   [<span data-ttu-id="d963f-110">Telefongeräte Funktionen</span><span class="sxs-lookup"><span data-stu-id="d963f-110">Phone Device Functions</span></span>](phone-device-functions.md)

<span data-ttu-id="d963f-111">Informationen zu TAPI-Funktionen, die nach Service Level und Task kategorisiert sind, finden Sie unter [TAPI Quick Function Reference](tapi-quick-function-reference.md)</span><span class="sxs-lookup"><span data-stu-id="d963f-111">For TAPI functions categorized by service level and task, see [TAPI Quick Function Reference](tapi-quick-function-reference.md).</span></span>

<span data-ttu-id="d963f-112">Beachten Sie, dass die Einschränkungen des Dienstanbieters möglicherweise in Bezug auf die tatsächlichen Zustände bestehen, in denen eine Funktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d963f-112">Please note that service provider limitations may exist concerning the actual states in which a function can be performed.</span></span> <span data-ttu-id="d963f-113">Anwendungen müssen den **dwcallfeatures** -Member in der [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) -Struktur, den **dwaddressfeatures** -Member in der [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) -Struktur und den **dwlinefeatures** -Member in der [**linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) -Struktur überprüfen, um zu bestimmen, ob eine Funktion innerhalb des aktuellen Aufruf Zustands zulässig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="d963f-113">Applications must check the **dwCallFeatures** member in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure, the **dwAddressFeatures** member in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure, and the **dwLineFeatures** member in the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure to determine whether or not a function is permitted within the current call state.</span></span>

 

 



