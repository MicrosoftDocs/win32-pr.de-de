---
description: Multi-Tier-Anwendungssicherheit
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Multi-Tier-Anwendungssicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150f7894c7d11e832786e31ab028f9dbac35f6e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346226"
---
# <a name="multi-tier-application-security"></a><span data-ttu-id="adf50-103">Multi-Tier-Anwendungssicherheit</span><span class="sxs-lookup"><span data-stu-id="adf50-103">Multi-Tier Application Security</span></span>

<span data-ttu-id="adf50-104">Sie können Schwierigkeiten bei der Entscheidung treffen, wie die Sicherheit in einer auf mehreren Ebenen basierenden, komponentenbasierten Anwendung in der Datenbank zu erzwingen ist.</span><span class="sxs-lookup"><span data-stu-id="adf50-104">You can face difficult choices in deciding precisely where to enforce security in a multi-tier, component-based application: At the database?</span></span> <span data-ttu-id="adf50-105">Auf der mittleren Ebene?</span><span class="sxs-lookup"><span data-stu-id="adf50-105">At the middle tier?</span></span> <span data-ttu-id="adf50-106">In den Komponenten?</span><span class="sxs-lookup"><span data-stu-id="adf50-106">In the components?</span></span> <span data-ttu-id="adf50-107">An einem anderen Ort?</span><span class="sxs-lookup"><span data-stu-id="adf50-107">Somewhere else?</span></span> <span data-ttu-id="adf50-108">Überall?</span><span class="sxs-lookup"><span data-stu-id="adf50-108">Everywhere?</span></span> <span data-ttu-id="adf50-109">Wenn die Anzahl und Komplexität der Sicherheitsmechanismen zunimmt, wird die Leistung beeinträchtigt, und das Anwendungsverhalten wird weniger vorhersagbar.</span><span class="sxs-lookup"><span data-stu-id="adf50-109">As security mechanisms increase in number and complexity, performance declines and application behavior becomes less predictable.</span></span> <span data-ttu-id="adf50-110">Dennoch müssen Sie sicherstellen, dass die Daten geschützt sind, dass Geschäftsregeln befolgt werden und dass eine beträchtliche Aktivität protokolliert wird und die Anwendung weiterhin für Clients funktioniert.</span><span class="sxs-lookup"><span data-stu-id="adf50-110">Nevertheless, you must ensure that data is protected, business rules are followed, and significant activity is logged, and still have your application work for clients as intended.</span></span> <span data-ttu-id="adf50-111">Sie müssen sicher sein, dass jeder Client Pfad über die Anwendung korrekt ist und dass die vorhandenen Sicherheits Prüfpunkte ausreichen.</span><span class="sxs-lookup"><span data-stu-id="adf50-111">You must be certain that every client path through your application is correct and that the security checkpoints you have in place will suffice.</span></span>

<span data-ttu-id="adf50-112">Die schwierigste Entscheidung besteht häufig darin, die Sicherheit in der Datenbank zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="adf50-112">The hardest decision is often whether to enforce security at the database.</span></span> <span data-ttu-id="adf50-113">In der Vergangenheit handelt es sich hierbei um eine enge Sicherheit der Sicherheit, da Sie als ein Königreich wahrgenommen wird, das wirklich sicher sein muss, und Datenbankadministratoren sehr ungern eine andere Person als vertrauenswürdig einstufen, um die Sicherheit zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="adf50-113">Historically, this is where security is tightest because it is perceived as the one kingdom that needs to be truly secure, and database administrators are very reluctant to trust someone else to enforce security for them.</span></span> <span data-ttu-id="adf50-114">Die Erzwingung der Sicherheit in der Datenbank kann jedoch sehr kostspielig und schwer zu skalieren sein. Dies ist genau der Punkt, an dem Sie Anwendungen mit mehreren Ebenen erstellen.</span><span class="sxs-lookup"><span data-stu-id="adf50-114">But enforcing security at the database can be quite expensive and difficult to scale, which is precisely the point of writing multi-tier applications in the first place.</span></span>

<span data-ttu-id="adf50-115">Die allgemeine Regel für skalierbare Anwendungen mit mehreren Ebenen mit com+ ist, dass Sie nach Möglichkeit eine detaillierte Sicherheit in der com+-Anwendung auf der mittleren Ebene erzwingen sollten.</span><span class="sxs-lookup"><span data-stu-id="adf50-115">The general rule to follow with scalable multi-tier applications using COM+ is that, whenever possible, you should enforce detailed security in the COM+ application at the middle tier.</span></span> <span data-ttu-id="adf50-116">Auf diese Weise können Sie die von com+ bereitgestellten skalierbaren Dienste vollständig nutzen.</span><span class="sxs-lookup"><span data-stu-id="adf50-116">Doing so enables you to fully leverage the scalable services provided by COM+.</span></span> <span data-ttu-id="adf50-117">Authentifizieren Sie sich nur dann bei der Datenbank, wenn dies unbedingt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="adf50-117">Authenticate at the database only when you absolutely need to, and fully weigh the performance implications of doing so.</span></span>

<span data-ttu-id="adf50-118">Eine Erörterung von Problemen bei der Entscheidung, wo Sicherheitsüberprüfungen durchgeführt werden sollen, finden Sie unter [entscheiden, wo die Sicherheit](deciding-where-to-enforce-security.md)erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="adf50-118">For a discussion of issues to consider in deciding where to perform security checks, see [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

<span data-ttu-id="adf50-119">Eine Erläuterung einiger grundlegender Szenarien zum Sichern von Anwendungen mit mehreren Ebenen finden Sie unter [grundlegende Szenarien zum Sichern von Daten in Anwendungen mit mehreren Ebenen](basic-scenarios-for-securing-data-in-multi-tier-applications.md).</span><span class="sxs-lookup"><span data-stu-id="adf50-119">For a discussion of some basic scenarios in securing multi-tier applications, see [Basic Scenarios for Securing Data in Multi-Tier Applications](basic-scenarios-for-securing-data-in-multi-tier-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="adf50-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="adf50-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adf50-121">Clientauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="adf50-121">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="adf50-122">Client Identitätswechsel und Delegierung</span><span class="sxs-lookup"><span data-stu-id="adf50-122">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="adf50-123">Sicherheit der Bibliothek Anwendungen</span><span class="sxs-lookup"><span data-stu-id="adf50-123">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="adf50-124">Sicherheit für programmgesteuerte Komponenten</span><span class="sxs-lookup"><span data-stu-id="adf50-124">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="adf50-125">Rollenbasierte Sicherheitsverwaltung</span><span class="sxs-lookup"><span data-stu-id="adf50-125">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="adf50-126">Verwenden der Richtlinie für Software Einschränkung in com+</span><span class="sxs-lookup"><span data-stu-id="adf50-126">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



