---
description: Die Kerberos-Ticket Richtlinie wird auf Domänen Ebene definiert und durch die Schlüsselverteilungscenter der Domäne (KDC) implementiert.
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Kerberos-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4559353e65a25a380c0c2aa4bb7e5d56f7681af1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359108"
---
# <a name="kerberos-policy"></a><span data-ttu-id="7ba26-103">Kerberos-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="7ba26-103">Kerberos Policy</span></span>

<span data-ttu-id="7ba26-104">Die Kerberos-Ticket Richtlinie wird auf Domänen Ebene definiert und durch die [*Schlüsselverteilungscenter*](../secgloss/k-gly.md) der Domäne (KDC) implementiert.</span><span class="sxs-lookup"><span data-stu-id="7ba26-104">Kerberos ticket policy is defined at the domain level and implemented by the domain's [*Key Distribution Center*](../secgloss/k-gly.md) (KDC).</span></span> <span data-ttu-id="7ba26-105">Die Kerberos-Richtlinie wird in der Active Directory als eine Teilmenge der Attribute der Domänen Sicherheitsrichtlinie gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7ba26-105">Kerberos policy is stored in the Active Directory as a subset of the attributes of domain security policy.</span></span> <span data-ttu-id="7ba26-106">Standardmäßig können Richtlinien Optionen nur von Mitgliedern der Gruppe "Domänen Administratoren" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7ba26-106">By default, policy options can be set only by members of the Domain Administrators group.</span></span> <span data-ttu-id="7ba26-107">Die Domänen Richtlinie umfasst folgende Optionen:</span><span class="sxs-lookup"><span data-stu-id="7ba26-107">Domain policy includes options that:</span></span>

-   <span data-ttu-id="7ba26-108">Unterstützung von postveralteten Tickets</span><span class="sxs-lookup"><span data-stu-id="7ba26-108">Support postdated tickets</span></span>
-   <span data-ttu-id="7ba26-109">Unterstützung der eingeschränkten Delegierung (nur Windows Server 2003)</span><span class="sxs-lookup"><span data-stu-id="7ba26-109">Support constrained delegation (Windows Server 2003 only)</span></span>
-   <span data-ttu-id="7ba26-110">Support Tickets, die weitergeleitet werden können</span><span class="sxs-lookup"><span data-stu-id="7ba26-110">Support tickets that can be forwarded</span></span>
-   <span data-ttu-id="7ba26-111">Unterstützen von erneuerbaren Tickets</span><span class="sxs-lookup"><span data-stu-id="7ba26-111">Support renewable tickets</span></span>
-   <span data-ttu-id="7ba26-112">Festlegen des maximalen Ticket Alters</span><span class="sxs-lookup"><span data-stu-id="7ba26-112">Set maximum ticket age</span></span>
-   <span data-ttu-id="7ba26-113">Festlegen des maximalen Erneuerungs Alters</span><span class="sxs-lookup"><span data-stu-id="7ba26-113">Set maximum renewal age</span></span>
-   <span data-ttu-id="7ba26-114">Festlegen des maximalen proxyticket-Alters</span><span class="sxs-lookup"><span data-stu-id="7ba26-114">Set maximum proxy ticket age</span></span>
-   <span data-ttu-id="7ba26-115">Abmeldung von Benutzern beim Ablaufen von Tickets erzwingen</span><span class="sxs-lookup"><span data-stu-id="7ba26-115">Forcibly log off users when tickets expire</span></span>

<span data-ttu-id="7ba26-116">Bei der [*eingeschränkten Delegierung*](../secgloss/c-gly.md)kann ein Computer so festgelegt werden, dass die Weiterleitung von Anmelde Informationen nur an eine bestimmte Liste von Diensten zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="7ba26-116">With [*constrained delegation*](../secgloss/c-gly.md), a computer can be set to allow forwarding of credentials only to a specific list of services.</span></span> <span data-ttu-id="7ba26-117">Diese Dienste müssen sich in derselben Domäne befinden wie der Computer, der die Anmelde Informationen weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="7ba26-117">Those services must reside in the same domain as the computer forwarding the credentials.</span></span> <span data-ttu-id="7ba26-118">Bei der *eingeschränkten Delegierung* werden Tickets nicht mehr vom Client an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="7ba26-118">Under *constrained delegation*, tickets are no longer sent from the client to the server.</span></span> <span data-ttu-id="7ba26-119">Der Server Computer erstellt nach Bedarf Dienst Tickets, die zum Authentifizieren des Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ba26-119">The server computer creates service tickets to forward as necessary from information used to authenticate the client.</span></span>

<span data-ttu-id="7ba26-120">Obwohl die Kerberos-Richtlinie für eine Domäne die delegierte Authentifizierung zulässt, indem Tickets weitergeleitet werden können, muss dieser Aspekt der Richtlinie nicht für alle Benutzer oder alle Computer gelten.</span><span class="sxs-lookup"><span data-stu-id="7ba26-120">Although Kerberos policy for a domain may permit delegated authentication by allowing tickets to be forwarded, that aspect of policy need not apply to all users or all computers.</span></span> <span data-ttu-id="7ba26-121">Ein Attribut eines einzelnen Benutzerkontos kann festgelegt werden, um die Weiterleitung der [*Anmelde*](../secgloss/c-gly.md) Informationen dieses Benutzers durch einen beliebigen Server zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7ba26-121">An attribute of an individual user account can be set to disable forwarding of that user's [*credentials*](../secgloss/c-gly.md) by any server.</span></span> <span data-ttu-id="7ba26-122">Ein Attribut des Kontos eines einzelnen Computers kann festgelegt werden, um die Weiterleitung von Anmelde Informationen von einem beliebigen Benutzer zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7ba26-122">An attribute of an individual computer's account can be set to disable forwarding of credentials from any user.</span></span> <span data-ttu-id="7ba26-123">In beiden Fällen können Sie die Delegierung deaktivieren, indem Sie eine Gruppenrichtlinie erstellen, die für alle Benutzer oder alle Computer in einer Organisationseinheit der Active Directory gilt.</span><span class="sxs-lookup"><span data-stu-id="7ba26-123">In both cases, delegation can be disabled by creating a group policy to apply to all users or all computers in an organizational unit of the Active Directory.</span></span>

<span data-ttu-id="7ba26-124">**Windows XP/2000:** Die eingeschränkte Delegierung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ba26-124">**Windows XP/2000:** Constrained delegation is not supported.</span></span>

 

 
