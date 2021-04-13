---
title: RADIUS-Authentifizierung,-Autorisierung und-Kontoführung
description: NPS unterstützt das RADIUS-Protokoll (Remote Authentication Dial-in User Service) vollständig. Das RADIUS-Protokoll ist der de-facto-Standard für die Remote Benutzerauthentifizierung und ist in RFC 2865 und RFC 2866 dokumentiert.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce45bbc6e4802ed5137849a5b22520c8a4badbb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390693"
---
# <a name="radius-authentication-authorization-and-accounting"></a><span data-ttu-id="49dda-104">RADIUS-Authentifizierung,-Autorisierung und-Kontoführung</span><span class="sxs-lookup"><span data-stu-id="49dda-104">RADIUS Authentication, Authorization, and Accounting</span></span>

> [!Note]  
> <span data-ttu-id="49dda-105">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="49dda-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="49dda-106">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="49dda-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="49dda-107">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="49dda-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="49dda-108">NPS unterstützt das RADIUS-Protokoll (Remote Authentication Dial-in User Service) vollständig.</span><span class="sxs-lookup"><span data-stu-id="49dda-108">NPS fully supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span> <span data-ttu-id="49dda-109">Das RADIUS-Protokoll ist der de-facto-Standard für die Remote Benutzerauthentifizierung und ist in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) und [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="49dda-109">The RADIUS protocol is the de facto standard for remote user authentication and it is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-authentication-and-authorization"></a><span data-ttu-id="49dda-110">RADIUS-Authentifizierung und-Autorisierung</span><span class="sxs-lookup"><span data-stu-id="49dda-110">RADIUS Authentication and Authorization</span></span>

<span data-ttu-id="49dda-111">Das folgende Diagramm zeigt einen authentifizier enden Client ("User"), der über eine DFÜ-Verbindung mithilfe des Point-to-Point-Protokoll (PPP) eine Verbindung mit einem Netzwerk Zugriffs Server (NAS) herstellt.</span><span class="sxs-lookup"><span data-stu-id="49dda-111">The following diagram shows an authenticating client ("User") connecting to a Network Access Server (NAS) over a dial-up connection, using the Point-to-Point Protocol (PPP).</span></span> <span data-ttu-id="49dda-112">Um den Benutzer zu authentifizieren, kontaktiert der NAS einen Remote Server, auf dem NPS ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49dda-112">In order to authenticate the User, the NAS contacts a remote server running NPS.</span></span> <span data-ttu-id="49dda-113">Der NAS-und der NPS-Server kommunizieren mit dem RADIUS-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="49dda-113">The NAS and the NPS server communicate using the RADIUS protocol.</span></span>

![Remote Benutzerauthentifizierung](images/ias01.png)

<span data-ttu-id="49dda-115">Ein NAS fungiert als Client eines Servers oder von Servern, die das RADIUS-Protokoll unterstützen.</span><span class="sxs-lookup"><span data-stu-id="49dda-115">A NAS operates as a client of a server or servers that support the RADIUS protocol.</span></span> <span data-ttu-id="49dda-116">Server, die das RADIUS-Protokoll unterstützen, werden im Allgemeinen als RADIUS-Server bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="49dda-116">Servers that support the RADIUS protocol are generally referred to as the RADIUS servers.</span></span> <span data-ttu-id="49dda-117">Der RADIUS-Client, d. h. das NAS, übergibt Informationen über den Benutzer an bestimmte RADIUS-Server und verhält sich dann mit der Antwort, die die Server zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="49dda-117">The RADIUS client, that is, the NAS, passes information about the User to designated RADIUS servers, and then acts on the response that the servers return.</span></span> <span data-ttu-id="49dda-118">Die Anforderung, die vom NAS an den RADIUS-Server gesendet wird, um den Benutzer zu authentifizieren, wird im Allgemeinen als "Authentifizierungsanforderung" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="49dda-118">The request sent by the NAS to the RADIUS server in order to authenticate the User is generally called an "authentication request."</span></span>

<span data-ttu-id="49dda-119">Wenn der Benutzer von einem RADIUS-Server erfolgreich authentifiziert wird, gibt der RADIUS-Server Konfigurationsinformationen an den NAS zurück, damit er dem Benutzer Netzwerkdienst bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="49dda-119">If a RADIUS server authenticates the User successfully, the RADIUS server returns configuration information to the NAS so that it can provide network service to the user.</span></span> <span data-ttu-id="49dda-120">Diese Konfigurationsinformationen bestehen aus "Autorisierungen" und enthalten unter anderem den Typ des dienstannas, den der Benutzer möglicherweise bereitstellt (z. b. PPP oder Telnet).</span><span class="sxs-lookup"><span data-stu-id="49dda-120">This configuration information is composed of "authorizations" and contains, among others, the type of service NAS may provide to the User (for example, PPP, or telnet).</span></span>

