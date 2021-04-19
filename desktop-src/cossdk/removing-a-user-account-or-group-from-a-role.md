---
description: Wenn sich Benutzerberechtigungen ändern oder einer Anwendung Rollen hinzugefügt werden, können Sie ein Konto von einer Rolle in eine andere Rolle verschieben.
ms.assetid: 2d81a45a-9762-48b9-8395-3c3a4dcd5e8c
title: Entfernen eines Benutzerkontos oder einer Gruppe aus einer Rolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176272aef16af0d0a65d90f6a1d7628a5af232fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342612"
---
# <a name="removing-a-user-account-or-group-from-a-role"></a><span data-ttu-id="fb3eb-103">Entfernen eines Benutzerkontos oder einer Gruppe aus einer Rolle</span><span class="sxs-lookup"><span data-stu-id="fb3eb-103">Removing a User Account or Group from a Role</span></span>

<span data-ttu-id="fb3eb-104">Wenn die Berechtigungen eines Benutzers geändert werden oder einer Anwendung Rollen hinzugefügt werden, können Sie ein Konto von einer Rolle in eine andere Rolle verschieben.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-104">If a user's privileges change or if roles are added to an application, you can move an account from one role to another role.</span></span> <span data-ttu-id="fb3eb-105">Wenn Sie ein Benutzerkonto oder eine Gruppe von Benutzern von einer Rolle in eine andere verschieben möchten, müssen Sie das Benutzerkonto oder die Gruppe aus der aktuellen Rolle entfernen und dann der neuen Rolle zuweisen.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-105">To move a user account or group of users from one role to another, you must remove the user account or group from its current role and then assign it to the new role.</span></span>

<span data-ttu-id="fb3eb-106">**So verschieben Sie ein Benutzerkonto oder eine Gruppe von einer Rolle in eine andere**</span><span class="sxs-lookup"><span data-stu-id="fb3eb-106">**To move a user account or group from one role to another**</span></span>

1.  <span data-ttu-id="fb3eb-107">Entfernen Sie das Benutzerkonto oder die Gruppe aus der Rolle, der Sie nicht mehr angehören soll, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fb3eb-107">Remove the user account or group from the role that it should no longer belong to, as follows:</span></span>

    1.  <span data-ttu-id="fb3eb-108">Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Anwendung, die die Rolle enthält, an der Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-108">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="fb3eb-109">Erweitern Sie die Ansicht in der Konsolen Struktur, bis die Benutzer für die Rolle sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-109">Expand the view in the console tree until the users for the role are visible.</span></span>

    2.  <span data-ttu-id="fb3eb-110">Klicken Sie mit der rechten Maustaste auf das Benutzerkonto oder die Gruppe, das Sie entfernen möchten, und klicken Sie auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-110">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

    3.  <span data-ttu-id="fb3eb-111">Wenn Sie im Dialogfeld **delete Element DELETE** aufgefordert werden, klicken Sie auf **Ja** , um das Benutzerkonto oder die Gruppe zu löschen.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-111">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

    <span data-ttu-id="fb3eb-112">Das Benutzerkonto oder die Gruppe, das Sie aus der Rolle entfernt haben, wird nicht mehr im Ordner " **Benutzer** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-112">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span>

2.  <span data-ttu-id="fb3eb-113">Weisen Sie das Benutzerkonto oder die Gruppe, das Sie entfernt haben, den Rollen zu, denen der Benutzer oder die Gruppe zugewiesen werden soll. gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="fb3eb-113">Assign the user account or group you have removed to the roles that the user or group should be assigned to, as follows:</span></span>

    1.  <span data-ttu-id="fb3eb-114">Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Anwendung, die die Rolle enthält, der Sie das Benutzerkonto oder die Gruppe hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-114">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="fb3eb-115">Erweitern Sie die Ansicht in der Konsolen Struktur, bis die Rollen der Anwendung sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-115">Expand the view in the console tree until the application's roles are visible.</span></span>

    2.  <span data-ttu-id="fb3eb-116">Suchen Sie die Rolle, der Sie das Benutzerkonto oder die Gruppe hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-116">Locate the role to which you want to add the user account or group.</span></span>

        > [!Note]  
        > <span data-ttu-id="fb3eb-117">Wenn sich die gesuchte Rolle nicht im Ordner " **Rollen** " befindet, wurde die Rolle der Anwendung nicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-117">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="fb3eb-118">Sie muss der Anwendung vom Entwickler hinzugefügt werden, bevor Sie der Rolle Benutzerkonten zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-118">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

         

    3.  <span data-ttu-id="fb3eb-119">Klicken Sie mit der rechten Maustaste auf den Ordner **Benutzer** in der Rolle, zeigen Sie auf **neu**, und klicken Sie dann auf **Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-119">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

    4.  <span data-ttu-id="fb3eb-120">Geben Sie im Fenster **Benutzer oder Gruppen auswählen** im unteren Bereich den voll qualifizierten Namen des Benutzers oder der Gruppe ein, den bzw. die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-120">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="fb3eb-121">Wenn Sie den Namen nicht kennen, klicken Sie auf die Schaltfläche **erweitert** , und klicken Sie dann auf **Jetzt suchen** , um eine Liste der Benutzer und Gruppen in der ausgewählten Domäne anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-121">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="fb3eb-122">Wählen Sie einen Benutzer oder eine Gruppe aus der Liste **Name (RDN)** aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-122">Select a user or group from the **Name (RDN)** list and click **OK**.</span></span>

    5.  <span data-ttu-id="fb3eb-123">Wenn Sie das Benutzerkonto oder die Gruppe der Rolle hinzugefügt haben, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-123">When you have finished adding the user account or group to the role, click **OK**.</span></span>

    <span data-ttu-id="fb3eb-124">Für jedes Benutzerkonto oder jede Gruppe, das Sie der Rolle zugewiesen haben, wird im Ordner **Benutzer** ein Symbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-124">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span>

<span data-ttu-id="fb3eb-125">Die geänderte Rollen Mitgliedschaft für das Benutzerkonto oder die Gruppe tritt beim nächsten Start der Anwendung in Kraft.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-125">The changed role membership for the user account or group takes effect the next time the application is started.</span></span>

 

 



