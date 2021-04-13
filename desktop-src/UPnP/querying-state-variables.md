---
title: Abfragen von Zustandsvariablen
description: Die iupnpservice-Schnittstelle stellt die querystatevariable-Methode bereit, die den Wert einer angegebenen Zustandsvariablen zurückgibt.
ms.assetid: 9e8b98b0-488a-4f9c-9ad7-039dbd470486
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a716bbe93c2306eca43b977a42f33a85187f92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309836"
---
# <a name="querying-state-variables"></a><span data-ttu-id="7a52e-103">Abfragen von Zustandsvariablen</span><span class="sxs-lookup"><span data-stu-id="7a52e-103">Querying State Variables</span></span>

<span data-ttu-id="7a52e-104">Die [**iupnpservice**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) -Schnittstelle stellt die [**querystatevariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) -Methode bereit, die den Wert einer angegebenen Zustandsvariablen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7a52e-104">The [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface provides the [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) method, that returns the value of a specified state variable.</span></span>

<span data-ttu-id="7a52e-105">Das UPnP-Forum verhindert die Verwendung von [**QueryStatus-ariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable).</span><span class="sxs-lookup"><span data-stu-id="7a52e-105">The UPnP Forum discourages the use of [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable).</span></span> <span data-ttu-id="7a52e-106">Geräte Schreiber wurde empfohlen, geeignete Aktionen zu schreiben, um diese Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7a52e-106">Device writers have been encouraged to write appropriate actions to provide this information.</span></span> <span data-ttu-id="7a52e-107">Geräte Schreiber sind nicht verpflichtet, **QueryStatus-ariable** zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="7a52e-107">Device writers are under no obligation to implement **QueryStateVariable**.</span></span>

<span data-ttu-id="7a52e-108">Weitere Informationen finden Sie im Abschnitt [Aufrufen von Aktionen](invoking-actions.md).</span><span class="sxs-lookup"><span data-stu-id="7a52e-108">See the section [Invoking Actions](invoking-actions.md).</span></span>

 

 




