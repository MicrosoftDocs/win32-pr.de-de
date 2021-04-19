---
description: Wenn ein Prozess versucht, auf ein Sicherungs fähiges Objekt zuzugreifen, durchläuft das System die Zugriffs Steuerungs Einträge (ACEs) in der Zugriffs Steuerungs Liste für Objekte (DACL), bis es ACEs findet, die den angeforderten Zugriff zulassen oder verweigern.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Reihenfolge von ACEs in einer DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc45d6fd286bb06bd4311a8a02010c68832735ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359154"
---
# <a name="order-of-aces-in-a-dacl"></a><span data-ttu-id="2f12e-103">Reihenfolge von ACEs in einer DACL</span><span class="sxs-lookup"><span data-stu-id="2f12e-103">Order of ACEs in a DACL</span></span>

<span data-ttu-id="2f12e-104">Wenn ein [*Prozess*](/windows/desktop/SecGloss/p-gly) versucht, auf ein Sicherungs fähiges Objekt zuzugreifen, durchläuft das System die [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) in der freigegebenen [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) des Objekts, bis es ACEs findet, die den angeforderten Zugriff zulassen oder verweigern.</span><span class="sxs-lookup"><span data-stu-id="2f12e-104">When a [*process*](/windows/desktop/SecGloss/p-gly) tries to access a securable object, the system steps through the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) in the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) until it finds ACEs that allow or deny the requested access.</span></span> <span data-ttu-id="2f12e-105">Die Zugriffsrechte, die eine DACL einem Benutzer ermöglicht, können abhängig von der Reihenfolge der ACEs in der DACL variieren.</span><span class="sxs-lookup"><span data-stu-id="2f12e-105">The access rights that a DACL allows a user could vary depending on the order of ACEs in the DACL.</span></span> <span data-ttu-id="2f12e-106">Folglich definiert das Betriebssystem Windows XP eine bevorzugte Reihenfolge für ACEs in der DACL eines Sicherungs fähigen Objekts.</span><span class="sxs-lookup"><span data-stu-id="2f12e-106">Consequently, the Windows XP operating system defines a preferred order for ACEs in the DACL of a securable object.</span></span> <span data-ttu-id="2f12e-107">Die bevorzugte Reihenfolge bietet ein einfaches Framework, mit dem sichergestellt wird, dass der Zugriff verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="2f12e-107">The preferred order provides a simple framework that ensures that an access-denied ACE actually denies access.</span></span> <span data-ttu-id="2f12e-108">Weitere Informationen zum Algorithmus des Systems zum Überprüfen des Zugriffs finden [Sie Untersteuern des Zugriffs auf ein Objekt durch DACLs](how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="2f12e-108">For more information about the system's algorithm for checking access, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="2f12e-109">Für Windows Server 2003 und Windows XP ist die richtige Reihenfolge von ACEs durch die Einführung von Objekt spezifischen ACEs und automatischer Vererbung kompliziert.</span><span class="sxs-lookup"><span data-stu-id="2f12e-109">For Windows Server 2003 and Windows XP, the proper order of ACEs is complicated by the introduction of object-specific ACEs and automatic inheritance.</span></span>

<span data-ttu-id="2f12e-110">In den folgenden Schritten wird die bevorzugte Reihenfolge beschrieben:</span><span class="sxs-lookup"><span data-stu-id="2f12e-110">The following steps describe the preferred order:</span></span>

1.  <span data-ttu-id="2f12e-111">Alle expliziten ACEs werden in einer Gruppe vor allen geerbten ACEs platziert.</span><span class="sxs-lookup"><span data-stu-id="2f12e-111">All explicit ACEs are placed in a group before any inherited ACEs.</span></span>
2.  <span data-ttu-id="2f12e-112">Innerhalb der Gruppe von expliziten ACEs werden Zugriffs Verweigerungs-ACEs vor Zugriffs zulässigen ACEs platziert.</span><span class="sxs-lookup"><span data-stu-id="2f12e-112">Within the group of explicit ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>
3.  <span data-ttu-id="2f12e-113">Geerbte ACEs werden in der Reihenfolge abgelegt, in der Sie geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="2f12e-113">Inherited ACEs are placed in the order in which they are inherited.</span></span> <span data-ttu-id="2f12e-114">ACEs, die vom übergeordneten Element des untergeordneten Objekts geerbt werden, werden zuerst angezeigt, dann ACEs, die vom übergeordneten Element geerbt wurden, usw., die Struktur von Objekten.</span><span class="sxs-lookup"><span data-stu-id="2f12e-114">ACEs inherited from the child object's parent come first, then ACEs inherited from the grandparent, and so on up the tree of objects.</span></span>
4.  <span data-ttu-id="2f12e-115">Für jede Ebene der geerbten ACEs werden Zugriffs Verweigerungs-ACEs vor Zugriffs zulässigen ACEs platziert.</span><span class="sxs-lookup"><span data-stu-id="2f12e-115">For each level of inherited ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>

<span data-ttu-id="2f12e-116">Natürlich sind nicht alle ACE-Typen in einer ACL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2f12e-116">Of course, not all ACE types are required in an ACL.</span></span>

<span data-ttu-id="2f12e-117">Funktionen wie [**addaccesszuwedaceex**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) und [**addaccesszuwedobjectace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) fügen am Ende einer ACL einen ACE hinzu.</span><span class="sxs-lookup"><span data-stu-id="2f12e-117">Functions such as [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) and [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) add an ACE to the end of an ACL.</span></span> <span data-ttu-id="2f12e-118">Es liegt in der Verantwortung des Aufrufers, sicherzustellen, dass die ACEs in der richtigen Reihenfolge hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2f12e-118">It is the caller's responsibility to ensure that the ACEs are added in the proper order.</span></span>

 

 
