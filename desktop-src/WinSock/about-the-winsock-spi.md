---
description: Winsock stellt eine Dienstanbieter Schnittstelle zum Erstellen von Winsock-Diensten bereit, die häufig als Winsock SPI bezeichnet werden.
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: Informationen über die Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe70d5d381505085e2794a57a1183e8bec505917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129232"
---
# <a name="about-the-winsock-spi"></a><span data-ttu-id="22b20-103">Informationen über die Winsock SPI</span><span class="sxs-lookup"><span data-stu-id="22b20-103">About the Winsock SPI</span></span>

<span data-ttu-id="22b20-104">Winsock stellt eine Dienstanbieter Schnittstelle zum Erstellen von Winsock-Diensten bereit, die häufig als Winsock SPI bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="22b20-104">Winsock provides a Service Provider Interface for creating Winsock services, commonly referred to as the Winsock SPI.</span></span> <span data-ttu-id="22b20-105">Es gibt zwei Typen von Dienstanbietern: Transportanbieter und Namespace Anbieter.</span><span class="sxs-lookup"><span data-stu-id="22b20-105">Two types of service providers exist: transport providers and namespace providers.</span></span> <span data-ttu-id="22b20-106">Beispiele für Transportanbieter sind Protokollstapel wie z. b. TCP/IP oder IPX/SPX. ein Beispiel für einen Namespace Anbieter wäre eine Schnittstelle zum DNS (Domain Naming System) des Internets.</span><span class="sxs-lookup"><span data-stu-id="22b20-106">Examples of transport providers include protocol stacks such as TCP/IP or IPX/SPX, while an example of a namespace provider would be an interface to the Internet's Domain Naming System (DNS).</span></span> <span data-ttu-id="22b20-107">Separate Abschnitte der Dienstanbieter Schnittstellen Spezifikation gelten für jeden Dienst Anbietertyp.</span><span class="sxs-lookup"><span data-stu-id="22b20-107">Separate sections of the service provider interface specification apply to each type of service provider.</span></span>

<span data-ttu-id="22b20-108">[Transport](transport-service-providers-2.md) -und [Namespace](name-space-service-providers-2.md) -Dienstanbieter müssen bei der Ws2- \_32.dll zum Zeitpunkt der Installation registriert werden.</span><span class="sxs-lookup"><span data-stu-id="22b20-108">[Transport](transport-service-providers-2.md) and [namespace](name-space-service-providers-2.md) service providers must be registered with the Ws2\_32.dll at the time they are installed.</span></span> <span data-ttu-id="22b20-109">Diese Registrierung muss nur einmal für jeden Anbieter durchgeführt werden, da die erforderlichen Informationen im persistenten Speicher aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="22b20-109">This registration need only be done once for each provider as the necessary information is retained in persistent storage.</span></span>

 

 



