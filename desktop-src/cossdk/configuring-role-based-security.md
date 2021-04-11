---
description: Wenn die COM+-Anwendung rollenbasierte Sicherheit verwendet, müssen mehrere Aufgaben abgeschlossen werden.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Konfigurieren von Role-Based Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eafa71430dfa13f497b0e4f7f7cea45229a422e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342139"
---
# <a name="configuring-role-based-security"></a><span data-ttu-id="b59a3-103">Konfigurieren von Role-Based Sicherheit</span><span class="sxs-lookup"><span data-stu-id="b59a3-103">Configuring Role-Based Security</span></span>

<span data-ttu-id="b59a3-104">Wenn die COM+-Anwendung rollenbasierte Sicherheit verwendet, müssen mehrere Aufgaben abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="b59a3-104">If your COM+ application uses role-based security, there are several tasks that need to be completed.</span></span> <span data-ttu-id="b59a3-105">Beim Entwerfen der Komponenten in Ihrer Anwendung definieren Sie die Rollen, die zum Schutz des Zugriffs auf diese Komponenten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b59a3-105">When designing the components in your application, you define the roles that are necessary to help protect access to those components.</span></span> <span data-ttu-id="b59a3-106">Außerdem entscheiden Sie, welche Rollen den Komponenten, Schnittstellen und Methoden der Anwendung zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b59a3-106">You also decide which roles to assign to the application's components, interfaces, and methods.</span></span> <span data-ttu-id="b59a3-107">Während der Anwendungsintegration verwenden Sie das Verwaltungs Programmkomponenten Dienste, um der Anwendung die definierten Rollen hinzuzufügen, und weisen die einzelnen Rollen den entsprechenden Komponenten, Schnittstellen und Methoden zu.</span><span class="sxs-lookup"><span data-stu-id="b59a3-107">During application integration, you use the Component Services administrative tool to add the defined roles to the application and assign each role to the appropriate components, interfaces, and methods.</span></span>

<span data-ttu-id="b59a3-108">Beim Konfigurieren der rollenbasierten Sicherheit führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="b59a3-108">In configuring role-based security, you perform the following steps:</span></span>

1.  <span data-ttu-id="b59a3-109">Aktivieren Sie Zugriffs Überprüfungen auf Anwendungsebene.</span><span class="sxs-lookup"><span data-stu-id="b59a3-109">Enable access checks at the application level.</span></span> <span data-ttu-id="b59a3-110">, Um die Sicherheitsüberprüfung für eine Anwendung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b59a3-110">To turn on security checking for an application.</span></span> <span data-ttu-id="b59a3-111">Ausführliche Informationen zum Ausführen dieses Schritts finden Sie unter [Aktivieren von Zugriffs Überprüfungen für eine Anwendung](enabling-access-checks-for-an-application.md) .</span><span class="sxs-lookup"><span data-stu-id="b59a3-111">See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md) for details on how to perform this step.</span></span>
2.  <span data-ttu-id="b59a3-112">Legen Sie die Sicherheitsstufe für Zugriffs Überprüfungen fest.</span><span class="sxs-lookup"><span data-stu-id="b59a3-112">Set security level for access checks.</span></span> <span data-ttu-id="b59a3-113">So legen Sie die Sicherheit entweder auf Prozess-, Prozess-und Komponentenebene fest</span><span class="sxs-lookup"><span data-stu-id="b59a3-113">To set security either at process or at process and component level.</span></span> <span data-ttu-id="b59a3-114">Ausführliche Informationen zum Ausführen dieses Schritts finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md) .</span><span class="sxs-lookup"><span data-stu-id="b59a3-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md) for details on how to perform this step.</span></span>
3.  <span data-ttu-id="b59a3-115">Aktivieren Sie Zugriffs Überprüfungen auf Komponentenebene.</span><span class="sxs-lookup"><span data-stu-id="b59a3-115">Enable access checks at the component level.</span></span> <span data-ttu-id="b59a3-116">Aktivieren der Sicherheitsüberprüfung auf der Komponenten-, Schnittstellen-und Methoden Ebene.</span><span class="sxs-lookup"><span data-stu-id="b59a3-116">To turn on security checking at the component, interface, and method levels.</span></span> <span data-ttu-id="b59a3-117">Ausführliche Informationen zum Ausführen dieses Schritts finden Sie [unter Aktivieren von Zugriffs Überprüfungen auf der Komponentenebene](enabling-access-checks-at-the-component-level.md) .</span><span class="sxs-lookup"><span data-stu-id="b59a3-117">See [Enabling Access Checks at the Component Level](enabling-access-checks-at-the-component-level.md) for details on how to perform this step.</span></span>
4.  <span data-ttu-id="b59a3-118">Definieren von Rollen für eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b59a3-118">Define roles for an application.</span></span> <span data-ttu-id="b59a3-119">Zum Erstellen von Rollen für eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b59a3-119">To create roles for an application.</span></span> <span data-ttu-id="b59a3-120">Ausführliche Informationen zum Ausführen dieses Schritts finden Sie unter [Definieren von Rollen für eine Anwendung](defining-roles-for-an-application.md) .</span><span class="sxs-lookup"><span data-stu-id="b59a3-120">See [Defining Roles for an Application](defining-roles-for-an-application.md) for details on how to perform this step.</span></span>
5.  <span data-ttu-id="b59a3-121">Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden.</span><span class="sxs-lookup"><span data-stu-id="b59a3-121">Assign roles to components, interfaces, or methods.</span></span> <span data-ttu-id="b59a3-122">Zum Zuweisen von Rollen zu bestimmten Ressourcen in einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b59a3-122">To assign roles to specific resources within an application.</span></span> <span data-ttu-id="b59a3-123">Ausführliche Informationen zum Ausführen dieses Schritts finden Sie unter [Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden](assigning-roles-to-components--interfaces--or-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="b59a3-123">See [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md) for details on how to perform this step.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b59a3-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b59a3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b59a3-125">Konfigurieren der Software Einschränkungs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b59a3-125">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="b59a3-126">Festlegen einer Identitätswechsel Ebene</span><span class="sxs-lookup"><span data-stu-id="b59a3-126">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 



