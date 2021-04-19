---
description: Unterschiede zwischen regulären Punkt-zu-Punkt-Sockets und c-Stamm- \_ Multipoint-Sockets im SPI von Windows Sockets (Winsock).
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Semantische Unterschiede zwischen Multipoint-Sockets und regulären Sockets in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e4e94583ee653a8ec0bf19c743dddd3e16253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345247"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a><span data-ttu-id="fba39-103">Semantische Unterschiede zwischen Multipoint-Sockets und regulären Sockets in der SPI</span><span class="sxs-lookup"><span data-stu-id="fba39-103">Semantic Differences Between Multipoint Sockets and Regular Sockets in the SPI</span></span>

<span data-ttu-id="fba39-104">Auf der Steuerungsebene gibt es einige bedeutende semantische Unterschiede zwischen einem c \_ -root-Socket und einem regulären Punkt-zu-Punkt-Socket:</span><span class="sxs-lookup"><span data-stu-id="fba39-104">In the control plane, there are some significant semantic differences between a c\_root socket and a regular point-to-point socket:</span></span>

-   <span data-ttu-id="fba39-105">Der c-Stamm \_ Socket kann in [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) verwendet werden, um einem neuen Blatt beizutreten.</span><span class="sxs-lookup"><span data-stu-id="fba39-105">The c\_root socket can be used in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) to join a new leaf.</span></span>
-   <span data-ttu-id="fba39-106">Durch das Platzieren eines c-Stamm \_ Sockets in den Empfangsmodus (durch Aufrufen von [**wsplauschen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) wird nicht verhindert, dass der c-Stamm \_ Socket in einem Aufruf von [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) zum Hinzufügen eines neuen Blatts oder zum Senden und empfangen von Multipoint-Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fba39-106">Placing a c\_root socket into the listening mode (by calling [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) does not preclude the c\_root socket from being used in a call to [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) to add a new leaf, or for sending and receiving multipoint data.</span></span>
-   <span data-ttu-id="fba39-107">Das Schließen eines c-Stamm \_ Sockets bewirkt, dass alle zugeordneten c- \_ Blatt Sockets eine Benachrichtigung über eine schließende FD erhalten \_ .</span><span class="sxs-lookup"><span data-stu-id="fba39-107">The closing of a c\_root socket will cause all the associated c\_leaf sockets to get FD\_CLOSE notification.</span></span>

<span data-ttu-id="fba39-108">Es gibt keine semantischen Unterschiede zwischen einem c \_ -Blatt Socket und einem regulären Socket in der Steuerungsebene, mit dem Unterschied, dass der c \_ -Blatt Socket in [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)verwendet werden kann und die Verwendung des c- \_ Blatt Sockets in [**wsplauschen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) anzeigt, dass nur Multipoint-Verbindungsanforderungen akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fba39-108">There are no semantic differences between a c\_leaf socket and a regular socket in the control plane, except that the c\_leaf socket can be used in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), and the use of c\_leaf socket in [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indicates that only multipoint connection requests should be accepted.</span></span>

<span data-ttu-id="fba39-109">In der Datenebene sind die semantischen Unterschiede zwischen dem d- \_ stammsocket und einem regulären Punkt-zu-Punkt-Socket</span><span class="sxs-lookup"><span data-stu-id="fba39-109">In the data plane, the semantic differences between the d\_root socket and a regular point-to-point socket are</span></span>

-   <span data-ttu-id="fba39-110">Die Daten, die auf dem d-Stamm Socket gesendet werden \_ , werden an alle Blätter in derselben Multipoint-Sitzung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="fba39-110">The data sent on the d\_root socket will be delivered to all the leaves in the same multipoint session.</span></span>
-   <span data-ttu-id="fba39-111">Die im Stamm-Socket von d empfangenen Daten \_ können von einem der Blätter stammen.</span><span class="sxs-lookup"><span data-stu-id="fba39-111">The data received on the d\_root socket may be from any of the leaves.</span></span>

<span data-ttu-id="fba39-112">Der d- \_ Blatt Socket in der Datenebene "Rooting" hat keinen semantischen Unterschied vom regulären Socket, aber in der Datenebene ohne Stamm werden die Daten, die auf dem d- \_ Blatt Socket gesendet werden, an alle anderen Endknoten gesendet, und die empfangenen Daten können von einem beliebigen anderen Blattknoten stammen.</span><span class="sxs-lookup"><span data-stu-id="fba39-112">The d\_leaf socket in the rooted data plane has no semantic difference from the regular socket, however, in the nonrooted data plane, the data sent on the d\_leaf socket will go to all of the other leaf nodes, and the data received could be from any of the other leaf nodes.</span></span> <span data-ttu-id="fba39-113">Wie bereits erwähnt, sind die Informationen darüber, ob der d- \_ Blatt Socket sich in einer Datenebene befindet, die sich in einem Stamm oder einem Datenblatt befindet, in der entsprechenden [**wsaprotocol \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) -Informationsstruktur für den Socket enthalten</span><span class="sxs-lookup"><span data-stu-id="fba39-113">As mentioned earlier, the information about whether the d\_leaf socket is in a rooted or nonrooted data plane is contained in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the socket.</span></span>

 

 
