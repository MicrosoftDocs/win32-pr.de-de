---
description: Die Secure Socket-Erweiterungen für Winsock ermöglichen es einer socketanwendung, die Sicherheit des Datenverkehrs über ein Netzwerk zu steuern.
ms.assetid: 023a9f96-814f-40c3-a186-ae0a0c9baef2
title: Winsock Secure Socket Extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b62ee593b3abbb3bb0f8dbf27b79d6868f04fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041720"
---
# <a name="winsock-secure-socket-extensions"></a><span data-ttu-id="30aa5-103">Winsock Secure Socket Extensions</span><span class="sxs-lookup"><span data-stu-id="30aa5-103">Winsock Secure Socket Extensions</span></span>

<span data-ttu-id="30aa5-104">Die Secure Socket-Erweiterungen für Winsock ermöglichen es einer socketanwendung, die Sicherheit des Datenverkehrs über ein Netzwerk zu steuern.</span><span class="sxs-lookup"><span data-stu-id="30aa5-104">The secure socket extensions to Winsock allow a socket application to control the security of their traffic over a network.</span></span> <span data-ttu-id="30aa5-105">Diese Erweiterungen ermöglichen es einer Anwendung, Sicherheitsrichtlinien und Anforderungen für den Netzwerk Datenverkehr bereitzustellen und die angewendeten Sicherheitseinstellungen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="30aa5-105">These extensions allow an application to provide security policy and requirements for their network traffic, and query the security settings applied.</span></span> <span data-ttu-id="30aa5-106">Beispielsweise kann eine Anwendung diese Erweiterungen verwenden, um das Peer-Sicherheits Token abzufragen, das zum Ausführen von Zugriffs Überprüfungen auf Anwendungsebene verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="30aa5-106">For example, an application can use these extensions to query the peer security token that can be used to perform application level access checks.</span></span>

<span data-ttu-id="30aa5-107">Die Secure Socket-Erweiterungen dienen dazu, die von IPSec bereitgestellten Dienste und andere Sicherheitsprotokolle mit dem Winsock-Framework zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="30aa5-107">The secure socket extensions are intended to integrate the services provided by IPsec and other security protocols with the Winsock framework.</span></span> <span data-ttu-id="30aa5-108">Vor Windows Vista wurde IPSec unter Windows Server 2003 und Windows XP von einem Administrator über lokale und Domänen Richtlinien konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="30aa5-108">Prior to Windows Vista, on Windows Server 2003 and Windows XP, IPsec has been configured by an administrator via local and domain policies.</span></span> <span data-ttu-id="30aa5-109">Unter Windows Vista ermöglichen die Secure Socket Extensions stattdessen, dass Anwendungen die Sicherheit Ihres Netzwerk Datenverkehrs auf Socketebene ganz oder teilweise zu konfigurieren und zu steuern.</span><span class="sxs-lookup"><span data-stu-id="30aa5-109">On Windows Vista, the secure socket extensions instead allow applications to entirely or partially configure and control the security of their network traffic at the socket level.</span></span>

<span data-ttu-id="30aa5-110">Anwendungen können den Netzwerk Datenverkehr bereits mithilfe von öffentlichen APIs sichern, z. b. IPSec-Verwaltung, Windows-Filter Plattform und Security Support Provider Interface (SSPI).</span><span class="sxs-lookup"><span data-stu-id="30aa5-110">Applications can already secure network traffic by using public APIs, such as IPsec management, Windows Filtering Platform and Security Support Provider Interface (SSPI).</span></span> <span data-ttu-id="30aa5-111">Allerdings kann die Verwendung dieser APIs die Entwicklung der Anwendung erschweren und das Konfigurieren und Bereitstellen erschweren.</span><span class="sxs-lookup"><span data-stu-id="30aa5-111">However, using these APIs may make the application more difficult to develop, and may make it more difficult to configure and deploy.</span></span> <span data-ttu-id="30aa5-112">Die Winsock Secure Socket Extensions wurden entwickelt, um die Entwicklung von Netzwerkanwendungen zu vereinfachen, die sicheren Netzwerk Datenverkehr erfordern, da Winsock den größten Teil der Komplexität bewältigen lässt.</span><span class="sxs-lookup"><span data-stu-id="30aa5-112">The Winsock secure socket extensions have been designed to simplify the development of network applications that require secure network traffic by letting Winsock handle most of the complexity.</span></span>

<span data-ttu-id="30aa5-113">Diese Secure Socket Extensions sind unter Windows Vista und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="30aa5-113">These secure socket extensions are available on Windows Vista and later.</span></span>

