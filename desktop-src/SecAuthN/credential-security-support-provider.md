---
description: Das Credential Security Support Provider Protocol (kredssp) ist ein Sicherheits Unterstützungs Anbieter, der mithilfe der Security Support Provider-Schnittstelle (Security Support Provider Interface, SSPI) implementiert wird.
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Anmelde Informationsanbieter für Sicherheitsunterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9aa961f37043d84dc21280ea7d5ecb9c27c075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214991"
---
# <a name="credential-security-support-provider"></a><span data-ttu-id="f29b9-103">Anmelde Informationsanbieter für Sicherheitsunterstützung</span><span class="sxs-lookup"><span data-stu-id="f29b9-103">Credential Security Support Provider</span></span>

<span data-ttu-id="f29b9-104">Das Credential Security Support Provider Protocol (kredssp) ist ein Sicherheits Unterstützungs Anbieter, der mithilfe der Security Support Provider-Schnittstelle (Security Support Provider Interface,[SSPI](sspi.md)) implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="f29b9-104">The Credential Security Support Provider protocol (CredSSP) is a Security Support Provider that is implemented by using the Security Support Provider Interface ([SSPI](sspi.md)).</span></span> <span data-ttu-id="f29b9-105">Mit "kredssp" kann eine Anwendung die Anmelde Informationen des Benutzers vom Client an den Zielserver für die Remote Authentifizierung delegieren.</span><span class="sxs-lookup"><span data-stu-id="f29b9-105">CredSSP lets an application delegate the user's credentials from the client to the target server for remote authentication.</span></span> <span data-ttu-id="f29b9-106">"Kredssp" stellt einen verschlüsselten [Transport Layer Security Protokoll](transport-layer-security-protocol.md) Kanal bereit.</span><span class="sxs-lookup"><span data-stu-id="f29b9-106">CredSSP provides an encrypted [Transport Layer Security Protocol](transport-layer-security-protocol.md) channel.</span></span> <span data-ttu-id="f29b9-107">Der Client wird über den verschlüsselten Kanal authentifiziert, indem das Simple and Protected Aushandlungs Protokoll (spnetgo) mit [Microsoft Kerberos](microsoft-kerberos.md) oder [Microsoft NTLM](microsoft-ntlm.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f29b9-107">The client is authenticated over the encrypted channel by using the Simple and Protected Negotiate (SPNEGO) protocol with either [Microsoft Kerberos](microsoft-kerberos.md) or [Microsoft NTLM](microsoft-ntlm.md).</span></span>

> [!Caution]  
> <span data-ttu-id="f29b9-108">Dies ist keine eingeschränkte Delegierung.</span><span class="sxs-lookup"><span data-stu-id="f29b9-108">This is not constrained delegation.</span></span> <span data-ttu-id="f29b9-109">"Kredssp" übergibt die vollständigen Anmelde Informationen des Benutzers ohne Einschränkung an den Server.</span><span class="sxs-lookup"><span data-stu-id="f29b9-109">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="f29b9-110">Weitere Informationen zu spnetgo finden Sie unter [Microsoft aushandeln](microsoft-negotiate.md).</span><span class="sxs-lookup"><span data-stu-id="f29b9-110">For information about SPNEGO, see [Microsoft Negotiate](microsoft-negotiate.md).</span></span>

<span data-ttu-id="f29b9-111">Nachdem Client und Server authentifiziert wurden, übergibt der Client die Anmelde Informationen des Benutzers an den Server.</span><span class="sxs-lookup"><span data-stu-id="f29b9-111">After the client and server are authenticated, the client passes the user's credentials to the server.</span></span> <span data-ttu-id="f29b9-112">Die Anmelde Informationen werden doppelt unter den spnetgo-und TLS-Sitzungs Schlüsseln verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="f29b9-112">The credentials are doubly encrypted under the SPNEGO and TLS session keys.</span></span> <span data-ttu-id="f29b9-113">"Kredssp" unterstützt die Kenn Wort basierte Anmeldung sowie die Smartcard-Anmeldung basierend auf " [*X. 509*](/windows/desktop/SecGloss/x-gly) " und "PKINIT".</span><span class="sxs-lookup"><span data-stu-id="f29b9-113">CredSSP supports password-based logon as well as smart card logon based on both [*X.509*](/windows/desktop/SecGloss/x-gly) and PKINIT.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f29b9-114">WOW64-Clients werden von "kredssp" nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f29b9-114">CredSSP does not support Wow64 clients.</span></span>

 

<span data-ttu-id="f29b9-115">Weitere Informationen zu "kredssp" finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="f29b9-115">For more information about CredSSP, see the following topics.</span></span>



| <span data-ttu-id="f29b9-116">Thema</span><span class="sxs-lookup"><span data-stu-id="f29b9-116">Topic</span></span>                                                                         | <span data-ttu-id="f29b9-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f29b9-117">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f29b9-118">Einstellungen für den Gruppenrichtlinie ""</span><span class="sxs-lookup"><span data-stu-id="f29b9-118">CredSSP Group Policy Settings</span></span>](credssp-group-policy-settings.md)<br/> | <span data-ttu-id="f29b9-119">Die Delegierung von Anmelde Informationen durch das-Skript kann mithilfe von Gruppenrichtlinien Einstellungen gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="f29b9-119">Delegation of credentials by CredSSP can be controlled by using group policy settings.</span></span><br/> |



 

 

