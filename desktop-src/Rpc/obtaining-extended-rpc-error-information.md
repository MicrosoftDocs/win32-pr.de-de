---
title: Abrufen erweiterter RPC-Fehlerinformationen
description: RPC bietet die Möglichkeit, erweiterte Fehlerinformationen zu erhalten. In diesem Abschnitt wird beschrieben, wie solche Fehlerinformationen abgerufen werden können, und es werden Empfehlungen zur Verwendung der Informationen angezeigt.
ms.assetid: 7a386def-c640-42f4-9869-b6a1c522984a
keywords:
- Remote Prozedur Aufruf RPC, bewährte Methoden, erweiterte Fehlerinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7856dd76a86763fc3f537577f9c547508fbf34ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710416"
---
# <a name="obtaining-extended-rpc-error-information"></a><span data-ttu-id="cfccf-105">Abrufen erweiterter RPC-Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="cfccf-105">Obtaining Extended RPC Error Information</span></span>

<span data-ttu-id="cfccf-106">RPC bietet die Möglichkeit, erweiterte Fehlerinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cfccf-106">RPC provides the capability to obtain extended error information.</span></span> <span data-ttu-id="cfccf-107">In diesem Abschnitt wird beschrieben, wie solche Fehlerinformationen abgerufen werden können, und es werden Empfehlungen zur Verwendung der Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cfccf-107">This section describes how such error information can be obtained, and offers recommendations on how to use the information.</span></span>

<span data-ttu-id="cfccf-108">Dieser Abschnitt ist in die folgenden Themen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="cfccf-108">This section is broken into the following topics:</span></span>

-   [<span data-ttu-id="cfccf-109">Der Bedarf an erweiterten Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="cfccf-109">The Need For Extended Error Information</span></span>](the-need-for-extended-error-information.md)
-   [<span data-ttu-id="cfccf-110">Sicherheit und erweiterte Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="cfccf-110">Security and Extended Error Information</span></span>](security-and-extended-error-information.md)
-   [<span data-ttu-id="cfccf-111">Aktivieren erweiterter Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="cfccf-111">Enabling Extended Error Information</span></span>](enabling-extended-error-information.md)
-   [<span data-ttu-id="cfccf-112">Grundlegendes zu erweiterten Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="cfccf-112">Understanding Extended Error Information</span></span>](understanding-extended-error-information.md)
-   [<span data-ttu-id="cfccf-113">Zuverlässigkeit erweiterter Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="cfccf-113">Reliability of Extended Error Information</span></span>](reliability-of-extended-error-information.md)
-   [<span data-ttu-id="cfccf-114">Unabhängigkeit von anderen Komponenten</span><span class="sxs-lookup"><span data-stu-id="cfccf-114">Independence From Other Components</span></span>](independence-from-other-components.md)
-   [<span data-ttu-id="cfccf-115">Erweiterte Fehlerinformationen für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="cfccf-115">Extended Error Information for the User</span></span>](extended-error-information-for-the-user.md)
-   [<span data-ttu-id="cfccf-116">Erweiterte Fehlerinformationen für den Server oder die Anwendung</span><span class="sxs-lookup"><span data-stu-id="cfccf-116">Extended Error Information for the Server or Application</span></span>](extended-error-information-for-the-server-or-application.md)
-   [<span data-ttu-id="cfccf-117">Speicherorte für erweiterte Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="cfccf-117">Extended Error Information Detection Locations</span></span>](extended-error-information-detection-locations.md)

<span data-ttu-id="cfccf-118">Dieser Abschnitt ist eng mit dem Debuggen von RPC-Anwendungen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="cfccf-118">This section is closely tied with RPC application debugging.</span></span> <span data-ttu-id="cfccf-119">Weitere Informationen zum RPC-Debuggen finden Sie unter \[ Debugger-Paket \] .</span><span class="sxs-lookup"><span data-stu-id="cfccf-119">For additional information about RPC debugging, see \[debugger package\].</span></span>

 

 




