---
description: Die folgenden Begriffe beschreiben Domänen, die auf Remote Systemen vorhanden sind.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Primäre und vertrauenswürdige Domänen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d69a8bf5f5a8363f8de726c6183fd4de820665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525718"
---
# <a name="primary-and-trusted-domains"></a><span data-ttu-id="79bde-103">Primäre und vertrauenswürdige Domänen</span><span class="sxs-lookup"><span data-stu-id="79bde-103">Primary and Trusted Domains</span></span>

<span data-ttu-id="79bde-104">Die folgenden Begriffe beschreiben Domänen, die auf Remote Systemen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="79bde-104">The following terms describe domains that exist on remote systems.</span></span>

-   [<span data-ttu-id="79bde-105">Primäre Domäne</span><span class="sxs-lookup"><span data-stu-id="79bde-105">Primary Domain</span></span>](#primary-domain)
-   [<span data-ttu-id="79bde-106">Vertrauenswürdige Domäne</span><span class="sxs-lookup"><span data-stu-id="79bde-106">Trusted Domain</span></span>](#primary-and-trusted-domains)

## <a name="primary-domain"></a><span data-ttu-id="79bde-107">Primäre Domäne</span><span class="sxs-lookup"><span data-stu-id="79bde-107">Primary Domain</span></span>

<span data-ttu-id="79bde-108">Eine primäre Domäne ist die Domäne, die für die Einrichtung weiterer Vertrauens Stellungen und die Durchführung der Authentifizierung (oder für die Übergabe einer Authentifizierungsanforderung an eine entsprechende vertrauenswürdige Domäne) zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="79bde-108">A primary domain is the domain that is responsible for establishing further trust relationships and performing authentication (or for passing an authentication request on to an appropriate trusted domain).</span></span> <span data-ttu-id="79bde-109">Die Domänen Controller in der primären Domäne verarbeiten oder übergeben Authentifizierungsanforderungen, die von der Arbeitsstation stammen.</span><span class="sxs-lookup"><span data-stu-id="79bde-109">The domain controllers in the primary domain handle or pass along authentication requests that originate at the workstation.</span></span>

<span data-ttu-id="79bde-110">Wenn die Anmeldung erfolgt, überprüft die LSA die integrierten Domänen und die Konto Domänen auf Authentifizierungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="79bde-110">When logon occurs, the LSA checks the built-in and account domains for authentication information.</span></span> <span data-ttu-id="79bde-111">Wenn sich das Konto, bei dem angemeldet wird, nicht in einer dieser Domänen befindet, wird die Anmelde Anforderung an die primäre Domäne des Systems übergeben.</span><span class="sxs-lookup"><span data-stu-id="79bde-111">If the account being logged on to is not in either of these domains, the logon request is handed off to the system's primary domain.</span></span>

## <a name="trusted-domain"></a><span data-ttu-id="79bde-112">Vertrauenswürdige Domäne</span><span class="sxs-lookup"><span data-stu-id="79bde-112">Trusted Domain</span></span>

<span data-ttu-id="79bde-113">Eine vertrauenswürdige Domäne ist eine Domäne, der das lokale System vertraut, um Benutzer zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="79bde-113">A trusted domain is a domain that the local system trusts to authenticate users.</span></span> <span data-ttu-id="79bde-114">Anders ausgedrückt: Wenn ein Benutzer oder eine Anwendung von einer vertrauenswürdigen Domäne authentifiziert wird, wird diese Authentifizierung von allen Domänen akzeptiert, die der authentifizier enden Domäne vertrauen.</span><span class="sxs-lookup"><span data-stu-id="79bde-114">In other words, if a user or application is authenticated by a trusted domain, this authentication is accepted by all domains that trust the authenticating domain.</span></span>

<span data-ttu-id="79bde-115">Jede untergeordnete Domäne verfügt automatisch über eine bidirektionale Vertrauensstellung mit der Hauptdomäne.</span><span class="sxs-lookup"><span data-stu-id="79bde-115">Each subordinate domain automatically has a two-way trust relationship with the main domain.</span></span> <span data-ttu-id="79bde-116">Standardmäßig ist diese Vertrauensstellung transitiv, d. h., wenn ein System Domäne a vertraut, vertraut Sie auch allen Domänen, denen eine Domäne vertraut.</span><span class="sxs-lookup"><span data-stu-id="79bde-116">By default, this trust is transitive, meaning that if a system trusts Domain A, it also trusts all domains that Domain A trusts.</span></span> <span data-ttu-id="79bde-117">Unidirektionale Vertrauens Stellungen werden auch für ältere Betriebssysteme als Windows 2000 unterstützt, die keine transitiven bidirektionalen Vertrauens Stellungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="79bde-117">One-way trusts are also supported for operating systems earlier than Windows 2000, which do not support transitive, two-way trusts.</span></span>

<span data-ttu-id="79bde-118">Die [*Lokale Sicherheits Autorität (Local Security Authority*](/windows/desktop/SecGloss/l-gly) , LSA) verfügt über den Objekttyp " [**Treuhänder Domäne**](the-trusteddomain-object-type.md)", der zum Speichern von Informationen über Vertrauens Stellungen verwendet wird, einschließlich des Namens und der [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) der vertrauenswürdigen Domäne, des Kontos in der Domäne, das für Authentifizierungsanforderungen verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="79bde-118">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) has an object type, [**TrustedDomain**](the-trusteddomain-object-type.md), that is used to store information about trust relationships, including the name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the trusted domain, the account in the domain to use for authentication requests, name and SID translation requests, and the names of domain controllers in the trusted domain.</span></span>

<span data-ttu-id="79bde-119">Auf Domänen Controllern erstellt die LSA eine Instanz eines vertrauenswürdigen [**Domänen**](the-trusteddomain-object-type.md) Objekts für jede Domäne, die vom lokalen System als vertrauenswürdig eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="79bde-119">On domain controllers, the LSA creates an instance of a [**TrustedDomain**](the-trusteddomain-object-type.md) object for each domain trusted by the local system.</span></span>

<span data-ttu-id="79bde-120">Wenn z. b. eine Windows XP-Arbeitsstation einem Windows 2000-Domänen Controller vertraut, der wiederum vier andere Systeme als vertrauenswürdig einstuft, erhält die Arbeitsstation, die über transitiv Vertrauensstellung verbunden ist, fünf vertrauenswürdige [**Domänen**](the-trusteddomain-object-type.md) Objekte auf dem lokalen System.</span><span class="sxs-lookup"><span data-stu-id="79bde-120">For example, if a Windows XP workstation trusts a Windows 2000 domain controller that in turn trusts four other systems, the workstation, connected using transitive trust, will have five [**TrustedDomain**](the-trusteddomain-object-type.md) objects on its local system.</span></span>

 

 
