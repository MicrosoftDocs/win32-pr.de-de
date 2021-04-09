---
title: Delegierung
description: Die Delegierung ist eines der wichtigsten Sicherheitsfunktionen von Active Directory Domain Services.
ms.assetid: ab8740c9-f5a2-40cc-abce-0ef80c3fca7a
ms.tgt_platform: multiple
keywords:
- Delegierungs-AD
- Security AD, Delegierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26be1f9350c664d289832874994e2b3ba2e696c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947401"
---
# <a name="delegation"></a><span data-ttu-id="b68ee-105">Delegierung</span><span class="sxs-lookup"><span data-stu-id="b68ee-105">Delegation</span></span>

<span data-ttu-id="b68ee-106">Die *Delegierung* ist eines der wichtigsten Sicherheitsfunktionen von Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="b68ee-106">*Delegation* is one of the most important security features of Active Directory Domain Services.</span></span> <span data-ttu-id="b68ee-107">Durch die Delegierung können Administratoren und Gruppen bestimmte Administratorrechte für Container und Unterstrukturen erteilen.</span><span class="sxs-lookup"><span data-stu-id="b68ee-107">Delegation enables a higher administrative authority to grant specific administrative rights for containers and subtrees to individuals and groups.</span></span> <span data-ttu-id="b68ee-108">Domänen Administratoren, die weitreichende Berechtigungen für große Benutzer Segmente haben, sind nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b68ee-108">Domain administrators, with broad authority over large segments of users, are no longer required.</span></span>

<span data-ttu-id="b68ee-109">Ein ACE kann einem Benutzer oder einer Gruppe bestimmte Administratorrechte für die Objekte in einem Container erteilen.</span><span class="sxs-lookup"><span data-stu-id="b68ee-109">An ACE can grant specific administrative rights for the objects in a container to a user or group.</span></span> <span data-ttu-id="b68ee-110">Rechte werden für bestimmte Vorgänge für bestimmte Objektklassen mithilfe von ACEs in der ACL des Containers erteilt.</span><span class="sxs-lookup"><span data-stu-id="b68ee-110">Rights are granted for specific operations on specific object classes using ACEs in the container's ACL.</span></span> <span data-ttu-id="b68ee-111">Um z. b. einen Benutzer mit dem Namen "Benutzer 1" als Administrator der Organisationseinheit "Unternehmens Buchhaltungs" zu aktivieren, fügen Sie ACEs der ACL in "Unternehmens Buchhaltungs" wie folgt hinzu:</span><span class="sxs-lookup"><span data-stu-id="b68ee-111">For example, to enable a user named "user 1" to be an administrator of the "Corporate Accounting" organizational unit, add ACEs to the ACL on "Corporate Accounting" as follows:</span></span>

<span data-ttu-id="b68ee-112">"Benutzer 1"; Schusses Erstellen, ändern, löschen; objektklassenbenutzer "Benutzer 1"; Schusses Erstellen, ändern, löschen; Objektklassen Gruppe "Benutzer 1"; Schusses Schreiben; objektklassenbenutzer; Attribut Kennwort "</span><span class="sxs-lookup"><span data-stu-id="b68ee-112">""user 1";Grant ;Create, Modify, Delete;Object-Class User"user 1";Grant ;Create, Modify, Delete;Object-Class Group"user 1";Grant ;Write;Object-Class User; Attribute Password"</span></span>

<span data-ttu-id="b68ee-113">Jetzt kann Benutzer 1 neue Benutzer und Gruppen in der Unternehmens Rechnung erstellen und die Kenn Wörter für vorhandene Benutzer festlegen. Benutzer 1 kann jedoch keine anderen Objektklassen erstellen und kann sich nicht auf Benutzer in anderen Containern auswirken, es sei denn, Benutzer 1 erhält Zugriff durch ACEs in den anderen Containern.</span><span class="sxs-lookup"><span data-stu-id="b68ee-113">Now, user 1 can create new users and groups in Corporate Accounting and set the passwords on existing users, but user 1 cannot create any other object classes and cannot affect users in any other containers, unless, of course, user 1 is granted that access by ACEs on the other containers.</span></span>

 

 




