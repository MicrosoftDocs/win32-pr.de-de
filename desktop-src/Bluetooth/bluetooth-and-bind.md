---
title: Bluetooth und BIND
description: Bluetooth verwendet die Bind-Funktion, um eine Bindung an einen Socket herzustellen.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth und BIND
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ccbd088ab61edcfa3dfc511ea591593d0cf781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858448"
---
# <a name="bluetooth-and-bind"></a><span data-ttu-id="e2664-107">Bluetooth und BIND</span><span class="sxs-lookup"><span data-stu-id="e2664-107">Bluetooth and bind</span></span>

<span data-ttu-id="e2664-108">Bluetooth verwendet die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion, um eine Bindung an einen Socket herzustellen.</span><span class="sxs-lookup"><span data-stu-id="e2664-108">Bluetooth uses the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function to bind to a socket.</span></span> <span data-ttu-id="e2664-109">Um einen Bluetooth-Socket zu binden, können Sie die **Bind** -Funktion mithilfe der [**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) -Struktur abrufen.</span><span class="sxs-lookup"><span data-stu-id="e2664-109">To bind a Bluetooth socket, call the **bind** function using the [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure.</span></span> <span data-ttu-id="e2664-110">Verwenden Sie die **sockaddr- \_ BTH** -Struktur mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e2664-110">Use the **SOCKADDR\_BTH** structure with the following settings:</span></span>

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

<span data-ttu-id="e2664-111">Bei Client Anwendungen muss der portmember NULL sein, damit ein geeigneter lokaler Endpunkt zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e2664-111">On client applications, the port member must be zero to enable an appropriate local endpoint to be assigned.</span></span> <span data-ttu-id="e2664-112">Bei Server Anwendungen muss es sich bei dem Porttyp um eine gültige Portnummer oder einen BT-Port handeln, und \_ \_ Ports, die mithilfe des BT-Ports automatisch zugewiesen \_ werden, \_ können anschließend mit einem Aufrufen der [**getsockname**](bluetooth-and-getsockname.md) -Funktion abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="e2664-112">On server applications, the port member must be a valid port number or BT\_PORT\_ANY; ports automatically assigned using BT\_PORT\_ANY may be queried subsequently with a call to the [**getsockname**](bluetooth-and-getsockname.md) function.</span></span> <span data-ttu-id="e2664-113">Der gültige Bereich für die Anforderung eines bestimmten RFCOMM-Ports liegt zwischen 1 und 30.</span><span class="sxs-lookup"><span data-stu-id="e2664-113">The valid range for requesting a specific RFCOMM port is 1 through 30.</span></span> <span data-ttu-id="e2664-114">Server Kanäle sind globale Ressourcen, und für RFCOMM sind nur 30 Server Kanäle auf allen Bluetooth-Geräten verfügbar, die von allen Windows-Sockets gemeinsam genutzt werden müssen, die zur Bluetooth-Adressfamilie gehören.</span><span class="sxs-lookup"><span data-stu-id="e2664-114">Server channels are global resource, and only 30 server channels are available for RFCOMM on any Bluetooth device, which must be shared by all Windows Sockets that belong to the Bluetooth address family.</span></span> <span data-ttu-id="e2664-115">Wenn kein Serverchannel verfügbar ist oder der angegebene Serverchannel bereits reserviert ist, schlägt der [**Bindungs**](/windows/desktop/api/winsock/nf-winsock-bind) Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="e2664-115">If no server channel is available, or if the specified server channel is already reserved, the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) call fails.</span></span>

<span data-ttu-id="e2664-116">Nach erfolgreicher Rückgabe von BIND wird der Serverchannel reserviert, bis der Socket geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="e2664-116">Upon successful return from bind, the server channel is reserved until the socket is closed.</span></span> <span data-ttu-id="e2664-117">Verwenden Sie die Funktion [**getsockname**](bluetooth-and-getsockname.md) , um die Kanalnummer für die SDP-Registrierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e2664-117">Use the [**getsockname**](bluetooth-and-getsockname.md) function to retrieve the channel number for SDP registration.</span></span>

<span data-ttu-id="e2664-118">Anwendungen sollten die automatische Zuordnung für den Serverchannel verwenden.</span><span class="sxs-lookup"><span data-stu-id="e2664-118">Applications should use auto-allocation for the server channel.</span></span>

<span data-ttu-id="e2664-119">Die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion kündigt die Serveranwendung nicht automatisch mit dem Bluetooth-SDP an. Anwendungen müssen die [**wsasetservice**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) -Funktion abrufen, die von Bluetooth-Remote Anwendungen gefunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2664-119">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function does not automatically advertise the server application using the Bluetooth SDP; applications must call the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to be found by remote Bluetooth applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2664-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2664-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2664-121">Windows-Sockets</span><span class="sxs-lookup"><span data-stu-id="e2664-121">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="e2664-122">**Zwick**</span><span class="sxs-lookup"><span data-stu-id="e2664-122">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 