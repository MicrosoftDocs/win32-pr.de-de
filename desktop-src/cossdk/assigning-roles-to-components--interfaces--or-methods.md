---
description: Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5efb66c9de865cbfcdc6e9cb047af92c95f6bc0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393142"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a><span data-ttu-id="959d3-103">Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden</span><span class="sxs-lookup"><span data-stu-id="959d3-103">Assigning Roles to Components, Interfaces, or Methods</span></span>

<span data-ttu-id="959d3-104">Sie können einem beliebigen Element innerhalb einer COM+-Anwendung, die über das Verwaltungs Programmkomponenten Dienste sichtbar ist, explizit eine Rolle zuweisen.</span><span class="sxs-lookup"><span data-stu-id="959d3-104">You can explicitly assign a role to any item within a COM+ application that is visible through the Component Services administrative tool.</span></span> <span data-ttu-id="959d3-105">Dadurch wird sichergestellt, dass alle Benutzer, die Mitglieder der Rolle sind, Zugriff auf dieses Element und alle anderen darin enthaltenen Elemente erhalten.</span><span class="sxs-lookup"><span data-stu-id="959d3-105">Doing so ensures that any users that are members of the role will be permitted access to that item and any other items that it contains.</span></span> <span data-ttu-id="959d3-106">Wenn Sie z. b. die Rolle "Reader" einer Komponente zuweisen, wird jedem Mitglied von "Readers" der Zugriff auf diese Komponente und alle von ihr verfügbar gemachten Schnittstellen und Methoden gestattet.</span><span class="sxs-lookup"><span data-stu-id="959d3-106">For example, if you assign the role "Readers" to a component, any member of "Readers" is allowed access to that component and any interfaces and methods it exposes.</span></span> <span data-ttu-id="959d3-107">"Readers" wird als geerbte Rolle für diese Schnittstellen und Methoden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="959d3-107">"Readers" will show up as an Inherited role for any of those interfaces and methods.</span></span>

<span data-ttu-id="959d3-108">Aufrufer können nur von Aufrufern aufgerufen werden, indem Sie Ihr eine Rolle zuweisen, indem Sie die Rolle entweder direkt der-Methode zuweisen oder der-Schnittstelle der Methode oder der-Komponente der Methode eine Rolle zuweisen. in diesem Fall wird die Rolle von der-Methode geerbt.</span><span class="sxs-lookup"><span data-stu-id="959d3-108">A method is accessible to callers only if you assign a role to it, either by explicitly assigning the role directly to the method or by assigning a role to the method's interface or the method's component, in which case the role will be inherited by the method.</span></span> <span data-ttu-id="959d3-109">Wenn keine Rolle zugewiesen ist und Zugriffs Überprüfungen aktiviert sind, schlagen alle Aufrufe der-Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="959d3-109">If no role is assigned and if access checks are enabled, all calls to the method will fail.</span></span>

<span data-ttu-id="959d3-110">Bevor Sie eine Rolle zuweisen können, müssen Sie Sie für die Anwendung [definieren](defining-roles-for-an-application.md) .</span><span class="sxs-lookup"><span data-stu-id="959d3-110">Before you can assign a role, you must [define](defining-roles-for-an-application.md) it for the application.</span></span> <span data-ttu-id="959d3-111">Alle für die Anwendung definierten Rollen werden im Fenster für **ausgewählte Elemente explizit** auf der Registerkarte **Sicherheit** für alle Komponenten, Methoden und Schnittstellen in der Anwendung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="959d3-111">All roles defined for the application will appear in the **Roles explicitly set for selected item(s)** window on the **Security** tab for any components, methods, and interfaces within the application.</span></span>

<span data-ttu-id="959d3-112">**So weisen Sie einer Komponente, Methode oder Schnittstelle Rollen zu**</span><span class="sxs-lookup"><span data-stu-id="959d3-112">**To assign roles to a component, method, or interface**</span></span>

1.  <span data-ttu-id="959d3-113">Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Anwendung, für die die Rolle definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="959d3-113">In the console tree of the Component Services administrative tool, locate the COM+ application for which the role has been defined.</span></span> <span data-ttu-id="959d3-114">Erweitern Sie die Struktur, um die Komponenten, Schnittstellen oder Methoden der Anwendung anzuzeigen, je nachdem, welchen Sie die Rolle zuweisen.</span><span class="sxs-lookup"><span data-stu-id="959d3-114">Expand the tree to view the application's components, interfaces, or methods, depending on what you are assigning the role to.</span></span>

2.  <span data-ttu-id="959d3-115">Klicken Sie mit der rechten Maustaste auf das Element, dem Sie die Rolle zuweisen möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="959d3-115">Right-click the item to which you want to assign the role, and then click **Properties**.</span></span>

3.  <span data-ttu-id="959d3-116">Klicken Sie im Dialogfeld Eigenschaften auf die Registerkarte **Sicherheit** .</span><span class="sxs-lookup"><span data-stu-id="959d3-116">In the properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="959d3-117">Wählen Sie im Feld **explizit für ausgewählte Element (e) festgelegte Rollen** die Rollen aus, die Sie dem Element zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="959d3-117">In the **Roles explicitly set for selected item(s)** box, select the roles that you want to assign to the item.</span></span>

5.  <span data-ttu-id="959d3-118">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="959d3-118">Click **OK**.</span></span>

<span data-ttu-id="959d3-119">Alle Rollen, die Sie explizit für ein Element festgelegt haben, werden von den darin enthaltenen Elementen auf niedrigerer Ebene geerbt und in den Rollen angezeigt, die **vom ausgewählten Element (en)** für diese Elemente geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="959d3-119">Any roles that you have explicitly set for an item will be inherited by any lower-level items it contains and will show up in the **Roles inherited by selected item(s)** window for those items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="959d3-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="959d3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="959d3-121">Konfigurieren von Role-Based Sicherheit</span><span class="sxs-lookup"><span data-stu-id="959d3-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="959d3-122">Definieren von Rollen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="959d3-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="959d3-123">Aktivieren von Zugriffs Überprüfungen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="959d3-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="959d3-124">Aktivieren von Zugriffs Überprüfungen auf Komponentenebene</span><span class="sxs-lookup"><span data-stu-id="959d3-124">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="959d3-125">Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="959d3-125">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



