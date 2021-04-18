---
description: Wenn Sie die rollenbasierte Sicherheit in der com+-Anwendung verwenden, die die Komponente enthält, haben Sie Zugriff auf programmgesteuerte Sicherheitsfunktionen innerhalb der Komponente.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Sicherheit für programmgesteuerte Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345444"
---
# <a name="programmatic-component-security"></a><span data-ttu-id="9eb7b-103">Sicherheit für programmgesteuerte Komponenten</span><span class="sxs-lookup"><span data-stu-id="9eb7b-103">Programmatic Component Security</span></span>

<span data-ttu-id="9eb7b-104">Wenn Sie die rollenbasierte Sicherheit in der com+-Anwendung verwenden, die die Komponente enthält, haben Sie Zugriff auf programmgesteuerte Sicherheitsfunktionen innerhalb der Komponente.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-104">When you use role-based security in the COM+ application that contains your component, you have access to programmatic security functionality from within your component.</span></span> <span data-ttu-id="9eb7b-105">Sie können die Rollen Mitgliedschaft überprüfen, um zu bestimmen, ob bestimmte Code Abschnitte ausgeführt werden. Sie können mithilfe des Kontext Objekts für den Sicherheits Rückruf auf Sicherheitsinformationen zugreifen, und Sie können ermitteln, ob die Sicherheit für den aktuellen-Befehl aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-105">You can check role membership to determine whether particular sections of code are executed, you can access security information using the security call context object, and you can determine whether security is enabled for the current call.</span></span> <span data-ttu-id="9eb7b-106">Sie können all diese Aufgaben durchführen, indem Sie einen Verweis auf ein [**SecurityCallContext**](securitycallcontext.md) -Objekt (für Microsoft Visual Basic-Anwendungen) oder einen Zeiger auf die [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) -Schnittstelle (für C-und Microsoft Visual C++-Anwendungen) verwenden.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-106">You can perform all of these tasks by using a reference to a [**SecurityCallContext**](securitycallcontext.md) object (for Microsoft Visual Basic applications) or a pointer to the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface (for C and Microsoft Visual C++ applications).</span></span>

<span data-ttu-id="9eb7b-107">Weitere Informationen zur programmgesteuerten rollenbasierten Sicherheit finden Sie in den folgenden Themen in diesem Abschnitt:</span><span class="sxs-lookup"><span data-stu-id="9eb7b-107">For more information regarding programmatic role-based security, see the following topics in this section:</span></span>

