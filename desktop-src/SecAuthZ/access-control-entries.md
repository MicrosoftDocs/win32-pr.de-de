---
description: Ein Zugriffs Steuerungs Eintrag (ACE) ist ein Element in einer Zugriffs Steuerungs Liste (Access Control List, ACL).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Access Control Einträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fe98cf1c1c4d5fb23091a6539564ff964202cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356112"
---
# <a name="access-control-entries"></a><span data-ttu-id="813c9-103">Access Control Einträge</span><span class="sxs-lookup"><span data-stu-id="813c9-103">Access Control Entries</span></span>

<span data-ttu-id="813c9-104">Ein [*Zugriffs Steuerungs Eintrag*](/windows/desktop/SecGloss/a-gly) (ACE) ist ein Element in einer [*Zugriffs Steuerungs Liste (Access Control List*](/windows/desktop/SecGloss/a-gly) , ACL).</span><span class="sxs-lookup"><span data-stu-id="813c9-104">An [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) is an element in an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL).</span></span> <span data-ttu-id="813c9-105">Eine ACL kann NULL oder mehr ACEs enthalten.</span><span class="sxs-lookup"><span data-stu-id="813c9-105">An ACL can have zero or more ACEs.</span></span> <span data-ttu-id="813c9-106">Jeder ACE steuert oder überwacht den Zugriff auf ein Objekt durch einen angegebenen Vertrauens nehmer.</span><span class="sxs-lookup"><span data-stu-id="813c9-106">Each ACE controls or monitors access to an object by a specified trustee.</span></span> <span data-ttu-id="813c9-107">Weitere Informationen zum Hinzufügen, entfernen oder Ändern von ACEs in den ACLs eines Objekts finden Sie unter [Ändern der ACLs eines Objekts in C++](modifying-the-acls-of-an-object-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="813c9-107">For information about adding, removing, or changing the ACEs in an object's ACLs, see [Modifying the ACLs of an Object in C++](modifying-the-acls-of-an-object-in-c--.md).</span></span>

<span data-ttu-id="813c9-108">Es gibt sechs Typen von ACEs, von denen drei von allen Sicherungs fähigen Objekten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="813c9-108">There are six types of ACEs, three of which are supported by all securable objects.</span></span> <span data-ttu-id="813c9-109">Die anderen drei Typen sind [objektspezifische ACEs](object-specific-aces.md) , die von Verzeichnisdienst Objekten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="813c9-109">The other three types are [Object-specific ACEs](object-specific-aces.md) supported by directory service objects.</span></span>

<span data-ttu-id="813c9-110">Alle Arten von ACEs enthalten die folgenden Zugriffs Steuerungsinformationen:</span><span class="sxs-lookup"><span data-stu-id="813c9-110">All types of ACEs contain the following access control information:</span></span>

-   <span data-ttu-id="813c9-111">Eine [Sicherheits](security-identifiers.md) -ID (SID), die [den Vertrauens nehmer identifiziert, für](trustees.md) den der ACE gilt.</span><span class="sxs-lookup"><span data-stu-id="813c9-111">A [security identifier](security-identifiers.md) (SID) that identifies the [trustee](trustees.md) to which the ACE applies.</span></span>
-   <span data-ttu-id="813c9-112">Eine [*Zugriffs Maske*](/windows/desktop/SecGloss/a-gly) , die die vom ACE kontrollierten [Zugriffsrechte](access-rights-and-access-masks.md) angibt.</span><span class="sxs-lookup"><span data-stu-id="813c9-112">An [*access mask*](/windows/desktop/SecGloss/a-gly) that specifies the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span>
-   <span data-ttu-id="813c9-113">Ein Flag, das den Typ des ACE angibt.</span><span class="sxs-lookup"><span data-stu-id="813c9-113">A flag that indicates the type of ACE.</span></span>
-   <span data-ttu-id="813c9-114">Ein Satz von Bitflags, die bestimmen, ob untergeordnete Container oder Objekte den ACE von dem primären Objekt erben können, an das die ACL angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="813c9-114">A set of bit flags that determine whether child containers or objects can inherit the ACE from the primary object to which the ACL is attached.</span></span>

<span data-ttu-id="813c9-115">In der folgenden Tabelle werden die drei ACE-Typen aufgelistet, die von allen Sicherungs fähigen Objekten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="813c9-115">The following table lists the three ACE types supported by all securable objects.</span></span>



| <span data-ttu-id="813c9-116">type</span><span class="sxs-lookup"><span data-stu-id="813c9-116">Type</span></span>               | <span data-ttu-id="813c9-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="813c9-117">Description</span></span>                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="813c9-118">Ace "Zugriff verweigert"</span><span class="sxs-lookup"><span data-stu-id="813c9-118">Access-denied ACE</span></span>  | <span data-ttu-id="813c9-119">Wird in einer freigegebenen [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) verwendet, um Zugriffsrechte für einen Vertrauens nehmer zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="813c9-119">Used in a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) to deny access rights to a trustee.</span></span>                                       |
| <span data-ttu-id="813c9-120">Zugriffs zulässiger ACE</span><span class="sxs-lookup"><span data-stu-id="813c9-120">Access-allowed ACE</span></span> | <span data-ttu-id="813c9-121">Wird in einer DACL verwendet, um Zugriffsrechte für einen Vertrauens nehmer zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="813c9-121">Used in a DACL to allow access rights to a trustee.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="813c9-122">System Überwachungs ACE</span><span class="sxs-lookup"><span data-stu-id="813c9-122">System-audit ACE</span></span>   | <span data-ttu-id="813c9-123">Wird in einer [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) verwendet, um einen Überwachungsdaten Satz zu generieren, wenn der Treuhänder versucht, die angegebenen Zugriffsrechte auszuüben.</span><span class="sxs-lookup"><span data-stu-id="813c9-123">Used in a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL) to generate an audit record when the trustee attempts to exercise the specified access rights.</span></span> |



 

<span data-ttu-id="813c9-124">Eine Tabelle mit Objekt spezifischen ACEs finden Sie unter [Object-Specific ACEs](object-specific-aces.md).</span><span class="sxs-lookup"><span data-stu-id="813c9-124">For a table of object-specific ACEs, see [Object-specific ACEs](object-specific-aces.md).</span></span>

> [!Note]  
> <span data-ttu-id="813c9-125">System-Wecker-Objekt-ACEs werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="813c9-125">System-alarm object ACEs are not currently supported.</span></span>

 

 

 
