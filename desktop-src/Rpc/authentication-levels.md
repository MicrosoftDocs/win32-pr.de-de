---
title: Authentifizierungs Ebenen
description: Microsoft RPC bietet mehrere Authentifizierungs Ebenen.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5fd25efb84b4ee2834e6f79c7fdd21dd903d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206710"
---
# <a name="authentication-levels"></a><span data-ttu-id="5ae60-103">Authentifizierungs Ebenen</span><span class="sxs-lookup"><span data-stu-id="5ae60-103">Authentication Levels</span></span>

<span data-ttu-id="5ae60-104">Microsoft RPC bietet mehrere Authentifizierungs Ebenen.</span><span class="sxs-lookup"><span data-stu-id="5ae60-104">Microsoft RPC provides multiple levels of authentication.</span></span> <span data-ttu-id="5ae60-105">Abhängig von der Authentifizierungs Ebene kann der Ursprung des Datenverkehrs (welcher Sicherheits Prinzipal den Datenverkehr gesendet hat) überprüft werden, wenn die Verbindung hergestellt wird, wenn der Client einen neuen Remote Prozedur aufzurufen startet oder während jedes Paket Austauschs zwischen Client und Server.</span><span class="sxs-lookup"><span data-stu-id="5ae60-105">Depending on the authentication level, the origin of the traffic (which security principal sent the traffic) can be verified when the connection is established, when the client starts a new remote procedure call, or during each packet exchange between the client and server.</span></span>

<span data-ttu-id="5ae60-106">Auch wenn der Absender des Datenverkehrs überprüft wird, ist die Sicherheit weiterhin schwach, da bei dieser Überprüfung nicht sichergestellt wird, dass das Paket nicht geändert oder beschädigt wurde. Es wird nur überprüft, ob das Paket vom angegebenen Prinzipal stammt.</span><span class="sxs-lookup"><span data-stu-id="5ae60-106">Even when the sender of the traffic is verified, security is still weak, since such verification does not ensure the packet was not modified or corrupted en route; it only verifies that the packet came from the given principal.</span></span> <span data-ttu-id="5ae60-107">Um die Sicherheit zu erhöhen, können verteilte Anwendungen die RPC-Lauf Zeit Bibliothek festlegen, um sicherzustellen, dass keine der zwischen Client und Server ausgetauschten Daten geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5ae60-107">For greater security, distributed applications can set the RPC run-time library to verify that none of the data exchanged between the client and server is modified.</span></span> <span data-ttu-id="5ae60-108">Die RPC-Bibliothek kann auch den Inhalt jedes Pakets verschlüsseln, bevor Sie gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ae60-108">The RPC library can also encrypt the contents of every packet before sending it.</span></span> <span data-ttu-id="5ae60-109">Im Allgemeinen sollten Anwendungen, die Ihren Datenverkehr sichern möchten, nur die letzten zwei Ebenen verwenden – Integrität und Datenschutz.</span><span class="sxs-lookup"><span data-stu-id="5ae60-109">In general, applications that want to secure their traffic should use only the last two levels—integrity and privacy.</span></span>

<span data-ttu-id="5ae60-110">Beachten Sie, dass ein höheres Maß an Authentifizierung einen höheren Berechnungs Aufwand erfordert.</span><span class="sxs-lookup"><span data-stu-id="5ae60-110">Be aware that higher levels of authentication require higher computational overhead.</span></span> <span data-ttu-id="5ae60-111">Als Entwickler müssen Sie sich entscheiden, was für Ihre Anwendung wichtiger ist – Geschwindigkeit oder Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="5ae60-111">You, as the developer, must decide which is more important for your application—speed or security.</span></span> <span data-ttu-id="5ae60-112">Die meisten Entwickler werden feststellen, dass Sie bei einigen Leistungstests akzeptable Leistungsstufen erzielen und gleichzeitig eine angemessene Sicherheit gewährleisten können.</span><span class="sxs-lookup"><span data-stu-id="5ae60-112">Most developers find that with some performance testing, they can achieve acceptable performance levels while maintaining adequate security.</span></span>

<span data-ttu-id="5ae60-113">Die Client-und Server Teile der verteilten Anwendung müssen die gleiche Authentifizierungs Ebene verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ae60-113">The client and the server portions of the distributed application must use the same authentication level.</span></span> <span data-ttu-id="5ae60-114">Eine Liste der RPC-Authentifizierungs Ebenen finden Sie unter [Konstanten auf Authentifizierungs Ebene](authentication-level-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5ae60-114">For a list of RPC authentication levels, see [Authentication-Level Constants](authentication-level-constants.md).</span></span>

 

 




