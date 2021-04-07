---
title: Löschen von Benutzern auf Mitglieds Servern und Windows 2000 Professional
description: In diesem Thema wird gezeigt, wie ein Benutzer von einem Mitglieds Server oder Computer, der unter Windows 2000 Professional ausgeführt wird, gelöscht wird.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- Benutzer AD, Löschen eines Benutzers auf Mitglieds Servern und Windows 2000 Professional
- Active Directory, verwenden von Benutzern, Löschen von Benutzern auf Mitglieds Servern und Windows 2000 Professional
- Löschen eines Benutzers
- Server, Löschen eines Benutzers
- Löschen von Benutzern auf Mitglieds Servern und Windows 2000 Professional AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae4287c8b7d32e15e7df3e73f365409d7fe49a0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038770"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="e3b34-108">Löschen von Benutzern auf Mitglieds Servern und Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e3b34-108">Deleting Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="e3b34-109">In diesem Thema wird gezeigt, wie ein Benutzer von einem Mitglieds Server oder Computer, der unter Windows 2000 Professional ausgeführt wird, gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="e3b34-109">This topic shows how to delete a user from a member server or computer running on Windows 2000 Professional.</span></span>

<span data-ttu-id="e3b34-110">**So löschen Sie einen Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e3b34-110">**To delete a user**</span></span>

1.  <span data-ttu-id="e3b34-111">Binden Sie den Computer mit den folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="e3b34-111">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="e3b34-112">Verwenden Sie ein Konto mit ausreichenden Rechten für den Zugriff auf diesen Computer.</span><span class="sxs-lookup"><span data-stu-id="e3b34-112">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="e3b34-113">Verwenden Sie das folgende Bindungs Zeichen folgen Format mit dem WinNT-Anbieter, dem Computernamen und einem zusätzlichen Parameter, um ADSI mitzuteilen, dass es an einen Computer gebunden ist: "Winnt:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="e3b34-113">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to tell ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="e3b34-114">Der &lt; Parameter "Computername &gt; " ist der Name des Computers, auf dessen Gruppen Sie zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="e3b34-114">The "&lt;computer name&gt;" parameter is the name of the computer whose groups you want to access.</span></span> <span data-ttu-id="e3b34-115">Dieser Parameter benachrichtigt ADSI, dass er an einen Computer gebunden ist, und ermöglicht es dem WinNT-Anbieter Parser, einige mehrdeutigkeits Auflösungs Abfragen zu überspringen, um zu bestimmen, an welchen Objekttyp Sie gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="e3b34-115">This parameter notifies ADSI that it is binding to a computer and allows the WinNT provider parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="e3b34-116">Binden an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e3b34-116">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="e3b34-117">Geben Sie "User" mithilfe von " [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) " als Klasse an, um den Benutzer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e3b34-117">Specify "user" as the class using [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) to delete the user.</span></span>

    <span data-ttu-id="e3b34-118">Beachten Sie, dass Sie [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) nicht zum Commit der Änderung an den Container anrufen müssen.</span><span class="sxs-lookup"><span data-stu-id="e3b34-118">Be aware that you do not need to call [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the change to the container.</span></span> <span data-ttu-id="e3b34-119">Der [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) -Befehl führt einen Commit für das Löschen des Benutzers direkt zum Verzeichnis aus.</span><span class="sxs-lookup"><span data-stu-id="e3b34-119">The [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) call commits the deletion of the user directly to the directory.</span></span>

 

 