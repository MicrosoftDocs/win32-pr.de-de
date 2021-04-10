---
title: Gruppen auf Mitglieds Servern und Windows 2000 Professional
description: Auf Mitglieds Servern und Computern, die unter Windows 2000 Professional ausgeführt werden, gibt es eine lokale Sicherheitsdatenbank.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- Gruppen auf Mitglieds Servern und Windows 2000 Professional AD
- Gruppen Ad, Gruppen auf Mitglieds Servern und Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530da03182d05764540a85f1c2529ced5877be5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309283"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="ea47d-105">Gruppen auf Mitglieds Servern und Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ea47d-105">Groups on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="ea47d-106">Auf Mitglieds Servern und Computern, die unter Windows 2000 Professional ausgeführt werden, gibt es eine lokale Sicherheitsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="ea47d-106">On member servers and computers running on Windows 2000 Professional, there is a local security database.</span></span> <span data-ttu-id="ea47d-107">Diese lokale Sicherheitsdatenbank kann eigene lokale Benutzer-und lokale Gruppen enthalten, deren Bereich nur dem Computer entspricht, auf dem Sie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ea47d-107">This local security database can contain its own local user and local groups whose scope is only the particular computer where they are created.</span></span> <span data-ttu-id="ea47d-108">Verwenden Sie den WinNT-Anbieter, wenn Sie diese Arten von Benutzern und Gruppen auf Mitglieds Servern und Computern verwalten, die auf Windows NT-Arbeitsstationen oder Windows 2000 Professional ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ea47d-108">When managing these types of users and groups on member servers and computers running on Windows NT Workstation or Windows 2000 Professional, use the WinNT provider.</span></span>

<span data-ttu-id="ea47d-109">Wenn ein Mitglieds Server oder ein Computer, auf dem Windows 2000 Professional oder Windows 2000 Professional ausgeführt wird, Mitglied einer Windows 2000-Domäne ist, können die Gruppen oder Benutzer in der Domäne in der lokalen Sicherheitsdatenbank verwendet werden, um der Gruppe auf dem betreffenden Computer Rechte zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="ea47d-109">When a member server or a computer running on Windows 2000 Professional or Windows 2000 Professional is a member of a Windows 2000 domain, the groups or users in the domain can be used in the local security database to grant rights to that group on that particular computer.</span></span>

<span data-ttu-id="ea47d-110">Verwenden Sie beim Verwalten von Gruppen in einer Windows 2000-Domäne mithilfe von ADSI den LDAP-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="ea47d-110">When managing groups on a Windows 2000 domain using ADSI, use the LDAP provider.</span></span> <span data-ttu-id="ea47d-111">Verwenden Sie den WinNT-Anbieter, wenn Sie Gruppen auf Mitglieds Servern und Computern verwalten, die auf der Windows NT-Arbeitsstation oder Windows 2000 Professional ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ea47d-111">When managing groups on member servers and computers running on Windows NT Workstation or Windows 2000 Professional, use the WinNT provider.</span></span>

<span data-ttu-id="ea47d-112">Sie müssen mindestens eine Instanz an jeden Anbieter binden: 1) binden Sie an den LDAP-Anbieter, um den ADsPath für die Gruppe oder den Benutzer abzurufen, die Sie einer Gruppe in der lokalen Datenbank hinzufügen möchten, und 2) binden an den WinNT-Anbieter, um diesen Benutzer bzw. diese Gruppe zu einer lokalen Gruppe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ea47d-112">You must bind, at least one instance, to each provider: 1) Bind to the LDAP provider to retrieve the ADsPath to the group or user you want to add to a group in the local database and 2) Bind to the WinNT provider to add that user or group to a local group.</span></span>

 

 




