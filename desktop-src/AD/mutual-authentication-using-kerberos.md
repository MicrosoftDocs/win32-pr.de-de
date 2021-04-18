---
title: Gegenseitige Authentifizierung mithilfe von Kerberos
description: Die gegenseitige Authentifizierung ist eine Sicherheitsfunktion, bei der ein Client Prozess die Identität eines Diensts nachweisen muss, und der Dienst muss die Identität des Clients nachweisen, bevor der Anwendungs Datenverkehr über die Client-/Dienst-Verbindung übertragen wird.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, Verwendung von gegenseitiger Authentifizierung
- Active Directory, Verwendung, Sicherheit, gegenseitige Authentifizierung
- Sicherheits-AD
- Sicherheits-AD, gegenseitige Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cf2e68c1983dde9221cc3fa89866b5358ee6eb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106340258"
---
# <a name="mutual-authentication-using-kerberos"></a><span data-ttu-id="253b8-107">Gegenseitige Authentifizierung mithilfe von Kerberos</span><span class="sxs-lookup"><span data-stu-id="253b8-107">Mutual Authentication Using Kerberos</span></span>

<span data-ttu-id="253b8-108">Die gegenseitige Authentifizierung ist eine Sicherheitsfunktion, bei der ein Client Prozess die Identität eines Diensts nachweisen muss, und der Dienst muss die Identität des Clients nachweisen, bevor der Anwendungs Datenverkehr über die Client-/Dienst-Verbindung übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="253b8-108">Mutual authentication is a security feature in which a client process must prove its identity to a service, and the service must prove its identity to the client, before any application traffic is transmitted over the client/service connection.</span></span>

<span data-ttu-id="253b8-109">Active Directory Domain Services und Windows unterstützen Dienst Prinzipal Namen (Service Principal Names, SPN), bei denen es sich um eine Schlüsselkomponente im Kerberos-Mechanismus handelt, mit der ein Client einen Dienst authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="253b8-109">Active Directory Domain Services and Windows provide support for service principal names (SPN), which are a key component in the Kerberos mechanism by which a client authenticates a service.</span></span> <span data-ttu-id="253b8-110">Ein SPN ist ein eindeutiger Name, der eine Instanz eines Diensts identifiziert und dem Anmelde Konto zugeordnet ist, unter dem die Dienst Instanz ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="253b8-110">An SPN is a unique name that identifies an instance of a service and is associated with the logon account under which the service instance runs.</span></span> <span data-ttu-id="253b8-111">Die Komponenten eines SPN sind so, dass ein Client einen SPN für einen Dienst ohne das Dienst Anmelde Konto verfassen kann.</span><span class="sxs-lookup"><span data-stu-id="253b8-111">The components of an SPN are such that a client can compose an SPN for a service without the service logon account.</span></span> <span data-ttu-id="253b8-112">Dies ermöglicht es dem Client, den Dienst zum Authentifizieren seines Kontos aufzufordern, auch wenn der Client nicht über den Kontonamen verfügt.</span><span class="sxs-lookup"><span data-stu-id="253b8-112">This enables the client to request the service to authenticate its account even though the client does not have the account name.</span></span>

<span data-ttu-id="253b8-113">Dieser Abschnitt enthält eine Übersicht über:</span><span class="sxs-lookup"><span data-stu-id="253b8-113">This section includes an overview of:</span></span>

