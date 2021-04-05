---
title: Objekt-und Attribut Schutz
description: Eine Zugriffs Steuerungs Liste (Access Control List, ACL) schützt alle Objekte in Active Directory Domain Services.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Objekt-und Attribut Schutz
- Sicherheit AD, Objekt-und Attribut Schutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c046df35740f21f8706120ee6e11cfad1d4f626
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707595"
---
# <a name="object-and-attribute-protection"></a><span data-ttu-id="7b4fa-105">Objekt-und Attribut Schutz</span><span class="sxs-lookup"><span data-stu-id="7b4fa-105">Object and Attribute Protection</span></span>

<span data-ttu-id="7b4fa-106">Eine Zugriffs Steuerungs Liste (Access Control List, ACL) schützt alle Objekte in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="7b4fa-106">An access-control list (ACL) protects all objects in Active Directory Domain Services.</span></span> <span data-ttu-id="7b4fa-107">ACLs legen fest, wer das Objekt anzeigen kann, welche Attribute Sie lesen können und welche Aktionen die einzelnen Benutzer für das Objekt ausführen können.</span><span class="sxs-lookup"><span data-stu-id="7b4fa-107">ACLs determine who can view the object, what attributes they can read, and what actions each user can perform on the object.</span></span> <span data-ttu-id="7b4fa-108">Das vorhanden sein eines Objekts oder Attributs wird niemals einem nicht autorisierten Benutzer offengelegt.</span><span class="sxs-lookup"><span data-stu-id="7b4fa-108">The existence of an object or an attribute is never revealed to an unauthorized user.</span></span>

<span data-ttu-id="7b4fa-109">Eine ACL ist eine Liste von Zugriffs Steuerungs Einträgen (ACEs), die mit dem Objekt gespeichert werden, das Sie schützt.</span><span class="sxs-lookup"><span data-stu-id="7b4fa-109">An ACL is a list of access-control entries (ACEs) stored with the object that it protects.</span></span> <span data-ttu-id="7b4fa-110">In Windows NT und Windows 2000 wird eine ACL als ein binärer Wert, der als Sicherheits Beschreibung bezeichnet wird, gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7b4fa-110">In Windows NT and Windows 2000, an ACL is stored as a binary value, called a security descriptor.</span></span> <span data-ttu-id="7b4fa-111">Jeder ACE enthält eine Sicherheits-ID (SID), die den Prinzipal (Benutzer oder Gruppe) identifiziert, auf den der ACE angewendet wird, sowie Daten darüber, welche Art von Zugriff der ACE gewährt oder verweigert.</span><span class="sxs-lookup"><span data-stu-id="7b4fa-111">Each ACE contains a security identifier (SID), which identifies the principal (user or group) to whom the ACE applies, and data about what type of access the ACE grants or denies.</span></span>

<span data-ttu-id="7b4fa-112">ACLs für Verzeichnisobjekte enthalten ACEs, die auf das Objekt als Ganzes und ACEs angewendet werden, die für die einzelnen Attribute des Objekts gelten.</span><span class="sxs-lookup"><span data-stu-id="7b4fa-112">ACLs for directory objects contain ACEs that apply to the object as a whole and ACEs that apply to the individual attributes of the object.</span></span> <span data-ttu-id="7b4fa-113">Dies ermöglicht es einem Administrator, nicht nur zu steuern, welche Benutzer ein Objekt sehen können, sondern auch die Eigenschaften, die diese Benutzer anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="7b4fa-113">This allows an administrator to control not only which users can see an object, but also what properties those users can view.</span></span> <span data-ttu-id="7b4fa-114">Beispielsweise können allen Benutzern Lesezugriff auf die e-Mail-und Telefonnummern Attribute für alle anderen Benutzer gewährt werden, aber Sicherheitseigenschaften von Benutzern werden möglicherweise allen Mitgliedern einer speziellen Sicherheitsadministrator Gruppe verweigert.</span><span class="sxs-lookup"><span data-stu-id="7b4fa-114">For example, all users might be granted read access to the email and telephone number attributes for all other users, but security properties of users might be denied to all but members of a special security administrators group.</span></span> <span data-ttu-id="7b4fa-115">Einzelnen Benutzern können Schreibzugriff auf persönliche Attribute erteilt werden, z. b. Telefon-und Mailing Adressen für Ihre eigenen Benutzer Objekte.</span><span class="sxs-lookup"><span data-stu-id="7b4fa-115">Individual users might be granted write access to personal attributes such as the telephone and mailing addresses on their own user objects.</span></span>

 

 




