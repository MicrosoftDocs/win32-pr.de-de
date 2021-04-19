---
description: Die Funktionen "getservbyname" und "getservbyport" verwenden die Funktion "wsalookupservicebegin", um svcid \_ inet \_ servicebyname als Dienst Klassen-GUID abzufragen.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Funktionen "getservbyname" und "getservbyport" in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0028b9ed090463234d01e2b13191ff2328baf2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353067"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a><span data-ttu-id="03531-103">Funktionen "getservbyname" und "getservbyport" in der API</span><span class="sxs-lookup"><span data-stu-id="03531-103">getservbyname and getservbyport Functions in the API</span></span>

<span data-ttu-id="03531-104">Die Funktionen " [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) " und " [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) " verwenden die Funktion " [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) ", um svcid \_ inet \_ servicebyname als Dienst Klassen-GUID abzufragen.</span><span class="sxs-lookup"><span data-stu-id="03531-104">The [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions use the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_SERVICEBYNAME as the service class GUID.</span></span> <span data-ttu-id="03531-105">Der *lpszserviceinstancename* -Member in der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur, der an die **wsalookupservicebegin** -Funktion übergeben wird, verweist auf eine Zeichenfolge, um den Dienstnamen oder den Dienstport und (optional) das Dienst Protokoll anzugeben.</span><span class="sxs-lookup"><span data-stu-id="03531-105">The *lpszServiceInstanceName* member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function references a string to indicate the service name or service port, and (optionally) the service protocol.</span></span> <span data-ttu-id="03531-106">Die Formatierung der Zeichenfolge wird als FTP, TCP oder 21/TCP oder nur FTP veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="03531-106">The formatting of the string is illustrated as FTP or TCP or 21/TCP or just FTP.</span></span> <span data-ttu-id="03531-107">Bei der Zeichenfolge wird Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="03531-107">The string is not case sensitive.</span></span> <span data-ttu-id="03531-108">Der Schrägstrich trennt, falls vorhanden, den Protokoll Bezeichner vom vorangehenden Teil der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="03531-108">The slash mark, if present, separates the protocol identifier from the preceding part of the string.</span></span> <span data-ttu-id="03531-109">Der Ws2 \_ -32.dll gibt das \_ luprückgabeblob \_ an, und der Namespace Anbieter fügt eine [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur in das BLOB ein (verwendet Offsets anstelle von Zeigern, wie oben beschrieben).</span><span class="sxs-lookup"><span data-stu-id="03531-109">The Ws2\_32.dll will specify LUP\_RETURN\_BLOB and the namespace provider will place a [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="03531-110">Namespace Anbieter sollten diese anderen Lup- \_ \_ \* rückgabeflags ebenfalls berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="03531-110">Namespace providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="03531-111">Flag</span><span class="sxs-lookup"><span data-stu-id="03531-111">Flag</span></span>              | <span data-ttu-id="03531-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03531-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03531-113">Name der Lup- \_ Rückgabe \_</span><span class="sxs-lookup"><span data-stu-id="03531-113">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="03531-114">Gibt das **s- \_ Namen** Element aus der [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur in *lpszserviceinstancename* zurück.</span><span class="sxs-lookup"><span data-stu-id="03531-114">Returns the **s\_name** member from [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="03531-115">- \_ \_ Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="03531-115">LUP\_RETURN\_TYPE</span></span> | <span data-ttu-id="03531-116">Gibt die kanonische GUID in *lpserviceclassid* zurück. es wird verstanden, dass sich ein als FTP oder 21 identifizierter Dienst gemäß den lokal festgelegten Konventionen an einem anderen Port befinden kann.</span><span class="sxs-lookup"><span data-stu-id="03531-116">Returns canonical GUID in *lpServiceClassId* It is understood that a service identified as FTP or 21 may be on another port according to locally established conventions.</span></span> <span data-ttu-id="03531-117">Der **s- \_ Port** Parameter der [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur sollte angeben, wo der Dienst in der lokalen Umgebung kontaktiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="03531-117">The **s\_port** parameter of the [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure should indicate where the service can be contacted in the local environment.</span></span> <span data-ttu-id="03531-118">Die kanonische GUID, die zurückgegeben wird, wenn der Lup- \_ \_ Rückgabetyp festgelegt ist, muss eine der vordefinierten GUIDs aus SVCs. h sein, die der in der **servent** -Struktur aufgeführten Portnummer entspricht.</span><span class="sxs-lookup"><span data-stu-id="03531-118">The canonical GUID returned when LUP\_RETURN\_TYPE is set should be one of the predefined GUIDs from Svcs.h that corresponds to the port number indicated in the **SERVENT** structure.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="03531-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="03531-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03531-120">Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API</span><span class="sxs-lookup"><span data-stu-id="03531-120">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="03531-121">Protokoll unabhängige Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="03531-121">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="03531-122">Registrierung und Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="03531-122">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



