---
description: Protokoll unabhängige Namensauflösung und Windows Sockets (Winsock).
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Auflösung von Protocol-Independent Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cafed9759a4ca5431dafb230e7f09578ff1c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343478"
---
# <a name="protocol-independent-name-resolution"></a><span data-ttu-id="77072-103">Auflösung von Protocol-Independent Namen</span><span class="sxs-lookup"><span data-stu-id="77072-103">Protocol-Independent Name Resolution</span></span>

<span data-ttu-id="77072-104">Beim Entwickeln einer Protokoll unabhängigen Client/Server-Anwendung gibt es zwei grundlegende Anforderungen in Bezug auf die Namensauflösung und Registrierung:</span><span class="sxs-lookup"><span data-stu-id="77072-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="77072-105">Die Fähigkeit der Server Hälfte der Anwendung (Dienst), Ihr vorhanden sein in einem oder mehreren Namespaces zu registrieren (oder für Sie zugänglich).</span><span class="sxs-lookup"><span data-stu-id="77072-105">The ability of the server half of the application ( service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="77072-106">Die Fähigkeit der Client Anwendung, den Dienst innerhalb eines Namespace zu finden und das erforderliche Transportprotokoll und die Adressierungs Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="77072-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="77072-107">Für diejenigen, die an die Entwicklung von TCP/IP-basierten Anwendungen gewöhnt sind, kann dies anscheinend kaum mehr als die Suche nach einer Host Adresse und dann die Verwendung einer vereinbarten Portnummer bedeuten.</span><span class="sxs-lookup"><span data-stu-id="77072-107">For those accustomed to developing TCP/IP-based applications, this may seem to involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="77072-108">Andere Netzwerk Schemas ermöglichen jedoch den Speicherort des Dienstanbieter, das Protokoll, das für den Dienst verwendet wird, und andere Attribute, die zur Laufzeit ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="77072-108">Other networking schemes however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run time.</span></span> <span data-ttu-id="77072-109">Die Windows Sockets 2-Schnittstelle übernimmt das in den Themen in diesem Abschnitt beschriebene Modell, um die umfangreiche Vielfalt der in vorhandenen namens Diensten gefundenen Funktionen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="77072-109">To accommodate the broad diversity of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described in the topics in this section.</span></span>

<span data-ttu-id="77072-110">In diesem Abschnitt werden die Protokoll unabhängigen namens Auflösungs Funktionen beschrieben, die Winsock-Entwicklern zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="77072-110">This section describes protocol-independent name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="77072-111">In der folgenden Liste werden die Themen in diesem Abschnitt beschrieben:</span><span class="sxs-lookup"><span data-stu-id="77072-111">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="77072-112">Namens Auflösungs Modell</span><span class="sxs-lookup"><span data-stu-id="77072-112">Name Resolution Model</span></span>](name-resolution-model-2.md)
-   [<span data-ttu-id="77072-113">Zusammenfassung der namens Auflösungs Funktionen</span><span class="sxs-lookup"><span data-stu-id="77072-113">Summary of Name Resolution Functions</span></span>](summary-of-name-resolution-functions-2.md)
-   [<span data-ttu-id="77072-114">Datenstrukturen für die Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="77072-114">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)

## <a name="related-topics"></a><span data-ttu-id="77072-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="77072-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77072-116">Registrierung und Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="77072-116">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



