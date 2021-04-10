---
description: Erläutert die Security Deskriptor Definition Language (SDDL).
ms.assetid: 2b15325e-34ed-497b-ae6d-3ec3ac168232
title: Definitions Sprache für Sicherheits Deskriptoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9de9d3535efe5c33ac633a9dbd295405d74b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863012"
---
# <a name="security-descriptor-definition-language"></a><span data-ttu-id="b4d6c-103">Definitions Sprache für Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="b4d6c-103">Security Descriptor Definition Language</span></span>

<span data-ttu-id="b4d6c-104">Die Security Deskriptor Definition Language (SDDL) definiert das Zeichen folgen Format, das von den Funktionen [**convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) verwendet wird, um eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) als Text Zeichenfolge zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b4d6c-104">The security descriptor definition language (SDDL) defines the string format that the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use to describe a [*security descriptor*](/windows/desktop/SecGloss/s-gly) as a text string.</span></span> <span data-ttu-id="b4d6c-105">Die Sprache definiert auch Zeichen folgen Elemente zum Beschreiben von Informationen in den Komponenten einer Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="b4d6c-105">The language also defines string elements for describing information in the components of a security descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="b4d6c-106">Bei bedingten [*Zugriffs Steuerungs Einträgen*](/windows/desktop/SecGloss/a-gly) (ACEs) handelt es sich um ein anderes SDDL-Format als bei anderen ACE-Typen.</span><span class="sxs-lookup"><span data-stu-id="b4d6c-106">Conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) have a different SDDL format than other ACE types.</span></span> <span data-ttu-id="b4d6c-107">Informationen zu ACEs finden Sie unter [ACE](ace-strings.md)-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="b4d6c-107">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="b4d6c-108">Informationen zu bedingten ACEs finden Sie unter [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="b4d6c-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b4d6c-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4d6c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4d6c-110">Format der Sicherheits Deskriptor-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b4d6c-110">Security Descriptor String Format</span></span>](security-descriptor-string-format.md)
</dt> <dt>

[<span data-ttu-id="b4d6c-111">Sicherheits Deskriptor-Definitions Sprache für bedingte ACEs</span><span class="sxs-lookup"><span data-stu-id="b4d6c-111">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="b4d6c-112">ACE-Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="b4d6c-112">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="b4d6c-113">SID-Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="b4d6c-113">SID Strings</span></span>](sid-strings.md)
</dt> <dt>

<span data-ttu-id="b4d6c-114">[\[MS-DYP \] : Beschreibung der Sicherheits Beschreibungssprache](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="b4d6c-114">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

 

 
