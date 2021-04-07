---
title: Auflisten von Benutzern auf Mitglieds Servern und Windows 2000 Professional
description: In diesem Thema wird gezeigt, wie alle Benutzer in einer lokalen Sicherheitsdatenbank auf Mitglieds Servern und Computern, die unter Windows 2000 Professional ausgeführt werden, aufgelistet werden.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- Auflisten von Benutzern auf Mitglieds Servern und Windows 2000 Professional AD
- Benutzer AD, Auflisten von Benutzern auf Mitglieds Servern und Windows 2000 Professional
- Active Directory, verwenden von Benutzern, Auflisten von Benutzern auf Mitglieds Servern und Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664af51b7feb2e0b9a683664659eefda11c9cb9d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724552"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="5c7cf-106">Auflisten von Benutzern auf Mitglieds Servern und Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5c7cf-106">Enumerating Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="5c7cf-107">In diesem Thema wird gezeigt, wie alle Benutzer in einer lokalen Sicherheitsdatenbank auf Mitglieds Servern und Computern, die unter Windows 2000 Professional ausgeführt werden, aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="5c7cf-107">This topic shows how to enumerate all users, in a local security database, on member servers and computers running on Windows 2000 Professional.</span></span>

<span data-ttu-id="5c7cf-108">**So zählen Sie die Benutzer auf**</span><span class="sxs-lookup"><span data-stu-id="5c7cf-108">**To enumerate the users**</span></span>

1.  <span data-ttu-id="5c7cf-109">Binden Sie den Computer mit den folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="5c7cf-109">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="5c7cf-110">Verwenden Sie ein Konto, das über ausreichende Rechte für den Zugriff auf den Computer verfügt.</span><span class="sxs-lookup"><span data-stu-id="5c7cf-110">Use an account that has sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="5c7cf-111">Verwenden Sie das folgende Bindungs Zeichen folgen Format mit dem WinNT-Anbieter, dem Computernamen und einem zusätzlichen Parameter, um ADSI anzuweisen, dass es an einen Computer gebunden ist: "Winnt:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="5c7cf-111">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="5c7cf-112">Der &lt; Parameter "Computername &gt; " ist der Name des Computers, auf dessen Gruppen zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c7cf-112">The "&lt;computer name&gt;" parameter is the name of the computer for whose groups to access.</span></span> <span data-ttu-id="5c7cf-113">Dieser Parameter weist ADSI an, dass er an einen Computer gebunden wird, und ermöglicht es dem WinNT-Anbieter Parser, einige mehrdeutigkeits Auflösungs Abfragen zu überspringen, um zu bestimmen, an welchen Objekttyp Sie gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="5c7cf-113">This parameter instructs ADSI that it is binding to a computer and enables the WinNT provider parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="5c7cf-114">Binden an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5c7cf-114">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="5c7cf-115">Fügen Sie "User" der Eigenschaft " [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) " hinzu.</span><span class="sxs-lookup"><span data-stu-id="5c7cf-115">Add "user" to the [**IADsContainer.Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) property.</span></span> <span data-ttu-id="5c7cf-116">Dies bewirkt, dass die Enumeration nur Objekte enthält, die über die Objektklasse "User" verfügen.</span><span class="sxs-lookup"><span data-stu-id="5c7cf-116">This causes the enumeration to only contain objects that have the "user" object class.</span></span>
3.  <span data-ttu-id="5c7cf-117">Listet die Objekte auf.</span><span class="sxs-lookup"><span data-stu-id="5c7cf-117">Enumerate the objects.</span></span> <span data-ttu-id="5c7cf-118">Verwenden Sie für jedes Benutzerobjekt die [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -oder [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) -Schnittstellen Methoden, um die Benutzereigenschaften zu lesen.</span><span class="sxs-lookup"><span data-stu-id="5c7cf-118">For each user object, use the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) interface methods to read the user properties.</span></span>

 

 