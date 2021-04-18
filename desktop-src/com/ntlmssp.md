---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706c788f103d3d616b5a3087522b5f06b417e972
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337265"
---
# <a name="ntlmssp"></a><span data-ttu-id="3a465-103">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="3a465-103">NTLMSSP</span></span>

<span data-ttu-id="3a465-104">NTLMSSP, dessen Authentifizierungsdienst Bezeichner RPC \_ C \_ authn \_ Winnt ist, ist eine Security Support Provider, die in allen Versionen von DCOM verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3a465-104">NTLMSSP, whose authentication service identifier is RPC\_C\_AUTHN\_WINNT, is a security support provider that is available on all versions of DCOM.</span></span> <span data-ttu-id="3a465-105">Er verwendet das NTLM-Protokoll für die Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="3a465-105">It uses the NTLM protocol for authentication.</span></span> <span data-ttu-id="3a465-106">NTLM überträgt das Kennwort des Benutzers bei der Authentifizierung nie an den Server.</span><span class="sxs-lookup"><span data-stu-id="3a465-106">NTLM never actually transmits the user's password to the server during authentication.</span></span> <span data-ttu-id="3a465-107">Daher kann der Server das Kennwort beim Identitätswechsel nicht verwenden, um auf Netzwerkressourcen zuzugreifen, auf die der Benutzer Zugriff hat.</span><span class="sxs-lookup"><span data-stu-id="3a465-107">Therefore, the server cannot use the password during impersonation to access network resources that the user would have access to.</span></span> <span data-ttu-id="3a465-108">Nur auf lokale Ressourcen kann zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="3a465-108">Only local resources can be accessed.</span></span>

<span data-ttu-id="3a465-109">NTLM funktioniert sowohl lokal als auch Computer übergreifend.</span><span class="sxs-lookup"><span data-stu-id="3a465-109">NTLM works both locally and across computers.</span></span> <span data-ttu-id="3a465-110">Das heißt, wenn sich der Client und der Server auf unterschiedlichen Computern befinden, kann NTLM weiterhin sicherstellen, dass der Client seine Ansprüche anfordert.</span><span class="sxs-lookup"><span data-stu-id="3a465-110">That is, if the client and server are on different computers, NTLM can still make sure the client is who it claims to be.</span></span>

<span data-ttu-id="3a465-111">Bei NTLM wird die Identität des Clients durch einen Domänen Namen, einen Benutzernamen und ein Kennwort oder Token repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="3a465-111">With NTLM, the client's identity is represented by a domain name, user name, and a password or token.</span></span> <span data-ttu-id="3a465-112">Wenn ein Server [**coqueryclientblanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)aufruft, werden der Domänen Name und der Benutzername des Clients zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3a465-112">When a server calls [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), the client's domain name and user name are returned.</span></span> <span data-ttu-id="3a465-113">Wenn jedoch ein Server " [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)" aufruft, wird das Token des Clients zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3a465-113">However, when a server calls [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), the client's token is returned.</span></span> <span data-ttu-id="3a465-114">Wenn keine Vertrauensstellung zwischen Client und Server besteht und der Server über ein lokales Konto mit dem gleichen Namen und Kennwort wie der Client verfügt, wird dieses Konto zur Darstellung des Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a465-114">If there is no trust relationship between client and server and if the server has a local account with the same name and password as the client, that account will be used to represent the client.</span></span>

<span data-ttu-id="3a465-115">NTLM unterstützt die gegenseitige Authentifizierung für Thread übergreifende und prozessübergreifende Authentifizierung (nur lokal).</span><span class="sxs-lookup"><span data-stu-id="3a465-115">NTLM supports mutual authentication cross-thread and cross-process (locally only).</span></span> <span data-ttu-id="3a465-116">Wenn der Client den Prinzipal Namen des Servers im Formular Domänen \\ Benutzer in einem [**IClientSecurity:: setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)-Befehl angibt, muss die Identität des Servers mit dem Prinzipal Namen übereinstimmen, andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="3a465-116">If the client specifies the principal name of the server in the form domain\\user in a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), the server's identity must match that principal name or the call will fail.</span></span> <span data-ttu-id="3a465-117">Wenn der Client **null** angibt, wird die Identität des Servers nicht geprüft.</span><span class="sxs-lookup"><span data-stu-id="3a465-117">If the client specifies **NULL**, the server's identity will not be checked.</span></span>

<span data-ttu-id="3a465-118">NTLM unterstützt zusätzlich die delegatidentitäts Wechsel-Ebene Thread übergreifend und Prozess übergreifend (nur lokal).</span><span class="sxs-lookup"><span data-stu-id="3a465-118">NTLM additionally supports the delegate impersonation level cross-thread and cross-process (locally only).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a465-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a465-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a465-120">COM-und Sicherheitspakete</span><span class="sxs-lookup"><span data-stu-id="3a465-120">COM and Security Packages</span></span>](com-and-security-packages.md)
</dt> </dl>

 

 