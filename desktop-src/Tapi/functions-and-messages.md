---
description: Die phonedevspecific-Funktion und die zugehörige Phone \_ DevSpecific-Nachricht ermöglichen einer Anwendung den Zugriff auf gerätespezifische Telefon Features, die über die gemeinsamen Telefoniedienste für Smartphones nicht verfügbar sind.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Funktionen und Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f85e2ea57ac11da8150d4d0a183c7c4fd2c88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959715"
---
# <a name="functions-and-messages"></a><span data-ttu-id="74e18-103">Funktionen und Nachrichten</span><span class="sxs-lookup"><span data-stu-id="74e18-103">Functions and Messages</span></span>

<span data-ttu-id="74e18-104">Die [**phonedevspecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) -Funktion und die zugehörige [**Phone \_ DevSpecific**](phone-devspecific.md) -Nachricht ermöglichen einer Anwendung den Zugriff auf gerätespezifische Telefon Features, die über die gemeinsamen Telefoniedienste für Smartphones nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="74e18-104">The [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function and its associated [**PHONE\_DEVSPECIFIC**](phone-devspecific.md) message enable an application to access device-specific phone features that are unavailable through the common telephony services for phones.</span></span> <span data-ttu-id="74e18-105">Mit anderen Worten: **phonedevspecific** ist die gerätespezifische Escape-Funktion, die Hersteller abhängige Erweiterungen zulässt, und Phone \_ DevSpecific ist die gerätespezifische Nachricht, die an die Anwendung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="74e18-105">In other words, **phoneDevSpecific** is the device-specific escape function that allows vendor-dependent extensions, and PHONE\_DEVSPECIFIC is the device-specific message that is sent to the application.</span></span>

<span data-ttu-id="74e18-106">Das Parameter Profil der [**phonedevspecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) -Funktion ist generisch, da die Parameter von TAPI nicht interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="74e18-106">The parameter profile of the [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function is generic in that little interpretation of the parameters is made by TAPI.</span></span> <span data-ttu-id="74e18-107">Stattdessen wird die Interpretation der Parameter vom Dienstanbieter definiert und muss von einer Anwendung verstanden werden, die Sie verwendet.</span><span class="sxs-lookup"><span data-stu-id="74e18-107">Rather, the interpretation of the parameters is defined by the service provider and must be understood by an application that uses them.</span></span> <span data-ttu-id="74e18-108">Die Parameter werden einfach von TAPI von der Anwendung an den Dienstanbieter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="74e18-108">The parameters are simply passed through by TAPI from the application to the service provider.</span></span> <span data-ttu-id="74e18-109">Eine Anwendung, die auf gerätespezifischen Erweiterungen basiert, funktioniert in der Regel nicht mit anderen Dienstanbietern, aber Anwendungen, die in die üblichen Telefoniedienste geschrieben werden, funktionieren mit dem erweiterten Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="74e18-109">An application that relies on device-specific extensions will usually not work with other service providers, but applications written to the common telephony phone services will work with the extended service provider.</span></span>

 

 