-   [<span data-ttu-id="9eb7b-108">Überprüfen der Rollen Mitgliedschaft</span><span class="sxs-lookup"><span data-stu-id="9eb7b-108">Checking Role Membership</span></span>](checking-role-membership.md)
-   [<span data-ttu-id="9eb7b-109">Bestimmen, ob Role-Based Sicherheit aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="9eb7b-109">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
-   [<span data-ttu-id="9eb7b-110">Aufrufen von Kontextinformationen für den Sicherheitskontext</span><span class="sxs-lookup"><span data-stu-id="9eb7b-110">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a><span data-ttu-id="9eb7b-111">Identitätswechsel und com-Sicherheits Features</span><span class="sxs-lookup"><span data-stu-id="9eb7b-111">Impersonation and COM Security Features</span></span>

<span data-ttu-id="9eb7b-112">Wenn die Komponente in einer COM+-Anwendung verwendet wird, für die keine rollenbasierte Sicherheit verwendet wird, sind keine programmatischen Rollen Überprüfung und keine Kontextinformationen zum Sicherheitsgespräch verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-112">If your component is used in a COM+ application that does not use role-based security, programmatic role checking and security call context information are not available.</span></span> <span data-ttu-id="9eb7b-113">Sie können jedoch die von com bereitgestellte programmgesteuerte Sicherheitsfunktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-113">However, you can use the programmatic security functionality provided by COM.</span></span> <span data-ttu-id="9eb7b-114">Weitere Informationen finden Sie unter [Sicherheit in com](/windows/desktop/com/security-in-com).</span><span class="sxs-lookup"><span data-stu-id="9eb7b-114">For more information, see [Security in COM](/windows/desktop/com/security-in-com).</span></span>

<span data-ttu-id="9eb7b-115">Obwohl Sie die meisten von com bereitgestellten Sicherheitsfunktionen verwenden können, können Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) nicht aus einer Komponente aufrufen, die Teil einer COM+-Anwendung ist, da **CoInitializeSecurity** von dem Ersatz Zeichen aufgerufen wird, in dem die COM+-Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-115">Although you can use most of the security functionality provided by COM, you cannot call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) from a component that is part of a COM+ application because **CoInitializeSecurity** is called by the surrogate that the COM+ application runs in.</span></span> <span data-ttu-id="9eb7b-116">Sie können jedoch auch andere Sicherheitsfunktionen, wie z. b. [**coqueryclientblanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), abrufen, die Informationen über den Client abrufen.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-116">However, you can call other security functions, such as [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), which retrieves information about the client.</span></span>

<span data-ttu-id="9eb7b-117">Insbesondere, wenn Sie die Identität des Clients für den Zugriff auf eine Ressource verwenden müssen – z. b. durch den Zugriff auf eine Datei, die durch eine Sicherheits Beschreibung geschützt ist, oder über die Weitergabe der Identität des Clients an eine Datenbank – können Sie den Identitätswechsel Programm gesteuert ausführen.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-117">In particular, when you need to use the client's identity to access some resource—for example, accessing a file protected by a security descriptor, or propagating the client's identity through to a database—you can perform impersonation programmatically.</span></span> <span data-ttu-id="9eb7b-118">Weitere Details dazu, wann und wie Sie vorgehen, finden Sie unter Client Identitätswechsel [und Delegierung](client-impersonation-and-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="9eb7b-118">For more detail about when and how to do this, see [Client Impersonation and Delegation](client-impersonation-and-delegation.md).</span></span>

## <a name="testing-security-functionality"></a><span data-ttu-id="9eb7b-119">Testen von Sicherheitsfunktionen</span><span class="sxs-lookup"><span data-stu-id="9eb7b-119">Testing Security Functionality</span></span>

<span data-ttu-id="9eb7b-120">Wenn Sie in Ihrer Komponente die programmgesteuerte com+-Sicherheit verwenden, müssen Sie die Komponente in eine COM+-Anwendung integrieren, wenn Sie bereit sind, die Sicherheitsfunktionen der Komponente zu testen.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-120">If you use COM+ programmatic security in your component, you must integrate the component into a COM+ application when you are ready to test the component's security functionality.</span></span> <span data-ttu-id="9eb7b-121">Wenn eine Komponente, die die programmgesteuerte com+-Sicherheit verwendet, ohne Integration in eine COM+-Anwendung ausgeführt wird, werden Ausnahmen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-121">If a component using COM+ programmatic security is run without being integrated into a COM+ application, exceptions will be thrown.</span></span> <span data-ttu-id="9eb7b-122">Wenn Sie also sicherstellen möchten, dass eine solche Komponente auch erfolgreich in eine Anwendung integriert werden kann, die nicht Teil der com+-Umgebung ist, müssen Sie sicherstellen, dass diese Ausnahmen ordnungsgemäß behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-122">Therefore, if you want to ensure that such a component is also capable of being successfully integrated into an application that is not part of the COM+ environment, you must ensure that these exceptions are handled appropriately.</span></span>

## <a name="documenting-security-requirements"></a><span data-ttu-id="9eb7b-123">Dokumentieren von Sicherheitsanforderungen</span><span class="sxs-lookup"><span data-stu-id="9eb7b-123">Documenting Security Requirements</span></span>

<span data-ttu-id="9eb7b-124">Wenn Sie eine eigenständige Komponente für COM+-Anwendungen schreiben, die rollenbasierte Sicherheit verwenden, müssen Sie die Komponente dokumentieren, damit die Sicherheit entsprechend konfiguriert werden kann, wenn die Komponente in eine COM+-Anwendung integriert ist.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-124">If you are writing a stand-alone component for COM+ applications that use role-based security, you need to document the component so that security can be configured appropriately when the component is integrated into a COM+ application.</span></span> <span data-ttu-id="9eb7b-125">Sie sollten z. b. die Rollen ermitteln, die hinzugefügt werden müssen, und erläutern, welchen Methoden und Schnittstellen die einzelnen Rollen zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-125">For example, you should identify the roles that must be added and explain which methods and interfaces each role should be assigned to.</span></span> <span data-ttu-id="9eb7b-126">Außerdem sollten Sie, wenn eine Methode wie isCallerInRole ("Teller") aufgerufen wird, die Funktionalität beschreiben, auf die nur der Kassierer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-126">In addition, if a method such as IsCallerInRole("Teller") is called, you should describe the functionality that only Tellers have access to.</span></span> <span data-ttu-id="9eb7b-127">Außerdem sollten Sie angeben, ob eine Rolle erforderlich ist, um den Zugriff auf die gesamte Komponente zu schützen.</span><span class="sxs-lookup"><span data-stu-id="9eb7b-127">You should also specify whether a role is required to help protect access to the entire component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9eb7b-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9eb7b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eb7b-129">Clientauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="9eb7b-129">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="9eb7b-130">Client Identitätswechsel und Delegierung</span><span class="sxs-lookup"><span data-stu-id="9eb7b-130">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="9eb7b-131">Sicherheit der Bibliothek Anwendungen</span><span class="sxs-lookup"><span data-stu-id="9eb7b-131">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="9eb7b-132">Multi-Tier-Anwendungssicherheit</span><span class="sxs-lookup"><span data-stu-id="9eb7b-132">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="9eb7b-133">Rollenbasierte Sicherheitsverwaltung</span><span class="sxs-lookup"><span data-stu-id="9eb7b-133">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="9eb7b-134">Verwenden der Richtlinie für Software Einschränkung in com+</span><span class="sxs-lookup"><span data-stu-id="9eb7b-134">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
