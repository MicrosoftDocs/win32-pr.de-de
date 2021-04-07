---
title: Unterstützung für RAS-Sicherheits Host
description: Windows NT 4,0 bietet eine Möglichkeit für eine Drittanbieter-RAS-Sicherheits-DLL, um die integrierten RAS-Sicherheitsfeatures zu verbessern. Windows 95 bietet diese Unterstützung nicht.
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- Host Unterstützung, RAS
- Unterstützung von Sicherheits Hosts, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711741"
---
# <a name="ras-security-host-support"></a><span data-ttu-id="a2835-106">Unterstützung für RAS-Sicherheits Host</span><span class="sxs-lookup"><span data-stu-id="a2835-106">RAS Security Host Support</span></span>

<span data-ttu-id="a2835-107">Windows NT 4,0 bietet eine Möglichkeit für eine Drittanbieter-RAS-Sicherheits-DLL, um die integrierten RAS-Sicherheitsfeatures zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="a2835-107">Windows NT 4.0 provides a way for a third-party RAS security DLL to enhance the built-in RAS security features.</span></span> <span data-ttu-id="a2835-108">Windows 95 bietet diese Unterstützung nicht.</span><span class="sxs-lookup"><span data-stu-id="a2835-108">Windows 95 does not provide this support.</span></span>

<span data-ttu-id="a2835-109">Ein Windows NT/Windows 2000-RAS-Server stellt Sicherheitsmechanismen für die Überprüfung des Netzwerk Zugriffs von Remote Benutzern bereit.</span><span class="sxs-lookup"><span data-stu-id="a2835-109">A Windows NT/Windows 2000 RAS server provides security mechanisms for validating the network access of remote users.</span></span> <span data-ttu-id="a2835-110">Wenn ein RAS-Server einen-Befehl empfängt, überprüft er die Anmelde Informationen des Benutzers anhand der lokalen oder Domänen Konto Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a2835-110">When a RAS server receives a call, it validates the user's credentials against the local or domain account database.</span></span> <span data-ttu-id="a2835-111">RAS unterstützt auch die Rückruf Sicherheit, bei der der RAS-Server nicht mehr aktiv ist, und ruft dann den Remote Benutzer zum Herstellen der Verbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="a2835-111">RAS also supports call-back security, in which the RAS server hangs up and then calls back to the remote user to establish the connection.</span></span> <span data-ttu-id="a2835-112">Bei Netzwerken, in denen diese Sicherheitsstufe nicht ausreicht, können Sie eine Drittanbieter-RAS-Sicherheits-DLL installieren.</span><span class="sxs-lookup"><span data-stu-id="a2835-112">For networks in which this level of security is not enough, you can install a third-party RAS security DLL.</span></span> <span data-ttu-id="a2835-113">Die Sicherheits-DLL kann dann einen Remote Benutzer authentifizieren, indem er Sicherheitsinformationen aus einer anderen Datenbank als der Standardbenutzer Konten Datenbank liest.</span><span class="sxs-lookup"><span data-stu-id="a2835-113">The security DLL can then authenticate a remote user by reading security information from a database other than the standard user account database.</span></span>

<span data-ttu-id="a2835-114">Wenn der RAS-Server einen Aufruf empfängt, ruft er die Sicherheits-DLL auf, um den Remote Benutzer zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="a2835-114">When the RAS server receives a call, it invokes the security DLL to authenticate the remote user.</span></span> <span data-ttu-id="a2835-115">Die Unterstützung des RAS-Sicherheits Hosts bietet einen Mechanismus, mit dem die Sicherheits-DLL über ein Terminalfenster auf dem Remote Computer mit dem Remote Benutzer kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="a2835-115">The RAS security host support provides a mechanism for the security DLL to communicate with the remote user through a terminal window on the remote computer.</span></span> <span data-ttu-id="a2835-116">In einem typischen Szenario fordert die Sicherheits-DLL den Anmelde Namen des Remote Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="a2835-116">In a typical scenario, the security DLL asks for the logon name of the remote user.</span></span> <span data-ttu-id="a2835-117">Die dll verwendet dann die private Sicherheitsdatenbank, um eine Herausforderung für das Senden an das Remote Terminal zu formulieren.</span><span class="sxs-lookup"><span data-stu-id="a2835-117">The DLL then uses its private security database to formulate a challenge to send to the remote terminal.</span></span> <span data-ttu-id="a2835-118">Die Herausforderung könnte z. b. ein Code sein, den der Benutzer als Eingabe für einen cardkey-Reader bereitstellen muss.</span><span class="sxs-lookup"><span data-stu-id="a2835-118">For example, the challenge could be a code that the user must provide as input to a cardkey reader.</span></span> <span data-ttu-id="a2835-119">Der cardkey-Reader zeigt dann eine Antwort an, die der Remote Benutzer im Terminalfenster eingibt.</span><span class="sxs-lookup"><span data-stu-id="a2835-119">The cardkey reader then displays a response that the remote user types in the terminal window.</span></span> <span data-ttu-id="a2835-120">Die Sicherheits-DLL überprüft dann die Antwort auf die Informationen des Benutzers in der privaten Sicherheitsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="a2835-120">The security DLL then validates the response against the user's information in the private security database.</span></span>

<span data-ttu-id="a2835-121">Wenn die Sicherheits-DLL den Remote Benutzer authentifiziert, führt der RAS-Server eine eigene Authentifizierung durch.</span><span class="sxs-lookup"><span data-stu-id="a2835-121">If the security DLL authenticates the remote user, the RAS server performs its own authentication.</span></span> <span data-ttu-id="a2835-122">Dadurch wird sichergestellt, dass RAS-Sicherheit immer einen Remote Benutzer authentifiziert, auch wenn eine Sicherheits-DLL installiert ist, die allen Benutzern Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="a2835-122">This ensures that RAS security always authenticates a remote user, even if a security DLL is installed that grants access to all users.</span></span>

> [!Note]  
> <span data-ttu-id="a2835-123">Windows NT/Windows 2000 bietet zurzeit Unterstützung für RAS-Sicherheits Hosts nur für asynchrone Modemverbindungen. andere Typen von Verbindungen, wie z. b. Ethernet (keine Modemverbindung), VPN (auch keine Modemverbindung) oder ISDN (synchron), werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a2835-123">Windows NT/Windows 2000 currently provides RAS security host support only for asynchronous modem connections; other types of connections such as Ethernet (which is not a modem connection), VPN (which is also not a modem connection), or ISDN (which is synchronous), are not supported.</span></span>

 

 

 