## <a name="secure-socket-functions"></a><span data-ttu-id="30aa5-114">Secure Socket-Funktionen</span><span class="sxs-lookup"><span data-stu-id="30aa5-114">Secure Socket Functions</span></span>

<span data-ttu-id="30aa5-115">Die Funktionen der Secure Socket-Erweiterung lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="30aa5-115">The secure socket extension functions are as follows:</span></span>

-   [<span data-ttu-id="30aa5-116">**Wsadeletesocketpeer-TargetName**</span><span class="sxs-lookup"><span data-stu-id="30aa5-116">**WSADeleteSocketPeerTargetName**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [<span data-ttu-id="30aa5-117">**Wsaidentität atesocketpeer**</span><span class="sxs-lookup"><span data-stu-id="30aa5-117">**WSAImpersonateSocketPeer**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [<span data-ttu-id="30aa5-118">**Wsaquerysocketsecurity**</span><span class="sxs-lookup"><span data-stu-id="30aa5-118">**WSAQuerySocketSecurity**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [<span data-ttu-id="30aa5-119">**Wsarevertimpersonations**</span><span class="sxs-lookup"><span data-stu-id="30aa5-119">**WSARevertImpersonation**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [<span data-ttu-id="30aa5-120">**Wsasetsocketpeer-TargetName**</span><span class="sxs-lookup"><span data-stu-id="30aa5-120">**WSASetSocketPeerTargetName**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [<span data-ttu-id="30aa5-121">**Wsasetsocketsecurity**</span><span class="sxs-lookup"><span data-stu-id="30aa5-121">**WSASetSocketSecurity**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> <span data-ttu-id="30aa5-122">Die Secure Socket-Funktionen unterstützen derzeit nur das IPSec-Protokoll und sind unter Windows Vista und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="30aa5-122">The secure socket functions currently support only the IPsec protocol and are available on Windows Vista and later.</span></span>

 

<span data-ttu-id="30aa5-123">Die von den Secure Socket Functions verwendeten Strukturen und Enumerationen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="30aa5-123">The structures and enumerations used by the secure socket functions are as follows:</span></span>

-   [<span data-ttu-id="30aa5-124">**\_Name des socketpeers \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30aa5-124">**SOCKET\_PEER\_TARGET\_NAME**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [<span data-ttu-id="30aa5-125">**\_ \_ socketsicherheitsprotokoll**</span><span class="sxs-lookup"><span data-stu-id="30aa5-125">**SOCKET\_SECURITY\_PROTOCOL**</span></span>](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [<span data-ttu-id="30aa5-126">**\_Informationen zur \_ socketsicherheitsabfrage \_**</span><span class="sxs-lookup"><span data-stu-id="30aa5-126">**SOCKET\_SECURITY\_QUERY\_INFO**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [<span data-ttu-id="30aa5-127">**\_socketsicherheitsabfrage- \_ \_ Vorlage**</span><span class="sxs-lookup"><span data-stu-id="30aa5-127">**SOCKET\_SECURITY\_QUERY\_TEMPLATE**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [<span data-ttu-id="30aa5-128">**\_ \_ socketsicherheitseinstellungen**</span><span class="sxs-lookup"><span data-stu-id="30aa5-128">**SOCKET\_SECURITY\_SETTINGS**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [<span data-ttu-id="30aa5-129">**\_ \_ socketsicherheitseinstellungen \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="30aa5-129">**SOCKET\_SECURITY\_SETTINGS\_IPSEC**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

<span data-ttu-id="30aa5-130">Die sicheren Socketfunktionen können für normale Anwendungen einfach verwendet werden und sind flexibel genug für Anwendungen, die ein hohes Maß an Kontrolle über Ihre Sicherheit benötigen.</span><span class="sxs-lookup"><span data-stu-id="30aa5-130">The secure socket functions are simple to use for normal applications and are flexible enough for applications that need a high degree of control over their security.</span></span> <span data-ttu-id="30aa5-131">Diese Funktionen ermöglichen es, den zugrunde liegenden Sicherheitsmechanismus vor der Anwendung zu verbergen.</span><span class="sxs-lookup"><span data-stu-id="30aa5-131">These functions make it possible to keep the underlying security mechanism hidden from the application.</span></span> <span data-ttu-id="30aa5-132">Eine Anwendung kann generische Sicherheitsanforderungen angeben und den Administrator das Sicherheitsprotokoll steuern lassen, das zur Unterstützung der Anforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="30aa5-132">An application can specify generic security requirements and let the administrator control the security protocol that is used to support the requirements.</span></span> <span data-ttu-id="30aa5-133">Obwohl es möglich ist, diese Funktionen zu erweitern, um andere Sicherheitsprotokolle hinzuzufügen, wird derzeit nur IPSec in die Secure Socket-Funktionen integriert.</span><span class="sxs-lookup"><span data-stu-id="30aa5-133">While it is possible to extend these functions to add other security protocols, currently only IPsec integrates with the secure socket functions.</span></span>

<span data-ttu-id="30aa5-134">Mit der [**wsasetsocketsecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) -Funktion kann eine Anwendung die Sicherheit aktivieren und Sicherheitseinstellungen anwenden, bevor eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="30aa5-134">The [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) function allows an application to enable security and apply security settings before a connection is established.</span></span>

<span data-ttu-id="30aa5-135">Die Funktion [**wsasetsocketpeertargetname**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) ermöglicht es einer Anwendung, den Zielnamen anzugeben, der einer Peer Entität entspricht.</span><span class="sxs-lookup"><span data-stu-id="30aa5-135">The [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) function allows an application to specify the target name corresponding to a peer entity.</span></span> <span data-ttu-id="30aa5-136">Das ausgewählte Sicherheitsprotokoll verwendet diese Informationen, wenn der Peer authentifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="30aa5-136">The selected security protocol will use this information when authenticating the peer.</span></span> <span data-ttu-id="30aa5-137">Diese Funktion behandelt Aspekte von vertrauenswürdigen man-in-the-Middle-Angriffen.</span><span class="sxs-lookup"><span data-stu-id="30aa5-137">This feature addresses concerns about trusted man-in-the-middle attacks.</span></span>

<span data-ttu-id="30aa5-138">Die Funktion [**wsadeletesocketpeertargetname**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) wird verwendet, um einen zuvor angegebenen Peernamen für einen Socket zu löschen.</span><span class="sxs-lookup"><span data-stu-id="30aa5-138">The [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) function is used to delete a previously specified peer name for a socket.</span></span>

<span data-ttu-id="30aa5-139">Nachdem eine Verbindung hergestellt wurde, ermöglicht die [**wsaquerysocketsecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) -Funktion einer Anwendung, die Sicherheitseigenschaften der Verbindung abzufragen, die den Peer Zugriff oder das Computer Zugriffs Token enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="30aa5-139">After a connection is established, the [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) function allows an application to query the security properties of the connection, which can include the peer access or computer access token.</span></span>

<span data-ttu-id="30aa5-140">Nachdem eine Verbindung hergestellt wurde, kann eine Anwendung mithilfe der [**wsaidentität atesocketpeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) -Funktion die Identität des Sicherheits Prinzipals, der einem socketpeer entspricht, annehmen, um die Autorisierung auf Anwendungsebene auszuführen.</span><span class="sxs-lookup"><span data-stu-id="30aa5-140">After a connection is established, the [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) function allows an application to impersonate the security principal corresponding to a socket peer in order to perform application-level authorization.</span></span>

<span data-ttu-id="30aa5-141">Mit [**wsarevertimpersonations**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) kann eine Anwendung den Identitätswechsel eines socketpeers beenden.</span><span class="sxs-lookup"><span data-stu-id="30aa5-141">The [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) allows an application to terminate the impersonation of a socket peer.</span></span>

## <a name="secure-socket-architecture"></a><span data-ttu-id="30aa5-142">Secure Socket-Architektur</span><span class="sxs-lookup"><span data-stu-id="30aa5-142">Secure Socket Architecture</span></span>

![grundlegende Architektur der Winsock Secure Socket Extensions](images/ss-arch.png)

-   <span data-ttu-id="30aa5-144">Eine Anwendung ruft die Secure Socket-Funktionen auf, um die Sicherheitseinstellungen für einen Socket festzulegen oder abzufragen.</span><span class="sxs-lookup"><span data-stu-id="30aa5-144">An application calls the secure socket functions to set or query security settings for a socket.</span></span>
-   <span data-ttu-id="30aa5-145">Bei den sicheren Socketfunktionen handelt es sich um einen Satz von typsicheren Erweiterungsfunktionen, die Aufrufe der [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion mithilfe von neu definierten Werten für den in Windows Vista und höher verfügbaren *dwIoControlCode* -Parameter umschließen.</span><span class="sxs-lookup"><span data-stu-id="30aa5-145">The secure socket functions are a set of type-safe extension functions that wrap calls to the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function using newly-defined values for the *dwIoControlCode* parameter available on Windows Vista and later.</span></span> <span data-ttu-id="30aa5-146">Diese IOCTLs werden vom Netzwerk Stapel verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="30aa5-146">These IOCTLs are handled by the network stack.</span></span>
-   <span data-ttu-id="30aa5-147">Der Netzwerk Stapel leitet den aufzurufenden [Anwendungs ebenenerzwingungs Vorgang (ALE)](../fwp/application-layer-enforcement--ale-.md) zusammen mit dem Endpunkt Handle weiter.</span><span class="sxs-lookup"><span data-stu-id="30aa5-147">The network stack will direct the call to [Application Layer Enforcement (ALE)](../fwp/application-layer-enforcement--ale-.md) along with the endpoint handle.</span></span> <span data-ttu-id="30aa5-148">Für die Funktionen [**wsadeletesocketetstargetname**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**wsasetsocketetertargetname**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)und [**wsasetsocketsecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) konfiguriert ALE die Einstellungen der Anwendung auf dem lokalen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="30aa5-148">For the [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname), and [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) functions, ALE will configure the application's settings on the local endpoint.</span></span> <span data-ttu-id="30aa5-149">Bei der [**wsaquerysocketsecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) -Funktion liest ALE die angeforderten Informationen von den anwendbaren lokalen und Remote Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="30aa5-149">For the [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) function, ALE will read the requested information from applicable local and remote endpoints.</span></span>
-   <span data-ttu-id="30aa5-150">Basierend auf socketereignissen erzwingt die Erzwingung der Anwendungsschicht Richtlinien für die sichere socketarchitektur mithilfe der Windows-Filter Plattform.</span><span class="sxs-lookup"><span data-stu-id="30aa5-150">Based on socket events, Application Layer Enforcement (ALE) enforces policies for the secure socket architecture using the Windows Filtering Platform.</span></span> <span data-ttu-id="30aa5-151">Weitere Informationen finden Sie unter Informationen [zur Windows-Filter Plattform](../fwp/about-windows-filtering-platform.md) und zur [Durchsetzung der Anwendungsschicht](../fwp/application-layer-enforcement--ale-.md).</span><span class="sxs-lookup"><span data-stu-id="30aa5-151">For more information, see [About Windows Filtering Platform](../fwp/about-windows-filtering-platform.md) and [Application Layer Enforcement (ALE)](../fwp/application-layer-enforcement--ale-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="30aa5-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="30aa5-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30aa5-153">Informationen zur Windows-Filter Plattform</span><span class="sxs-lookup"><span data-stu-id="30aa5-153">About Windows Filtering Platform</span></span>](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[<span data-ttu-id="30aa5-154">Erweiterte Winsock-Beispiele mit Secure Socket Extensions</span><span class="sxs-lookup"><span data-stu-id="30aa5-154">Advanced Winsock Samples Using Secure Socket Extensions</span></span>](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="30aa5-155">Durchsetzung der Anwendungsschicht (ALE)</span><span class="sxs-lookup"><span data-stu-id="30aa5-155">Application Layer Enforcement (ALE)</span></span>](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="30aa5-156">IPSec-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="30aa5-156">IPsec Configuration</span></span>](../fwp/ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="30aa5-157">IPSec-Funktionen</span><span class="sxs-lookup"><span data-stu-id="30aa5-157">IPsec Functions</span></span>](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[<span data-ttu-id="30aa5-158">Sichere Winsock-Programmierung</span><span class="sxs-lookup"><span data-stu-id="30aa5-158">Secure Winsock Programming</span></span>](secure-winsock-programming.md)
</dt> <dt>

[<span data-ttu-id="30aa5-159">Security Support Provider Interface (SSPI)</span><span class="sxs-lookup"><span data-stu-id="30aa5-159">Security Support Provider Interface (SSPI)</span></span>](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[<span data-ttu-id="30aa5-160">Verwenden von Secure Socket Extensions</span><span class="sxs-lookup"><span data-stu-id="30aa5-160">Using Secure Socket Extensions</span></span>](using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="30aa5-161">Windows-Filterplattform</span><span class="sxs-lookup"><span data-stu-id="30aa5-161">Windows Filtering Platform</span></span>](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[<span data-ttu-id="30aa5-162">API-Funktionen der Windows-Filter Plattform</span><span class="sxs-lookup"><span data-stu-id="30aa5-162">Windows Filtering Platform API Functions</span></span>](../fwp/fwp-functions.md)
</dt> </dl>

 

 
