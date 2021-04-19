---
description: Sie bestimmen eine Sicherheitsrichtlinie für eine Anwendung, indem Sie die erforderlichen Sicherheits Privilegien definieren.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Definieren von Rollen für eine Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e46eb2cb857a2b2dee2aabe41cb571e12ed98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342585"
---
# <a name="defining-roles-for-an-application"></a><span data-ttu-id="bd200-103">Definieren von Rollen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="bd200-103">Defining Roles for an Application</span></span>

<span data-ttu-id="bd200-104">Sie bestimmen eine Sicherheitsrichtlinie für eine Anwendung, indem Sie die erforderlichen Sicherheits Privilegien definieren.</span><span class="sxs-lookup"><span data-stu-id="bd200-104">You determine a security policy for an application by defining the security privileges that it requires.</span></span> <span data-ttu-id="bd200-105">Zu diesem Zweck deklarieren Sie eine symbolische Berechtigungsebene als Rolle – definieren Sie die Rolle für die Anwendung – und [weisen Sie die Rolle](assigning-roles-to-components--interfaces--or-methods.md) dann bestimmten Ressourcen innerhalb der Anwendung zu.</span><span class="sxs-lookup"><span data-stu-id="bd200-105">To do this you declare a symbolic level of privilege as a role—that is, define the role for the application—and then [assign the role](assigning-roles-to-components--interfaces--or-methods.md) to specific resources within the application.</span></span> <span data-ttu-id="bd200-106">Dieser Entwurf wird erfüllt, wenn die Anwendung bereitgestellt wird und Systemadministratoren die Rolle mit den tatsächlichen Benutzern und Benutzergruppen auffüllen.</span><span class="sxs-lookup"><span data-stu-id="bd200-106">This design is fulfilled when the application is deployed and system administrators populate the role with actual users and user groups.</span></span> <span data-ttu-id="bd200-107">Ausführlichere Informationen finden Sie unter [rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="bd200-107">For greater detail, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

<span data-ttu-id="bd200-108">**So fügen Sie einer Anwendung eine Rolle hinzu**</span><span class="sxs-lookup"><span data-stu-id="bd200-108">**To add a role to an application**</span></span>

1.  <span data-ttu-id="bd200-109">Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Anwendung, der Sie die Rolle hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="bd200-109">In the console tree of the Component Services administrative tool, locate the COM+ application to which you want to add the role.</span></span> <span data-ttu-id="bd200-110">Erweitern Sie die Struktur, um die Ordner für die Anwendung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bd200-110">Expand the tree to view the folders for the application.</span></span>

2.  <span data-ttu-id="bd200-111">Klicken Sie mit der rechten Maustaste auf den Ordner **Rollen** für die Anwendung, zeigen Sie auf **neu**, und klicken Sie dann auf **Rolle**.</span><span class="sxs-lookup"><span data-stu-id="bd200-111">Right-click the **Roles** folder for the application, point to **New**, and then click **Role**.</span></span>

3.  <span data-ttu-id="bd200-112">Geben Sie im Dialogfeld **Rolle** den Namen der neuen Rolle in das bereitgestellte Feld ein.</span><span class="sxs-lookup"><span data-stu-id="bd200-112">In the **Role** dialog box, type the name of the new role in the box provided.</span></span>

4.  <span data-ttu-id="bd200-113">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd200-113">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="bd200-114">Nachdem Sie der Anwendung Rollen hinzugefügt haben, müssen Sie sicherstellen, dass Sie die Rollen den entsprechenden Komponenten, Schnittstellen und Methoden zuweisen.</span><span class="sxs-lookup"><span data-stu-id="bd200-114">After adding roles to the application, you must be sure to assign the roles to the appropriate components, interfaces, and methods.</span></span> <span data-ttu-id="bd200-115">Andernfalls treten bei allen Aufrufen der Anwendung Fehler auf, wenn rollenbasierte Sicherheit ausgewählt und aktiviert wurde und Rollen hinzugefügt, aber nicht zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="bd200-115">Otherwise, if role-based security has been chosen and enabled and if roles have been added but not assigned, all calls to the application will fail.</span></span> <span data-ttu-id="bd200-116">Weitere Informationen finden Sie unter [Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden](assigning-roles-to-components--interfaces--or-methods.md).</span><span class="sxs-lookup"><span data-stu-id="bd200-116">For more information, see [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bd200-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bd200-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd200-118">Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden</span><span class="sxs-lookup"><span data-stu-id="bd200-118">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="bd200-119">Konfigurieren von Role-Based Sicherheit</span><span class="sxs-lookup"><span data-stu-id="bd200-119">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="bd200-120">Aktivieren von Zugriffs Überprüfungen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="bd200-120">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="bd200-121">Aktivieren von Zugriffs Überprüfungen auf Komponentenebene</span><span class="sxs-lookup"><span data-stu-id="bd200-121">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="bd200-122">Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="bd200-122">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



