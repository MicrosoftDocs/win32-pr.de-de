---
description: Role-Based Sicherheitsverwaltung
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Role-Based Sicherheitsverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714cede74e105a68b0a5fed2371858054add954e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524040"
---
# <a name="role-based-security-administration"></a><span data-ttu-id="bfeaf-103">Role-Based Sicherheitsverwaltung</span><span class="sxs-lookup"><span data-stu-id="bfeaf-103">Role-Based Security Administration</span></span>

<span data-ttu-id="bfeaf-104">Die rollenbasierte Sicherheit ist ein von com+ bereitgestellter automatischer Dienst, mit dem Sie eine Zugriffs Steuerungs Richtlinie für Ihre COM+-Anwendung administrativ erstellen und erzwingen können.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-104">Role-based security is an automatic service provided by COM+ that enables you to administratively construct and enforce an access control policy for your COM+ application.</span></span> <span data-ttu-id="bfeaf-105">Mit einem flexiblen und erweiterbaren Sicherheits Konfigurations Modell bietet die rollenbasierte Sicherheit einen erheblichen Vorteil gegenüber der Durchsetzung der gesamten Sicherheit in ihren Komponenten und bietet die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="bfeaf-105">With a flexible and extensible security configuration model, role-based security offers a considerable advantage over enforcing all security within your components and provides the following benefits:</span></span>

-   <span data-ttu-id="bfeaf-106">Sie können die Sicherheit administrativ konfigurieren, indem Sie entweder das Verwaltungs Programmkomponenten Dienste oder die Verwaltungsfunktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-106">You can configure security administratively, using either the Component Services administrative tool or the Administrative functions.</span></span>
-   <span data-ttu-id="bfeaf-107">Sie müssen keine sicherheitsbezogene Logik in Ihre Komponenten schreiben, wenn der Rollen Schutz auf Methoden Ebene Ihnen ausreichend Zugriffs Steuerung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-107">You don't have to write security-related logic into your components when role protection at the method level provides you with fine enough access control.</span></span>
-   <span data-ttu-id="bfeaf-108">Sie müssen die Sicherheit nicht in eine Schnittstelle oder einen Komponenten Entwurf einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-108">You don't have to factor security into interface or component design.</span></span> <span data-ttu-id="bfeaf-109">Stattdessen können Sie die Sicherheit auf Methoden Basis festlegen.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-109">Instead, you can set security on a method-by-method basis.</span></span>
-   <span data-ttu-id="bfeaf-110">Sie können sich auf die Struktur der Sicherheitsrichtlinie konzentrieren, die Sie erzwingen möchten, und überrollen kann diese Richtlinie den Administratoren, die Ihre Anwendung bereitstellen, eindeutig ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-110">You can focus on the structure of the security policy you want to enforce, and through roles, that policy can be clearly expressed to the administrators deploying your application.</span></span>
-   <span data-ttu-id="bfeaf-111">Sie können eine Sicherheitsrichtlinie auf einfache Weise ändern, um sich an sich entwickelnde Sicherheitsanforderungen für eine Anwendung anzupassen.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-111">You can easily modify a security policy to adapt to evolving security requirements for an application.</span></span>
-   <span data-ttu-id="bfeaf-112">Sie können bei Bedarf differenziertere Sicherheitsrichtlinien erstellen, wenn Sie die rollenbasierte Sicherheit als unterstützende Plattform verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-112">You can build more granular security policies programmatically if you need to, using role-based security as a supporting platform.</span></span>
-   <span data-ttu-id="bfeaf-113">Sie können die rollenbasierte Sicherheit für eine ausführliche Überwachung nutzen, da Sie Aufrufer-Sicherheitsinformationen für eine ganze Kette von upstreamaufrufen abrufen können.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-113">You can leverage role-based security to do detailed auditing, because you can obtain caller security information for an entire chain of upstream calls.</span></span>

> [!Note]  
> <span data-ttu-id="bfeaf-114">Benutzer in der Administrator Rolle für die System Anwendung müssen Mitglieder der lokalen Administratoren Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-114">Users in the Administrator role for the System Application must be members of the local administrators group.</span></span> <span data-ttu-id="bfeaf-115">Ab Windows Server 2003 enthält die Authentifizierungsfunktion für die com+-System Anwendung auch den Wert eoac- \_ deaktivierte \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-115">Also, as of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="bfeaf-116">Dieser Wert, der Aktivierungen von Aktivierungen durch aktivierte Aktivierungen deaktiviert, wird beim Starten der System Anwendung im [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Befehl verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-116">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="bfeaf-117">Wenn Sie die Authentifizierungsfunktion auf eoac \_ deaktivieren, \_ kann eine Anwendung, die unter einem privilegierten Konto (z. b. LocalSystem) ausgeführt wird, verhindern, dass Ihre Identität verwendet wird, um nicht vertrauenswürdige Komponenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-117">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

 

<span data-ttu-id="bfeaf-118">In den folgenden Themen dieses Abschnitts finden Sie Informationen zur Funktionsweise der rollenbasierten Sicherheit und zu berücksichtigende Aspekte bei der Verwendung, um eine Sicherheitsrichtlinie für eine Anwendung zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="bfeaf-118">See the following topics in this section for information about how role-based security works and issues to consider when using it to construct a security policy for an application:</span></span>

-   [<span data-ttu-id="bfeaf-119">Verwenden von Rollen für die Client Autorisierung</span><span class="sxs-lookup"><span data-stu-id="bfeaf-119">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
-   [<span data-ttu-id="bfeaf-120">Effektives Entwerfen von Rollen</span><span class="sxs-lookup"><span data-stu-id="bfeaf-120">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
-   [<span data-ttu-id="bfeaf-121">Sicherheitsgrenzen</span><span class="sxs-lookup"><span data-stu-id="bfeaf-121">Security Boundaries</span></span>](security-boundaries.md)
-   [<span data-ttu-id="bfeaf-122">Informationen zum Sicherheits Aufrufkontext</span><span class="sxs-lookup"><span data-stu-id="bfeaf-122">Security Call Context Information</span></span>](security-call-context-information.md)
-   [<span data-ttu-id="bfeaf-123">Sicherheitskontext Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bfeaf-123">Security Context Property</span></span>](security-context-property.md)

<span data-ttu-id="bfeaf-124">Ausführliche Beschreibungen der Schritte, die zum Konfigurieren der rollenbasierten Sicherheit für eine Anwendung erforderlich sind, finden Sie unter [Konfigurieren von Role-Based Sicherheit](configuring-role-based-security.md).</span><span class="sxs-lookup"><span data-stu-id="bfeaf-124">For detailed how-to descriptions of the steps involved in configuring role-based security for an application, see [Configuring Role-Based Security](configuring-role-based-security.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfeaf-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bfeaf-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfeaf-126">Clientauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="bfeaf-126">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="bfeaf-127">Client Identitätswechsel und Delegierung</span><span class="sxs-lookup"><span data-stu-id="bfeaf-127">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="bfeaf-128">Sicherheit der Bibliothek Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bfeaf-128">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="bfeaf-129">Multi-Tier-Anwendungssicherheit</span><span class="sxs-lookup"><span data-stu-id="bfeaf-129">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="bfeaf-130">Sicherheit für programmgesteuerte Komponenten</span><span class="sxs-lookup"><span data-stu-id="bfeaf-130">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="bfeaf-131">Verwenden der Richtlinie für Software Einschränkung in com+</span><span class="sxs-lookup"><span data-stu-id="bfeaf-131">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
