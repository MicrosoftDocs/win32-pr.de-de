---
description: Client-/Server-Exchange
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Client-/Server-Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6274705ef6719c846f0551f90fca8790ba89f2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131060"
---
# <a name="clientserver-exchange"></a><span data-ttu-id="ca51d-103">Client-/Server-Exchange</span><span class="sxs-lookup"><span data-stu-id="ca51d-103">Client/Server Exchange</span></span>

<span data-ttu-id="ca51d-104">Wenn ein Benutzer ein Ticket für einen Server hat, kann der Arbeitsstations Client eine sichere Kommunikationssitzung mit diesem Server einrichten.</span><span class="sxs-lookup"><span data-stu-id="ca51d-104">After a user has a ticket to a server, the workstation client can establish a secure communications session with that server.</span></span>

<span data-ttu-id="ca51d-105">**So richten Sie eine sichere Kommunikationssitzung mit einem Server ein**</span><span class="sxs-lookup"><span data-stu-id="ca51d-105">**To establish a secure communications session with a server**</span></span>

1.  <span data-ttu-id="ca51d-106">Der Client sendet dem Server eine Nachricht vom Typ krb \_ AP \_ req (Kerberos-Anwendungsanforderung).</span><span class="sxs-lookup"><span data-stu-id="ca51d-106">The client sends the server a message of type KRB\_AP\_REQ (Kerberos Application Request).</span></span> <span data-ttu-id="ca51d-107">Diese Nachricht enthält eine Authentifikator-Nachricht, die mit dem Schlüssel verschlüsselt ist, der vom [*Schlüsselverteilungscenter*](/windows/desktop/SecGloss/k-gly) (KDC) für die Sitzung mit dem Server gesendet wird, das Ticket für Sitzungen mit dem Server und ein Flag, das angibt, ob der Client die gegenseitige Authentifizierung anfordert.</span><span class="sxs-lookup"><span data-stu-id="ca51d-107">This message contains an authenticator message that is encrypted with the key sent by the [*Key Distribution Center*](/windows/desktop/SecGloss/k-gly) (KDC) for the session with the server, the ticket for sessions with the server, and a flag that indicates whether the client requests mutual authentication.</span></span> <span data-ttu-id="ca51d-108">Das Festlegen des Flags, das die gegenseitige Authentifizierung anfordert, ist eine der Optionen beim Konfigurieren von [*Kerberos*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="ca51d-108">Setting the flag that requests mutual authentication is one of the options in configuring [*Kerberos*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="ca51d-109">Der Benutzer wird nie gefragt, ob eine gegenseitige Authentifizierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca51d-109">The user is never asked whether mutual authentication should be used.</span></span>
2.  <span data-ttu-id="ca51d-110">Der Server empfängt krb \_ AP \_ req, entschlüsselt das Ticket und extrahiert die Autorisierungs Daten des Benutzers und den [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="ca51d-110">The server receives KRB\_AP\_REQ, decrypts the ticket, and extracts the user's authorization data and the [*session key*](/windows/desktop/SecGloss/s-gly).</span></span>
3.  <span data-ttu-id="ca51d-111">Der Server verwendet den Sitzungsschlüssel aus dem Ticket zum Entschlüsseln der Authentifikator-Nachricht des Benutzers und wertet den Zeitstempel in aus.</span><span class="sxs-lookup"><span data-stu-id="ca51d-111">The server uses the session key from the ticket to decrypt the user's authenticator message and evaluates the time stamp inside.</span></span>
4.  <span data-ttu-id="ca51d-112">Wenn die Authentifikator-Nachricht gültig ist, überprüft der Server das Flag für die gegenseitige Authentifizierung in der Client Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ca51d-112">If the authenticator message is valid, the server checks the mutual authentication flag in the client's request.</span></span>
5.  <span data-ttu-id="ca51d-113">Wenn das Flag für die gegenseitige Authentifizierung festgelegt ist, verwendet der Server den Sitzungsschlüssel, um die Uhrzeit aus der Authentifikator-Nachricht des Benutzers zu verschlüsseln, und gibt das Ergebnis in einer Nachricht vom Typ krb \_ AP \_ Rep (Kerberos-Anwendungs Antwort) zurück.</span><span class="sxs-lookup"><span data-stu-id="ca51d-113">If the mutual authentication flag is set, the server uses the session key to encrypt the time from the user's authenticator message and returns the result in a message of type KRB\_AP\_REP (Kerberos Application Reply).</span></span>
6.  <span data-ttu-id="ca51d-114">Wenn der Client krb \_ AP \_ Rep empfängt, entschlüsselt er die Authenticator-Nachricht des Servers mit dem Sitzungsschlüssel, den er mit dem Server freigibt, und vergleicht die vom Dienst zurück gesendete Zeit mit dem Zeitpunkt in der ursprünglichen authentifikatornachricht.</span><span class="sxs-lookup"><span data-stu-id="ca51d-114">When the client receives KRB\_AP\_REP, it decrypts the server's authenticator message with the session key it shares with the server and compares the time sent back by the service with the time in its original authenticator message.</span></span> <span data-ttu-id="ca51d-115">Wenn Sie einander entsprechen, ist der Client sicher, dass der Dienst echt ist und die Verbindung fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="ca51d-115">If they match, the client is assured that the service is genuine, and the connection proceeds.</span></span>

 

 
