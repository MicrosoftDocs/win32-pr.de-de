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
# <a name="default-security-descriptor"></a>Standard Sicherheits Beschreibung

Mit Active Directory Domain Services können Sie auch die Standard Sicherheit für jeden Objekttyp angeben. Dies wird im [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) -Attribut in der [**classSchema**](/windows/desktop/ADSchema/c-classschema) -Objektdefinition im [Active Directory Schema](active-directory-schema.md)angegeben. Diese Sicherheits Beschreibung wird verwendet, um den Standardschutz für das Objekt bereitzustellen, wenn während der Erstellung des Objekts keine Sicherheits Beschreibung angegeben ist.

> [!Note]  
> Aces von einer Standard Sicherheits Beschreibung werden so behandelt, als würden Sie als Teil der Objekt Erstellung angegeben werden. Aus diesem Grund werden die standardaces vor geerbten ACEs abgelegt und Sie nach Bedarf überschrieben. Weitere Informationen finden Sie unter [Reihenfolge von ACEs in einer DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

Der [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) wird in einem speziellen Zeichen folgen Format mithilfe der [Sicherheits Deskriptor-Definitions Sprache (Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) , SDDL) angegeben. Zwei Funktionen können verwendet werden, um die binäre Form der Sicherheits Beschreibung in das Zeichen folgen Format zu konvertieren und umgekehrt. Dabei handelt es sich um diese Funktionen:

-   [Convertsecuritydescriptortostringsecuritydescriptor](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [Wurde von convertstringsecuritydescriptortosecuritydescriptor](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

Weitere Informationen und die Standard Sicherheits Beschreibungen der vordefinierten Objektklassen finden Sie auf den Klassen Verweis Seiten im Active Directory Schema Verweis der [Active Directory Domain Services Referenz](active-directory-domain-services-reference.md).

Weitere Informationen und ein Codebeispiel, das die [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) -Eigenschaft einer Objektklasse liest oder ändert, finden Sie unter [Lesen von defaultSecurityDescriptor für eine Objekt](reading-the-defaultsecuritydescriptor-for-an-object-class.md) Klasse und [Ändern von defaultSecurityDescriptor für eine Objektklasse](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).

 

 