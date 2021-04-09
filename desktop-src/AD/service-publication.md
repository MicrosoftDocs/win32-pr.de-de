---
title: Dienstveröffentlichung
description: Dienste kündigen sich selbst mithilfe von in Active Directory Domain Services gespeicherten Objekten an.
ms.assetid: 69e9256f-40ee-4aed-8213-1bbda0e508af
ms.tgt_platform: multiple
keywords:
- Dienst Veröffentlichung AD
- Active Directory, Verwendung von, Dienst Veröffentlichung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9437d9f4aa5184c53f2962d7b2640e933107501f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036340"
---
# <a name="service-publication"></a><span data-ttu-id="7fe4d-105">Dienstveröffentlichung</span><span class="sxs-lookup"><span data-stu-id="7fe4d-105">Service Publication</span></span>

<span data-ttu-id="7fe4d-106">Dienste kündigen sich selbst mithilfe von in Active Directory Domain Services gespeicherten Objekten an.</span><span class="sxs-lookup"><span data-stu-id="7fe4d-106">Services advertise themselves using objects stored in Active Directory Domain Services.</span></span> <span data-ttu-id="7fe4d-107">Dies wird als *Dienst Veröffentlichung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fe4d-107">This is known as *service publication*.</span></span> <span data-ttu-id="7fe4d-108">Clients Fragen das Verzeichnis nach Diensten ab.</span><span class="sxs-lookup"><span data-stu-id="7fe4d-108">Clients query the directory to locate services.</span></span> <span data-ttu-id="7fe4d-109">Dies wird als *Client-Dienst Rendezvous* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fe4d-109">This is called *client-service rendezvous*.</span></span> <span data-ttu-id="7fe4d-110">In diesem Abschnitt werden die Typen von Verzeichnis Objekten erläutert, die für die Dienst Veröffentlichung verwendet werden, und es wird erläutert, wie Sie für Client-Dienst Rendezvous verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7fe4d-110">This section discusses the types of directory objects used for service publication and explains how they are used for client-service rendezvous.</span></span>

<span data-ttu-id="7fe4d-111">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="7fe4d-111">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="7fe4d-112">Eine Übersicht über die Dienst Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="7fe4d-112">An overview of service publication</span></span>](about-service-publication.md)
-   [<span data-ttu-id="7fe4d-113">Sicherheitsprobleme bei der Dienst Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="7fe4d-113">Security issues for service publication</span></span>](security-issues-for-service-publication.md)
-   [<span data-ttu-id="7fe4d-114">Verbindungspunkt Objekte</span><span class="sxs-lookup"><span data-stu-id="7fe4d-114">Connection point objects</span></span>](connection-points.md)
-   [<span data-ttu-id="7fe4d-115">Veröffentlichen mit Dienst Verbindungs Punkten (SCPs)</span><span class="sxs-lookup"><span data-stu-id="7fe4d-115">Publishing with service connection points (SCPs)</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="7fe4d-116">Welche Informationen werden in einem Dienst Verbindungspunkt gespeichert?</span><span class="sxs-lookup"><span data-stu-id="7fe4d-116">What information to store in a service connection point</span></span>](service-connection-point-properties.md)
-   [<span data-ttu-id="7fe4d-117">Erstellen eines Dienst Verbindungs Punkts</span><span class="sxs-lookup"><span data-stu-id="7fe4d-117">Where to create a service connection point</span></span>](where-to-create-a-service-connection-point.md)
-   [<span data-ttu-id="7fe4d-118">Veröffentlichen von replizierbaren, Host basierten und Daten Bank Diensten mithilfe von Dienst Verbindungs Punkten</span><span class="sxs-lookup"><span data-stu-id="7fe4d-118">How to publish replicable, host-based, and database services using service connection points</span></span>](service-connection-points-for-replicated-host-based-and-database-services.md)
-   [<span data-ttu-id="7fe4d-119">Erstellen und Verwalten eines Dienst Verbindungs Punkts</span><span class="sxs-lookup"><span data-stu-id="7fe4d-119">Creating and maintaining a service connection point</span></span>](creating-and-maintaining-a-service-connection-point.md)
-   [<span data-ttu-id="7fe4d-120">Wie ein Client einen SCP abfragt und verwendet, um eine Bindung an eine Dienst Instanz herzustellen</span><span class="sxs-lookup"><span data-stu-id="7fe4d-120">How a client queries for an SCP and uses it to bind to a service instance</span></span>](how-clients-find-and-use-a-service-connection-point.md)
-   [<span data-ttu-id="7fe4d-121">Verwenden der RPC-Namensdienst-APIs (RpcNs) zum Veröffentlichen eines RPC-Diensts</span><span class="sxs-lookup"><span data-stu-id="7fe4d-121">Using the RPC name service (RpcNs) APIs to publish an RPC service</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="7fe4d-122">Windows Sockets-Registrierung und-Lösung (RNR) zum Veröffentlichen eines Windows Sockets-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="7fe4d-122">Windows Sockets registration and resolution (RnR) to publish a Windows Sockets service</span></span>](publishing-with-windows-sockets-registration-and-resolution.md)
-   [<span data-ttu-id="7fe4d-123">Veröffentlichung von COM-basierten Diensten im com+-Klassen Speicher</span><span class="sxs-lookup"><span data-stu-id="7fe4d-123">Publication of COM-based services in the COM+ class store</span></span>](publishing-com-services.md)

<span data-ttu-id="7fe4d-124">Weitere Informationen dazu, wie sich Dienste und Clients gegenseitig authentifizieren, finden [Sie unter gegenseitige Authentifizierung mithilfe von Kerberos](mutual-authentication-using-kerberos.md).</span><span class="sxs-lookup"><span data-stu-id="7fe4d-124">For more information about how services and clients authenticate each other, see [Mutual Authentication Using Kerberos](mutual-authentication-using-kerberos.md).</span></span> <span data-ttu-id="7fe4d-125">Weitere Informationen zu Dienst Sicherheits Kontexten und Anmeldekonten finden Sie unter [Dienst Anmeldekonten](service-logon-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="7fe4d-125">For more information about service security contexts and logon accounts, see [Service Logon Accounts](service-logon-accounts.md).</span></span>

 

 




