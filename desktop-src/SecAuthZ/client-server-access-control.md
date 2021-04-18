---
description: Eine Serveranwendung stellt Dienste für Clients bereit.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Client/Server-Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b1d349abb2d55f00b9801c9bb493437fa858eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368156"
---
# <a name="clientserver-access-control"></a><span data-ttu-id="11dbe-103">Client/Server-Access Control</span><span class="sxs-lookup"><span data-stu-id="11dbe-103">Client/Server Access Control</span></span>

<span data-ttu-id="11dbe-104">Eine Serveranwendung stellt Dienste für Clients bereit.</span><span class="sxs-lookup"><span data-stu-id="11dbe-104">A server application provides services to clients.</span></span> <span data-ttu-id="11dbe-105">Beispielsweise könnte ein Server die folgenden Dienste im Auftrag eines Clients ausführen:</span><span class="sxs-lookup"><span data-stu-id="11dbe-105">For example, a server could perform the following services on behalf of a client:</span></span>

-   <span data-ttu-id="11dbe-106">Speichern und Abrufen von Informationen aus einer privaten Datenbank</span><span class="sxs-lookup"><span data-stu-id="11dbe-106">Save and retrieve information from a private database</span></span>
-   <span data-ttu-id="11dbe-107">Zugreifen auf Netzwerkressourcen</span><span class="sxs-lookup"><span data-stu-id="11dbe-107">Access network resources</span></span>
-   <span data-ttu-id="11dbe-108">Starten von [*Prozessen*](/windows/desktop/SecGloss/p-gly) im [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des Clients auf dem Computer des Servers</span><span class="sxs-lookup"><span data-stu-id="11dbe-108">Start [*processes*](/windows/desktop/SecGloss/p-gly) in the client's [*security context*](/windows/desktop/SecGloss/s-gly) on the server's computer</span></span>

<span data-ttu-id="11dbe-109">Ein geschützter Server steuert den Zugriff auf seine Dienste.</span><span class="sxs-lookup"><span data-stu-id="11dbe-109">A protected server controls access to its services.</span></span> <span data-ttu-id="11dbe-110">Windows bietet Sicherheitsunterstützung, die es einem Server ermöglicht, folgende Aufgaben durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="11dbe-110">Windows provides security support that enables a server to do the following:</span></span>

-   <span data-ttu-id="11dbe-111">Nimmt die Identität des [*Sicherheits Kontexts*](/windows/desktop/SecGloss/s-gly)eines Clients an. Dies bewirkt, dass das System die meisten Zugriffs-und [*Berechtigungs*](/windows/desktop/SecGloss/p-gly) Prüfungen für das [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) des Clients anstelle des Servers durchführt.</span><span class="sxs-lookup"><span data-stu-id="11dbe-111">Impersonate a client's [*security context*](/windows/desktop/SecGloss/s-gly), which causes the system to perform most access and [*privilege*](/windows/desktop/SecGloss/p-gly) checks against the client's [*access token*](/windows/desktop/SecGloss/a-gly) rather than the server's</span></span>
-   <span data-ttu-id="11dbe-112">Anmelden eines Clients auf dem Computer des Servers</span><span class="sxs-lookup"><span data-stu-id="11dbe-112">Log a client on to the server's computer</span></span>
-   <span data-ttu-id="11dbe-113">Herstellen einer Verbindung mit Netzwerkressourcen über den Sicherheitskontext des Clients</span><span class="sxs-lookup"><span data-stu-id="11dbe-113">Connect to network resources using the client's security context</span></span>
-   <span data-ttu-id="11dbe-114">Erstellen von [*Sicherheits Deskriptoren*](/windows/desktop/SecGloss/s-gly) zum Schutz privater Objekte</span><span class="sxs-lookup"><span data-stu-id="11dbe-114">Create [*security descriptors*](/windows/desktop/SecGloss/s-gly) to protect private objects</span></span>
-   <span data-ttu-id="11dbe-115">Bestimmen, ob eine Sicherheits Beschreibung den Zugriff auf einen Client zulässt</span><span class="sxs-lookup"><span data-stu-id="11dbe-115">Determine whether a security descriptor allows access to a client</span></span>
-   <span data-ttu-id="11dbe-116">Bestimmen, ob ein Berechtigungs Satz im Token eines Clients aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="11dbe-116">Determine whether a set of privileges are enabled in a client's token</span></span>
-   <span data-ttu-id="11dbe-117">Generieren von Überwachungs Meldungen im Sicherheits Ereignisprotokoll zum Aufzeichnen von versuchen eines Clients, auf Objekte zuzugreifen oder Berechtigungen zu verwenden</span><span class="sxs-lookup"><span data-stu-id="11dbe-117">Generate audit messages in the security event log to record attempts by a client to access objects or use privileges</span></span>

 

 
