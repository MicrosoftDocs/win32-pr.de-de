---
description: In einem Client-/Serveranwendungsmodell sind Clients Programme, die im Auftrag von Benutzern agieren, die etwas erledigt haben.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Grundlegende Authentifizierungs Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130429"
---
# <a name="basic-authentication-concepts"></a><span data-ttu-id="3568f-103">Grundlegende Authentifizierungs Konzepte</span><span class="sxs-lookup"><span data-stu-id="3568f-103">Basic Authentication Concepts</span></span>

<span data-ttu-id="3568f-104">In einem Client-/Serveranwendungsmodell sind Clients Programme, die im Auftrag von Benutzern agieren, die etwas erledigt haben.</span><span class="sxs-lookup"><span data-stu-id="3568f-104">In a client/server application model, clients are programs acting on behalf of users who need something done.</span></span> <span data-ttu-id="3568f-105">Dabei kann es sich um das Öffnen und Verwenden einer Datei, das Zugreifen auf ein Postfach, das Abfragen einer Datenbank oder das Drucken eines Dokuments handeln.</span><span class="sxs-lookup"><span data-stu-id="3568f-105">This might be opening and using a file, accessing a mailbox, querying a database, or printing a document.</span></span> <span data-ttu-id="3568f-106">Server sind Programme, die Dienste für Clients bereitstellen, z. b. Dateispeicher, e-Mail-Verarbeitung, Abfrage Verarbeitung und Druck Spoolvorgang.</span><span class="sxs-lookup"><span data-stu-id="3568f-106">Servers are programs providing services to clients such as file storage, mail handling, query processing, and print spooling.</span></span> <span data-ttu-id="3568f-107">Von Clients wird eine Aktion initiiert, die Server antwortet.</span><span class="sxs-lookup"><span data-stu-id="3568f-107">Clients initiate action, servers respond.</span></span> <span data-ttu-id="3568f-108">Ein Server lauscht in der Regel an einem Kommunikationsport, der darauf wartet, dass Clients eine Verbindung herstellen und Dienst anfordern.</span><span class="sxs-lookup"><span data-stu-id="3568f-108">Typically, a server listens at a communications port waiting for clients to connect and ask for service.</span></span>

<span data-ttu-id="3568f-109">Im Kerberos-Protokollmodell beginnt jede Client/Server-Verbindung mit der Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="3568f-109">In the Kerberos protocol model, every client/server connection begins with authentication.</span></span> <span data-ttu-id="3568f-110">Client und Server wiederum durchlaufen schrittweise eine Reihenfolge von Aktionen, um für die Teilnehmer auf beiden Seiten der Verbindung die Echtheit des anderen Teilnehmers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3568f-110">Client and server, in turn, step through a sequence of actions designed to verify to the party on each end of the connection that the party on the other end is genuine.</span></span> <span data-ttu-id="3568f-111">Wenn die Authentifizierung erfolgreich war, wird das Setup für die Sitzung abgeschlossen, und es wird eine sichere Client-/Serversitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="3568f-111">If authentication is successful, session setup completes and a secure client/server session is established.</span></span>

<span data-ttu-id="3568f-112">Das Kerberos-Protokoll verwendet Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3568f-112">The Kerberos protocol makes use of:</span></span>

-   [<span data-ttu-id="3568f-113">Schlüssel Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="3568f-113">Key authentication</span></span>](key-authentication.md)
-   [<span data-ttu-id="3568f-114">Authenticator-Meldungen</span><span class="sxs-lookup"><span data-stu-id="3568f-114">Authenticator messages</span></span>](authenticator-messages.md)
-   [<span data-ttu-id="3568f-115">Schlüsselverteilung</span><span class="sxs-lookup"><span data-stu-id="3568f-115">Key distribution</span></span>](key-distribution.md)
-   [<span data-ttu-id="3568f-116">Sitzungs Tickets</span><span class="sxs-lookup"><span data-stu-id="3568f-116">Session tickets</span></span>](session-tickets.md)
-   [<span data-ttu-id="3568f-117">Tickets mit Ticket Gewährung</span><span class="sxs-lookup"><span data-stu-id="3568f-117">Ticket-granting tickets</span></span>](ticket-granting-tickets.md)

 

 



