---
title: Steuern des Zugriffs auf Objekte und deren Eigenschaften
description: Um den Zugriff auf Anwendungs Objekte zu steuern, arbeiten Sie mit der Objekt Sicherheits Beschreibung und insbesondere mit der freigegebenen Zugriffs Steuerungs Liste (DACL) und der Liste der Zugriffs Steuerungs Einträge (ACEs).
ms.assetid: cfcb0998-4400-45cd-bbee-415d43b96a99
ms.tgt_platform: multiple
keywords:
- Objekt-AD, Steuern des Zugriffs auf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4534f383fa3747e0a53b402098f5a8338812c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206213"
---
# <a name="controlling-access-to-objects-and-their-properties"></a><span data-ttu-id="2b1fe-104">Steuern des Zugriffs auf Objekte und deren Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b1fe-104">Controlling Access to Objects and Their Properties</span></span>

<span data-ttu-id="2b1fe-105">Um den Zugriff auf Anwendungs Objekte zu steuern, arbeiten Sie mit der Objekt Sicherheits Beschreibung und insbesondere mit der freigegebenen Zugriffs Steuerungs Liste (DACL) und der Liste der Zugriffs Steuerungs Einträge (ACEs).</span><span class="sxs-lookup"><span data-stu-id="2b1fe-105">To control access to application objects, work with the object security descriptor, and specifically, with the discretionary access-control list (DACL) and its list of access-control entries (ACEs).</span></span>

<span data-ttu-id="2b1fe-106">Wenn ein Objekt erstellt wird, empfängt es eine Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-106">When an object is created, it receives a security descriptor.</span></span> <span data-ttu-id="2b1fe-107">Weitere Informationen und eine Beschreibung der Regeln, die das System verwendet, um die DACL für ein neues Objekt zu erstellen, finden Sie unter [Festlegen von Sicherheits Deskriptoren für neue Verzeichnisobjekte](how-security-descriptors-are-set-on-new-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2b1fe-107">For more information, and a description of the rules that the system uses to create the DACL for a new object, see [How Security Descriptors are Set on New Directory Objects](how-security-descriptors-are-set-on-new-directory-objects.md).</span></span> <span data-ttu-id="2b1fe-108">Diese Regeln zeigen, dass Sie folgende Aktionen ausführen können:</span><span class="sxs-lookup"><span data-stu-id="2b1fe-108">These rules reveal that you can:</span></span>

-   <span data-ttu-id="2b1fe-109">Erstellen Sie eine neue Sicherheits Beschreibung, und fügen Sie Sie zum Zeitpunkt der Erstellung an das Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-109">Create a new security descriptor and attach it to the object at creation time.</span></span> <span data-ttu-id="2b1fe-110">Weitere Informationen finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Verzeichnis Objekt](creating-a-security-descriptor-for-a-new-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="2b1fe-110">For more information, see [Creating a Security Descriptor for a New Directory Object](creating-a-security-descriptor-for-a-new-directory-object.md).</span></span>
-   <span data-ttu-id="2b1fe-111">Anwenden eines vererbbaren ACE an einem beliebigen Punkt in der Verzeichnishierarchie, sodass ein ACE von Objekten in der Struktur geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-111">Apply an inheritable ACE, at any point in the directory hierarchy, such that an ACE is inherited by objects down the tree.</span></span> <span data-ttu-id="2b1fe-112">Ein Objekt kann einen ACE von seinem übergeordneten Container erben.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-112">An object can inherit an ACE from its parent container.</span></span> <span data-ttu-id="2b1fe-113">Weitere Informationen finden Sie unter [Vererbung und Delegierung der Verwaltung](inheritance-and-delegation-of-administration.md).</span><span class="sxs-lookup"><span data-stu-id="2b1fe-113">For more information, see [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md).</span></span>
-   <span data-ttu-id="2b1fe-114">Geben Sie einen ACE in der standarddacl im Schema an, wenn Sie über die erforderlichen Zugriffsrechte verfügen.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-114">Specify an ACE in the default DACL in the schema, if you have the necessary access rights.</span></span> <span data-ttu-id="2b1fe-115">Jede Objektklassen Definition im Schema enthält eine Standard Sicherheits Beschreibung, die über eine standardmäßige DACL verfügen kann.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-115">Every object class definition in the schema includes a default security descriptor that can have a default DACL.</span></span> <span data-ttu-id="2b1fe-116">Weitere Informationen finden Sie unter [Standard Sicherheits Beschreibung](default-security-descriptor.md).</span><span class="sxs-lookup"><span data-stu-id="2b1fe-116">For more information, see [Default Security Descriptor](default-security-descriptor.md).</span></span>

