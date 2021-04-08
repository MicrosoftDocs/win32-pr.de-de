---
title: Vorgangs Kontext Lebensdauer und Threading
description: Die Lebensdauer des Vorgangs Kontexts, der durch ein WS- \_ Vorgangs \_ Kontext Handle dargestellt wird, bestimmt die Lebensdauer der enthaltenen Eigenschaften.
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- Vorgangs Kontext Lebensdauer und Threading Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea27b0b1dc41ccd029df7d726fe92631adc1ee4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734880"
---
# <a name="operation-context-lifetime-and-threading"></a><span data-ttu-id="456d6-106">Vorgangs Kontext Lebensdauer und Threading</span><span class="sxs-lookup"><span data-stu-id="456d6-106">Operation Context Lifetime and Threading</span></span>

<span data-ttu-id="456d6-107">Die Lebensdauer des Vorgangs Kontexts, der durch ein [WS- \_ Vorgangs \_ Kontext](ws-operation-context.md) Handle dargestellt wird, bestimmt die Lebensdauer der enthaltenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="456d6-107">The lifetime of the operation context, represented by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) handle, determines the lifetime of the properties it contains.</span></span> <span data-ttu-id="456d6-108">Daher sollte ein Kontext nur innerhalb der Lebensdauer des [Dienst Vorgangs](service-operation.md) oder des Rückrufs verwendet werden, zu dem er bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="456d6-108">Therefore, a context should only be used within the lifetime of the [service operation](service-operation.md) or the callback to which its provided.</span></span> <span data-ttu-id="456d6-109">Die Lebensdauer eines synchronen Aufrufes ist die Ausführung der Funktion selbst.</span><span class="sxs-lookup"><span data-stu-id="456d6-109">The lifetime of a synchronous call is the execution of function itself.</span></span> <span data-ttu-id="456d6-110">Bei einem asynchronen-Aufrufvorgang endet die Lebensdauer, sobald der asynchrone-Befehl abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="456d6-110">For an asynchronous call the lifetime ends once the asynchronous call is completed.</span></span> <span data-ttu-id="456d6-111">Das Dienstmodell bietet keine Garantie für den Kontext, wenn der-Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="456d6-111">The Service Model gives no guarantees about the context once the call is completed.</span></span> <span data-ttu-id="456d6-112">Das Verhalten der Verwendung eines Vorgangs Kontexts oder seiner Eigenschaften über die Lebensdauer hinaus ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="456d6-112">The behavior of relying on operation context or any of its properties beyond its lifetime is undefined.</span></span>


<span data-ttu-id="456d6-113">Siehe auch, das Sitzungs basierte Rechner Beispiel [sessionfullcalculatorserviceexample](sessionfullcalculatorserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="456d6-113">See also, the session based calculator example, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).</span></span>

## <a name="threading-model"></a><span data-ttu-id="456d6-114">Threading-Modell</span><span class="sxs-lookup"><span data-stu-id="456d6-114">Threading Model</span></span>

<span data-ttu-id="456d6-115">Der Vorgangs Kontext unterstützt das kostenlose Threading, dies gilt jedoch für den Vorgangs Kontext selbst und gilt nicht für die darin enthaltenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="456d6-115">The operation context supports free threading, however this is true of the operation context itself and does not apply to any of the properties it contains.</span></span>

<span data-ttu-id="456d6-116">Beachten Sie, dass die erste Registrierung erfolgreich ist, wenn Sie einen Abbruch Rückruf für einen Dienst Vorgang über die [**wsregisteroperationforcancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) -Funktion registrieren. Wenn Sie den Abbruch Rückruf mehrmals festlegen, tritt jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="456d6-116">When you register a cancel callback for a service operation through the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function, note that the first registration will succeed; setting the cancel callback multiple times, however, will fail.</span></span>

 

 




