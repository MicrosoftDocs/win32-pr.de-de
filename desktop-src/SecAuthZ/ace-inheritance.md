---
description: Eine Objekt-ACL kann ACEs enthalten, die Sie von ihrem übergeordneten Container geerbt hat.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: ACE-Vererbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6462ed9523c94090924981db252b938f2056cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959484"
---
# <a name="ace-inheritance"></a><span data-ttu-id="cb7d5-103">ACE-Vererbung</span><span class="sxs-lookup"><span data-stu-id="cb7d5-103">ACE Inheritance</span></span>

<span data-ttu-id="cb7d5-104">Die ACL eines Objekts kann ACEs enthalten, die es von seinem übergeordneten Container geerbt hat.</span><span class="sxs-lookup"><span data-stu-id="cb7d5-104">An object's ACL can contain ACEs that it inherited from its parent container.</span></span> <span data-ttu-id="cb7d5-105">Beispielsweise kann ein Registrierungs Unterschlüssel ACEs von dem übergeordneten Schlüssel in der Registrierungs Hierarchie erben.</span><span class="sxs-lookup"><span data-stu-id="cb7d5-105">For example, a registry subkey can inherit ACEs from the key above it in the registry hierarchy.</span></span> <span data-ttu-id="cb7d5-106">Ebenso kann eine Datei in einem NTFS-Dateisystem ACEs von dem Verzeichnis erben, in dem Sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cb7d5-106">Likewise, a file in an NTFS file system can inherit ACEs from the directory that contains it.</span></span>

<span data-ttu-id="cb7d5-107">Die [**ACE- \_ Header**](/windows/desktop/api/Winnt/ns-winnt-ace_header) Struktur eines ACE enthält einen Satz von Vererbungsflags, die die ACE-Vererbung steuern, und die Auswirkung eines ACE auf das Objekt, an das Sie angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="cb7d5-107">The [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure of an ACE contains a set of inheritance flags that control ACE inheritance and the effect of an ACE on the object to which it is attached.</span></span> <span data-ttu-id="cb7d5-108">Das System interpretiert die Vererbungs Flags und andere Vererbungs Informationen gemäß den [Regeln für die ACE-Vererbung](ace-inheritance-rules.md).</span><span class="sxs-lookup"><span data-stu-id="cb7d5-108">The system interprets the inheritance flags and other inheritance information according to the [rules of ACE inheritance](ace-inheritance-rules.md).</span></span>

<span data-ttu-id="cb7d5-109">Diese Regeln wurden durch die folgenden Features erweitert:</span><span class="sxs-lookup"><span data-stu-id="cb7d5-109">These rules have been enhanced with the following features:</span></span>

-   <span data-ttu-id="cb7d5-110">Unterstützung für die [Automatische Propagierung von vererbbaren ACEs](automatic-propagation-of-inheritable-aces.md).</span><span class="sxs-lookup"><span data-stu-id="cb7d5-110">Support for [automatic propagation of inheritable ACEs](automatic-propagation-of-inheritable-aces.md).</span></span>
-   <span data-ttu-id="cb7d5-111">Ein Flag, das zwischen geerbten ACEs und ACEs unterscheidet, die direkt auf ein Objekt angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="cb7d5-111">A flag that differentiates between inherited ACEs and ACEs that were directly applied to an object.</span></span>
-   <span data-ttu-id="cb7d5-112">Objektspezifische ACEs, die es Ihnen ermöglichen, den Typ des untergeordneten Objekts anzugeben, das den ACE erben kann.</span><span class="sxs-lookup"><span data-stu-id="cb7d5-112">Object-specific ACEs that allow you to specify the type of child object that can inherit the ACE.</span></span>
-   <span data-ttu-id="cb7d5-113">Die Möglichkeit, zu verhindern, dass eine DACL oder SACL ACEs erbt, indem die von SE \_ DACL \_ geschützten oder SE \_ SACL \_ -geschützten Bits in den Steuerelementen der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) festgelegt werden, mit Ausnahme des System \_ Ressourcen \_ Attribut \_ ACE und der \_ Richtlinien-ID ACE für systemweite \_ Richtlinien \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cb7d5-113">The ability to prevent a DACL or SACL from inheriting ACEs by setting the SE\_DACL\_PROTECTED or SE\_SACL\_PROTECTED bits in the [*security descriptor's*](/windows/desktop/SecGloss/s-gly) control bits except for SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE and SYSTEM\_SCOPED\_POLICY\_ID\_ACE.</span></span>

 

 
