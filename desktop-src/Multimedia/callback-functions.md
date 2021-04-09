---
title: Rückruffunktionen
description: Rückruffunktionen
ms.assetid: d96e93e5-ebc9-4ad4-aaec-dcc4197a3fc5
keywords:
- installierbare Treiber, Rückruf Funktionen
- installierbare Treiber, drivercallback-Funktion
- installierbare Treiber, Ereignisse
- Drivercallback-Funktion
- DRV_OPEN Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e23f933567d125dd07f81047ea8868c12f41ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858234"
---
# <a name="callback-functions"></a><span data-ttu-id="952ff-108">Rückruffunktionen</span><span class="sxs-lookup"><span data-stu-id="952ff-108">Callback Functions</span></span>

<span data-ttu-id="952ff-109">Installierbare Treiber können die Anwendung, das Fenster oder den Task, der die angegebene Instanz zu Ereignissen geöffnet hat, mithilfe der [drivercallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) -Funktion benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="952ff-109">Installable drivers can notify the application, window, or task that opened the given instance about events by using the [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) function.</span></span> <span data-ttu-id="952ff-110">Diese Funktion ermöglicht dem Treiber das Zurückgeben von Informationen an eine Anwendung oder dll, während eine Anforderung weiterhin verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="952ff-110">This function gives the driver the means to return information to an application or DLL while continuing to process a request.</span></span>

<span data-ttu-id="952ff-111">Wenn ein Treiber Rückruf Funktionen unterstützt, muss die Anwendung oder dll, die die Instanz öffnet, einen Wert bereitstellen, der entweder die Adresse einer Rückruffunktion, ein Fenster Handle oder ein Task Handle ist.</span><span class="sxs-lookup"><span data-stu-id="952ff-111">If a driver supports callback functions, the application or DLL that opens the instance must supply a value this is either the address of a callback function, a window handle, or a task handle.</span></span> <span data-ttu-id="952ff-112">Dieser Wert und ein Flag, das den Typ des Werts identifiziert, werden in der Regel in einer Struktur übergeben, auf die der zweite Parameter der von [**drv \_ geöffneten**](drv-open.md) Nachricht zeigt.</span><span class="sxs-lookup"><span data-stu-id="952ff-112">This value and a flag identifying the type of the value are typically passed in a structure pointed to by the second parameter of the [**DRV\_OPEN**](drv-open.md) message.</span></span>

 

 