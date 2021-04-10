---
description: In diesem Abschnitt werden TCP/IP-Funktionen (Transmission Control Protocol/Internet Protocol), Datenstrukturen und Steuerelemente beschrieben.
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Winsock-TCP/IP-Anhang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214985"
---
# <a name="winsock-tcpip-annex"></a><span data-ttu-id="fe52a-103">Winsock-TCP/IP-Anhang</span><span class="sxs-lookup"><span data-stu-id="fe52a-103">Winsock TCP/IP Annex</span></span>

<span data-ttu-id="fe52a-104">In diesem Abschnitt werden TCP/IP-Funktionen (Transmission Control Protocol/Internet Protocol), Datenstrukturen und Steuerelemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fe52a-104">This section describes Transmission Control Protocol/Internet Protocol (TCP/IP) functions, data structures, and controls.</span></span>



| <span data-ttu-id="fe52a-105">Element</span><span class="sxs-lookup"><span data-stu-id="fe52a-105">Element</span></span>          | <span data-ttu-id="fe52a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe52a-106">Description</span></span>                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe52a-107">Protokoll Name (n)</span><span class="sxs-lookup"><span data-stu-id="fe52a-107">Protocol name(s)</span></span> | <span data-ttu-id="fe52a-108">TCP, UDP</span><span class="sxs-lookup"><span data-stu-id="fe52a-108">TCP, UDP</span></span>                                                                                                                                    |
| <span data-ttu-id="fe52a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe52a-109">Description</span></span>      | <span data-ttu-id="fe52a-110">Stellt Transportdienste über die IP-Netzwerkschicht bereit: UDP für unzuverlässige Datagramme, TCP für zuverlässige, Verbindungs orientierte Byte Datenströme.</span><span class="sxs-lookup"><span data-stu-id="fe52a-110">Provides transport services over the IP networking layer: UDP for unreliable datagrams, TCP for reliable, connection-oriented byte streams.</span></span> |
| <span data-ttu-id="fe52a-111">Adressfamilie</span><span class="sxs-lookup"><span data-stu-id="fe52a-111">Address family</span></span>   | <span data-ttu-id="fe52a-112">**AF \_ INET**, **AF \_ inet6**</span><span class="sxs-lookup"><span data-stu-id="fe52a-112">**AF\_INET**, **AF\_INET6**</span></span>                                                                                                                 |
| <span data-ttu-id="fe52a-113">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fe52a-113">Header file</span></span>      | <span data-ttu-id="fe52a-114">*Ws2tcpip. h*</span><span class="sxs-lookup"><span data-stu-id="fe52a-114">*Ws2tcpip.h*</span></span>                                                                                                                                |



 

<span data-ttu-id="fe52a-115">Es werden zwei grundlegende Arten von Transportdiensten angeboten: unzuverlässige Datagramme (UDP) und zuverlässige Verbindungs orientierte – Byte Datenströme (TCP).</span><span class="sxs-lookup"><span data-stu-id="fe52a-115">Two basic types of transport services are offered: unreliable datagrams (UDP), and reliable connection oriented–byte streams (TCP).</span></span> <span data-ttu-id="fe52a-116">Außerdem wird optional ein RAW-Socket unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe52a-116">In addition, a raw socket is optionally supported.</span></span> <span data-ttu-id="fe52a-117">Mit unformatierten Sockets kann eine Anwendung über andere Protokolle als TCP und UDP, wie z. b. ICMP, kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="fe52a-117">Raw sockets allow an application to communicate through protocols other than TCP and UDP such as ICMP.</span></span> <span data-ttu-id="fe52a-118">Unformatierte Sockets werden von **der \_ AF** -und der **AF \_ inet6** -Adressfamilie mit einigen Einschränkungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe52a-118">Raw sockets are supported on the **AF\_INET** and **AF\_INET6** address families with some limitations.</span></span>

<span data-ttu-id="fe52a-119">In diesem Abschnitt werden die für TCP/IP-Protokolle spezifischen Erweiterungen von Winsock behandelt.</span><span class="sxs-lookup"><span data-stu-id="fe52a-119">This section covers extensions to Winsock that are specific to TCP/IP protocols.</span></span> <span data-ttu-id="fe52a-120">Außerdem werden Aspekte von Basis-Winsock-Funktionen beschrieben, die besondere Überlegungen erfordern oder bei der Verwendung von TCP/IP das einmalige Verhalten aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="fe52a-120">It also describes aspects of base Winsock functions that require special consideration or that may exhibit unique behavior when using TCP/IP.</span></span>

 

 



