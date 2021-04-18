---
description: Eine neue COM+-Anwendung wird erstellt.
ms.assetid: eec4e871-36c2-4e60-9808-1400efcfc60c
title: Eine neue COM+-Anwendung wird erstellt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09eb296ad0a5f2326b5d931f59a5075d001d89f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344002"
---
# <a name="creating-a-new-com-application"></a><span data-ttu-id="d0eab-103">Eine neue COM+-Anwendung wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="d0eab-103">Creating a New COM+ Application</span></span>

<span data-ttu-id="d0eab-104">Zum Erstellen einer neuen COM+-Anwendung sind zwei grundlegende Schritte erforderlich:</span><span class="sxs-lookup"><span data-stu-id="d0eab-104">Creating a new COM+ application requires two basic steps, as follows:</span></span>

-   <span data-ttu-id="d0eab-105">Erstellen einer leeren COM+-Anwendung (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="d0eab-105">Creating an empty COM+ application (described below).</span></span>
-   <span data-ttu-id="d0eab-106">Hinzufügen von Komponenten zur Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d0eab-106">Adding components to the application.</span></span> <span data-ttu-id="d0eab-107">(Weitere Informationen finden Sie unter [Installieren neuer Komponenten](installing-new-components.md) und [Importieren von Komponenten](importing-components.md).)</span><span class="sxs-lookup"><span data-stu-id="d0eab-107">(See [Installing New Components](installing-new-components.md) and [Importing Components](importing-components.md).)</span></span>

<span data-ttu-id="d0eab-108">**So erstellen Sie eine leere com+-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="d0eab-108">**To create an empty COM+ application**</span></span>

1.  <span data-ttu-id="d0eab-109">Wählen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste den Computer aus, auf dem Sie eine Anwendung erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="d0eab-109">In the console tree of the Component Services administrative tool, select the computer on which you want to create an application.</span></span>

2.  <span data-ttu-id="d0eab-110">Wählen Sie den Ordner **com+-Anwendungen** für diesen Computer aus.</span><span class="sxs-lookup"><span data-stu-id="d0eab-110">Select the **COM+ Applications** folder for that computer.</span></span>

3.  <span data-ttu-id="d0eab-111">Zeigen Sie im Menü **Aktion** auf **neu**, und klicken Sie dann auf **Anwendung**.</span><span class="sxs-lookup"><span data-stu-id="d0eab-111">On the **Action** menu, point to **New**, and then click **Application**.</span></span> <span data-ttu-id="d0eab-112">Sie können auch mit der rechten Maustaste auf den Ordner **com+-Anwendungen** , zeigen Sie auf **neu**, und klicken Sie dann auf **Anwendung**.</span><span class="sxs-lookup"><span data-stu-id="d0eab-112">You can also right-click the **COM+ Applications** folder, point to **New**, and then click **Application**.</span></span>

4.  <span data-ttu-id="d0eab-113">Klicken Sie auf der **Willkommens** Seite des COM+-Anwendungsinstallations-Assistenten auf **weiter**, und klicken Sie dann im Dialogfeld **neue Anwendung installieren oder erstellen** auf **leere Anwendung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="d0eab-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Install or Create a New Application** dialog box, click **Create an empty application**.</span></span>

5.  <span data-ttu-id="d0eab-114">Geben Sie in das bereitgestellte Feld einen Namen für die neue Anwendung ein.</span><span class="sxs-lookup"><span data-stu-id="d0eab-114">In the box provided, type a name for the new application.</span></span> <span data-ttu-id="d0eab-115">(Beachten Sie, dass die folgenden Sonderzeichen nicht in einem Anwendungsnamen verwendet werden können: \\ ,/, ~,!, @, \# ,%, ^, &, \* , (,), \| ,}, {, \] , \[ , ', ', >, <,.,?,:, und;.) Klicken Sie unter **Aktivierungstyp** auf **Bibliotheks Anwendung** oder **Server Anwendung**.</span><span class="sxs-lookup"><span data-stu-id="d0eab-115">(Note that the following special characters cannot be used in an application name: \\, /, ~, !, @, \#, %, ^, &, \*, (, ), \|, }, {, \], \[, ', ", >, <, ., ?, :, and ;.) Under **Activation type**, click **Library application** or **Server application**.</span></span> <span data-ttu-id="d0eab-116">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="d0eab-116">Click **Next**.</span></span>

    > [!Note]  
    > <span data-ttu-id="d0eab-117">Eine Serveranwendung wird in einem eigenen Prozess ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0eab-117">A server application runs in its own process.</span></span> <span data-ttu-id="d0eab-118">Server Anwendungen können alle com+-Dienste unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d0eab-118">Server applications can support all COM+ services.</span></span> <span data-ttu-id="d0eab-119">Eine Bibliotheks Anwendung wird im Prozess des Clients ausgeführt, von dem Sie erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d0eab-119">A library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="d0eab-120">Bibliotheksanwendungen können rollenbasierte Sicherheit verwenden, aber keinen Remote Zugriff oder in die Warteschlange eingereihten Komponenten unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d0eab-120">Library applications can use role-based security but do not support remote access or queued components.</span></span>

     

6.  <span data-ttu-id="d0eab-121">Wählen Sie im Dialogfeld **Anwendungs Identität festlegen** eine Identität aus, unter der die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0eab-121">In the **Set Application Identity** dialog box, choose an identity under which the application will run.</span></span> <span data-ttu-id="d0eab-122">Wenn Sie **diesen Benutzer** auswählen, geben Sie den Benutzernamen und das Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="d0eab-122">If you select **This user**, type the user name and password.</span></span> <span data-ttu-id="d0eab-123">Außerdem müssen Sie das Kennwort erneut in das Feld **Kennwort bestätigen** eingeben.</span><span class="sxs-lookup"><span data-stu-id="d0eab-123">You must also retype the password in the **Confirm password** box.</span></span> <span data-ttu-id="d0eab-124">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="d0eab-124">Click **Next**.</span></span> <span data-ttu-id="d0eab-125">(Die Standardauswahl für Anwendungs Identität ist **interaktiver Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="d0eab-125">(The default selection for application identity is **Interactive User**.</span></span> <span data-ttu-id="d0eab-126">Der interaktive Benutzer ist der Benutzer, der zu einem beliebigen Zeitpunkt am Server Computer angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="d0eab-126">The interactive user is the user logged on to the server computer at any given time.</span></span> <span data-ttu-id="d0eab-127">Sie können einen anderen Benutzer auswählen, indem Sie **diesen Benutzer** auswählen und einen bestimmten Benutzer oder eine bestimmte Gruppe eingeben.)</span><span class="sxs-lookup"><span data-stu-id="d0eab-127">You can select a different user by selecting **This user** and entering a specific user or group.)</span></span>

    > [!Note]  
    > <span data-ttu-id="d0eab-128">Das Dialogfeld **Anwendungs Identität festlegen** wird nur angezeigt, wenn Sie im vorherigen Dialogfeld COM-Anwendungsinstallations-Assistent die Option **Server Anwendung** für den Aktivierungstyp der neuen Anwendung ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="d0eab-128">The **Set Application Identity** dialog box appears only if you selected **Server application** for the new application's activation type in the COM Application Install Wizard's preceding dialog box.</span></span> <span data-ttu-id="d0eab-129">Die Identity-Eigenschaft wird nicht für Bibliotheksanwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0eab-129">The identity property is not used for library applications.</span></span>

     

7.  <span data-ttu-id="d0eab-130">Fügen Sie im Dialogfeld **Anwendungs Rollen hinzufügen** alle Rollen hinzu, die Sie der Anwendung zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="d0eab-130">In the **Add Application Roles** dialog box, add any roles you want to associate with the application.</span></span> <span data-ttu-id="d0eab-131">Standardmäßig ist nur die Rolle " **kreatorowner** " definiert.</span><span class="sxs-lookup"><span data-stu-id="d0eab-131">By default, only the **CreatorOwner** role is defined.</span></span> <span data-ttu-id="d0eab-132">Weitere Informationen zu Rollen finden Sie unter [rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="d0eab-132">For information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

8.  <span data-ttu-id="d0eab-133">Füllen Sie im Dialogfeld **Benutzer zu Rollen hinzufügen** jede Rolle, die Sie im letzten Schritt erstellt haben, mit den Benutzern, Gruppen oder integrierten Sicherheits Prinzipale auf, denen Sie die Berechtigungen erteilen möchten, die dieser Rolle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d0eab-133">In the **Add Users to Roles** dialog box, populate each role you created in the last step with the users, groups, or built-in security principals to which you want to grant the privileges associated with that role.</span></span> <span data-ttu-id="d0eab-134">Standardmäßig wird der interaktive Benutzer in der Rolle "Administrator **Besitzer** " platziert.</span><span class="sxs-lookup"><span data-stu-id="d0eab-134">By default, the interactive user is placed in the **CreatorOwner** role.</span></span>

9.  <span data-ttu-id="d0eab-135">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="d0eab-135">Click **Finish**.</span></span>

<span data-ttu-id="d0eab-136">Die neue Anwendung wird jetzt unter dem Ordner **com+-Anwendungen** in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d0eab-136">The new application will now be displayed under the **COM+ Applications** folder in the console tree of the Component Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="d0eab-137">Ab Windows Server 2003 sind Zugriffs Überprüfungen beim Erstellen einer COM+-Anwendung standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d0eab-137">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="d0eab-138">In früheren Versionen wurden Zugriffs Überprüfungen standardmäßig auf Anwendungsebene deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d0eab-138">In previous versions, access checks were disabled by default at the application level.</span></span> <span data-ttu-id="d0eab-139">Das Ergebnis ist, dass der Zugriff auf eine COM+-Anwendung standardmäßig nur Benutzern gestattet wird, die sich in den Rollen befinden, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d0eab-139">The result is that by default, access to a COM+ application is allowed only to users that are in the roles associated with the application.</span></span> <span data-ttu-id="d0eab-140">(Siehe [rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md).) Alternativ können Sie den Zugriff auf alle Benutzer zulassen, indem Sie die Zugriffs Überprüfungen für eine COM+-Anwendung deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d0eab-140">(See [Role-Based Security Administration](role-based-security-administration.md).) Alternatively, you can allow access to all users by disabling access checks on a COM+ application.</span></span> <span data-ttu-id="d0eab-141">(Siehe [Aktivieren von Zugriffs Überprüfungen für eine Anwendung](enabling-access-checks-for-an-application.md).)</span><span class="sxs-lookup"><span data-stu-id="d0eab-141">(See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md).)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d0eab-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d0eab-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0eab-143">Kopieren von Komponenten</span><span class="sxs-lookup"><span data-stu-id="d0eab-143">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="d0eab-144">Eine COM+-Anwendung wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d0eab-144">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="d0eab-145">Importieren von Komponenten</span><span class="sxs-lookup"><span data-stu-id="d0eab-145">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="d0eab-146">Installieren neuer Komponenten</span><span class="sxs-lookup"><span data-stu-id="d0eab-146">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="d0eab-147">Verschieben von Komponenten</span><span class="sxs-lookup"><span data-stu-id="d0eab-147">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="d0eab-148">Entfernen einer Komponente aus einer COM+-Anwendung</span><span class="sxs-lookup"><span data-stu-id="d0eab-148">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



