---
title: Erstellen von lokalen Gruppen
description: Für Mitglieds Server und Windows 2000 Professional können nur lokale Gruppen erstellt werden.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Erstellen von lokalen Gruppen Ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705902b0066913fcd6eed56ba7c74e299144595f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314637"
---
# <a name="creating-local-groups"></a><span data-ttu-id="9611f-104">Erstellen von lokalen Gruppen</span><span class="sxs-lookup"><span data-stu-id="9611f-104">Creating Local Groups</span></span>

<span data-ttu-id="9611f-105">Für Mitglieds Server und Windows 2000 Professional können nur lokale Gruppen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9611f-105">Only local groups can be created for member servers and Windows 2000 Professional.</span></span>

<span data-ttu-id="9611f-106">**So erstellen Sie eine lokale Gruppe für einen Mitglieds Server oder Computer, auf dem Windows 2000 Professional ausgeführt wird**</span><span class="sxs-lookup"><span data-stu-id="9611f-106">**To create a local group for a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="9611f-107">Binden Sie den Computer mit den folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="9611f-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="9611f-108">Verwenden Sie ein Konto mit ausreichenden Rechten für den Zugriff auf diesen Computer.</span><span class="sxs-lookup"><span data-stu-id="9611f-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="9611f-109">Verwenden Sie das folgende Bindungs Zeichen folgen Format mit dem WinNT-Anbieter, dem Computernamen und einem zusätzlichen Parameter, um ADSI anzuweisen, dass es an einen Computer gebunden ist: "Winnt:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="9611f-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="9611f-110">Der &lt; Parameter "Computername &gt; " ist der Name der Computer Gruppen, auf die zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9611f-110">The "&lt;computer name&gt;" parameter is the name of the computer groups to access.</span></span>

        <span data-ttu-id="9611f-111">Der Parameter "Computer" weist ADSI in der Bindungs Zeichenfolge &lt; &gt; an, dass er an einen Computer gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="9611f-111">In the binding string, the "&lt;computer&gt;" parameter instructs ADSI that it is binding to a computer.</span></span> <span data-ttu-id="9611f-112">ADSI stellt diese Daten dem Parser des WinNT-Anbieters zur Verfügung, sodass er einige mehrdeutigkeits Auflösungs Abfragen überspringen kann, um zu bestimmen, an welchen Objekttyp Sie gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="9611f-112">ADSI makes this data available to the WinNT provider's parser so that it can skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="9611f-113">Binden an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9611f-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="9611f-114">Geben Sie "localgroup" als Klasse an, indem Sie [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) verwenden, um die Gruppe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9611f-114">Specify "localGroup" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the group.</span></span>
    > [!Note]  
    > <span data-ttu-id="9611f-115">Wenn Sie "Group" als Klasse angeben, wird von ADSI "localgroup" verwendet.</span><span class="sxs-lookup"><span data-stu-id="9611f-115">If you specify "group" as the class, ADSI uses "localGroup".</span></span> <span data-ttu-id="9611f-116">Geben Sie die Klasse nicht als "globalgroup" an.</span><span class="sxs-lookup"><span data-stu-id="9611f-116">Do not specify the class as "globalGroup".</span></span> <span data-ttu-id="9611f-117">Gruppen der Klasse "globalgroup" können nicht auf Mitglieds Servern oder einem Computer erstellt werden, auf dem Windows NT Workstation/Windows 2000 Professional ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9611f-117">Groups of class "globalGroup" cannot be created on member servers or a computer running Windows NT Workstation/Windows 2000 Professional.</span></span> <span data-ttu-id="9611f-118">Wenn Sie "globalgroup" angeben, erstellt [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) die Gruppe im Eigenschaften Cache, [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) schreibt die Gruppe jedoch nicht in die Sicherheitsdatenbank und gibt keinen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9611f-118">If you specify "globalGroup", [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) creates the group in the property cache, but [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) does not write the group to the security database and it does not return an error.</span></span>

     

3.  <span data-ttu-id="9611f-119">Schreiben Sie die Gruppe mithilfe von " [**IADs. \* tinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)" in die Computer Sicherheitsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="9611f-119">Write the group to the computer security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 