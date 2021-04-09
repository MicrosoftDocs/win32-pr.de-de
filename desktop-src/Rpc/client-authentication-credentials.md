---
title: Anmelde Informationen zur Client Authentifizierung
description: Jeder authentifizierte Client muss Anmelde Informationen für die Authentifizierung für den Server bereitstellen.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3704663411fc33340a462d8e3b356041b6061468
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037539"
---
# <a name="client-authentication-credentials"></a><span data-ttu-id="ba2a3-103">Anmelde Informationen zur Client Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="ba2a3-103">Client Authentication Credentials</span></span>

<span data-ttu-id="ba2a3-104">Jeder authentifizierte Client muss Anmelde Informationen für die Authentifizierung für den Server bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ba2a3-104">Each authenticated client must provide authentication credentials to the server.</span></span> <span data-ttu-id="ba2a3-105">Unter RPC speichert der Client seine Anmelde Informationen für die Authentifizierung in der Bindung zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="ba2a3-105">Under RPC, the client stores its authentication credentials in the binding between the client and the server.</span></span> <span data-ttu-id="ba2a3-106">Hierzu ruft der Client [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) oder [**rpcbindingsetauthinfoex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)auf.</span><span class="sxs-lookup"><span data-stu-id="ba2a3-106">To do this, the client calls [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).</span></span>

<span data-ttu-id="ba2a3-107">Es gibt zwei Arten von Anmelde Informationen – implizit und explizit:</span><span class="sxs-lookup"><span data-stu-id="ba2a3-107">There are two types of credentials—implicit and explicit:</span></span>

-   <span data-ttu-id="ba2a3-108">Wenn der Client Benutzername, Kennwort und Domäne angibt, sind explizite Anmelde Informationen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba2a3-108">Explicit credentials exist when the client supplies username, password, and domain.</span></span>
-   <span data-ttu-id="ba2a3-109">Implizite Anmelde Informationen sind vorhanden, wenn der Client Anmelde Informationen aus dem Thread oder Prozess Token verwendet, die die Funktionen **rpcbindingsetauthinfo** oder **rpcbindingsetauthinfoex** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ba2a3-109">Implicit credentials exist when the client uses credentials from the thread or process token calling the **RpcBindingSetAuthInfo** or **RpcBindingSetAuthInfoEx** functions.</span></span>

<span data-ttu-id="ba2a3-110">Clients sollten keine expliziten Anmelde Informationen bereitstellen, da das Speichern, bearbeiten und Abrufen eines Benutzer Kennworts eine Sicherheitslücke in einem verteilten System darstellen kann, wenn explizite Anmelde Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba2a3-110">Clients should refrain from supplying explicit credentials because storing, manipulating, and retrieving a user password can introduce a security vulnerability into a distributed system if explicit credentials are used.</span></span>

<span data-ttu-id="ba2a3-111">Um implizite Anmelde Informationen zu verwenden, ruft der Client **rpcbindingsetauthinfo**(*Ex*) auf.</span><span class="sxs-lookup"><span data-stu-id="ba2a3-111">To use implicit credentials, the client calls **RpcBindingSetAuthInfo**(*Ex*).</span></span> <span data-ttu-id="ba2a3-112">Das Sicherheitssystem und RPC erhalten Anmelde Informationen aus dem Thread-oder Prozess Token für die Verwendung in der Authentifizierungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="ba2a3-112">The security system and RPC obtain credentials from the thread or process token for use in the authentication session.</span></span>

<span data-ttu-id="ba2a3-113">Wenn der Client explizite Anmelde Informationen verwendet, ist der fünfte Parameter dieser beiden Funktionen vom Typ [**RPC \_ auth \_ Identity \_ handle**](rpc-auth-identity-handle.md).</span><span class="sxs-lookup"><span data-stu-id="ba2a3-113">If the client uses explicit credentials, the fifth parameter of these two functions is of type [**RPC\_AUTH\_IDENTITY\_HANDLE**](rpc-auth-identity-handle.md).</span></span> <span data-ttu-id="ba2a3-114">Dabei handelt es sich um einen flexiblen Typ, der ein Zeiger auf eine Datenstruktur ist.</span><span class="sxs-lookup"><span data-stu-id="ba2a3-114">This is a flexible type that is a pointer to a data structure.</span></span> <span data-ttu-id="ba2a3-115">Der Inhalt der Datenstruktur kann sich je nach Authentifizierungsdienst unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ba2a3-115">The contents of the data structure can differ with each authentication service.</span></span> <span data-ttu-id="ba2a3-116">Derzeit erfordern die von RPC unterstützten SSPs, dass Ihre Anwendung das RPC-Authentifizierungs **\_ \_ Identitäts \_ handle** so festlegen muss, dass es auf eine [**Sek. \_ Winnt \_ auth- \_ Identitäts**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) Struktur verweist.</span><span class="sxs-lookup"><span data-stu-id="ba2a3-116">Currently, the SSPs that RPC supports require that your application set **RPC\_AUTH\_IDENTITY\_HANDLE** to point to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) structure.</span></span> <span data-ttu-id="ba2a3-117">Die **Identitäts Struktur "sec \_ Winnt \_ auth \_** " enthält Felder für einen Benutzernamen, eine Domäne und ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="ba2a3-117">The **SEC\_WINNT\_AUTH\_IDENTITY** structure contains fields for a user name, domain, and password.</span></span>

 

 




