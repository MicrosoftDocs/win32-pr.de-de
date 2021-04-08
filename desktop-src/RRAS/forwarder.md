---
title: Weiterleitung
description: Bei der Weiterleitung handelt es sich um die Kernelmoduskomponente des Routers, die für die Weiterleitung von Daten von einer Routerschnittstelle an andere zuständig ist.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52885000a9f1fcc117cd1fefc207531b9b524e74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037010"
---
# <a name="forwarder"></a><span data-ttu-id="d4cc5-103">Weiterleitung</span><span class="sxs-lookup"><span data-stu-id="d4cc5-103">Forwarder</span></span>

<span data-ttu-id="d4cc5-104">Bei der Weiterleitung handelt es sich um die Kernelmoduskomponente des Routers, die für die Weiterleitung von Daten von einer Routerschnittstelle an andere zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="d4cc5-104">The forwarder is the kernel-mode component of the router that is responsible for forwarding data from one router interface to the others.</span></span> <span data-ttu-id="d4cc5-105">Die Weiterleitung entscheidet auch, ob ein Paket für die lokale Übermittlung bestimmt ist, ob es für die Weiterleitung aus einer anderen Schnittstelle oder beides bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="d4cc5-105">The forwarder also decides whether a packet is destined for local delivery, whether it is destined to be forwarded out of another interface, or both.</span></span>

<span data-ttu-id="d4cc5-106">Es gibt zwei Weiterleitungen im kernelmodusmodus: Unicast und Multicast.</span><span class="sxs-lookup"><span data-stu-id="d4cc5-106">There are two kernel-mode forwarders: unicast and multicast.</span></span>

<span data-ttu-id="d4cc5-107">Der routermanager erhält die besten Routen für alle Ziele aus dem Routing Tabellen-Manager.</span><span class="sxs-lookup"><span data-stu-id="d4cc5-107">The router manager obtains the best routes to all destinations from the routing table manager.</span></span> <span data-ttu-id="d4cc5-108">Diese Routen werden an die Unicastweiterleitung übergeben.</span><span class="sxs-lookup"><span data-stu-id="d4cc5-108">These routes are passed to the unicast forwarder.</span></span> <span data-ttu-id="d4cc5-109">Die Unicastweiterleitung verwendet diese Routen, um die tatsächliche Weiterleitung von Unicastdaten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d4cc5-109">The unicast forwarder uses these routes to perform the actual forwarding of unicast data.</span></span> <span data-ttu-id="d4cc5-110">Auf diese Weise behält die Unicastweiterleitung einen Cache der besten Routen in der unicastansicht der Routing Tabelle bei.</span><span class="sxs-lookup"><span data-stu-id="d4cc5-110">In this manner, the unicast forwarder maintains a cache of the best routes in the unicast view of the routing table.</span></span>

<span data-ttu-id="d4cc5-111">Der Multicast-Gruppen-Manager verwendet Informationen aus der Multicast Ansicht der Routing Tabelle, um Multicast Weiterleitungs Einträge zur Multicast Weiterleitung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d4cc5-111">The multicast group manager uses information from the multicast view of the routing table to add multicast forwarding entries to the multicast forwarder.</span></span>

 

 




