---
title: Auswählen des Typs der zu verwendenden Bindungs Handles
description: Auswählen des Typs der zu verwendenden Bindungs Handles
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd07716b3618766b3ea8aa07fb766f154285207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036676"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a><span data-ttu-id="373c9-103">Auswählen des Typs der zu verwendenden Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="373c9-103">Choosing the Type of Binding Handles to Use</span></span>

<span data-ttu-id="373c9-104">**Bewährte Methoden:** Wenn Sie wissen, welcher Server von der Anwendung verwendet werden soll, verwenden Sie explizite Handles.</span><span class="sxs-lookup"><span data-stu-id="373c9-104">**Best practice:** If you know which server the application will use, use explicit handles.</span></span> <span data-ttu-id="373c9-105">Wenn Sie dies nicht tun, verwenden Sie jedes Mal explizite Handles, oder verwenden Sie generische Handles mit **\_ Bindungs** -und **\_ Bindung** -Routinen.</span><span class="sxs-lookup"><span data-stu-id="373c9-105">If you don't, use explicit handles construct every time, or use generic handles with **\_bind** and **\_unbind** routines.</span></span>

<span data-ttu-id="373c9-106">Verwenden Sie keine impliziten Handles oder automatischen Handles.</span><span class="sxs-lookup"><span data-stu-id="373c9-106">Do not use implicit handles or auto handles.</span></span> <span data-ttu-id="373c9-107">Implizite Handles sind nicht Thread sicher, und auch wenn die Thread Sicherheit unnötig erscheinen mag, könnte Sie später erforderlich werden.</span><span class="sxs-lookup"><span data-stu-id="373c9-107">Implicit handles are not thread safe, and even though thread safety may seem unnecessary, it could become necessary later.</span></span> <span data-ttu-id="373c9-108">Automatische Handles haben einen hohen Verwaltungsaufwand und erfordern eine Menge an Setup, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="373c9-108">Auto handles have large overhead and require a lot of setup to work properly.</span></span> <span data-ttu-id="373c9-109">Die Suchfunktionen wurden durch Active Directory Dienste abgelöst.</span><span class="sxs-lookup"><span data-stu-id="373c9-109">Their search capabilities have been superseded by Active Directory services.</span></span>

<span data-ttu-id="373c9-110">Explizite Handles sind sehr effizient, und viele attraktive Funktionen sind nur für explizite Handles verfügbar.</span><span class="sxs-lookup"><span data-stu-id="373c9-110">Explicit handles are highly efficient, and many attractive capabilities are available only for explicit handles.</span></span> <span data-ttu-id="373c9-111">Wenn z. b. mehrere RPC-Aufrufe an denselben Server weitergeben, können Sie das Bindungs handle einmal erstellen und alle Aufrufe damit ausführen.</span><span class="sxs-lookup"><span data-stu-id="373c9-111">For example, if several RPC calls will be going to the same server, you can construct the binding handle once and make all calls with it.</span></span> <span data-ttu-id="373c9-112">Diese Vorgehensweise ist viel effizienter als jede andere Methode.</span><span class="sxs-lookup"><span data-stu-id="373c9-112">This approach is much more efficient than any other method.</span></span> <span data-ttu-id="373c9-113">Wenn der Server, zu dem der-Vorgang gehört, unbekannt ist, erstellen Sie für jeden-Rückruf ein explizites Bindungs handle, oder verwenden Sie generische Bindungs Handles.</span><span class="sxs-lookup"><span data-stu-id="373c9-113">If the server to which the call will go is unknown, construct an explicit binding handle for every call, or use generic binding handles.</span></span>

<span data-ttu-id="373c9-114">In Microsoft™ Windows XP ist die RPC-Laufzeit sehr effizient bei der Wiederverwendung und Zwischenspeicherung von aufrufen. Wenn also der Aufruf von " *n*+ 1" auf dem gleichen Server wie der *n*-te Aufruf läuft, verwendet RPC die für den *n*-ten Aufruf zugeordneten Ressourcen erneut, wodurch die Notwendigkeit zum Zwischenspeichern von Bindungs Handles umgangen wird, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="373c9-114">In Microsoft™ Windows XP, the RPC run time is quite efficient in re-using and caching calls, so if the *n*+1st call ends up on the same server as the *n* th call, RPC re-uses the resources allocated for the *n* th call, circumventing the need to cache binding handles to improve performance.</span></span>

 

 




