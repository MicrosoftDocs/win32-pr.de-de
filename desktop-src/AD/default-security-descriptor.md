---
title: Standard Sicherheits Beschreibung
description: Mit Active Directory Domain Services können Sie auch die Standard Sicherheit für jeden Objekttyp angeben.
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- Standard Sicherheits Beschreibung AD
- Sicherheits Deskriptoren, Standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372f285c3e8c17b481811d7356c40ae07316801d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038775"
---
# <a name="default-security-descriptor"></a><span data-ttu-id="ee971-105">Standard Sicherheits Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee971-105">Default Security Descriptor</span></span>

<span data-ttu-id="ee971-106">Mit Active Directory Domain Services können Sie auch die Standard Sicherheit für jeden Objekttyp angeben.</span><span class="sxs-lookup"><span data-stu-id="ee971-106">With Active Directory Domain Services, you can also specify default security for each type of object.</span></span> <span data-ttu-id="ee971-107">Dies wird im [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) -Attribut in der [**classSchema**](/windows/desktop/ADSchema/c-classschema) -Objektdefinition im [Active Directory Schema](active-directory-schema.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="ee971-107">This is specified in the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) attribute in the [**classSchema**](/windows/desktop/ADSchema/c-classschema) object definition in the [Active Directory schema](active-directory-schema.md).</span></span> <span data-ttu-id="ee971-108">Diese Sicherheits Beschreibung wird verwendet, um den Standardschutz für das Objekt bereitzustellen, wenn während der Erstellung des Objekts keine Sicherheits Beschreibung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ee971-108">This security descriptor is used to provide default protection on the object if there is no security descriptor specified during the creation of the object.</span></span>

> [!Note]  
> <span data-ttu-id="ee971-109">Aces von einer Standard Sicherheits Beschreibung werden so behandelt, als würden Sie als Teil der Objekt Erstellung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ee971-109">ACEs from a default security descriptor are handled as if they were specified as part of object creation.</span></span> <span data-ttu-id="ee971-110">Aus diesem Grund werden die standardaces vor geerbten ACEs abgelegt und Sie nach Bedarf überschrieben.</span><span class="sxs-lookup"><span data-stu-id="ee971-110">Therefore, the default ACEs are placed preceding inherited ACEs and override them as appropriate.</span></span> <span data-ttu-id="ee971-111">Weitere Informationen finden Sie unter [Reihenfolge von ACEs in einer DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="ee971-111">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="ee971-112">Der [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) wird in einem speziellen Zeichen folgen Format mithilfe der [Sicherheits Deskriptor-Definitions Sprache (Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) , SDDL) angegeben.</span><span class="sxs-lookup"><span data-stu-id="ee971-112">The [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) is specified in a special string format using the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span></span> <span data-ttu-id="ee971-113">Zwei Funktionen können verwendet werden, um die binäre Form der Sicherheits Beschreibung in das Zeichen folgen Format zu konvertieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="ee971-113">Two functions can be used to convert binary form of the security descriptor to string format and vice versa.</span></span> <span data-ttu-id="ee971-114">Dabei handelt es sich um diese Funktionen:</span><span class="sxs-lookup"><span data-stu-id="ee971-114">These functions are:</span></span>

-   [<span data-ttu-id="ee971-115">Convertsecuritydescriptortostringsecuritydescriptor</span><span class="sxs-lookup"><span data-stu-id="ee971-115">ConvertSecurityDescriptorToStringSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [<span data-ttu-id="ee971-116">Wurde von convertstringsecuritydescriptortosecuritydescriptor</span><span class="sxs-lookup"><span data-stu-id="ee971-116">ConvertStringSecurityDescriptorToSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

<span data-ttu-id="ee971-117">Weitere Informationen und die Standard Sicherheits Beschreibungen der vordefinierten Objektklassen finden Sie auf den Klassen Verweis Seiten im Active Directory Schema Verweis der [Active Directory Domain Services Referenz](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ee971-117">For more information and the default security descriptors of the predefined object classes, see the class reference pages in the Active Directory Schema Reference of the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

<span data-ttu-id="ee971-118">Weitere Informationen und ein Codebeispiel, das die [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) -Eigenschaft einer Objektklasse liest oder ändert, finden Sie unter [Lesen von defaultSecurityDescriptor für eine Objekt](reading-the-defaultsecuritydescriptor-for-an-object-class.md) Klasse und [Ändern von defaultSecurityDescriptor für eine Objektklasse](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).</span><span class="sxs-lookup"><span data-stu-id="ee971-118">For more information and a code example that reads or modifies the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) property of an object class, see [Reading the defaultSecurityDescriptor for an Object Class](reading-the-defaultsecuritydescriptor-for-an-object-class.md) and [Modifying the defaultSecurityDescriptor for an Object Class](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).</span></span>

 

 