---
title: Grundlagen zu RPC
description: Um einen Remote Prozedur aufzurufen, müssen alle verteilten Anwendungen eine Bindung zwischen dem Client und dem Server erstellen.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856767"
---
# <a name="rpc-security-essentials"></a><span data-ttu-id="a96f2-103">Grundlagen zu RPC</span><span class="sxs-lookup"><span data-stu-id="a96f2-103">RPC Security Essentials</span></span>

<span data-ttu-id="a96f2-104">Um einen Remote Prozedur aufzurufen, müssen alle verteilten Anwendungen eine Bindung zwischen dem Client und dem Server erstellen.</span><span class="sxs-lookup"><span data-stu-id="a96f2-104">To complete any remote procedure call, all distributed applications must create a binding between the client and the server.</span></span> <span data-ttu-id="a96f2-105">Weitere Informationen zu Bindungen finden Sie unter [Bindung und Handles](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="a96f2-105">For more information on bindings, see [Binding and Handles](binding-and-handles.md).</span></span> <span data-ttu-id="a96f2-106">Um einen sicheren Remote Prozedur aufzurufen, sind zusätzliche Schritte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a96f2-106">To complete a secure remote procedure call, additional steps are necessary.</span></span> <span data-ttu-id="a96f2-107">Zuerst muss der Server einen Sicherheitsanbieter (Authentifizierungsdienst in der DCE-Terminologie) auswählen.</span><span class="sxs-lookup"><span data-stu-id="a96f2-107">First, the server must choose a security provider (authentication service in DCE terminology).</span></span> <span data-ttu-id="a96f2-108">Anschließend muss er sich für den Authentifizierungsmechanismus entscheiden.</span><span class="sxs-lookup"><span data-stu-id="a96f2-108">Then it must decide on its authentication mechanism.</span></span> <span data-ttu-id="a96f2-109">Danach erhält der Client eine Bindung an den Server und fordert einen sicheren Remote Prozedur Aufruf von der RPC-Laufzeit an und gibt verschiedene Sicherheitsoptionen an, z. b. Sicherheitsanbieter, Sicherheits-QoS-Optionen usw.</span><span class="sxs-lookup"><span data-stu-id="a96f2-109">After that, the client obtains a binding to the server, and requests a secure remote procedure call from the RPC run time, and specifies various security options, such as security provider, security QOS options, and so on.</span></span>

<span data-ttu-id="a96f2-110">In diesem Abschnitt werden die wesentlichen Konzepte und Informationen erläutert, die für die Verwendung der RPC-Funktionen erforderlich sind, um einen Client und Server für eine authentifizierte verteilte Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a96f2-110">This section explains the essential concepts and information required to use the RPC functions to create a client and server for an authenticated distributed application.</span></span> <span data-ttu-id="a96f2-111">Es ist in die folgenden Themen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="a96f2-111">It is organized into the following topics:</span></span>

-   [<span data-ttu-id="a96f2-112">Prinzipal Namen</span><span class="sxs-lookup"><span data-stu-id="a96f2-112">Principal Names</span></span>](principal-names.md)
-   [<span data-ttu-id="a96f2-113">Authentifizierungs Ebenen</span><span class="sxs-lookup"><span data-stu-id="a96f2-113">Authentication Levels</span></span>](authentication-levels.md)
-   [<span data-ttu-id="a96f2-114">Authentifizierungsdienste</span><span class="sxs-lookup"><span data-stu-id="a96f2-114">Authentication Services</span></span>](authentication-services.md)
-   [<span data-ttu-id="a96f2-115">Anmelde Informationen zur Client Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="a96f2-115">Client Authentication Credentials</span></span>](client-authentication-credentials.md)
-   [<span data-ttu-id="a96f2-116">Autorisierungs Dienste</span><span class="sxs-lookup"><span data-stu-id="a96f2-116">Authorization Services</span></span>](authorization-services.md)
-   [<span data-ttu-id="a96f2-117">Quality of Service (QoS, Dienstqualität)</span><span class="sxs-lookup"><span data-stu-id="a96f2-117">Quality of Service</span></span>](quality-of-service.md)
-   [<span data-ttu-id="a96f2-118">Autorisierungs Funktionen</span><span class="sxs-lookup"><span data-stu-id="a96f2-118">Authorization Functions</span></span>](authorization-functions.md)
-   [<span data-ttu-id="a96f2-119">Schlüssel Erwerbs Funktionen</span><span class="sxs-lookup"><span data-stu-id="a96f2-119">Key Acquisition Functions</span></span>](key-acquisition-functions.md)
-   [<span data-ttu-id="a96f2-120">Clientidentitätswechsel</span><span class="sxs-lookup"><span data-stu-id="a96f2-120">Client Impersonation</span></span>](client-impersonation.md)

 

 




