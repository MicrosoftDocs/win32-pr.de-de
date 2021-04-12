---
description: Die meisten getxbyy-Funktionen werden vom Ws2- \_32.dll in eine wsalookupservicebegin-, WSALookupServiceNext-und WSALookupServiceEnd-Sequenz übersetzt, die eine Reihe spezieller GUIDs als Dienstklasse verwendet.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Grundlegender Ansatz für getxbyy in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4c038c87d6eb6e7ab2a4476271662d5b9567ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526207"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a><span data-ttu-id="3f3f8-103">Grundlegender Ansatz für getxbyy in der API</span><span class="sxs-lookup"><span data-stu-id="3f3f8-103">Basic Approach for GetXbyY in the API</span></span>

<span data-ttu-id="3f3f8-104">Die meisten **getxbyy** -Funktionen werden vom Ws2- \_32.dll in eine [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)-, [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)-und [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) -Sequenz übersetzt, die eine Reihe spezieller GUIDs als Dienstklasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="3f3f8-104">Most **getXbyY** functions are translated by the Ws2\_32.dll to a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), and [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) sequence that uses one of a set of special GUIDs as the service class.</span></span> <span data-ttu-id="3f3f8-105">Diese GUIDs bestimmen den Typ des **getxbyy** -Vorgangs, der emuliert wird.</span><span class="sxs-lookup"><span data-stu-id="3f3f8-105">These GUIDs identify the type of **getXbyY** operation that is being emulated.</span></span> <span data-ttu-id="3f3f8-106">Die Abfrage wird auf solche namens Dienstanbieter beschränkt, die AF inet unterstützen \_ .</span><span class="sxs-lookup"><span data-stu-id="3f3f8-106">The query is constrained to those name service providers that support AF\_INET.</span></span> <span data-ttu-id="3f3f8-107">Wenn eine **getxbyy** -Funktion eine [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) -oder eine [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur zurückgibt, gibt die Ws2- \_32.dll das Lup- \_ \_ blobflag "BLOB" in **wsalookupservicebegin** an, sodass die gewünschten Informationen vom namens Dienstanbieter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3f3f8-107">Whenever a **getXbyY** function returns a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) or [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure, the Ws2\_32.dll specifies the LUP\_RETURN\_BLOB flag in **WSALookupServiceBegin** so that the desired information is returned by the name service provider.</span></span> <span data-ttu-id="3f3f8-108">Diese Strukturen müssen geringfügig geändert werden, da die in enthaltenen Zeiger durch Offsets ersetzt werden müssen, die relativ zum Anfang der Daten des BLOBs sind.</span><span class="sxs-lookup"><span data-stu-id="3f3f8-108">These structures must be modified slightly in that the pointers contained within must be replaced with offsets that are relative to the start of the blob's data.</span></span> <span data-ttu-id="3f3f8-109">Alle Werte, auf die von diesen Zeiger Parametern verwiesen wird, müssen natürlich vollständig im BLOB enthalten sein, und alle Zeichen folgen sind ASCII.</span><span class="sxs-lookup"><span data-stu-id="3f3f8-109">All values referenced by these pointer parameters must, of course, be completely contained within the blob, and all strings are ASCII.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f3f8-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f3f8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f3f8-111">Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API</span><span class="sxs-lookup"><span data-stu-id="3f3f8-111">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="3f3f8-112">Protokoll unabhängige Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="3f3f8-112">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="3f3f8-113">Registrierung und Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="3f3f8-113">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



