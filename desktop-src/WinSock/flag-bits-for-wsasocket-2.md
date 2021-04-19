---
description: In einigen Fällen können Sockets, die einer Multipoint-Sitzung beitreten, einige Unterschiede im Verhalten von Punkt-zu-Punkt-Sockets aufweisen.
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: Bits für wsasocket markieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51fede5d160d89b08064d8dff1c1a901c048526f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372815"
---
# <a name="flag-bits-for-wsasocket"></a><span data-ttu-id="0abf8-103">Bits für wsasocket markieren</span><span class="sxs-lookup"><span data-stu-id="0abf8-103">Flag Bits for WSASocket</span></span>

<span data-ttu-id="0abf8-104">In einigen Fällen können Sockets, die einer Multipoint-Sitzung beitreten, einige Unterschiede im Verhalten von Punkt-zu-Punkt-Sockets aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0abf8-104">In some instances sockets joined to a multipoint session may have some differences in behavior from point-to-point sockets.</span></span> <span data-ttu-id="0abf8-105">So kann z. b. ein d- \_ Blatt-Socket in einem Daten Ebenen Schema, das nur Informationen an den d-Stamm \_ Teilnehmer sendet.</span><span class="sxs-lookup"><span data-stu-id="0abf8-105">For example, a d\_leaf socket in a rooted data plane scheme can only send information to the d\_root participant.</span></span> <span data-ttu-id="0abf8-106">Dies führt dazu, dass die Anwendung in der Lage ist, die beabsichtigte Verwendung eines socketcovorfalls mit ihrer Erstellung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0abf8-106">This creates a need for the application to be able to indicate the intended use of a socket coincident with its creation.</span></span> <span data-ttu-id="0abf8-107">Dies erfolgt über vier-Flag-Bits, die im *dwFlags* -Parameter auf [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)festgelegt werden können:</span><span class="sxs-lookup"><span data-stu-id="0abf8-107">This is done through four-flag bits that can be set in the *dwFlags* parameter to [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):</span></span>

-   <span data-ttu-id="0abf8-108">WSA \_ Flag \_ -Multipoint- \_ C \_ -Stamm für die Erstellung eines als C-Stamm fungierenden Sockets \_ und nur zulässig, wenn im entsprechenden [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Eintrag eine Stamm Steuerungsebene angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0abf8-108">WSA\_FLAG\_MULTIPOINT\_C\_ROOT, for the creation of a socket acting as a c\_root, and only allowed if a rooted control plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="0abf8-109">WSA \_ Flag \_ \_ \_ für das Multipoint-C-Blatt, für die Erstellung eines als C-Blatt fungierenden Sockets \_ und nur zulässig, wenn die XP1- \_ Unterstützung \_ für Multipoint im entsprechenden [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Eintrag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0abf8-109">WSA\_FLAG\_MULTIPOINT\_C\_LEAF, for the creation of a socket acting as a c\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="0abf8-110">WSA \_ Flag \_ Multipoint \_ D \_ root für die Erstellung eines als D-Stamm fungierenden Sockets \_ und nur zulässig, wenn im entsprechenden [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Eintrag eine Datenebene mit Stamms angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0abf8-110">WSA\_FLAG\_MULTIPOINT\_D\_ROOT, for the creation of a socket acting as a d\_root, and only allowed if a rooted data plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="0abf8-111">WSA \_ Flag \_ -Multipoint \_ -D- \_ Blatt für die Erstellung eines als D-Blatt fungierenden Sockets \_ und nur zulässig, wenn die XP1- \_ Unterstützung von \_ Multipoint im entsprechenden [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Eintrag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0abf8-111">WSA\_FLAG\_MULTIPOINT\_D\_LEAF, for the creation of a socket acting as a d\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>

<span data-ttu-id="0abf8-112">Beachten Sie, dass beim Erstellen eines Multipoint-Sockets genau eines der beiden Flags der Steuerungsebene und eines der beiden Flags für die Datenebene im *dwFlags* -Parameter von [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="0abf8-112">Note that when creating a multipoint socket, exactly one of the two control-plane flags, and one of the two data-plane flags must be set in [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)'s *dwFlags* parameter.</span></span> <span data-ttu-id="0abf8-113">Daher sind die vier Möglichkeiten zum Erstellen von Multipoint-Sockets:</span><span class="sxs-lookup"><span data-stu-id="0abf8-113">Thus, the four possibilities for creating multipoint sockets are:</span></span>

-   <span data-ttu-id="0abf8-114">"c \_ root/d \_ root"</span><span class="sxs-lookup"><span data-stu-id="0abf8-114">"c\_root/d\_root"</span></span>
-   <span data-ttu-id="0abf8-115">"c \_ root/d- \_ Blatt"</span><span class="sxs-lookup"><span data-stu-id="0abf8-115">"c\_root/d\_leaf"</span></span>
-   <span data-ttu-id="0abf8-116">"c- \_ Blatt/d-Stamm \_ "</span><span class="sxs-lookup"><span data-stu-id="0abf8-116">"c\_leaf/d\_root"</span></span>
-   <span data-ttu-id="0abf8-117">"c- \_ Blatt/d \_ Blatt"</span><span class="sxs-lookup"><span data-stu-id="0abf8-117">"c\_leaf /d\_leaf"</span></span>

 

 