-   <span data-ttu-id="253b8-114">Gegenseitige Authentifizierung mithilfe von Kerberos.</span><span class="sxs-lookup"><span data-stu-id="253b8-114">Mutual authentication using Kerberos.</span></span>
-   <span data-ttu-id="253b8-115">Erstellen eines eindeutigen SPN.</span><span class="sxs-lookup"><span data-stu-id="253b8-115">Composing a unique SPN.</span></span>
-   <span data-ttu-id="253b8-116">Gibt an, wie ein Dienst Installationsprogramm SPNs für das Konto Objekt registriert, das einer Dienst Instanz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="253b8-116">How a service installer registers SPNs on the account object associated with a service instance.</span></span>
-   <span data-ttu-id="253b8-117">Wie eine Client Anwendung das Dienst Verbindungspunkt-Objekt (Service Connection Point, Dienst Verbindungspunkt) einer Dienst Instanz in Active Directory Domain Services verwendet, um Daten abzurufen, aus denen ein SPN für den Dienst verfasst werden soll.</span><span class="sxs-lookup"><span data-stu-id="253b8-117">How a client application uses a service instance's service connection point (SCP) object in Active Directory Domain Services to retrieve data from which to compose an SPN for the service.</span></span>
-   <span data-ttu-id="253b8-118">Wie eine Client Anwendung einen Dienst-SPN in Verbindung mit der Security Support Provider Interface (SSPI) zum Authentifizieren des Diensts verwendet.</span><span class="sxs-lookup"><span data-stu-id="253b8-118">How a client application uses a service SPN in conjunction with the Security Support Provider Interface (SSPI) to authenticate the service.</span></span>
-   <span data-ttu-id="253b8-119">Ein Codebeispiel für eine Windows Sockets-Client-/Dienst-Anwendung, die einen SCP und SSPI verwendet, um die gegenseitige Authentifizierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="253b8-119">A code example for a Windows Sockets client/service application that uses an SCP and SSPI to perform mutual authentication.</span></span>
-   <span data-ttu-id="253b8-120">Ein Codebeispiel für einen RPC-Client/-Dienst, der die gegenseitige Authentifizierung mit dem RPC-Namensdienst und der RPC-Authentifizierung ausführt.</span><span class="sxs-lookup"><span data-stu-id="253b8-120">A code example for an RPC client/service that performs mutual authentication using the RPC name service and RPC authentication.</span></span>
-   <span data-ttu-id="253b8-121">Verwendung von SPNs für die gegenseitige Authentifizierung durch einen Windows Sockets Registration and Resolution-Dienst (RNR).</span><span class="sxs-lookup"><span data-stu-id="253b8-121">How a Windows Sockets Registration and Resolution (RnR) service uses SPNs to perform mutual authentication.</span></span>

<span data-ttu-id="253b8-122">In diesem Abschnitt wird die Verwendung Active Directory-Domäne Dienstanbieter für die gegenseitige Authentifizierung erläutert, insbesondere der Zweck von Dienst Verbindungs Punkten und Dienst Prinzipal Namen bei gegenseitiger Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="253b8-122">This section discusses using Active Directory Domain Service for mutual authentication, in particular, the purpose of service connection points and service principal names in mutual authentication.</span></span> <span data-ttu-id="253b8-123">Es handelt sich nicht um eine umfassende Erörterung der Verwendung von SSPI für die gegenseitige Authentifizierung oder die Authentifizierungs-und Sicherheitsunterstützung, die für RPC-und Windows Sockets-Anwendungen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="253b8-123">It is not a complete discussion of how to use SSPI for mutual authentication or the authentication and security support available for RPC and Windows Sockets applications.</span></span>

<span data-ttu-id="253b8-124">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="253b8-124">For more information, see:</span></span>

-   [<span data-ttu-id="253b8-125">Veröffentlichen mit Dienst Verbindungs Punkten</span><span class="sxs-lookup"><span data-stu-id="253b8-125">Publishing with service connection points</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="253b8-126">SSPI</span><span class="sxs-lookup"><span data-stu-id="253b8-126">SSPI</span></span>](/windows/desktop/SecAuthN/sspi)
-   [<span data-ttu-id="253b8-127">Windows-Sockets</span><span class="sxs-lookup"><span data-stu-id="253b8-127">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [<span data-ttu-id="253b8-128">RPC</span><span class="sxs-lookup"><span data-stu-id="253b8-128">RPC</span></span>](/windows/desktop/Rpc/rpc-start-page)

 

 