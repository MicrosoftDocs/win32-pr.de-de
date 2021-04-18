---
title: Semantische Unterschiede zwischen Multipoint-Sockets und regulären Sockets
description: Unterschiede zwischen c \_ -Stamm-Multipoint-Sockets und regulären Punkt-zu-Punkt-Sockets.
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d95b2637a4f805cea5ee6f138cc6992080a238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343822"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a><span data-ttu-id="d3892-103">Semantische Unterschiede zwischen Multipoint-Sockets und regulären Sockets</span><span class="sxs-lookup"><span data-stu-id="d3892-103">Semantic differences between multipoint sockets and regular sockets</span></span>

<span data-ttu-id="d3892-104">Auf der Steuerungsebene gibt es einige bedeutende semantische Unterschiede zwischen einem c \_ -root-Socket und einem regulären Punkt-zu-Punkt-Socket:</span><span class="sxs-lookup"><span data-stu-id="d3892-104">In the control plane, there are some significant semantic differences between a c\_root socket and a regular point-to-point socket:</span></span>

-   <span data-ttu-id="d3892-105">Der c-Stamm \_ Socket kann in [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) verwendet werden, um ein neues Blatt zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d3892-105">The c\_root socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to join a new a leaf.</span></span>
-   <span data-ttu-id="d3892-106">Das Platzieren eines c-Stamm \_ Sockets in den Empfangsmodus (durch Aufrufen von " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)") verhindert nicht, dass der c-Stamm \_ Socket in einem Aufruf von [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) zum Hinzufügen eines neuen Blatts oder zum Senden und empfangen von Multipoint-Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3892-106">Placing a c\_root socket into listening mode (by calling [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) does not preclude the c\_root socket from being used in a call to [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add a new leaf, or for sending and receiving multipoint data.</span></span>
-   <span data-ttu-id="d3892-107">Das Schließen eines c-Stamm \_ Sockets bewirkt, dass alle zugeordneten c- \_ Blatt Sockets eine Benachrichtigung über eine schließende FD erhalten \_ .</span><span class="sxs-lookup"><span data-stu-id="d3892-107">The closing of a c\_root socket causes all of the associated c\_leaf sockets to get FD\_CLOSE notification.</span></span>

<span data-ttu-id="d3892-108">Es gibt keine semantischen Unterschiede zwischen einem c \_ -Blatt Socket und einem regulären Socket in der Steuerungsebene, mit dem Unterschied, dass der c \_ -Blatt Socket in [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)verwendet werden kann und die Verwendung des c- \_ Blatt Sockets in " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) " anzeigt, dass nur Multipoint-Verbindungsanforderungen akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d3892-108">There are no semantic differences between a c\_leaf socket and a regular socket in the control plane, except that the c\_leaf socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), and the use of c\_leaf socket in [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indicates that only multipoint connection requests should be accepted.</span></span>

<span data-ttu-id="d3892-109">In der Datenebene sind die semantischen Unterschiede zwischen dem d- \_ stammsocket und einem regulären Punkt-zu-Punkt-Socket:</span><span class="sxs-lookup"><span data-stu-id="d3892-109">In the data plane, the semantic differences between the d\_root socket and a regular point-to-point socket are:</span></span>

-   <span data-ttu-id="d3892-110">Die Daten, die auf dem d-Stamm Socket gesendet werden \_ , werden an alle Blätter in derselben Multipoint-Sitzung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d3892-110">The data sent on the d\_root socket is delivered to all the leaves in the same multipoint session.</span></span>
-   <span data-ttu-id="d3892-111">Die im Stamm-Socket von d empfangenen Daten \_ können von einem der Blätter stammen.</span><span class="sxs-lookup"><span data-stu-id="d3892-111">The data received on the d\_root socket may be from any of the leaves.</span></span>

<span data-ttu-id="d3892-112">Der d- \_ Blatt Socket in der Datenebene für das Stammverzeichnis weist keinen semantischen Unterschied vom regulären Socket auf, aber in der Datenebene, die keine Daten enthält, werden die Daten, die auf dem d-Blatt Socket gesendet werden, \_ an alle anderen Endknoten gesendet, und die empfangenen Daten können von beliebigen anderen Endknoten stammen.</span><span class="sxs-lookup"><span data-stu-id="d3892-112">The d\_leaf socket in the rooted data plane has no semantic difference from the regular socket, however, in the nonrooted data plane, the data sent on the d\_leaf socket goes to all the other leaf nodes, and the data received could be from any other leaf nodes.</span></span> <span data-ttu-id="d3892-113">Wie bereits erwähnt, sind die Informationen darüber, ob der d- \_ Blatt Socket sich in einer Datenebene befindet, die sich in einem Stamm oder einem Datenblatt befindet, in der entsprechenden [**wsaprotocol \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) -Informationsstruktur für den Socket enthalten</span><span class="sxs-lookup"><span data-stu-id="d3892-113">As mentioned earlier, the information about whether the d\_leaf socket is in a rooted or nonrooted data plane is contained in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the socket.</span></span>

 

 
