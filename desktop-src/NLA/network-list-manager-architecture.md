---
title: Netzwerk Listen-Manager-Architektur
description: Netzwerk Listen-Manager-Architektur
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567b103cfd5d9944aa33a799c2cc1bc4b983759
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948073"
---
# <a name="network-list-manager-architecture"></a><span data-ttu-id="20481-103">Netzwerk Listen-Manager-Architektur</span><span class="sxs-lookup"><span data-stu-id="20481-103">Network List Manager Architecture</span></span>

<span data-ttu-id="20481-104">Der Netzwerk Listen-Manager wird im Zusammenhang mit Svchost.exe als Dienst ausgeführt und während der Computer Start Prozedur gestartet.</span><span class="sxs-lookup"><span data-stu-id="20481-104">Network List Manager runs as a service in the context of Svchost.exe and is started during the computer boot procedure.</span></span> <span data-ttu-id="20481-105">Der Netzwerk Listen-Manager-Dienst verwaltet eine Tabelle mit verfügbaren Netzwerken und Netzwerk Attributen, die von Anwendungen über die Netzwerk Listen-Manager-API abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="20481-105">The Network List Manager service maintains a table of available networks and network attributes that are retrieved by applications through the Network List Manager API.</span></span> <span data-ttu-id="20481-106">Der Netzwerk Listen-Manager stellt grundlegende Funktionen zum Filtern und Abfragen des Netzwerk Listen-Manager-Dienstanbieter für bestimmte Netzwerke und zum Abrufen der Attribute dieser Netzwerke bereit.</span><span class="sxs-lookup"><span data-stu-id="20481-106">Network List Manager provides basic functions to filter and query the Network List Manager service for specific networks and retrieve the attributes of these networks.</span></span> <span data-ttu-id="20481-107">Das folgende Diagramm zeigt die Architektur des Netzwerk Listen-Managers und die Interaktion zwischen dem Netzwerk Listen-Manager-Dienst und der Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="20481-107">The following diagram shows the Network List Manager architecture and the interaction between the Network List Manager service and the client application.</span></span>

![Diagramm zur Netzwerk Bewusstsein-Architektur](images/architecture.png)

 

 




