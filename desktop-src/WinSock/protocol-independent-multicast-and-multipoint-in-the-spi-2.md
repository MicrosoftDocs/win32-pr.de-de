---
description: Windows Sockets (Winsock) und Protokoll unabhängige Multipoint-und Multicast-Funktionen von Transporten.
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent Multicast und Multipoint in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda9e5cab1b790a1e2d2c64c4451063a94dd8bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131176"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a><span data-ttu-id="e1421-103">Protocol-Independent Multicast und Multipoint in der SPI</span><span class="sxs-lookup"><span data-stu-id="e1421-103">Protocol-Independent Multicast and Multipoint in the SPI</span></span>

<span data-ttu-id="e1421-104">Ebenso wie Windows Sockets 2 ermöglicht, dass die grundlegenden Datentransport Funktionen von zahlreichen Transportprotokollen auf generische Weise aufgerufen werden können, bietet es auch eine generische Möglichkeit, Multipoint-und Multicast-Funktionen von Transporten zu verwenden, die diese Features implementieren.</span><span class="sxs-lookup"><span data-stu-id="e1421-104">Just as Windows Sockets 2 allows the basic data transport capabilities of numerous transport protocols to be accessed in a generic manner, it also provides a generic way to use multipoint and multicast capabilities of transports that implement these features.</span></span> <span data-ttu-id="e1421-105">Um dies zu vereinfachen, wird im folgenden der Begriff *Multipoint* verwendet, um auf Multicast-und Multipoint-Kommunikation zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="e1421-105">To simplify, the term *multipoint* is used hereafter to refer to both multicast and multipoint communications.</span></span>

<span data-ttu-id="e1421-106">Aktuelle Multipoint-Implementierungen (z. b. IP-Multicast, St-II, T. 120, ATM Uni) variieren in Bezug darauf, wie Knoten mit einer Multipoint-Sitzung verknüpft werden, ob ein bestimmter Knoten als zentraler Knoten oder Stamm Knoten festgelegt ist und ob zwischen allen Knoten oder nur zwischen einem Stamm Knoten und verschiedenen Blattknoten Daten ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="e1421-106">Current multipoint implementations (for example, IP multicast, ST-II, T.120, ATM UNI) vary widely with respect to how nodes join a multipoint session, whether a particular node is designated as a central or root node, and whether data is exchanged between all nodes or only between a root node and various leaf nodes.</span></span> <span data-ttu-id="e1421-107">Die [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur von Windows Sockets 2 wird zum Deklarieren der Multipoint-Attribute eines Protokolls verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1421-107">The Windows Sockets 2 [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure is used to declare the multipoint attributes of a protocol.</span></span> <span data-ttu-id="e1421-108">Durch die Untersuchung dieser Attribute weiß der Programmierer, welche Konventionen bei der Einrichtung, Verwendung und Löschung von Multipoint-Sitzungen bei der Verwendung der anwendbaren Winsock-Funktionen befolgt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e1421-108">By examining these attributes the programmer will know what conventions to follow in using the applicable Winsock functions to set up, use, and tear down multipoint sessions.</span></span>

<span data-ttu-id="e1421-109">Die Features von Windows Sockets 2, die Multicast unterstützen, können wie folgt zusammengefasst werden:</span><span class="sxs-lookup"><span data-stu-id="e1421-109">The features of Windows Sockets 2 that support multicast can be summarized as follows:</span></span>

-   <span data-ttu-id="e1421-110">Drei Attribut Bits in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur.</span><span class="sxs-lookup"><span data-stu-id="e1421-110">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="e1421-111">Vier Flags, die für den *dwFlags* -Parameter von [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) definiert sind</span><span class="sxs-lookup"><span data-stu-id="e1421-111">Four flags defined for the *dwFlags* parameter of [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)</span></span>
-   <span data-ttu-id="e1421-112">Eine Funktion, [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), zum Hinzufügen von Blattknoten zu einer Multipoint-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e1421-112">One function, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="e1421-113">Zwei [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) -Befehls Codes zum Steuern des Multipoint-Loopbacks und zum Festlegen des Bereichs für Multicast Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="e1421-113">Two [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) command codes for controlling multipoint loopback and establishing the scope for multicast transmissions.</span></span> <span data-ttu-id="e1421-114">(Letzteres entspricht dem IP-Multicast-"Time-to-Live"-oder "TTL"-Parameter.)</span><span class="sxs-lookup"><span data-stu-id="e1421-114">(The latter corresponds to the IP multicast time-to-live or TTL parameter.)</span></span>

> [!Note]  
> <span data-ttu-id="e1421-115">Durch die Einbindung dieser Multipoint-Features in Windows Sockets 2 wird verhindert, dass ein Dienstanbieter auch eine vorhandene Protokoll abhängige Schnittstelle unterstützt, wie z. b. das Deering von Socketoptionen für IP-Multicast.</span><span class="sxs-lookup"><span data-stu-id="e1421-115">The inclusion of these multipoint features in Windows Sockets 2 does not preclude a service provider from also supporting an existing protocol-dependent interface, such as the Deering socket options for IP multicast.</span></span>

 

 

 
