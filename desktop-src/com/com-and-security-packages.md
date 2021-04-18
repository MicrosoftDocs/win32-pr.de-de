---
title: COM-und Sicherheitspakete
description: Windows unterstützt NTLMSSP (LAN Manager Security Support Provider), das Kerberos V5-Authentifizierungsprotokoll und das SChannel-Sicherheitspaket, das die Protokolle PCT 1,0, SSL 2,0, SSL 3,0 und TLS 1,0 bereitstellt.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6720ddd56869c5ce93ae70eb313fbe12c140b42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341438"
---
# <a name="com-and-security-packages"></a><span data-ttu-id="ed20d-103">COM-und Sicherheitspakete</span><span class="sxs-lookup"><span data-stu-id="ed20d-103">COM and Security Packages</span></span>

<span data-ttu-id="ed20d-104">Windows unterstützt NTLMSSP (LAN Manager Security Support Provider), das Kerberos V5-Authentifizierungsprotokoll und das SChannel-Sicherheitspaket, das die Protokolle PCT 1,0, SSL 2,0, SSL 3,0 und TLS 1,0 bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ed20d-104">Windows supports NTLMSSP (LAN Manager Security Support Provider), the Kerberos v5 authentication protocol, and the Schannel security package, which provides the PCT 1.0, SSL 2.0, SSL 3.0, and TLS 1.0 protocols.</span></span> <span data-ttu-id="ed20d-105">Unterstützt wird auch das spogo, das auf verfügbare Sicherheitspakete prüft und das geeignetste-Paket auswählt.</span><span class="sxs-lookup"><span data-stu-id="ed20d-105">Also supported is Snego, which checks for available security packages and selects the most appropriate one.</span></span>

<span data-ttu-id="ed20d-106">In der folgenden Tabelle sind die Authentifizierungs Ebenen aufgeführt, die von den verschiedenen Sicherheitspaketen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ed20d-106">The following table shows the levels of authentication supported by the various security packages.</span></span>



| <span data-ttu-id="ed20d-107">Server/Client-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="ed20d-107">Server/Client Authentication</span></span>                                                                                           | <span data-ttu-id="ed20d-108">Unterstützung von Sicherheitspaketen</span><span class="sxs-lookup"><span data-stu-id="ed20d-108">Security Package Support</span></span>                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="ed20d-109">Keines der beiden kann den Namen der anderen erhalten.</span><span class="sxs-lookup"><span data-stu-id="ed20d-109">Neither can get the name of the other.</span></span><br/>                                                                      | <span data-ttu-id="ed20d-110">Keine</span><span class="sxs-lookup"><span data-stu-id="ed20d-110">None</span></span><br/>                                                  |
| <span data-ttu-id="ed20d-111">Der Client kann den Server authentifizieren, aber nicht umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="ed20d-111">The client can authenticate the server, but not vice versa.</span></span><br/>                                                 | <span data-ttu-id="ed20d-112">Schannel</span><span class="sxs-lookup"><span data-stu-id="ed20d-112">Schannel</span></span><br/>                                              |
| <span data-ttu-id="ed20d-113">Der Client kann den Server nicht ermitteln, aber der Server kann die Benutzer-ID des Clients erhalten.</span><span class="sxs-lookup"><span data-stu-id="ed20d-113">The client cannot discover the server, but the server can get the user ID of the client.</span></span><br/>                    | <span data-ttu-id="ed20d-114">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="ed20d-114">NTLMSSP</span></span><br/>                                               |
| <span data-ttu-id="ed20d-115">Gegenseitige Authentifizierung: sowohl der Client als auch der Server können den Namen des anderen kennen, wenn die Berechtigung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="ed20d-115">Mutual authentication: Both the client and server can know the name of the other, if permission is granted.</span></span><br/> | <span data-ttu-id="ed20d-116">NTLMSSP (lokal), Kerberos V5-Protokoll und SChannel</span><span class="sxs-lookup"><span data-stu-id="ed20d-116">NTLMSSP (locally), Kerberos v5 protocol, and Schannel</span></span><br/> |



 

<span data-ttu-id="ed20d-117">Weitere Informationen zu diesen Sicherheitspaketen finden Sie in den folgenden Themen in diesem Abschnitt:</span><span class="sxs-lookup"><span data-stu-id="ed20d-117">For more information about these security packages, see the following topics in this section:</span></span>

-   [<span data-ttu-id="ed20d-118">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="ed20d-118">NTLMSSP</span></span>](ntlmssp.md)
-   [<span data-ttu-id="ed20d-119">Kerberos V5-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ed20d-119">Kerberos v5 Protocol</span></span>](kerberos-v5-protocol.md)
-   [<span data-ttu-id="ed20d-120">SChannel</span><span class="sxs-lookup"><span data-stu-id="ed20d-120">Schannel</span></span>](schannel.md)
-   [<span data-ttu-id="ed20d-121">Spogo</span><span class="sxs-lookup"><span data-stu-id="ed20d-121">Snego</span></span>](snego.md)

## <a name="related-topics"></a><span data-ttu-id="ed20d-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed20d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed20d-123">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="ed20d-123">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 





