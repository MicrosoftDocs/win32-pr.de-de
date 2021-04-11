---
description: Namensauflösung und Registrierungs Modell für den Windows Sockets (Winsock) SPI.
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: Namens Auflösungs Modell für den SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e79593f56cd11671b3c16ef9098d455bf548505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129149"
---
# <a name="name-resolution-model-for-the-spi"></a><span data-ttu-id="e15b3-103">Namens Auflösungs Modell für den SPI</span><span class="sxs-lookup"><span data-stu-id="e15b3-103">Name Resolution Model for the SPI</span></span>

<span data-ttu-id="e15b3-104">Beim Entwickeln einer Protokoll unabhängigen Client/Server-Anwendung gibt es zwei grundlegende Anforderungen in Bezug auf die Namensauflösung und Registrierung:</span><span class="sxs-lookup"><span data-stu-id="e15b3-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="e15b3-105">Die Möglichkeit der Server Hälfte der Anwendung (im folgenden als Dienst bezeichnet), das vorhanden sein in einem oder mehreren Namespaces zu registrieren (oder für Sie zugänglich).</span><span class="sxs-lookup"><span data-stu-id="e15b3-105">The ability of the server half of the application (hereafter referred to as a service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="e15b3-106">Die Fähigkeit der Client Anwendung, den Dienst innerhalb eines Namespace zu finden und das erforderliche Transportprotokoll und die Adressierungs Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e15b3-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="e15b3-107">Für diejenigen, die an die Entwicklung von TCP/IP-basierten Anwendungen gewöhnt sind, kann dies möglicherweise kaum mehr als die Suche nach einer Host Adresse und dann die Verwendung einer vereinbarten Portnummer bedeuten.</span><span class="sxs-lookup"><span data-stu-id="e15b3-107">For those accustomed to developing TCP/IP-based applications, this may involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="e15b3-108">Andere Netzwerk Schemas ermöglichen jedoch den Speicherort des Dienstanbieter, das Protokoll, das für den Dienst verwendet wird, und andere Attribute, die zur Laufzeit ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="e15b3-108">Other networking schemes, however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run-time.</span></span> <span data-ttu-id="e15b3-109">Um den Umfang der in vorhandenen namens Diensten gefundenen Funktionen zu unterstützen, übernimmt die Windows Sockets 2-Schnittstelle das unten beschriebene Modell.</span><span class="sxs-lookup"><span data-stu-id="e15b3-109">To accommodate the range of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described below.</span></span>

<span data-ttu-id="e15b3-110">Ein *Namespace* bezieht sich auf eine Funktion, mit der (minimal) das Protokoll und die Adressierungs Attribute eines Netzwerk Dienstanbieter mit einem oder mehreren benutzerfreundlichen Namen verknüpft werden können.</span><span class="sxs-lookup"><span data-stu-id="e15b3-110">A *namespace* refers to some capability to associate (as a minimum) the protocol and addressing attributes of a network service with one or more human-friendly names.</span></span> <span data-ttu-id="e15b3-111">Derzeit werden viele Namespaces verwendet, einschließlich der Domain Name System des Internets (DNS), NetWare-Verzeichnisdienste (NDS), X. 500 usw. Diese Namespaces unterscheiden sich stark von der Organisation und Implementierung.</span><span class="sxs-lookup"><span data-stu-id="e15b3-111">Many namespaces are currently in wide use including the Internet's Domain Name System (DNS), NetWare Directory Services (NDS), X.500, etc. These namespaces vary widely in how they are organized and implemented.</span></span> <span data-ttu-id="e15b3-112">Einige der Eigenschaften sind besonders wichtig, um aus der Perspektive der Windows Sockets-Namensauflösung zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="e15b3-112">Some of their properties are particularly important to understand from the perspective of Windows Sockets name resolution.</span></span>

 

 



