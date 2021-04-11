---
description: Das Kerberos-Protokoll besteht aus drei unter Protokollen.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Kerberos-Unterprotokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c06c26013e065254458ad403cdff99fbb2edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216341"
---
# <a name="kerberos-subprotocols"></a><span data-ttu-id="64e2e-103">Kerberos-Unterprotokolle</span><span class="sxs-lookup"><span data-stu-id="64e2e-103">Kerberos Subprotocols</span></span>

<span data-ttu-id="64e2e-104">Das [*Kerberos-Protokoll*](../secgloss/k-gly.md) besteht aus drei unter Protokollen.</span><span class="sxs-lookup"><span data-stu-id="64e2e-104">The [*Kerberos protocol*](../secgloss/k-gly.md) is composed of three subprotocols.</span></span>



| <span data-ttu-id="64e2e-105">Unter Protokoll</span><span class="sxs-lookup"><span data-stu-id="64e2e-105">Subprotocol</span></span>                                                                         | <span data-ttu-id="64e2e-106">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64e2e-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64e2e-107">Authentifizierungsdienstaustausch</span><span class="sxs-lookup"><span data-stu-id="64e2e-107">Authentication Service Exchange</span></span>](authentication-service-exchange.md)<br/>   | <span data-ttu-id="64e2e-108">In diesem unter Protokoll gibt der [*Schlüsselverteilungscenter*](../secgloss/k-gly.md) (KDC) dem Client einen Anmelde [*Sitzungsschlüssel*](../secgloss/s-gly.md) und ein Ticket-Zuteilungs Ticket (TGT).</span><span class="sxs-lookup"><span data-stu-id="64e2e-108">In this subprotocol, the [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) gives the client a logon [*session key*](../secgloss/s-gly.md) and a ticket-granting ticket (TGT).</span></span><br/> |
| [<span data-ttu-id="64e2e-109">Ticket-Granting-Dienstaustausch</span><span class="sxs-lookup"><span data-stu-id="64e2e-109">Ticket-Granting Service Exchange</span></span>](ticket-granting-service-exchange.md)<br/> | <span data-ttu-id="64e2e-110">In diesem Subprotokoll verteilt der KDC einen Dienst Sitzungsschlüssel und ein Ticket für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="64e2e-110">In this subprotocol, the KDC distributes a service session key and a ticket for the service.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="64e2e-111">Client-/Server-Exchange</span><span class="sxs-lookup"><span data-stu-id="64e2e-111">Client/Server Exchange</span></span>](client-server-exchange.md)<br/>                     | <span data-ttu-id="64e2e-112">In diesem Subprotokoll stellt der Client das Ticket für den Zutritt zu einem Dienst dar.</span><span class="sxs-lookup"><span data-stu-id="64e2e-112">In this subprotocol, the client presents the ticket for admission to a service.</span></span><br/>                                                                                                                                                                                                                         |



 

 

 
