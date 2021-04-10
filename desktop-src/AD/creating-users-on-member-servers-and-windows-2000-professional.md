---
title: Erstellen von Benutzern auf Mitglieds Servern und Windows 2000 Professional
description: In diesem Thema werden die Schritte beschrieben, die zum Erstellen eines Benutzers auf einem Mitglieds Server oder einem Computer mit Windows 2000 Professional verwendet werden.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- Erstellen von Benutzern auf Mitglieds Servern und Windows 2000 Professional AD
- Benutzer AD, Erstellen eines Benutzers auf Mitglieds Servern und Windows 2000 Professional
- Active Directory, verwenden von Benutzern, Erstellen eines Benutzers auf Mitglieds Servern und Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050c9e8ecf68465097f2c185d2d31e0195c25a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038778"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="20bfa-106">Erstellen von Benutzern auf Mitglieds Servern und Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="20bfa-106">Creating Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="20bfa-107">**So erstellen Sie einen Benutzer**</span><span class="sxs-lookup"><span data-stu-id="20bfa-107">**To create a user**</span></span>

1.  <span data-ttu-id="20bfa-108">Binden Sie den Computer mit den folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="20bfa-108">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="20bfa-109">Verwenden Sie ein Konto, das über ausreichende Rechte für den Zugriff auf den Computer verfügt.</span><span class="sxs-lookup"><span data-stu-id="20bfa-109">Use an account that has sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="20bfa-110">Verwenden Sie das folgende Bindungs Zeichen folgen Format mit dem WinNT-Anbieter, dem Computernamen und einem zusätzlichen Parameter, um ADSI mitzuteilen, dass es an einen Computer gebunden ist: "Winnt:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="20bfa-110">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to tell ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="20bfa-111">Der Computer &lt; Name &gt; ist der Name des Computers, auf dessen Gruppen Sie zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="20bfa-111">The "&lt;computer name&gt;" computer is the name of the computer whose groups you want to access.</span></span> <span data-ttu-id="20bfa-112">Mit diesem Parameter wird ADSI mitgeteilt, dass es an einen Computer gebunden ist. der Parser des WinNT-Anbieters kann einige mehrdeutigkeits Auflösungs Abfragen überspringen, um zu bestimmen, an welchen Objekttyp Sie gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="20bfa-112">This parameter tells ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="20bfa-113">Binden an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="20bfa-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="20bfa-114">Geben Sie "User" als Klasse an, indem Sie [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) verwenden, um den Benutzer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="20bfa-114">Specify "user" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the user.</span></span>
3.  <span data-ttu-id="20bfa-115">Schreiben Sie den Benutzer mithilfe von " [**IADs. \* tinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)" in die Sicherheitsdatenbank des Computers.</span><span class="sxs-lookup"><span data-stu-id="20bfa-115">Write the user to the computer's security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 