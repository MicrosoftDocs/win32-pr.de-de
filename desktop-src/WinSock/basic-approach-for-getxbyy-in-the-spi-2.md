---
description: Die meisten getxbyy-Funktionen werden durch Ws2- \_32.dll in eine wsalookupservicebegin-, WSALookupServiceNext-und WSALookupServiceEnd-Sequenz übersetzt, die eine Reihe spezieller GUIDs als Dienstklasse verwendet.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Grundlegender Ansatz für getxbyy in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d635230bb1c1205d0f6e1aee16fe7c7ac9eab5b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862587"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a><span data-ttu-id="feab7-103">Grundlegender Ansatz für getxbyy in der SPI</span><span class="sxs-lookup"><span data-stu-id="feab7-103">Basic Approach for GetXbyY in the SPI</span></span>

<span data-ttu-id="feab7-104">Die meisten **getxbyy** -Funktionen werden durch Ws2- \_32.dll in eine [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)-, [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)-und [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) -Sequenz übersetzt, die eine Reihe spezieller GUIDs als Dienstklasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="feab7-104">Most **GetXbyY** functions are translated by Ws2\_32.dll to a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) sequence that uses one of a set of special GUIDs as the service class.</span></span> <span data-ttu-id="feab7-105">Diese GUIDs bestimmen den Typ des **getxbyy** -Vorgangs, der emuliert wird.</span><span class="sxs-lookup"><span data-stu-id="feab7-105">These GUIDs identify the type of **GetXbyY** operation that is being emulated.</span></span> <span data-ttu-id="feab7-106">Die Abfrage wird auf die NSPs beschränkt, die AF \_ inet unterstützen.</span><span class="sxs-lookup"><span data-stu-id="feab7-106">The query is constrained to those NSPs that support AF\_INET.</span></span> <span data-ttu-id="feab7-107">Wenn eine **getxbyy** -Funktion eine [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) -oder eine [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur zurückgibt, gibt die Ws2- \_32.dll das Lup- \_ \_ blobflag "BLOB" in **wsalookupservicebegin** an, sodass die gewünschten Informationen vom NSP zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="feab7-107">Whenever a **GetXbyY** function returns a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) or [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure, the Ws2\_32.dll will specify the LUP\_RETURN\_BLOB flag in **WSALookupServiceBegin** so that the desired information will be returned by the NSP.</span></span> <span data-ttu-id="feab7-108">Diese Strukturen müssen geringfügig geändert werden, da die in enthaltenen Zeiger durch Offsets ersetzt werden müssen, die relativ zum Anfang der Daten des BLOBs sind.</span><span class="sxs-lookup"><span data-stu-id="feab7-108">These structures must be modified slightly in that the pointers contained within must be replaced with offsets that are relative to the start of the blob's data.</span></span> <span data-ttu-id="feab7-109">Alle Werte, auf die durch diese Zeiger Elemente verwiesen wird, müssen natürlich vollständig im BLOB enthalten sein, und alle Zeichen folgen sind ASCII.</span><span class="sxs-lookup"><span data-stu-id="feab7-109">All values referenced by these pointer members must, of course, be completely contained within the blob, and all strings are ASCII.</span></span>

 

 



