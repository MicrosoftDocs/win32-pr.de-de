---
title: Schützen von Objekten vor den Auswirkungen von geerbten rechten
description: Wie im Thema Vererbung und Delegierung der Verwaltung erläutert, kann ACEs für ein Container Objekt festgelegt werden, z. b. eine OrganizationalUnit, eine domainDNS, einen Container usw., und basierend auf den ACE-Flags, die für diese ACEs festgelegt wurden, an untergeordnete Objekte weitergegeben.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Schützen von Objekten vor den Auswirkungen von geerbten rechten AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e49991cd8a479e05b024c6ea2538783a843025
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038743"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a><span data-ttu-id="afb04-104">Schützen von Objekten vor den Auswirkungen von geerbten rechten</span><span class="sxs-lookup"><span data-stu-id="afb04-104">Protecting Objects from the Effects of Inherited Rights</span></span>

<span data-ttu-id="afb04-105">Wie im Thema [Vererbung und Delegierung der Verwaltung](inheritance-and-delegation-of-administration.md)erläutert, kann ACEs für ein Container Objekt festgelegt werden, z. b. eine **OrganizationalUnit**, eine **domainDns**, einen **Container** usw., und basierend auf den ACE-Flags, die für diese ACEs festgelegt wurden, an untergeordnete Objekte weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="afb04-105">As discussed in the topic [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md), ACEs can be set on a container object, such as an **organizationalUnit**, **domainDNS**, **container**, and so on, and propagated to child objects based on the ACE flags set on those ACEs.</span></span>

<span data-ttu-id="afb04-106">Wenn Sie über ein sicheres Objekt oder ein Objekt verfügen, dessen ACEs Sie explizit steuern möchten (z. b. eine private OE oder ein spezieller Benutzer), können Sie verhindern, dass ACEs über den übergeordneten Container oder die Vorgänger des übergeordneten Containers an das Objekt weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="afb04-106">If you have a secure object or an object whose ACEs you want to explicitly control, such as a private OU or a special user, you can prevent ACEs from being propagated to the object by its parent container or its parent container's predecessors.</span></span>

<span data-ttu-id="afb04-107">Verwenden Sie die Eigenschaft [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) , um zu steuern, ob DACLs und SACLs von dem Objekt von seinem übergeordneten Container geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="afb04-107">Use the [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property to control whether DACLs and SACLs are inherited by the object from its parent container.</span></span>

<span data-ttu-id="afb04-108">Die [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) -Eigenschaft kann verwendet werden, um ein Objekt vor den Auswirkungen von geerbten ACEs zu schützen.</span><span class="sxs-lookup"><span data-stu-id="afb04-108">The [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property can be used to protect an object from the effects of inherited ACEs.</span></span> <span data-ttu-id="afb04-109">Die folgenden Flags erzwingen, dass die Zugriffs Steuerung explizit für das-Objekt festgelegt wird, und verhindern, dass ein Benutzer die Zugriffs Steuerung für das Objekt ändert, indem vererbbare ACEs für den übergeordneten Container des Objekts oder die Vorgänger des übergeordneten Containers festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="afb04-109">The following flags force access control to be set explicitly on the object and prevent a user from modifying access control to the object by setting inheritable ACEs on the object's parent container, or its parent container's predecessors.</span></span>



| <span data-ttu-id="afb04-110">Flag</span><span class="sxs-lookup"><span data-stu-id="afb04-110">Flag</span></span>                               | <span data-ttu-id="afb04-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="afb04-111">Description</span></span>                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afb04-112">**SE \_ DACL \_ Protected**</span><span class="sxs-lookup"><span data-stu-id="afb04-112">**SE\_DACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="afb04-113">Verhindert, dass für die DACL des übergeordneten Containers festgelegte ACEs und alle Objekte oberhalb des übergeordneten Containers in der Verzeichnishierarchie auf die DACL des Objekts angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="afb04-113">Prevents ACEs set on the DACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object DACL.</span></span><br/> |
| <span data-ttu-id="afb04-114">**SE \_ SACL \_ Protected**</span><span class="sxs-lookup"><span data-stu-id="afb04-114">**SE\_SACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="afb04-115">Verhindert, dass für die SACL des übergeordneten Containers festgelegte ACEs und alle Objekte oberhalb des übergeordneten Containers in der Verzeichnishierarchie auf die SACL des Objekts angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="afb04-115">Prevents ACEs set on the SACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object SACL.</span></span><br/> |



 

<span data-ttu-id="afb04-116">Beachten Sie, dass das Flag für die **SE \_ DACL- \_ Darstellung** vorhanden sein muss, um die **SE \_ DACL- \_ geschützte** und **SE- \_ SACL \_** vorhanden zu **legen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="afb04-116">Be aware that the **SE\_DACL\_PRESENT** flag must be present to set **SE\_DACL\_PROTECTED** and **SE\_SACL\_PRESENT** must be present to set **SE\_SACL\_PROTECTED**.</span></span>

 

