---
description: Microsoft aushandeln ist eine Security Support Provider, die als Anwendungsschicht zwischen der Security Support Provider-Schnittstelle und den anderen SSPs fungiert.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Microsoft aushandeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ce57a8f8924120dcce51e50e05de90fd6774b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958873"
---
# <a name="microsoft-negotiate"></a><span data-ttu-id="77ec5-103">Microsoft aushandeln</span><span class="sxs-lookup"><span data-stu-id="77ec5-103">Microsoft Negotiate</span></span>

<span data-ttu-id="77ec5-104">Bei Microsoft Aushandlungen handelt es sich um einen [*Security Support Provider*](../secgloss/s-gly.md) (SSP), der als Anwendungsschicht zwischen [*Security Support Provider Interface*](../secgloss/s-gly.md) ([SSPI](sspi.md)) und den anderen SSPs fungiert.</span><span class="sxs-lookup"><span data-stu-id="77ec5-104">Microsoft Negotiate is a [*security support provider*](../secgloss/s-gly.md) (SSP) that acts as an application layer between [*Security Support Provider Interface*](../secgloss/s-gly.md) ([SSPI](sspi.md)) and the other SSPs.</span></span> <span data-ttu-id="77ec5-105">Wenn eine SSPI zur Anmeldung bei einem Netzwerk von einer Anwendung aufgerufen wird, kann ein SSP zur Verarbeitung der Anforderung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="77ec5-105">When an application calls into SSPI to log on to a network, it can specify an SSP to process the request.</span></span> <span data-ttu-id="77ec5-106">Wenn die Anwendung aushandeln angibt, analysiert aushandeln die Anforderung und wählt den besten SSP für die Verarbeitung der Anforderung basierend auf der vom Kunden konfigurierten Sicherheitsrichtlinie aus.</span><span class="sxs-lookup"><span data-stu-id="77ec5-106">If the application specifies Negotiate, Negotiate analyzes the request and picks the best SSP to handle the request based on customer-configured security policy.</span></span>

<span data-ttu-id="77ec5-107">Derzeit wählt das Aushandlungs Sicherheitspaket zwischen [Kerberos](microsoft-kerberos.md) und [NTLM](microsoft-ntlm.md)aus.</span><span class="sxs-lookup"><span data-stu-id="77ec5-107">Currently, the Negotiate security package selects between [Kerberos](microsoft-kerberos.md) and [NTLM](microsoft-ntlm.md).</span></span> <span data-ttu-id="77ec5-108">Aushandeln wählt Kerberos aus, es sei denn, Sie kann von einem der an der Authentifizierung beteiligten Systeme verwendet werden, oder die aufrufende Anwendung hat keine ausreichenden Informationen für die Verwendung von Kerberos bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="77ec5-108">Negotiate selects Kerberos unless it cannot be used by one of the systems involved in the authentication or the calling application did not provide sufficient information to use Kerberos.</span></span>

<span data-ttu-id="77ec5-109">Damit der [Kerberos](microsoft-kerberos.md) -Sicherheitsanbieter von aushandeln ausgewählt werden kann, muss die Client Anwendung einen [*Dienst Prinzipal Namen*](../secgloss/s-gly.md) (SPN), einen Benutzer Prinzipal Namen (User Principal Name, UPN) oder einen NetBIOS-Kontonamen als Zielnamen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="77ec5-109">To allow Negotiate to select the [Kerberos](microsoft-kerberos.md) security provider, the client application must provide a [*service principal name*](../secgloss/s-gly.md) (SPN), a user principal name (UPN), or a NetBIOS account name as the target name.</span></span> <span data-ttu-id="77ec5-110">Andernfalls wählt aushandeln immer den [NTLM](microsoft-ntlm.md) -Sicherheitsanbieter aus.</span><span class="sxs-lookup"><span data-stu-id="77ec5-110">Otherwise, Negotiate always selects the [NTLM](microsoft-ntlm.md) security provider.</span></span>

<span data-ttu-id="77ec5-111">Ein Server, der das Aushandlungs Paket verwendet, kann auf Client Anwendungen Antworten, die speziell den [Kerberos](microsoft-kerberos.md) -oder [NTLM](microsoft-ntlm.md) -Sicherheitsanbieter auswählen.</span><span class="sxs-lookup"><span data-stu-id="77ec5-111">A server that uses the Negotiate package is able to respond to client applications that specifically select either the [Kerberos](microsoft-kerberos.md) or [NTLM](microsoft-ntlm.md) security provider.</span></span> <span data-ttu-id="77ec5-112">Eine Client Anwendung muss jedoch wissen, dass ein Server das Aushandlungs Paket unterstützt, um die Authentifizierung mithilfe von aushandeln anzufordern.</span><span class="sxs-lookup"><span data-stu-id="77ec5-112">However, a client application must know that a server supports the Negotiate package to request authentication using Negotiate.</span></span> <span data-ttu-id="77ec5-113">Ein Server, der keine Aushandlung unterstützt, kann nicht immer auf Anforderungen von Clients antworten, die aushandeln als SSP angeben.</span><span class="sxs-lookup"><span data-stu-id="77ec5-113">A server that does not support Negotiate cannot always respond to requests from clients that specify Negotiate as the SSP.</span></span>

## <a name="reasons-to-use-the-negotiate-package"></a><span data-ttu-id="77ec5-114">Gründe für die Verwendung des Aushandlungs Pakets</span><span class="sxs-lookup"><span data-stu-id="77ec5-114">Reasons to Use the Negotiate Package</span></span>

-   <span data-ttu-id="77ec5-115">Ermöglicht dem System, das stärkste (sicherste) verfügbare Protokoll zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="77ec5-115">Allows the system to use the strongest (most secure) available protocol.</span></span>
-   <span data-ttu-id="77ec5-116">Gewährleistet die Vorwärtskompatibilität für Ihre Anwendung.</span><span class="sxs-lookup"><span data-stu-id="77ec5-116">Ensures forward compatibility for your application.</span></span>
-   <span data-ttu-id="77ec5-117">Stellt sicher, dass Ihre Anwendung ein Verhalten aufweist, das mit der vom Kunden festgelegten Sicherheitsrichtlinie übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="77ec5-117">Ensures that your application exhibits behavior that is in accordance with the security policy set by the customer.</span></span>

 

 
