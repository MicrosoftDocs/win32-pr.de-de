---
title: Direct2D debugschicht
description: Eine Lauf Zeit Erweiterung für Direct2D, die beschreibende Fehlermeldungen, Erkennung von Objekt Lecks, Leistungs Hinweise und andere Hinweise bietet, die Sie beim Erstellen von Direct2D-apps unterstützen.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f71b1364e645859059fb090634cbdae6f8c084e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388046"
---
# <a name="direct2d-debug-layer"></a><span data-ttu-id="f7c2f-103">Direct2D debugschicht</span><span class="sxs-lookup"><span data-stu-id="f7c2f-103">Direct2D Debug Layer</span></span>

## <a name="purpose"></a><span data-ttu-id="f7c2f-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="f7c2f-104">Purpose</span></span>

<span data-ttu-id="f7c2f-105">Die Direct2D-debugschicht, die separat von Direct2D in der eigenen dll mit dem Namen d2d1debug.dll implementiert wurde, stellt Entwurfszeit-Debugmeldungen bereit, um den Lauf Zeit Anwendungsfehler zu minimieren</span><span class="sxs-lookup"><span data-stu-id="f7c2f-105">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="f7c2f-106">Die Debugmeldungen resultieren häufig aus Verstößen gegen API-Verträge, wie z. b. ungültige Parameter (Direct3D-bezogen), ungültigen Ressourcen, Threading Verstößen und anderen Leistungsproblemen, wie z. b. der Verwendung einer Ebene, wenn ein Clip ausreichen würde.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-106">The debug messages often result from violations of API contracts such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and other performance issues such as using a layer when a clip would suffice.</span></span>

<span data-ttu-id="f7c2f-107">Um Ihnen bei der Entscheidung zu helfen, wie viele Informationen von der debugschicht verfolgt werden, bietet die debugschicht drei debugebenen: Information, Warnung und Fehler.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-107">To help you decide how much information is traced by the debug layer, the debug layer offers three debug levels: information, warning, and error.</span></span> <span data-ttu-id="f7c2f-108">Diese drei Ebenen werden wie folgt interpretiert:</span><span class="sxs-lookup"><span data-stu-id="f7c2f-108">These three levels are interpreted as follows:</span></span>

-   <span data-ttu-id="f7c2f-109">**Fehler:** Direct2D sendet schwerwiegende Fehlermeldungen an die debugschicht.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-109">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="f7c2f-110">Beispielsweise wird durch das Unterbrechen einer Threading Einschränkung ein schwerwiegender Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-110">For example, breaking a threading constraint will generate a severe error.</span></span>

    <span data-ttu-id="f7c2f-111">Außerdem löst eine Meldung vom Typ Fehler den Haltepunkt aus, um Sie beim Debuggen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-111">Further, a message of level error triggers the breakpoint to help you debug.</span></span>

-   <span data-ttu-id="f7c2f-112">**Warnung:** Direct2D sendet Fehlermeldungen und Warnungen an die debugschicht, damit Sie diese Nachrichten adressieren können.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-112">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="f7c2f-113">**Informationen:** Direct2D sendet Fehlermeldungen, Warnungen und zusätzliche Diagnoseinformationen an die debugschicht.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-113">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="f7c2f-114">Beispielsweise werden Meldungen zur Leistungsverbesserung auf dieser Debugebene gesendet.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-114">For example, performance improvement messages will be sent at this debug level.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f7c2f-115">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f7c2f-115">In this section</span></span>



| <span data-ttu-id="f7c2f-116">Thema</span><span class="sxs-lookup"><span data-stu-id="f7c2f-116">Topic</span></span>                                                                                     | <span data-ttu-id="f7c2f-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7c2f-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="f7c2f-118">Installieren der Direct2D Debug-Ebene</span><span class="sxs-lookup"><span data-stu-id="f7c2f-118">Installing the Direct2D Debug Layer</span></span>](installing-the-direct2d-debug-layer.md)<br/> | <span data-ttu-id="f7c2f-119">Beschreibt, wie die Direct2D-debugschicht installiert wird.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-119">Describes how to install the Direct2D debug layer.</span></span><br/>      |
| [<span data-ttu-id="f7c2f-120">Direct2D Übersicht über die Debug-Ebene</span><span class="sxs-lookup"><span data-stu-id="f7c2f-120">Direct2D Debug Layer Overview</span></span>](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [<span data-ttu-id="f7c2f-121">Debugmeldungen</span><span class="sxs-lookup"><span data-stu-id="f7c2f-121">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)<br/>                         | <span data-ttu-id="f7c2f-122">Listet die Debugmeldungen von der Direct2D Debug-Ebene auf.</span><span class="sxs-lookup"><span data-stu-id="f7c2f-122">Lists the debug messages from the Direct2D Debug Layer.</span></span><br/> |



 

 

 





