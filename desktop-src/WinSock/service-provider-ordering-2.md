---
description: Die Reihenfolge, in der Transport Dienstanbieter anfänglich installiert werden, steuert die Reihenfolge, in der Sie über wscenumprotokolls und WSCEnumProtocols32 an der Dienstanbieter Schnittstelle oder über wsaenumprotokolls auf der Anwendungs Schnittstelle aufgelistet werden. Noch wichtiger ist, dass diese Reihenfolge auch die Reihenfolge bestimmt, in der Protokolle und Dienstanbieter berücksichtigt werden, wenn ein Client die Erstellung eines Sockets basierend auf der Adressfamilie, dem Typ und der Protokoll Kennung anfordert.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Dienstanbieter-Reihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c23d9357d30c94b084bf6288013c38a2d46a4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863811"
---
# <a name="service-provider-ordering"></a><span data-ttu-id="537af-104">Dienstanbieter-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="537af-104">Service Provider Ordering</span></span>

<span data-ttu-id="537af-105">Die Reihenfolge, in der Transport Dienstanbieter anfänglich installiert werden, steuert die Reihenfolge, in der Sie über [**wscenumprotokolls**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) und [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) an der Dienstanbieter Schnittstelle oder über [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) auf der Anwendungs Schnittstelle aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="537af-105">The order in which transport service providers are initially installed governs the order in which they are enumerated through [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) and [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) at the service provider interface, or through [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) at the application interface.</span></span> <span data-ttu-id="537af-106">Noch wichtiger ist, dass diese Reihenfolge auch die Reihenfolge bestimmt, in der Protokolle und Dienstanbieter berücksichtigt werden, wenn ein Client die Erstellung eines Sockets basierend auf der Adressfamilie, dem Typ und der Protokoll Kennung anfordert.</span><span class="sxs-lookup"><span data-stu-id="537af-106">More importantly, this order also governs the order in which protocols and service providers are considered when a client requests creation of a socket based on its address family, type, and protocol identifier.</span></span>

<span data-ttu-id="537af-107">Windows Sockets 2 enthält ein Applet namens Sporder.exe, mit dem der Katalog installierter Protokolle interaktiv neu angeordnet werden kann, nachdem Protokolle bereits installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="537af-107">Windows Sockets 2 includes an applet called Sporder.exe that allows the catalog of installed protocols to be reordered interactively after protocols have already been installed.</span></span> <span data-ttu-id="537af-108">Winsock umfasst auch eine zusätzliche dll, Sporder.dll, die eine prozedurale Schnittstelle zum Neuanordnen von Protokollen exportiert.</span><span class="sxs-lookup"><span data-stu-id="537af-108">Winsock also includes an auxiliary DLL, Sporder.dll, that exports a procedural interface for reordering protocols.</span></span> <span data-ttu-id="537af-109">Diese prozedurale Schnittstelle besteht aus einer einzelnen Prozedur namens [**wscschreiteproviderorder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).</span><span class="sxs-lookup"><span data-stu-id="537af-109">This procedural interface consists of a single procedure called [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).</span></span>

<span data-ttu-id="537af-110">Die Schnittstellen Definition kann mithilfe der Includedatei sporder. h in ein C-oder C++-Programm importiert werden.</span><span class="sxs-lookup"><span data-stu-id="537af-110">The interface definition may be imported into a C or C++ program by means of the include file Sporder.h.</span></span> <span data-ttu-id="537af-111">Der Einstiegspunkt kann mithilfe der LIB-Datei sporder. lib verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="537af-111">The entry point may be linked by means of the lib file Sporder.lib.</span></span>

 

 



