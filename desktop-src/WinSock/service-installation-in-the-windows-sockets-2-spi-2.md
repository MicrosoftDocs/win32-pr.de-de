---
description: Dienst Installation in Windows Sockets 2 (Winsock) SPI.
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Dienst Installation in Windows Sockets 2 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9028f35c21cc7055e8b8dde060c1c178dbf76715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367860"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a><span data-ttu-id="df2cc-103">Dienst Installation in Windows Sockets 2 SPI</span><span class="sxs-lookup"><span data-stu-id="df2cc-103">Service Installation in the Windows Sockets 2 SPI</span></span>

-   [<span data-ttu-id="df2cc-104">**Nspinstallserviceclass**</span><span class="sxs-lookup"><span data-stu-id="df2cc-104">**NSPInstallServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [<span data-ttu-id="df2cc-105">**N-viveserviceclass**</span><span class="sxs-lookup"><span data-stu-id="df2cc-105">**NSPRemoveServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [<span data-ttu-id="df2cc-106">**Nspsetservice**</span><span class="sxs-lookup"><span data-stu-id="df2cc-106">**NSPSetService**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

<span data-ttu-id="df2cc-107">Wenn die erforderliche Dienstklasse nicht bereits vorhanden ist, verwendet ein Namespace-SPI-Client [**nspinstallserviceclass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) zum Installieren einer neuen Dienstklasse, indem ein Dienst Klassenname, eine GUID für den Dienst Klassen Bezeichner und eine Reihe von [**wsansclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) -Strukturen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="df2cc-107">When the required service class does not already exist, a namespace SPI client uses [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="df2cc-108">Diese Strukturen sind jeweils spezifisch für einen bestimmten Namespace und geben allgemeine Werte wie empfohlene TCP-Portnummern oder NetWare-SAP-IDs an.</span><span class="sxs-lookup"><span data-stu-id="df2cc-108">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="df2cc-109">Eine Dienstklasse kann durch Aufrufen von [**nspree-veserviceclass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) entfernt werden und stellt die GUID bereit, die dem Klassen Bezeichner entspricht.</span><span class="sxs-lookup"><span data-stu-id="df2cc-109">A service class can be removed by calling [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="df2cc-110">Sobald eine Dienstklasse vorhanden ist, können bestimmte Instanzen eines Dienstanbieter über [**nspsetservice**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)installiert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="df2cc-110">Once a service class exists, specific instances of a service can be installed or removed via [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice).</span></span> <span data-ttu-id="df2cc-111">Diese Funktion nimmt eine [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur als Eingabeparameter zusammen mit einem Vorgangs Code und Vorgangs Flags an.</span><span class="sxs-lookup"><span data-stu-id="df2cc-111">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="df2cc-112">Der Vorgangs Code gibt an, ob der Dienst installiert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="df2cc-112">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="df2cc-113">Die **wsaqueryset** -Struktur enthält alle relevanten Informationen über den Dienst, einschließlich der Dienst Klassen-ID, des Dienst namens (für diese Instanz), der anwendbaren Namespace-ID und der Protokollinformationen sowie einer Gruppe von Transport Adressen, die vom Dienst überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="df2cc-113">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses to which the service listens.</span></span>

 

 



