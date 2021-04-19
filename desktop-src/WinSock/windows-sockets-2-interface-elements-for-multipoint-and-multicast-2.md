---
description: Winsock-Schnittstellen Elemente (Windows Sockets 2) für Multipoint und Multicast.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Windows Sockets 2-Schnittstellen Elemente für Multipoint und Multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86905fe19c5c4c603db488874039b7cc8a0b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360118"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a><span data-ttu-id="60f87-103">Windows Sockets 2-Schnittstellen Elemente für Multipoint und Multicast</span><span class="sxs-lookup"><span data-stu-id="60f87-103">Windows Sockets 2 Interface Elements for Multipoint and Multicast</span></span>

<span data-ttu-id="60f87-104">Die Mechanismen, die für die Verwendung von Multipoint-Funktionen in Windows Sockets 2 integriert wurden, können wie folgt zusammengefasst werden:</span><span class="sxs-lookup"><span data-stu-id="60f87-104">The mechanisms that have been incorporated into Windows Sockets 2 for utilizing multipoint capabilities can be summarized as follows:</span></span>

-   <span data-ttu-id="60f87-105">Drei Attribut Bits in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur.</span><span class="sxs-lookup"><span data-stu-id="60f87-105">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="60f87-106">Vier Flags, die für den *dwFlags* -Parameter von [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)definiert sind.</span><span class="sxs-lookup"><span data-stu-id="60f87-106">Four flags defined for the *dwFlags* parameter of [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span></span>
-   <span data-ttu-id="60f87-107">Eine Funktion, [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), zum Hinzufügen von Blattknoten zu einer Multipoint-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="60f87-107">One function, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="60f87-108">Zwei [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Befehls Codes zum Steuern des Multipoint-Loopbacks und des Bereichs von Multicast Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="60f87-108">Two [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) command codes for controlling multipoint loopback and the scope of multicast transmissions.</span></span>

<span data-ttu-id="60f87-109">In den folgenden Abschnitten werden diese Schnittstellen Elemente ausführlicher beschrieben:</span><span class="sxs-lookup"><span data-stu-id="60f87-109">The following sections describe these interface elements in more detail:</span></span>

-   [<span data-ttu-id="60f87-110">Semantik für das beitreten von Multipoint-Blättern</span><span class="sxs-lookup"><span data-stu-id="60f87-110">Semantics for Joining Multipoint Leaves</span></span>](semantics-for-joining-multipoint-leaves-2.md)
-   [<span data-ttu-id="60f87-111">Unterstützung für diese Erweiterungen durch vorhandene Multipoint-Protokolle</span><span class="sxs-lookup"><span data-stu-id="60f87-111">How Existing Multipoint Protocols Support These Extensions</span></span>](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
