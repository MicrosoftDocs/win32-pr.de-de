---
title: Bluetooth und getaddrinfo
description: Die getaddrinfo-Funktion ermöglicht die Übersetzung von Hostnamen in Adressen für IP-basierte Transporte. Da die getaddrinfo-Funktion spezifisch für IP-basierte Transporte ist, schlägt Sie an Bluetooth-Sockets fehl.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth und getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c2e62b83ac947b74479ff435b93914661aa8da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729849"
---
# <a name="bluetooth-and-getaddrinfo"></a><span data-ttu-id="5e144-105">Bluetooth und getaddrinfo</span><span class="sxs-lookup"><span data-stu-id="5e144-105">Bluetooth and getaddrinfo</span></span>

<span data-ttu-id="5e144-106">Die [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion ermöglicht die Übersetzung von Hostnamen in Adressen für IP-basierte Transporte.</span><span class="sxs-lookup"><span data-stu-id="5e144-106">The [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) function provides translation from host name to address for IP-based transports.</span></span> <span data-ttu-id="5e144-107">Da die **getaddrinfo** -Funktion spezifisch für IP-basierte Transporte ist, schlägt Sie an Bluetooth-Sockets fehl.</span><span class="sxs-lookup"><span data-stu-id="5e144-107">Because the **getaddrinfo** function is specific to IP-based transports, it fails on Bluetooth sockets.</span></span>

<span data-ttu-id="5e144-108">Um die Übersetzung vom Hostnamen zur Adresse für Bluetooth-Sockets auszuführen, verwenden Sie die [**wsalookupservicebegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) -Funktion mit **\_ lupcontainern** , um Remote Geräte abzufragen, und suchen Sie dann nach einem bestimmten Remote Namen und der entsprechenden Adresse.</span><span class="sxs-lookup"><span data-stu-id="5e144-108">To perform translation from host name to address for Bluetooth sockets, use the [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) function with **LUP\_CONTAINERS** to query remote devices, then search for a specific matching Remote Name and corresponding address.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e144-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e144-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e144-110">Windows-Sockets</span><span class="sxs-lookup"><span data-stu-id="5e144-110">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="5e144-111">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="5e144-111">**getaddrinfo**</span></span>](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[<span data-ttu-id="5e144-112">**Wsalookupservicebegin**</span><span class="sxs-lookup"><span data-stu-id="5e144-112">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 