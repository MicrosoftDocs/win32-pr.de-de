---
description: Windows Sockets 2 bietet eine generische Methode für die Verwendung der Multipoint-und Multicast-Funktionen von Transporten.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Multicast-und Multipoint-Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e409c18752b32af7cf65b4a55862ec75cec7a3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348288"
---
# <a name="protocol-independent-multicast-and-multipoint"></a><span data-ttu-id="46e54-103">Multicast-und Multipoint-Protocol-Independent</span><span class="sxs-lookup"><span data-stu-id="46e54-103">Protocol-Independent Multicast and Multipoint</span></span>

<span data-ttu-id="46e54-104">Windows Sockets 2 bietet eine generische Methode für die Verwendung der Multipoint-und Multicast-Funktionen von Transporten.</span><span class="sxs-lookup"><span data-stu-id="46e54-104">Windows Sockets 2 provides a generic method for utilizing the multipoint and multicast capabilities of transports.</span></span> <span data-ttu-id="46e54-105">Diese generische Methode implementiert diese Features genauso wie die grundlegenden Datentransport Funktionen von zahlreichen Transportprotokollen.</span><span class="sxs-lookup"><span data-stu-id="46e54-105">This generic method implements these features just as it allows the basic data transport capabilities of numerous transport protocols to be accessed.</span></span> <span data-ttu-id="46e54-106">Der Begriff "MultiPoint" wird im folgenden verwendet, um auf Multicast-und Multipoint-Kommunikationen zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="46e54-106">The term, multipoint, is used hereafter to refer to both multicast and multipoint communications.</span></span>

<span data-ttu-id="46e54-107">Die aktuellen Multipoint-Implementierungen (z. b. IP-Multicast, St-II, T. 120 und ATM Uni) variieren stark.</span><span class="sxs-lookup"><span data-stu-id="46e54-107">Current multipoint implementations (for example, IP multicast, ST-II, T.120, and ATM UNI) vary widely.</span></span> <span data-ttu-id="46e54-108">Gibt an, wie Knoten einer Multipoint-Sitzung beitreten, ob ein bestimmter Knoten als zentraler Knoten oder als Stamm Knoten festgelegt ist und ob zwischen allen Knoten oder nur zwischen einem Stamm Knoten und den verschiedenen Blattknoten zwischen den einzelnen Implementierungen Daten ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="46e54-108">How nodes join a multipoint session, whether a particular node is designated as a central or root node, and whether data is exchanged between all nodes or only between a root node and the various leaf nodes differ among implementations.</span></span> <span data-ttu-id="46e54-109">Die [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für Windows Sockets 2 wird verwendet, um die verschiedenen Multipoint-Attribute eines Protokolls zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="46e54-109">The [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for Windows Sockets 2 is used to declare the various multipoint attributes of a protocol.</span></span> <span data-ttu-id="46e54-110">Durch die Untersuchung dieser Attribute weiß der Programmierer, welche Konventionen mit den entsprechenden Windows Sockets 2-Funktionen zum Einrichten, verwenden und Beenden von Multipoint-Sitzungen befolgt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="46e54-110">By examining these attributes, the programmer knows what conventions to follow with the applicable Windows Sockets 2 functions to set up, utilize, and tear down multipoint sessions.</span></span>

<span data-ttu-id="46e54-111">Im folgenden werden die Winsock-Funktionen zusammengefasst, die Multipoint unterstützen</span><span class="sxs-lookup"><span data-stu-id="46e54-111">The following summarizes Winsock features that support multipoint:</span></span>

-   <span data-ttu-id="46e54-112">Two-Attribute Bits in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur.</span><span class="sxs-lookup"><span data-stu-id="46e54-112">Two-attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="46e54-113">Vier Flags, die für den *dwFlags* -Parameter der [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) -Funktion definiert sind.</span><span class="sxs-lookup"><span data-stu-id="46e54-113">Four flags defined for the *dwFlags* parameter of the [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function.</span></span>
-   <span data-ttu-id="46e54-114">Eine Funktion, [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), zum Hinzufügen von Blattknoten zu einer Multipoint-Sitzung</span><span class="sxs-lookup"><span data-stu-id="46e54-114">One function, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), for adding leaf nodes into a multipoint session</span></span>
-   <span data-ttu-id="46e54-115">Zwei [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Befehls Codes zum Steuern des Multipoint-Loopbacks und zum Festlegen des Bereichs für Multicast Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="46e54-115">Two [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) command codes for controlling multipoint loopback and establishing the scope for multicast transmissions.</span></span> <span data-ttu-id="46e54-116">(Letzteres entspricht dem IP-Multicast-"Time-to-Live"-oder "TTL"-Parameter.)</span><span class="sxs-lookup"><span data-stu-id="46e54-116">(The latter corresponds to the IP multicast time-to-live or TTL parameter.)</span></span>

> [!Note]  
> <span data-ttu-id="46e54-117">Durch die Einbindung dieser Multipoint-Features in Windows Sockets 2 wird verhindert, dass eine Anwendung eine vorhandene Protokoll abhängige Schnittstelle verwendet, wie z. b. das Deering von Socketoptionen für IP-Multicast.</span><span class="sxs-lookup"><span data-stu-id="46e54-117">The inclusion of these multipoint features in Windows Sockets 2 does not preclude an application from using an existing protocol-dependent interface, such as the Deering socket options for IP multicast.</span></span>

 

<span data-ttu-id="46e54-118">Ausführliche Informationen dazu, wie die verschiedenen Multipoint-Schemas charakterisiert sind und wie die entsprechenden Features von Windows Sockets 2 verwendet werden, finden Sie unter [Multipoint-und Multicast-Semantik](multipoint-and-multicast-semantics-2.md) .</span><span class="sxs-lookup"><span data-stu-id="46e54-118">See [Multipoint and Multicast Semantics](multipoint-and-multicast-semantics-2.md) for detailed information on how the various multipoint schemes are characterized and how the applicable features of Windows Sockets 2 are utilized.</span></span>

 

 
