---
description: Da eine COM+-Bibliotheks Anwendung von einem anderen Prozess gehostet wird, der möglicherweise über eigene Sicherheitseinstellungen verfügt, müssen für die Sicherheit von Bibliotheksanwendungen besondere Aspekte berücksichtigt werden.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Sicherheit der Bibliothek Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2885173f3798d33ed26a5b447fde4429b9bf96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523419"
---
# <a name="library-application-security"></a><span data-ttu-id="1eaf9-103">Sicherheit der Bibliothek Anwendungen</span><span class="sxs-lookup"><span data-stu-id="1eaf9-103">Library Application Security</span></span>

<span data-ttu-id="1eaf9-104">Da eine COM+-Bibliotheks Anwendung von einem anderen Prozess gehostet wird, der möglicherweise über eigene Sicherheitseinstellungen verfügt, müssen für die Sicherheit von Bibliotheksanwendungen besondere Aspekte berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="1eaf9-104">Because a COM+ library application is hosted by another process, which may have its own security settings, security for library applications requires special consideration.</span></span>

<span data-ttu-id="1eaf9-105">Die folgenden Einschränkungen gelten für die Anwendungssicherheit von Bibliotheken:</span><span class="sxs-lookup"><span data-stu-id="1eaf9-105">The following constraints apply to library application security:</span></span>

-   <span data-ttu-id="1eaf9-106">Bibliotheksanwendungen werden unter dem Client Prozess-Sicherheits Token und nicht unter ihrer eigenen Benutzeridentität ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1eaf9-106">Library applications run under the client process security token rather than under their own user identity.</span></span> <span data-ttu-id="1eaf9-107">Sie haben nur so viele Berechtigungen wie der Client.</span><span class="sxs-lookup"><span data-stu-id="1eaf9-107">They have only as much privilege as the client has.</span></span>
-   <span data-ttu-id="1eaf9-108">Bibliotheksanwendungen Steuern keine Sicherheit auf Prozessebene.</span><span class="sxs-lookup"><span data-stu-id="1eaf9-108">Library applications do not control process-level security.</span></span> <span data-ttu-id="1eaf9-109">Der Sicherheits Beschreibung für den Prozess werden keine Benutzer in Rollen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1eaf9-109">No users in roles will be added to the security descriptor for the process.</span></span> <span data-ttu-id="1eaf9-110">Die einzige Möglichkeit für eine Bibliotheks Anwendung, eigene Zugriffs Überprüfungen durchzuführen, ist die Verwendung der Sicherheit auf Komponentenebene.</span><span class="sxs-lookup"><span data-stu-id="1eaf9-110">The only way for a library application to perform its own access checks is to use component-level security.</span></span> <span data-ttu-id="1eaf9-111">(Siehe [Sicherheitsgrenzen](security-boundaries.md).)</span><span class="sxs-lookup"><span data-stu-id="1eaf9-111">(See [Security Boundaries](security-boundaries.md).)</span></span>
-   <span data-ttu-id="1eaf9-112">Bibliotheksanwendungen können so konfiguriert werden, dass Sie entweder teilnehmen oder nicht an der Host Prozess Authentifizierung teilnehmen, indem Sie die Authentifizierung aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1eaf9-112">Library applications can be configured to either participate or not participate in host process authentication, by enabling or disabling authentication.</span></span> <span data-ttu-id="1eaf9-113">(Informationen hierzu finden Sie unter [Aktivieren der Authentifizierung für eine Bibliotheks Anwendung](enabling-authentication-for-a-library-application.md).)</span><span class="sxs-lookup"><span data-stu-id="1eaf9-113">(See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).)</span></span>
-   <span data-ttu-id="1eaf9-114">Bibliotheksanwendungen können keine Identitätswechsel Ebene festlegen. Diese verwenden den Host Prozess.</span><span class="sxs-lookup"><span data-stu-id="1eaf9-114">Library applications cannot set an impersonation level; they use that of the host process.</span></span>

## <a name="using-library-applications-to-limit-application-privilege"></a><span data-ttu-id="1eaf9-115">Verwenden von Bibliotheksanwendungen zum Einschränken von Anwendungs Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="1eaf9-115">Using Library Applications to Limit Application Privilege</span></span>

<span data-ttu-id="1eaf9-116">In einigen Fällen möchten Sie möglicherweise eine Anwendung speziell als Bibliotheks Anwendung konfigurieren, damit Sie unter der Identität des Host Prozesses ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1eaf9-116">In some cases, you may want to configure an application specifically as a library application so that it runs under the identity of the hosting process.</span></span> <span data-ttu-id="1eaf9-117">Dadurch wird die Anwendung grundsätzlich eingeschränkt, sodass nur auf die Ressourcen zugegriffen werden kann, auf die der Client, der Host Prozess, zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="1eaf9-117">Doing so fundamentally limits the application so that it can access only those resources that its client, the host process, can access.</span></span> <span data-ttu-id="1eaf9-118">Die Threads, auf denen die Bibliotheks Anwendungskomponenten ausgeführt werden, verwenden standardmäßig das-Prozess Token. Wenn Sie also Aufrufe außerhalb der Anwendung ausführen oder auf Ressourcen zugreifen, z. b. Dateien, die mit einer Sicherheits Beschreibung geschützt sind, werden Sie als Client angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1eaf9-118">The threads that the library application components run on will use the process token by default, and therefore when they make calls outside of the application or access resources such as files guarded with a security descriptor, they will appear to be the client.</span></span> <span data-ttu-id="1eaf9-119">Bei Anwendungen, die sensible Aufgaben ausführen, kann dies eine einfache Möglichkeit sein, den Umfang ihrer Aktionen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="1eaf9-119">For applications that perform sensitive work, this may be an easy way to control the scope of their actions.</span></span>

## <a name="effectively-securing-library-applications"></a><span data-ttu-id="1eaf9-120">Effektive Sicherung von Bibliotheksanwendungen</span><span class="sxs-lookup"><span data-stu-id="1eaf9-120">Effectively Securing Library Applications</span></span>

<span data-ttu-id="1eaf9-121">Bei der Konfiguration der rollenbasierten Sicherheit und Authentifizierung für Bibliotheksanwendungen sind besondere Aspekte zu beachten, damit Sie erwartungsgemäß ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1eaf9-121">There are special considerations in configuring role-based security and authentication for library applications so that they perform as expected.</span></span> <span data-ttu-id="1eaf9-122">Weitere Informationen finden Sie unter [Konfigurieren der Sicherheit für Bibliotheksanwendungen](configuring-security-for-library-applications.md).</span><span class="sxs-lookup"><span data-stu-id="1eaf9-122">For details, see [Configuring Security for Library Applications](configuring-security-for-library-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1eaf9-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1eaf9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eaf9-124">Clientauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="1eaf9-124">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="1eaf9-125">Client Identitätswechsel und Delegierung</span><span class="sxs-lookup"><span data-stu-id="1eaf9-125">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="1eaf9-126">Multi-Tier-Anwendungssicherheit</span><span class="sxs-lookup"><span data-stu-id="1eaf9-126">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="1eaf9-127">Sicherheit für programmgesteuerte Komponenten</span><span class="sxs-lookup"><span data-stu-id="1eaf9-127">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="1eaf9-128">Rollenbasierte Sicherheitsverwaltung</span><span class="sxs-lookup"><span data-stu-id="1eaf9-128">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="1eaf9-129">Verwenden der Richtlinie für Software Einschränkung in com+</span><span class="sxs-lookup"><span data-stu-id="1eaf9-129">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



