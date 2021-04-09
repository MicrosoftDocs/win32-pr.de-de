---
description: Eine gültige funktionale Sicherheits Beschreibung enthält Sicherheitsinformationen im Binärformat.
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: Sicherheitsbeschreibungerzeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb875bee4d35267b578193ca7cd08420722400a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129901"
---
# <a name="security-descriptor-strings"></a><span data-ttu-id="fca1c-103">Sicherheitsbeschreibungerzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="fca1c-103">Security Descriptor Strings</span></span>

<span data-ttu-id="fca1c-104">Eine gültige funktionale [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) enthält Sicherheitsinformationen im Binärformat.</span><span class="sxs-lookup"><span data-stu-id="fca1c-104">A valid functional [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains security information in binary format.</span></span> <span data-ttu-id="fca1c-105">Die Windows-API bietet Funktionen zum Umrechnen von binären Sicherheits Deskriptoren in und aus Text Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="fca1c-105">The Windows API provides functions for converting binary security descriptors to and from text strings.</span></span> <span data-ttu-id="fca1c-106">Sicherheits Deskriptoren im Zeichen folgen Format sind nicht funktionsfähig, aber Sie können zum Speichern oder Transportieren von Sicherheits Deskriptorinformationen hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="fca1c-106">Security descriptors in string format are not functional, but they can be useful for storing or transporting security descriptor information.</span></span>

<span data-ttu-id="fca1c-107">Um eine Sicherheits Beschreibung in ein Zeichen folgen Format zu konvertieren, wird die [**convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="fca1c-107">To convert a security descriptor to a string format, call the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) function.</span></span> <span data-ttu-id="fca1c-108">Um eine Sicherheits Beschreibung für das Zeichen folgen Format zurück in eine gültige funktionale Sicherheits Beschreibung zu konvertieren, wird die [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="fca1c-108">To convert a string-format security descriptor back to a valid functional security descriptor, call the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function.</span></span>

<span data-ttu-id="fca1c-109">Weitere Informationen finden Sie unter [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span><span class="sxs-lookup"><span data-stu-id="fca1c-109">For more information, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

 

 