<span data-ttu-id="49dda-121">Während der RADIUS-Server die Authentifizierungsanforderung verarbeitet, kann er Autorisierungs Funktionen ausführen, wie z. b. das Überprüfen der Telefonnummer des Benutzers und das überprüfen, ob der Benutzer bereits über eine Sitzung verfügt.</span><span class="sxs-lookup"><span data-stu-id="49dda-121">While the RADIUS server is processing the authentication request, it can perform authorization functions such as verifying the user's telephone number and checking whether the user already has a session in progress.</span></span> <span data-ttu-id="49dda-122">Der RADIUS-Server kann ermitteln, ob der Benutzer bereits über eine Sitzung verfügt, indem er eine Verbindung mit einem Zustands Server aufnimmt.</span><span class="sxs-lookup"><span data-stu-id="49dda-122">The RADIUS server can determine whether the user already has a session in progress by contacting a state server.</span></span>

<span data-ttu-id="49dda-123">Weitere Informationen zur RADIUS-Authentifizierung und-Autorisierung finden Sie unter [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).</span><span class="sxs-lookup"><span data-stu-id="49dda-123">For more information on RADIUS authentication and authorization, see [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).</span></span>

## <a name="radius-accounting"></a><span data-ttu-id="49dda-124">RADIUS-Kontoführung</span><span class="sxs-lookup"><span data-stu-id="49dda-124">RADIUS Accounting</span></span>

<span data-ttu-id="49dda-125">Der RADIUS-Server sammelt außerdem eine Vielzahl von Informationen, die vom NAS gesendet werden, die für die Buchhaltung und die Berichterstellung zur Netzwerkaktivität verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="49dda-125">The RADIUS server also collects a variety of information sent by the NAS that can be used for accounting and for reporting on network activity.</span></span> <span data-ttu-id="49dda-126">Der RADIUS-Client sendet Informationen an bestimmte RADIUS-Server, wenn sich der Benutzer anmeldet und abmeldet.</span><span class="sxs-lookup"><span data-stu-id="49dda-126">The RADIUS client sends information to designated RADIUS servers when the User logs on and logs off.</span></span> <span data-ttu-id="49dda-127">Der RADIUS-Client sendet möglicherweise regelmäßig zusätzliche Verwendungs Informationen, während die Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49dda-127">The RADIUS client may send additional usage information on a periodic basis while the session is in progress.</span></span> <span data-ttu-id="49dda-128">Die Anforderungen, die vom Client an den Server gesendet werden, um Anmelde-/Abmelde-und Verwendungs Informationen aufzuzeichnen, werden im Allgemeinen als "Buchhaltungs Anforderungen" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="49dda-128">The requests sent by the client to the server to record logon/logoff and usage information are generally called "accounting requests."</span></span>

<span data-ttu-id="49dda-129">Weitere Informationen zur RADIUS-Buchhaltung finden Sie unter [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="49dda-129">For more information on RADIUS accounting, see [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-proxy"></a><span data-ttu-id="49dda-130">RADIUS-Proxy</span><span class="sxs-lookup"><span data-stu-id="49dda-130">RADIUS Proxy</span></span>

<span data-ttu-id="49dda-131">Ein RADIUS-Server kann als Proxy Client für andere RADIUS-Server fungieren.</span><span class="sxs-lookup"><span data-stu-id="49dda-131">A RADIUS server can act as a proxy client to other RADIUS servers.</span></span> <span data-ttu-id="49dda-132">In diesen Fällen übergibt der vom NAS angewandte RADIUS-Server die Authentifizierungs-oder Buchhaltungs Anforderung an einen anderen RADIUS-Server, der die Authentifizierung oder die Buchhaltungs Aufgabe ausführt.</span><span class="sxs-lookup"><span data-stu-id="49dda-132">In these cases, the RADIUS server contacted by the NAS passes the authentication or accounting request to another RADIUS server that actually performs the authentication or the accounting task.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49dda-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49dda-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49dda-134">Internet Authentifizierungsdienst und Netzwerk Richtlinien Server</span><span class="sxs-lookup"><span data-stu-id="49dda-134">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="49dda-135">RADIUS-Buchhaltungs Pakete</span><span class="sxs-lookup"><span data-stu-id="49dda-135">RADIUS Accounting Packets</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="49dda-136">Arbeiten mit einem Zustands Server</span><span class="sxs-lookup"><span data-stu-id="49dda-136">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 