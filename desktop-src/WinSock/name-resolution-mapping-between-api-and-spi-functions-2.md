---
description: Die Installation von Dienst Klassen, die Registrierung von Dienst Instanzen und grundlegenden Abfrage Vorgängen werden direkt direkt von der API zum SPI zugeordnet.
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: Namens Auflösungs Zuordnung zwischen API-und SPI-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a031ea8af72bb2733fc647c817a850ab7f311b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862556"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a><span data-ttu-id="1c65f-103">Namens Auflösungs Zuordnung zwischen API-und SPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1c65f-103">Name Resolution Mapping Between API and SPI Functions</span></span>

<span data-ttu-id="1c65f-104">Die Installation von Dienst Klassen, die Registrierung von Dienst Instanzen und grundlegenden Abfrage Vorgängen werden direkt direkt von der API zum SPI zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1c65f-104">The installation of service classes, registration of service instances and basic query operations all map fairly directly from the API to the SPI.</span></span> <span data-ttu-id="1c65f-105">Die [**wsagetserviceclassnamebyclassid-**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) Funktion verfügt nicht über eine entsprechende Funktion in der SPI, da diese Funktion in32.dll Ws2 implementiert wird, \_ indem Sie [**nspgetserviceclassinfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)aufruft.</span><span class="sxs-lookup"><span data-stu-id="1c65f-105">The [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) function does not have a corresponding function in the SPI, as this function is implemented in Ws2\_32.dll by making a call to [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).</span></span>

<span data-ttu-id="1c65f-106">Die Hilfsfunktionen [**wsaadresssstostring**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) und [**wsastringtoaddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) werden den entsprechenden Funktionen in der Transport-API zugeordnet, da nur ein Transportanbieter notwendigerweise weiß, wie die Übersetzung in einer [**sockaddr**](sockaddr-2.md) -Struktur durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c65f-106">The helper functions [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) and [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) are mapped to the corresponding functions in the transport API, as only a transport provider will necessarily know how to perform the translation on a [**sockaddr**](sockaddr-2.md) structure.</span></span>

 

 



