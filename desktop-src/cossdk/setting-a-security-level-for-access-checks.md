---
description: Nachdem Sie die Zugriffs Überprüfungen aktiviert haben, müssen Sie für die COM+-Anwendung die Ebene auswählen, auf der Sie die Zugriffs Überprüfungen durchführen möchten.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646a49a4966bff7c593f12cb7481f4a4aad8859e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127396"
---
# <a name="setting-a-security-level-for-access-checks"></a><span data-ttu-id="383f3-103">Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="383f3-103">Setting a Security Level for Access Checks</span></span>

<span data-ttu-id="383f3-104">Nachdem Sie die [Zugriffs Überprüfungen](enabling-access-checks-for-an-application.md)aktiviert haben, müssen Sie für die COM+-Anwendung die Ebene auswählen, auf der Sie die Zugriffs Überprüfungen durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="383f3-104">After you have enabled [access checks](enabling-access-checks-for-an-application.md), for your COM+ application, you must select the level at which you wish to have access checks performed.</span></span>

<span data-ttu-id="383f3-105">**So wählen Sie eine Sicherheitsstufe aus**</span><span class="sxs-lookup"><span data-stu-id="383f3-105">**To select a security level**</span></span>

1.  <span data-ttu-id="383f3-106">Klicken Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die Zugriffs Überprüfungen aktivieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="383f3-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="383f3-107">Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .</span><span class="sxs-lookup"><span data-stu-id="383f3-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="383f3-108">Wählen Sie unter **Sicherheitsstufe** eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="383f3-108">Under **Security level**, select one of the following:</span></span>

    -   <span data-ttu-id="383f3-109">**Nur Zugriffs Prüfungen auf Prozessebene ausführen**– diese Einstellung gibt an, dass Benutzer in Rollen, die der Anwendung zugewiesen sind, der Prozess Sicherheits Beschreibung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="383f3-109">**Perform access checks only at the process level**— This setting indicates that users in roles that are assigned to the application will be added to the process security descriptor.</span></span> <span data-ttu-id="383f3-110">Dies hat folgende Auswirkungen und Implikationen:</span><span class="sxs-lookup"><span data-stu-id="383f3-110">This has the following effects and implications:</span></span>

        <span data-ttu-id="383f3-111">Die differenzierte Rollen Überprüfung ist auf Komponenten-, Methoden-und Schnittstellen Ebene deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="383f3-111">Fine-grained role checking is turned off at the component, method, and interface levels.</span></span> <span data-ttu-id="383f3-112">Sicherheitsüberprüfungen werden nur auf Anwendungsebene durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="383f3-112">Security checks are performed only at the application level.</span></span>

        <span data-ttu-id="383f3-113">Die Security-Eigenschaft ist nicht im Kontext für Objekte enthalten, die in der Anwendung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="383f3-113">The security property is not included on the context for any objects running within the application.</span></span> <span data-ttu-id="383f3-114">Dies kann sich potenziell auf die Aktivierung von Objekten auswirken.</span><span class="sxs-lookup"><span data-stu-id="383f3-114">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="383f3-115">Siehe [Sicherheitskontext Eigenschaft](security-context-property.md).</span><span class="sxs-lookup"><span data-stu-id="383f3-115">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="383f3-116">Der Sicherheits Aufrufkontext wird nicht verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="383f3-116">The security call context will not be made available.</span></span> <span data-ttu-id="383f3-117">Programmgesteuerte Sicherheit, die auf Sicherheitskontext Informationen basiert, funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="383f3-117">Programmatic security that relies on security call context information will not function.</span></span> <span data-ttu-id="383f3-118">Siehe [Kontextinformationen zum Sicherheitsgespräch](security-call-context-information.md).</span><span class="sxs-lookup"><span data-stu-id="383f3-118">See [Security Call Context Information](security-call-context-information.md).</span></span>

    -   <span data-ttu-id="383f3-119">**Ausführen von Zugriffs Überprüfungen auf Prozess-und Komponentenebene**– diese Einstellung gibt an, dass Sicherheits Deskriptoren auf Prozessebene und vollständige rollenbasierte Sicherheitsüberprüfungen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="383f3-119">**Perform access checks at the process and component level**—This setting indicates that process-level security descriptor checks and full role-based security checks will be performed.</span></span> <span data-ttu-id="383f3-120">Dies hat folgende Auswirkungen und Implikationen:</span><span class="sxs-lookup"><span data-stu-id="383f3-120">This has the following effects and implications:</span></span>

        <span data-ttu-id="383f3-121">Um die Rollen Überprüfung für bestimmte Komponenten zu aktivieren, müssen Sie [Zugriffs Überprüfungen auf Komponentenebene aktivieren](enabling-access-checks-at-the-component-level.md).</span><span class="sxs-lookup"><span data-stu-id="383f3-121">To enable role checking for particular components, you must [enable access checks at the component level](enabling-access-checks-at-the-component-level.md).</span></span>

        <span data-ttu-id="383f3-122">Die Security-Eigenschaft ist im Kontext für alle Objekte enthalten, die in der Anwendung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="383f3-122">The security property is included on the context for any objects running within the application.</span></span> <span data-ttu-id="383f3-123">Dies kann sich potenziell auf die Aktivierung von Objekten auswirken.</span><span class="sxs-lookup"><span data-stu-id="383f3-123">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="383f3-124">Siehe [Sicherheitskontext Eigenschaft](security-context-property.md).</span><span class="sxs-lookup"><span data-stu-id="383f3-124">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="383f3-125">Der Sicherheits Aufrufkontext ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="383f3-125">The security call context is available.</span></span> <span data-ttu-id="383f3-126">Programmgesteuerte rollenbasierte Sicherheit ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="383f3-126">Programmatic role-based security is enabled.</span></span> <span data-ttu-id="383f3-127">Siehe [Kontextinformationen zum Sicherheitsgespräch](security-call-context-information.md).</span><span class="sxs-lookup"><span data-stu-id="383f3-127">See [Security Call Context Information](security-call-context-information.md).</span></span>

        > [!Note]  
        > <span data-ttu-id="383f3-128">Für COM+-Bibliotheksanwendungen müssen Sie sowohl auf der Prozess-als auch auf der Komponentenebene prüfen, ob eine sinnvolle Zugriffs Überprüfung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="383f3-128">For COM+ library applications, you must choose to check both at process and at component levels for any meaningful access checking to work.</span></span> <span data-ttu-id="383f3-129">Bibliotheksanwendungen basieren auf dem Host Prozess für Sicherheit auf Prozessebene.</span><span class="sxs-lookup"><span data-stu-id="383f3-129">Library applications rely on the host process for process-level security.</span></span> <span data-ttu-id="383f3-130">Sie können bestimmen, wie die Bibliotheks Anwendung mit der vom Host Prozess durchgeführten Authentifizierung interagiert, indem Sie die- [Authentifizierung festlegen](enabling-authentication-for-a-library-application.md).</span><span class="sxs-lookup"><span data-stu-id="383f3-130">You can determine how the library application interacts with authentication performed by the host process by [setting authentication](enabling-authentication-for-a-library-application.md).</span></span> <span data-ttu-id="383f3-131">Weitere Informationen finden Sie unter [Bibliotheks Anwendungssicherheit](library-application-security.md).</span><span class="sxs-lookup"><span data-stu-id="383f3-131">For more information, see [Library Application Security](library-application-security.md).</span></span>

         

4.  <span data-ttu-id="383f3-132">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="383f3-132">Click **OK**.</span></span>

<span data-ttu-id="383f3-133">Wenn die Anwendung das nächste Mal gestartet wird, wird die Sicherheit automatisch auf der angegebenen Ebene geprüft.</span><span class="sxs-lookup"><span data-stu-id="383f3-133">The next time the application is started, security will automatically be checked at the specified level.</span></span> <span data-ttu-id="383f3-134">Nur Benutzer, die Rollen zugewiesen sind, die der Anwendung zugewiesen sind, erhalten Zugriff auf die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="383f3-134">Only users assigned to roles assigned to the application will be given access to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="383f3-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="383f3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="383f3-136">Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden</span><span class="sxs-lookup"><span data-stu-id="383f3-136">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="383f3-137">Konfigurieren von Role-Based Sicherheit</span><span class="sxs-lookup"><span data-stu-id="383f3-137">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="383f3-138">Definieren von Rollen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="383f3-138">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="383f3-139">Aktivieren von Zugriffs Überprüfungen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="383f3-139">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="383f3-140">Aktivieren von Zugriffs Überprüfungen auf Komponentenebene</span><span class="sxs-lookup"><span data-stu-id="383f3-140">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