<span data-ttu-id="2b1fe-117">Außerdem kann die DACL eines vorhandenen Objekts geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-117">In addition the DACL of an existing object can be modified.</span></span> <span data-ttu-id="2b1fe-118">Ihre Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="2b1fe-118">You can:</span></span>

-   <span data-ttu-id="2b1fe-119">Ersetzen Sie die DACL durch eine neue.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-119">Replace the DACL with a new one.</span></span>
-   <span data-ttu-id="2b1fe-120">Lesen Sie die vorhandene DACL, ändern Sie Sie, und wenden Sie die geänderte DACL an.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-120">Read the existing DACL, modify it, and apply the modified DACL.</span></span> <span data-ttu-id="2b1fe-121">Weitere Informationen finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="2b1fe-121">For more information, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="2b1fe-122">In der folgenden Liste wird die wichtigste Funktion eines ACE in Active Directory Domain Services beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-122">The following list describes the most important function of an ACE in Active Directory Domain Services.</span></span> <span data-ttu-id="2b1fe-123">Mit einem ACE haben Sie folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="2b1fe-123">With an ACE, you can:</span></span>

-   <span data-ttu-id="2b1fe-124">Steuern, wer bestimmte Vorgänge für ein Objekt ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-124">Control who can perform specific operations on an object.</span></span>
-   <span data-ttu-id="2b1fe-125">Steuern, wer Zugriff auf eine bestimmte Eigenschaft oder einen Satz von Eigenschaften für ein Objekt hat.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-125">Control who has access to a specific property, or set of properties, of an object.</span></span>
-   <span data-ttu-id="2b1fe-126">Steuern, wer untergeordnete Objekte in einem Container erstellen kann, einschließlich der Person, die einen bestimmten Typ von untergeordnetem Objekt erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-126">Control who can create child objects in a container, including who can create a specific type of child object.</span></span>
-   <span data-ttu-id="2b1fe-127">Definieren privater Zugriffsrechte für einen Objekttyp und Steuern, wer die durch die privaten Rechte geschützten Vorgänge ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-127">Define private control-access rights for an object type and control who can perform the operations protected by the private rights.</span></span>
-   <span data-ttu-id="2b1fe-128">Wenden Sie einen ACE auf ein Container Objekt am Stamm einer Verzeichnis Unterstruktur an, sodass der Schutz von allen untergeordneten Objekten in der Struktur automatisch geerbt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-128">Apply an ACE to a container object at the root of a directory subtree, such that the protections can be inherited automatically by all child objects down the tree.</span></span>
-   <span data-ttu-id="2b1fe-129">Anwenden eines ACE, der automatisch von einem bestimmten Typ eines untergeordneten Objekts in einer Unterstruktur geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-129">Apply an ACE that is inherited automatically by a specific type of child object in a subtree.</span></span>
-   <span data-ttu-id="2b1fe-130">Erstellen Sie einen ACE, der der Sicherheitsgruppe Rechte erteilt, nicht einem einzelnen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-130">Create an ACE that grants rights to a security group, rather than to a single user.</span></span>
-   <span data-ttu-id="2b1fe-131">Wenden Sie einen ACE auf Gruppenrichtlinie Objekte an, um die von der Richtlinie betroffenen Konten und Computer zu steuern.</span><span class="sxs-lookup"><span data-stu-id="2b1fe-131">Apply an ACE to Group Policy Objects to control the accounts and computers affected by the policy.</span></span>

 

 




