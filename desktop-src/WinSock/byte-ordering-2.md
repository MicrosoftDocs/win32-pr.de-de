---
description: Es muss stets darauf geachtet werden, dass Unterschiede zwischen der Byte Reihenfolge, die zum Speichern ganzer Zahlen in der Host Architektur verwendet wird, und der Byte-Reihenfolge, die von einzelnen Transportprotokollen verwendet wird, berücksichtigt werden.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: Bytereihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47af5ea9d22c01e6ae1ad3d78af48b4216f71ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484955"
---
# <a name="byte-ordering"></a><span data-ttu-id="59898-103">Bytereihenfolge</span><span class="sxs-lookup"><span data-stu-id="59898-103">Byte Ordering</span></span>

<span data-ttu-id="59898-104">Es muss stets darauf geachtet werden, dass Unterschiede zwischen der Byte Reihenfolge, die zum Speichern ganzer Zahlen in der Host Architektur verwendet wird, und der Byte-Reihenfolge, die von einzelnen Transportprotokollen verwendet wird, berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="59898-104">Care must always be taken to account for any differences between the byte ordering used for storing integers by the host architecture and the byte ordering used on the wire by individual transport protocols.</span></span> <span data-ttu-id="59898-105">Alle Verweise auf eine Adresse oder eine Portnummer, die an eine oder von einer Windows Sockets-Routine übergeben wird, müssen sich in der Netzwerk Reihenfolge (Big-enumdian) für das verwendete Protokoll befinden.</span><span class="sxs-lookup"><span data-stu-id="59898-105">Any reference to an address or port number passed to or from a Windows Sockets routine must be in the network order (big-endian) for the protocol being utilized.</span></span> <span data-ttu-id="59898-106">Im Fall von IP umfasst dies die IP-Adresse und die Port Parameter einer [**sockaddr**](sockaddr-2.md) -Struktur (aber nicht den *Sin- \_ Family* -Parameter).</span><span class="sxs-lookup"><span data-stu-id="59898-106">In the case of IP, this includes the IP address and port parameters of a [**sockaddr**](sockaddr-2.md) structure (but not the *sin\_family* parameter).</span></span>

<span data-ttu-id="59898-107">Eine Reihe von UNIX-Systemen funktioniert mit CPUs, die ganze Zahlen in der Netzwerk-Byte Reihenfolge (Big-Endian) darstellen.</span><span class="sxs-lookup"><span data-stu-id="59898-107">A number of the UNIX systems operate on CPUs that represent integers in network byte order (big-endian).</span></span> <span data-ttu-id="59898-108">Daher kann die Notwendigkeit, ganze Zahlen von der Host-Byte Reihenfolge in die Netzwerk-Byte Reihenfolge zu konvertieren, ignoriert werden, auch wenn dies für die Portabilität nicht empfehlenswert ist.</span><span class="sxs-lookup"><span data-stu-id="59898-108">So the need to convert integers from host byte order to network byte order can be ignored without causing problems even if this is not recommended for portability.</span></span>

<span data-ttu-id="59898-109">Im Gegensatz dazu ist die Byte-Reihenfolge, die zur Darstellung ganzer Zahlen für die meisten Intel® CPUs verwendet wird, Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="59898-109">In contrast, the byte ordering used to represent integers by most Intel® CPUs is little-endian.</span></span> <span data-ttu-id="59898-110">Daher ist es obligatorisch, dass ganze Zahlen von der Host-Byte Reihenfolge in die Netzwerk-Byte Reihenfolge konvertiert werden, bevor Sie in Winsock Sockets-Funktionen und-Strukturen verwendet werden</span><span class="sxs-lookup"><span data-stu-id="59898-110">So it is becomes mandatory that integers be converted from host byte-order to network byte order before being used in Winsock Sockets functions and structures.</span></span>

