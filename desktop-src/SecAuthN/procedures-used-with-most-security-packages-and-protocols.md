---
description: Das SSPI-Modell (Security Support Provider Interface) bietet eine einzige Schnittstelle für eine Client/Server-Transport Anwendung, die die verschiedenen auf einem Computer oder Netzwerk verfügbaren Sicherheitspakete verwendet.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Prozeduren für die meisten Sicherheitspakete und Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1053f21fdd085680da1e72f0acf9c7f816e788ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525853"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a><span data-ttu-id="6c3e8-103">Prozeduren für die meisten Sicherheitspakete und Protokolle</span><span class="sxs-lookup"><span data-stu-id="6c3e8-103">Procedures Used with Most Security Packages and Protocols</span></span>

<span data-ttu-id="6c3e8-104">Das SSPI-Modell ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) bietet eine einzige Schnittstelle für eine Client/Server-Transport Anwendung, die die verschiedenen auf einem Computer oder Netzwerk verfügbaren [*Sicherheitspakete*](../secgloss/s-gly.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c3e8-104">The [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) model provides a single interface for a client/server transport application using the various [*security packages*](../secgloss/s-gly.md) available on a computer or network.</span></span> <span data-ttu-id="6c3e8-105">SSPI ermöglicht einer Anwendung die Verwendung eines Sicherheitspakets, ohne die zugrunde liegenden [*Sicherheitsprotokolle*](../secgloss/s-gly.md) des Pakets zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="6c3e8-105">SSPI allows an application to use a security package without dealing with the underlying [*security protocols*](../secgloss/s-gly.md) of the package.</span></span> <span data-ttu-id="6c3e8-106">Gleichzeitig ermöglicht SSPI auch anspruchsvolle, sicherheitsbewusste Anwendungen, um die erweiterten Funktionen bestimmter Sicherheitspakete nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="6c3e8-106">At the same time, SSPI also allows sophisticated, security-aware applications to take advantage of the advanced capabilities of specific security packages.</span></span>

<span data-ttu-id="6c3e8-107">Anwendungen initialisieren SSPI mithilfe der folgenden Schritte, um eine Netzwerkverbindung für die meisten Sicherheitspakete zu sichern:</span><span class="sxs-lookup"><span data-stu-id="6c3e8-107">Applications initialize SSPI using the following steps to secure a network connection for most security packages:</span></span>

-   [<span data-ttu-id="6c3e8-108">Verwenden von secbufferde SC und secbuffer</span><span class="sxs-lookup"><span data-stu-id="6c3e8-108">Using SecBufferDesc and SecBuffer</span></span>](using-secbufferdesc-and-secbuffer.md)
-   [<span data-ttu-id="6c3e8-109">SSPI wird initialisiert.</span><span class="sxs-lookup"><span data-stu-id="6c3e8-109">Initializing SSPI</span></span>](initializing-sspi.md)
-   [<span data-ttu-id="6c3e8-110">Einrichten einer sicheren Verbindung mit der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="6c3e8-110">Establishing a Secure Connection with Authentication</span></span>](establishing-a-secure-connection-with-authentication.md)
-   [<span data-ttu-id="6c3e8-111">Sicherstellen der Kommunikations Integrität während des Nachrichten Austauschs</span><span class="sxs-lookup"><span data-stu-id="6c3e8-111">Ensuring Communication Integrity During Message Exchange</span></span>](ensuring-communication-integrity-during-message-exchange.md)
-   [<span data-ttu-id="6c3e8-112">Beenden einer SSPI-Sitzung</span><span class="sxs-lookup"><span data-stu-id="6c3e8-112">Ending an SSPI Session</span></span>](ending-an-sspi-session.md)

 

 
