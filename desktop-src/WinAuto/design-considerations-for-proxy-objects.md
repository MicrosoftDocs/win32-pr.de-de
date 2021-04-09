---
title: Entwurfs Überlegungen für Proxy Objekte
description: Der Proxy und der barrierefreie Objekt Entwurf hängen vom Entwurf der Benutzeroberflächen Elemente des Servers ab. Unabhängig vom Entwurf muss ein Benutzeroberflächen Element sein Proxy Objekt direkt benachrichtigen, bevor es zerstört wird, damit das Proxy Objekt Aufrufe von Clients entsprechend verarbeitet.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9578c79f93f91834dec14808a1a1867f40b215a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036550"
---
# <a name="design-considerations-for-proxy-objects"></a><span data-ttu-id="a30e4-104">Entwurfs Überlegungen für Proxy Objekte</span><span class="sxs-lookup"><span data-stu-id="a30e4-104">Design Considerations for Proxy Objects</span></span>

<span data-ttu-id="a30e4-105">Der Proxy und der barrierefreie Objekt Entwurf hängen vom Entwurf der Benutzeroberflächen Elemente des Servers ab.</span><span class="sxs-lookup"><span data-stu-id="a30e4-105">Proxy and accessible object design depends on the design of the server UI elements.</span></span> <span data-ttu-id="a30e4-106">Unabhängig vom Entwurf muss ein Benutzeroberflächen Element sein Proxy Objekt direkt benachrichtigen, bevor es zerstört wird, damit das Proxy Objekt Aufrufe von Clients entsprechend verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a30e4-106">Regardless of the design, a UI element must notify its proxy object right before it is destroyed so that the proxy object handles calls from clients appropriately.</span></span>

<span data-ttu-id="a30e4-107">In der folgenden Liste werden zwei Entwurfs Möglichkeiten beschrieben:</span><span class="sxs-lookup"><span data-stu-id="a30e4-107">The following list describes two design possibilities:</span></span>

-   <span data-ttu-id="a30e4-108">Platzieren Sie den Code, der die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle implementiert, im gleichen Modul wie der Code, der das Benutzeroberflächen Element implementiert, wenn der Code der Benutzeroberfläche leicht erweiterbar ist.</span><span class="sxs-lookup"><span data-stu-id="a30e4-108">Place the code that implements the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface in the same module as the code that implements the user interface element if the user interface code is easily extensible.</span></span> <span data-ttu-id="a30e4-109">In diesem Fall ist der Proxy "Lightweight" in dem Sinne, dass er lediglich die Lebensdauer des barrierefreien Objekts überwacht, Aufrufe an das barrierefreie Objekt weiterleiten und die Ergebnisse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a30e4-109">In this case, the proxy is "lightweight" in the sense that all it does is monitor the life span of the accessible object, forward calls to the accessible object, and return the results.</span></span>
-   <span data-ttu-id="a30e4-110">Platzieren Sie den Code, der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementiert, im gleichen Modul wie der Code, der das Proxy Objekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="a30e4-110">Place the code that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) in the same module as the code that implements the proxy object.</span></span> <span data-ttu-id="a30e4-111">In diesem Fall verwendet das barrierefreie Objekt interne Funktionen zum Abrufen von Informationen über das UI-Element.</span><span class="sxs-lookup"><span data-stu-id="a30e4-111">In this case, the accessible object uses internal functions to obtain information about the UI element.</span></span>

## <a name="trackbar-controls"></a><span data-ttu-id="a30e4-112">TrackBar-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="a30e4-112">Trackbar Controls</span></span>

<span data-ttu-id="a30e4-113">Wenn Sie TrackBar-Steuerelemente implementieren, verwenden Sie die **TSB \_** für das TrackBar-Format, um aussagekräftige Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a30e4-113">When implementing trackbar controls, use the trackbar style **TBS\_REVERSED** to provide more meaningful information.</span></span> <span data-ttu-id="a30e4-114">Dieser Stil kehrt die von [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)verwendete Skala um.</span><span class="sxs-lookup"><span data-stu-id="a30e4-114">This style reverses the scale used by [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="a30e4-115">Bei vertikalen trackbars ohne diesen Stil gibt [**IAccessible:: get- \_ accValue den Wert**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) NULL (0) zurück, wenn sich der TrackBar-Ziehpunkt am oberen Rand des Steuer Elements befindet. die Werte erhöhen sich, wenn Sie den Ziehpunkt auf den unteren Rand verschieben.</span><span class="sxs-lookup"><span data-stu-id="a30e4-115">For vertical trackbars without this style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns zero (0) when the trackbar thumb is at the top of the control; the values increase as you slide the thumb toward the bottom.</span></span> <span data-ttu-id="a30e4-116">Beim **\_ umgekehrten TSB** -Format gibt **IAccessible:: get \_ accValue** 100 (100) zurück, wenn sich der TrackBar-Ziehpunkt im oberen Bereich befindet. die Zahlen verringern sich, wenn Sie den TrackBar-Ziehpunkt in den unteren Bereich verschieben.</span><span class="sxs-lookup"><span data-stu-id="a30e4-116">With the **TBS\_REVERSED** style, **IAccessible::get\_accValue** returns one hundred (100) when the trackbar thumb is at the top; the numbers decrease as you move the trackbar thumb toward the bottom.</span></span>

<span data-ttu-id="a30e4-117">Bei horizontalen trackbars ohne diesen Stil wird 0 (null) zurückgegeben, wenn sich der TrackBar-Ziehpunkt am linken Ende des Steuer Elements befindet. die Werte erhöhen sich, wenn Sie den TrackBar-Ziehpunkt nach rechts verschieben.</span><span class="sxs-lookup"><span data-stu-id="a30e4-117">For horizontal trackbars without this style, zero (0) is returned when the trackbar thumb is at the left end of the control; the values increase as you move the trackbar thumb to the right.</span></span> <span data-ttu-id="a30e4-118">Bei einem **\_ umgekehrten TSB** -Stil gibt [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) 100 (100) zurück, wenn sich der Ziehpunkt auf der linken Seite befindet. die Werte verringern sich, wenn Sie den TrackBar-Ziehpunkt nach rechts verschieben.</span><span class="sxs-lookup"><span data-stu-id="a30e4-118">With the **TBS\_REVERSED** style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns one hundred (100) when the trackbar thumb is at the left; the values decrease as you move the trackbar thumb to the right.</span></span>

 

 




