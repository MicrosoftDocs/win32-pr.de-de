---
title: Löschen von lokalen Gruppen
description: In diesem Thema wird gezeigt, wie Sie eine lokale Gruppe von einem Mitglieds Server oder Computer löschen, der unter Windows 2000 Professional ausgeführt wird.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Lokale Gruppen werden gelöscht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b55f90a8e6ac5cb77bf878d5ac680a6da91f73
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472604"
---
# <a name="deleting-local-groups"></a><span data-ttu-id="9526d-104">Löschen von lokalen Gruppen</span><span class="sxs-lookup"><span data-stu-id="9526d-104">Deleting Local Groups</span></span>

<span data-ttu-id="9526d-105">In diesem Thema wird gezeigt, wie Sie eine lokale Gruppe von einem Mitglieds Server oder Computer löschen, der unter Windows 2000 Professional ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9526d-105">This topic shows how to delete a local group from a member server or computer running on Windows 2000 Professional.</span></span>

<span data-ttu-id="9526d-106">**So löschen Sie eine lokale Gruppe**</span><span class="sxs-lookup"><span data-stu-id="9526d-106">**To delete a local group**</span></span>

1.  <span data-ttu-id="9526d-107">Binden Sie den Computer mit den folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="9526d-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="9526d-108">Verwenden Sie ein Konto mit ausreichenden Rechten für den Zugriff auf diesen Computer.</span><span class="sxs-lookup"><span data-stu-id="9526d-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="9526d-109">Verwenden Sie das folgende Bindungs Zeichen folgen Format mit dem WinNT-Anbieter, dem Computernamen und einem zusätzlichen Parameter, um ADSI anzuweisen, dass es an einen Computer gebunden ist: "Winnt:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="9526d-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="9526d-110">Der &lt; Parameter "Computername &gt; " ist der Name der Computergruppe, auf die zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9526d-110">The "&lt;computer name&gt;" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="9526d-111">Dieser Parameter weist ADSI an, dass er an einen Computer gebunden wird, und ermöglicht es dem Parser des WinNT-Anbieters, einige Abfragen zur mehrdeutigkeitsauflösung zu überspringen, um zu bestimmen, an welchen Objekttyp Sie gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="9526d-111">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="9526d-112">Binden an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9526d-112">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="9526d-113">Geben Sie "Group" als Klasse an, indem Sie [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)zum Löschen der Gruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="9526d-113">Specify "group" as the class using [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)to delete the group.</span></span>

    <span data-ttu-id="9526d-114">Sie müssen " [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) " nicht anrufen, um die Änderung im Container zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="9526d-114">You do not need to call [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the change to the container.</span></span> <span data-ttu-id="9526d-115">Der [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) -Befehl führt ein Commit für das Löschen der Gruppe direkt in das Verzeichnis aus.</span><span class="sxs-lookup"><span data-stu-id="9526d-115">The [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) call commits the deletion of the group directly to the directory.</span></span>

 

 