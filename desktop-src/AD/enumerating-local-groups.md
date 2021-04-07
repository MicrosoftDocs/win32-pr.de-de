---
title: Auflisten von lokalen Gruppen
description: Auf Mitglieds Servern und Computern, die unter Windows 2000 Professional ausgeführt werden, können Sie alle lokalen Gruppen auflisten.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Auflisten von lokalen Gruppen anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e106fc2517cfedd8fb5fa40e4b99798ee32de8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724553"
---
# <a name="enumerating-local-groups"></a><span data-ttu-id="9529c-104">Auflisten von lokalen Gruppen</span><span class="sxs-lookup"><span data-stu-id="9529c-104">Enumerating Local Groups</span></span>

<span data-ttu-id="9529c-105">Auf Mitglieds Servern und Computern, die unter Windows 2000 Professional ausgeführt werden, können Sie alle lokalen Gruppen auflisten.</span><span class="sxs-lookup"><span data-stu-id="9529c-105">On member servers and computers running on Windows 2000 Professional, you can enumerate all local groups.</span></span>

<span data-ttu-id="9529c-106">Auf Mitglieds Servern und Windows 2000 Professional können nur lokale Gruppen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9529c-106">Only local groups can be created on member servers and Windows 2000 Professional.</span></span> <span data-ttu-id="9529c-107">Diese lokalen Gruppen können jedoch Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="9529c-107">However, those local groups can contain:</span></span>

-   <span data-ttu-id="9529c-108">Universelle und globale Gruppen aus der Gesamtstruktur, die die Domäne enthält, der der Computer angehört.</span><span class="sxs-lookup"><span data-stu-id="9529c-108">Universal and Global groups from the forest that contains the domain to which the computer is a member.</span></span>
-   <span data-ttu-id="9529c-109">Lokale Domänen Gruppen aus der Domäne dieses Computers.</span><span class="sxs-lookup"><span data-stu-id="9529c-109">Domain local groups from that computer's domain.</span></span>
-   <span data-ttu-id="9529c-110">Benutzer aus einer beliebigen Domäne in der Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="9529c-110">Users from any domain in the forest.</span></span>

<span data-ttu-id="9529c-111">**So zählen Sie die lokalen Gruppen auf einem Mitglieds Server oder Computer auf, auf dem Windows 2000 Professional ausgeführt wird**</span><span class="sxs-lookup"><span data-stu-id="9529c-111">**To enumerate the local groups on a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="9529c-112">Binden Sie den Computer mit den folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="9529c-112">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="9529c-113">Verwenden Sie ein Konto mit ausreichenden Rechten für den Zugriff auf diesen Computer.</span><span class="sxs-lookup"><span data-stu-id="9529c-113">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="9529c-114">Verwenden Sie das folgende Bindungs Zeichen folgen Format mit dem WinNT-Anbieter, dem Computernamen und einem zusätzlichen Parameter, um ADSI anzuweisen, dass es an einen Computer gebunden ist: "Winnt:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="9529c-114">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="9529c-115">"Der <computer name> "-Parameter ist der Name der Computergruppe, auf die zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9529c-115">"The <computer name>" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="9529c-116">Dieser Parameter weist ADSI an, dass er an einen Computer gebunden wird, und ermöglicht es dem Parser des WinNT-Anbieters, einige Abfragen zur mehrdeutigkeitsauflösung zu überspringen, um zu bestimmen, an welchen Objekttyp Sie gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="9529c-116">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="9529c-117">Binden an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9529c-117">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="9529c-118">Legen Sie mithilfe der [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Eigenschaft einen Filter fest, der "Groups" enthält.</span><span class="sxs-lookup"><span data-stu-id="9529c-118">Set a filter that contains "groups" using the [**IADsContainer.Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) property.</span></span> <span data-ttu-id="9529c-119">Dies ermöglicht es Ihnen, den Container aufzuzählen und nur Gruppen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9529c-119">This enables you to enumerate the container and retrieve only groups.</span></span>
3.  <span data-ttu-id="9529c-120">Zählen Sie die Gruppen Objekte mithilfe der [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="9529c-120">Enumerate the group objects, using the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) method.</span></span>
4.  <span data-ttu-id="9529c-121">Verwenden Sie für jedes Group-Objekt die [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) -Schnittstelle, um den Namen und die Mitglieder der Gruppe zu lesen.</span><span class="sxs-lookup"><span data-stu-id="9529c-121">For each the group object, use the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface to read the name and members of the group.</span></span>

 

 