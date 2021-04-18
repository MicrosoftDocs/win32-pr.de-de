---
description: Mit dem Verwaltungs Programmkomponenten Dienste können Sie eine Rolle mit Benutzerkonten oder Gruppen auffüllen.
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: Zuweisen eines Benutzerkontos oder einer Gruppe zu einer Rolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53b37c9f0265e02c7abdf74eeaf81bd0b12e3d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338918"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a><span data-ttu-id="51eb1-103">Zuweisen eines Benutzerkontos oder einer Gruppe zu einer Rolle</span><span class="sxs-lookup"><span data-stu-id="51eb1-103">Assigning a User Account or Group to a Role</span></span>

<span data-ttu-id="51eb1-104">Mit dem Verwaltungs Programmkomponenten Dienste können Sie eine Rolle mit Benutzerkonten oder Gruppen auffüllen.</span><span class="sxs-lookup"><span data-stu-id="51eb1-104">You can use the Component Services administrative tool to populate a role with user accounts or groups.</span></span> <span data-ttu-id="51eb1-105">Die bevorzugte Methode zum Zuweisen eines Benutzerkontos zu einer Rolle besteht darin, das Benutzerkonto einer Gruppe zuzuweisen und die Gruppe dann der Rolle zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="51eb1-105">The preferred way to assign a user account to a role is to assign the user account to a group and then assign the group to the role.</span></span> <span data-ttu-id="51eb1-106">Die Verwendung von Gruppen zum Auffüllen von Rollen erleichtert Ihnen die Verwaltung einer großen Anzahl von Benutzern.</span><span class="sxs-lookup"><span data-stu-id="51eb1-106">Using groups to populate roles makes it easier for you to manage large numbers of users.</span></span> <span data-ttu-id="51eb1-107">Weitere Informationen zum Erstellen von Gruppen oder Zuweisen eines Benutzerkontos zu einer Gruppe finden Sie in der Online Hilfe für das Verwaltungs Tool "Computer Verwaltung" im Thema "lokale Benutzer und Gruppen".</span><span class="sxs-lookup"><span data-stu-id="51eb1-107">In the online help for the Computer Management administrative tool, see the topic "Local Users and Groups" for more information about creating groups or assigning a user account to a group.</span></span>

> [!Note]  
> <span data-ttu-id="51eb1-108">Damit nicht authentifizierte Netzwerk Benutzer eine COM+-Anwendung ausführen können, müssen die Anwendungs Rollen den anonymen Benutzer einschließen.</span><span class="sxs-lookup"><span data-stu-id="51eb1-108">To allow unauthenticated network users to run a COM+ application, the application roles must include the Anonymous user.</span></span> <span data-ttu-id="51eb1-109">Ab Windows Server 2003 ist der anonyme Benutzer standardmäßig nicht in der Gruppe "jeder" enthalten.</span><span class="sxs-lookup"><span data-stu-id="51eb1-109">Starting with Windows Server 2003, by default, the Anonymous user is not included in the Everyone group.</span></span>

 

<span data-ttu-id="51eb1-110">Nachdem Sie das Benutzerkonto der entsprechenden Windows-Gruppe zugewiesen haben, führen Sie die folgenden Schritte aus, um die Windows-Gruppe der Rolle zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="51eb1-110">After you have assigned the user account to the appropriate Windows group, follow these steps to assign the Windows group to the role.</span></span>

<span data-ttu-id="51eb1-111">**So weisen Sie einer Sicherheitsrolle eine Windows-Gruppe zu**</span><span class="sxs-lookup"><span data-stu-id="51eb1-111">**To assign a Windows group to a security role**</span></span>

1.  <span data-ttu-id="51eb1-112">Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Anwendung, die die Rolle enthält, der Sie das Benutzerkonto oder die Gruppe hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="51eb1-112">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="51eb1-113">Erweitern Sie die Ansicht in der Konsolen Struktur, bis die Rollen der Anwendung sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="51eb1-113">Expand the view in the console tree until the application's roles are visible.</span></span>

2.  <span data-ttu-id="51eb1-114">Suchen Sie die Rolle, der Sie das Benutzerkonto oder die Gruppe hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="51eb1-114">Locate the role to which you want to add the user account or group.</span></span>

    > [!Note]  
    > <span data-ttu-id="51eb1-115">Wenn sich die gesuchte Rolle nicht im Ordner " **Rollen** " befindet, wurde die Rolle der Anwendung nicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="51eb1-115">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="51eb1-116">Sie muss der Anwendung vom Entwickler hinzugefügt werden, bevor Sie der Rolle Benutzerkonten zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="51eb1-116">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

     

3.  <span data-ttu-id="51eb1-117">Klicken Sie mit der rechten Maustaste auf den Ordner **Benutzer** in der Rolle, zeigen Sie auf **neu**, und klicken Sie dann auf **Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="51eb1-117">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

4.  <span data-ttu-id="51eb1-118">Geben Sie im Fenster **Benutzer oder Gruppen auswählen** im unteren Bereich den voll qualifizierten Namen des Benutzers oder der Gruppe ein, den bzw. die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="51eb1-118">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="51eb1-119">Wenn Sie den Namen nicht kennen, klicken Sie auf die Schaltfläche **erweitert** , und klicken Sie dann auf **Jetzt suchen** , um eine Liste der Benutzer und Gruppen in der ausgewählten Domäne anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="51eb1-119">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="51eb1-120">Wählen Sie einen Benutzer oder eine Gruppe aus der Liste **Name (RDN)** aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="51eb1-120">Select a user or group from the **Name (RDN)** list, and click **OK**.</span></span>

5.  <span data-ttu-id="51eb1-121">Wenn Sie weitere Benutzerkonten oder Gruppen hinzufügen möchten, wiederholen Sie Schritt 4.</span><span class="sxs-lookup"><span data-stu-id="51eb1-121">To add more user accounts or groups, repeat step 4.</span></span>

6.  <span data-ttu-id="51eb1-122">Wenn Sie das Hinzufügen von Benutzerkonten und Gruppen zur Rolle abgeschlossen haben, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="51eb1-122">When you have finished adding user accounts and groups to the role, click **OK**.</span></span>

<span data-ttu-id="51eb1-123">Für jedes Benutzerkonto oder jede Gruppe, das Sie der Rolle zugewiesen haben, wird im Ordner **Benutzer** ein Symbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51eb1-123">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span> <span data-ttu-id="51eb1-124">Die neue Rollen Mitgliedschaft tritt beim nächsten Start der Anwendung in Kraft.</span><span class="sxs-lookup"><span data-stu-id="51eb1-124">The new role membership takes effect the next time the application is started.</span></span>

 

 



