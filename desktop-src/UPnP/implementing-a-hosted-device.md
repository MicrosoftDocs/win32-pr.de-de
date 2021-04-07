---
title: Implementieren eines gehosteten Geräts
description: Der Geräte Host mit der UPnP-Technologie implementiert die zentralen UPnP-Protokolle Ermittlung, Beschreibung, Steuerung und Ereignis Ereignisse.
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172e9935dcbca73dbb285ba73270375fb5bfb6cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713577"
---
# <a name="implementing-a-hosted-device"></a><span data-ttu-id="9d684-103">Implementieren eines gehosteten Geräts</span><span class="sxs-lookup"><span data-stu-id="9d684-103">Implementing a Hosted Device</span></span>

<span data-ttu-id="9d684-104">Der Geräte Host mit der UPnP-Technologie implementiert die zentralen UPnP-Protokolle: Ermittlung, Beschreibung, Steuerung und Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="9d684-104">The device host with UPnP technology implements the core UPnP protocols: discovery, description, control, and eventing.</span></span> <span data-ttu-id="9d684-105">Der Entwickler, der ein gehosteter Gerät implementiert, muss nur Folgendes bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="9d684-105">The developer who implements a hosted device only needs to provide:</span></span>

-   <span data-ttu-id="9d684-106">Eine Beschreibung des Geräts und seiner Dienste.</span><span class="sxs-lookup"><span data-stu-id="9d684-106">A description of the device and its services.</span></span>
-   <span data-ttu-id="9d684-107">Eine Implementierung der Funktionalität des Geräts.</span><span class="sxs-lookup"><span data-stu-id="9d684-107">An implementation of the device's functionality.</span></span>

<span data-ttu-id="9d684-108">Beispielsweise muss der Entwickler eines uhrgeräts UPnP-basierte Geräte-und Dienst Beschreibungen für das Gerät und eine Implementierung der Clock-Funktionen bereitstellen (z. b. die Zeit, die Festlegung der Zeit und die Reaktion auf Abfragen für die aktuelle Zeit).</span><span class="sxs-lookup"><span data-stu-id="9d684-108">For example, the developer of a clock device must provide UPnP-based device and service descriptions for it, and an implementation of the clock functions (such as keeping time, setting time, and responding to queries for the current time).</span></span> <span data-ttu-id="9d684-109">Geräte Host:</span><span class="sxs-lookup"><span data-stu-id="9d684-109">The device host:</span></span>

-   <span data-ttu-id="9d684-110">Kündigt das Gerät gemäß dem UPnP Discovery-Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="9d684-110">Announces the device according to the UPnP discovery protocol.</span></span>
-   <span data-ttu-id="9d684-111">Reagiert auf Abfragen für die Beschreibung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="9d684-111">Responds to queries for the device's description.</span></span>
-   <span data-ttu-id="9d684-112">Leitet Steuerungsanforderungen an den Teil des Geräte Codes weiter, der die Clock-Funktionen implementiert.</span><span class="sxs-lookup"><span data-stu-id="9d684-112">Routes control requests to the part of the device's code that implements the clock functions.</span></span>
-   <span data-ttu-id="9d684-113">Verwaltet Ereignis Abonnements für Dienste.</span><span class="sxs-lookup"><span data-stu-id="9d684-113">Maintains event subscriptions to services.</span></span>
-   <span data-ttu-id="9d684-114">Sendet Ereignis Benachrichtigungen an Abonnenten, wenn sich der Dienststatus ändert.</span><span class="sxs-lookup"><span data-stu-id="9d684-114">Sends event notifications to subscribers when the service's state changes.</span></span>

 

 