<span data-ttu-id="59898-111">Stellen Sie sich eine Anwendung vor, die normalerweise einen Server auf dem TCP-Port kontaktiert, der dem Zeit Dienst entspricht, aber einen Mechanismus bereitstellt, mit dem der Benutzer einen alternativen Port angeben kann.</span><span class="sxs-lookup"><span data-stu-id="59898-111">Consider an application that normally contacts a server on the TCP port corresponding to the time service, but provides a mechanism for the user to specify an alternative port.</span></span> <span data-ttu-id="59898-112">Die von [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) zurückgegebene Portnummer ist bereits in der Netzwerk Reihenfolge vorhanden. Dies ist das Format, das zum Erstellen einer Adresse erforderlich ist, sodass keine Übersetzung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="59898-112">The port number returned by [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) is already in network order, which is the format required for constructing an address so that no translation is required.</span></span> <span data-ttu-id="59898-113">Wenn sich der Benutzer jedoch [**für die Verwendung**](/windows/desktop/api/winsock/nf-winsock-htons) eines anderen Ports entscheidet, der als Ganzzahl eingegeben wird, muss die Anwendung diese in eine TCP/IP-Netzwerk Reihenfolge konvertieren, bevor [](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) Sie zum Erstellen einer Adresse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="59898-113">However, if the user elects to use a different port, entered as an integer, the application must convert this from host to TCP/IP network order (using the [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) or [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) function) before using it to construct an address.</span></span> <span data-ttu-id="59898-114">Wenn im Gegensatz dazu die Anwendung die Nummer des Ports innerhalb einer Adresse anzeigen soll (z. b. von [**getPeer Name**](/windows/desktop/api/winsock/nf-winsock-getpeername) ), muss die Portnummer aus dem Netzwerk in die Host Reihenfolge (mithilfe der [**ndehs**](/windows/desktop/api/winsock/nf-winsock-ntohs) -oder [**wsandehs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) -Funktion) konvertiert werden, bevor Sie angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="59898-114">Conversely, if the application were to display the number of the port within an address (returned by [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) for example), the port number must be converted from network to host order (using the [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) or [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) function) before it can be displayed.</span></span>

<span data-ttu-id="59898-115">Da sich die Intel-und Internet-Byte Bestellungen unterscheiden, sind die in der obigen beschriebenen Konvertierungen unvermeidlich.</span><span class="sxs-lookup"><span data-stu-id="59898-115">Since the Intel and Internet byte orders are different, the conversions described in the preceding are unavoidable.</span></span> <span data-ttu-id="59898-116">Anwendungs Schreiber werden gewarnt, dass Sie die Standard Konvertierungs Funktionen verwenden sollten, die als Teil von Winsock bereitgestellt werden, anstatt ihren eigenen Konvertierungs Code zu schreiben, da zukünftige Implementierungen von Winsock wahrscheinlich auf Systemen ausgeführt werden, für die die Host Reihenfolge mit der Netzwerk-Byte Reihenfolge identisch ist.</span><span class="sxs-lookup"><span data-stu-id="59898-116">Application writers are cautioned that they should use the standard conversion functions provided as part of Winsock rather than writing their own conversion code since future implementations of Winsock are likely to run on systems for which the host order is identical to the network byte order.</span></span> <span data-ttu-id="59898-117">Nur Anwendungen, die die Standard Konvertierungs Funktionen zwischen der Host-und der Netzwerk-Byte Reihenfolge verwenden, sind wahrscheinlich portabel.</span><span class="sxs-lookup"><span data-stu-id="59898-117">Only applications that use the standard conversion functions between host and network byte order are likely to be portable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59898-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59898-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59898-119">**getPeer Name**</span><span class="sxs-lookup"><span data-stu-id="59898-119">**getpeername**</span></span>](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[<span data-ttu-id="59898-120">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="59898-120">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[<span data-ttu-id="59898-121">**htonl**</span><span class="sxs-lookup"><span data-stu-id="59898-121">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="59898-122">**htonnen**</span><span class="sxs-lookup"><span data-stu-id="59898-122">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="59898-123">**nzu HLS**</span><span class="sxs-lookup"><span data-stu-id="59898-123">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="59898-124">**NUM**</span><span class="sxs-lookup"><span data-stu-id="59898-124">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="59898-125">Portieren von Socketanwendungen auf Winsock</span><span class="sxs-lookup"><span data-stu-id="59898-125">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="59898-126">**sockaddr**</span><span class="sxs-lookup"><span data-stu-id="59898-126">**sockaddr**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="59898-127">Überlegungen zur Winsock-Programmierung</span><span class="sxs-lookup"><span data-stu-id="59898-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="59898-128">**Wsahtonl**</span><span class="sxs-lookup"><span data-stu-id="59898-128">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="59898-129">**Wsahtonnen**</span><span class="sxs-lookup"><span data-stu-id="59898-129">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="59898-130">**Wsanum**</span><span class="sxs-lookup"><span data-stu-id="59898-130">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="59898-131">**Wsanum**</span><span class="sxs-lookup"><span data-stu-id="59898-131">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



