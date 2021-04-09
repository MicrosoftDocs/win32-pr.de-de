---
title: RAS-Schnittstellen
description: Eine Schnittstelle stellt ein Netzwerk dar, das über ein LAN oder einen WAN-Adapter erreicht werden kann.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea285a625377709a4eca3bc8b9947106c2f5cfd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "103857835"
---
# <a name="ras-interfaces"></a><span data-ttu-id="51b29-103">RAS-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="51b29-103">RAS interfaces</span></span>

<span data-ttu-id="51b29-104">Eine Schnittstelle stellt ein Netzwerk dar, das über ein LAN oder einen WAN-Adapter erreicht werden kann.</span><span class="sxs-lookup"><span data-stu-id="51b29-104">An interface represents a network that can be reached over a LAN or WAN adapter.</span></span> <span data-ttu-id="51b29-105">Jede Schnittstelle verfügt über einen eindeutigen Bezeichner auf dem Router.</span><span class="sxs-lookup"><span data-stu-id="51b29-105">Each interface has a unique identifier on the router.</span></span> <span data-ttu-id="51b29-106">Aktive Schnittstellen verfügen über einen Adapter, der Konnektivität mit dem Netzwerk bereitstellt, das Sie darstellen.</span><span class="sxs-lookup"><span data-stu-id="51b29-106">Interfaces that are active have an adapter that is providing connectivity to the network they represent.</span></span> <span data-ttu-id="51b29-107">Inaktive Schnittstellen verfügen über keinen Adapter, der Konnektivität bereitstellt, es sei denn, ein Administrator hat die Schnittstelle deaktiviert, nachdem Sie bereits einen Adapter besaß.</span><span class="sxs-lookup"><span data-stu-id="51b29-107">Interfaces that are inactive do not have an adapter providing connectivity, unless an administrator disabled the interface after it already had an adapter.</span></span>

<span data-ttu-id="51b29-108">Das Routing eines Pakets an ein Netzwerk, das durch eine Schnittstelle dargestellt wird, weist den Router an, einen Adapter für diese Schnittstelle zuzuweisen und eine WAN-Verbindung mit dem Remote Netzwerk herzustellen.</span><span class="sxs-lookup"><span data-stu-id="51b29-108">Routing a packet to a network represented by an interface will cause the router to allocate an adapter for that interface, and establish a WAN connection to the remote network.</span></span> <span data-ttu-id="51b29-109">Das Zuordnen eines Adapters zu einer Schnittstelle wird als *Bindung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="51b29-109">Allocating an adapter to an interface is referred to as *binding*.</span></span>

<span data-ttu-id="51b29-110">Schnittstellen sind verwaltbare Objekte.</span><span class="sxs-lookup"><span data-stu-id="51b29-110">Interfaces are manageable objects.</span></span> <span data-ttu-id="51b29-111">Jede Schnittstelle wird als Zeile in der Schnittstellen Tabelle der entsprechenden SNMP-MIB angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51b29-111">Each interface appears as a row in the Interface Table of the appropriate SNMP MIB.</span></span>