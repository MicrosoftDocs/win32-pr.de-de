---
description: Sie können Benutzerkonten oder Gruppen aus einer Rolle entfernen, wenn die Benutzer oder Mitglieder der Gruppen keinen Zugriff mehr auf die Anwendungs Ressourcen erhalten sollen, denen die Rolle zugewiesen ist.
ms.assetid: d2cfa5cb-a143-41de-9aa2-7af7fce10ed7
title: Verschieben eines Benutzerkontos oder einer Gruppe in eine andere Rolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2401d792066212269d4eaa4eb11eadfef6e2d73e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127405"
---
# <a name="moving-a-user-account-or-group-to-a-different-role"></a><span data-ttu-id="10d19-103">Verschieben eines Benutzerkontos oder einer Gruppe in eine andere Rolle</span><span class="sxs-lookup"><span data-stu-id="10d19-103">Moving a User Account or Group to a Different Role</span></span>

<span data-ttu-id="10d19-104">Sie können Benutzerkonten oder Gruppen aus einer Rolle entfernen, wenn die Benutzer oder Mitglieder der Gruppen keinen Zugriff mehr auf die Anwendungs Ressourcen erhalten sollen, denen die Rolle zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="10d19-104">You can remove user accounts or groups from a role when the users or members of the groups should no longer be given access to the application resources to which the role is assigned.</span></span>

<span data-ttu-id="10d19-105">**So entfernen Sie ein Benutzerkonto oder eine Gruppe aus einer Rolle**</span><span class="sxs-lookup"><span data-stu-id="10d19-105">**To remove a user account or group from a role**</span></span>

1.  <span data-ttu-id="10d19-106">Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Anwendung, die die Rolle enthält, an der Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="10d19-106">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="10d19-107">Erweitern Sie die Ansicht in der Konsolen Struktur, bis die Benutzer für die Rolle sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="10d19-107">Expand the view in the console tree until the users for the role are visible.</span></span>

2.  <span data-ttu-id="10d19-108">Klicken Sie mit der rechten Maustaste auf das Benutzerkonto oder die Gruppe, das Sie entfernen möchten, und klicken Sie auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="10d19-108">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

3.  <span data-ttu-id="10d19-109">Wenn Sie im Dialogfeld **delete Element DELETE** aufgefordert werden, klicken Sie auf **Ja** , um das Benutzerkonto oder die Gruppe zu löschen.</span><span class="sxs-lookup"><span data-stu-id="10d19-109">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

<span data-ttu-id="10d19-110">Das Benutzerkonto oder die Gruppe, das Sie aus der Rolle entfernt haben, wird nicht mehr im Ordner " **Benutzer** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="10d19-110">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span> <span data-ttu-id="10d19-111">Die neue Rollen Mitgliedschaft tritt beim nächsten Start der Anwendung in Kraft.</span><span class="sxs-lookup"><span data-stu-id="10d19-111">The new role membership takes effect the next time the application is started.</span></span> <span data-ttu-id="10d19-112">Wenn Sie Änderungen an der **System Anwendung** vorgenommen haben, müssen Sie den Computer neu starten, damit die Änderungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="10d19-112">If you have made changes to the **System Application**, you must restart the computer for the changes to take effect.</span></span>

 

 



