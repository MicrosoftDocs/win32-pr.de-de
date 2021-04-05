---
description: Wenn Multicasting verwendet wird, ist es in der Regel erforderlich, den Bereich anzugeben, in dem der Multicast auftreten soll.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: SIO_MULTICAST_SCOPE Befehls Code für WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a43e461907dcded8e59c6ffee9b1376989d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042009"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a><span data-ttu-id="c3e2d-103">SIO- \_ Multicast- \_ Bereichs Befehls Code für WSAIoctl</span><span class="sxs-lookup"><span data-stu-id="c3e2d-103">SIO\_MULTICAST\_SCOPE Command Code for WSAIoctl</span></span>

<span data-ttu-id="c3e2d-104">Wenn Multicasting verwendet wird, ist es in der Regel erforderlich, den *Bereich* anzugeben, in dem der Multicast auftreten soll.</span><span class="sxs-lookup"><span data-stu-id="c3e2d-104">When multicasting is employed, it is usually necessary to specify the *scope* over which the multicast should occur.</span></span> <span data-ttu-id="c3e2d-105">Der Bereich wird als die Anzahl der zu deckenden Routing Netzwerksegmente definiert.</span><span class="sxs-lookup"><span data-stu-id="c3e2d-105">Scope is defined as the number of routed network segments to be covered.</span></span> <span data-ttu-id="c3e2d-106">Ein Bereich von 0 (null) gibt an, dass die Multicast Übertragung nicht bei der Übertragung platziert würde, sondern über Sockets innerhalb des lokalen Hosts verteilt werden könnte.</span><span class="sxs-lookup"><span data-stu-id="c3e2d-106">A scope of zero would indicate that the multicast transmission would not be placed on the wire but could be disseminated across sockets within the local host.</span></span> <span data-ttu-id="c3e2d-107">Ein Bereichs Wert von 1 (Standardwert) gibt an, dass die Übertragung in das Netzwerk übertragen wird, ohne Router zu überschreiten.</span><span class="sxs-lookup"><span data-stu-id="c3e2d-107">A scope value of 1 (the default) indicates that the transmission will be placed on the wire, but will not cross any routers.</span></span> <span data-ttu-id="c3e2d-108">Höhere Bereichs Werte bestimmen die Anzahl von Routern, die möglicherweise überschritten werden.</span><span class="sxs-lookup"><span data-stu-id="c3e2d-108">Higher scope values determine the number of routers that may be crossed.</span></span> <span data-ttu-id="c3e2d-109">Beachten Sie, dass dies dem Time-to-Live (TTL)-Parameter in IP-Multicasting entspricht.</span><span class="sxs-lookup"><span data-stu-id="c3e2d-109">Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.</span></span>

<span data-ttu-id="c3e2d-110">Die Funktion " [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) " wird verwendet, um einen Blattknoten mit der Multipoint-Sitzung zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="c3e2d-110">The function [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) is used to join a leaf node into the multipoint session.</span></span> <span data-ttu-id="c3e2d-111">Im folgenden finden Sie eine Erläuterung zur Verwendung dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="c3e2d-111">See the following for a discussion on how this function is utilized.</span></span>

 

 



