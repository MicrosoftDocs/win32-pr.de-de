---
description: Ab Windows 8 hat Microsoft damit begonnen, die Anbieter zu verteilen, mit denen Sie verschlüsselte Geheimnisse und Nachrichten auf allen Computern sicher freigeben können.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Schutz Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c262fcfbfa5ab0842f103849af3d67b20f8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959434"
---
# <a name="protection-providers"></a>Schutz Anbieter

Ab Windows 8 hat Microsoft damit begonnen, die Anbieter zu verteilen, mit denen Sie verschlüsselte Geheimnisse und Nachrichten auf allen Computern sicher freigeben können. Zurzeit sind zwei Schlüsselschutz Anbieter vorhanden. Mit dem Microsoft-Schlüsselschutz Anbieter können Sie Inhalte für eine Gruppe in einer Active Directory-Gesamtstruktur schützen. Mit dem Microsoft-Client Schlüsselschutz-Anbieter können Sie Inhalte für eine Reihe von webanmelde Informationen schützen.

Die richtige zu verwendende Schutzvorrichtung wird automatisch für Sie ausgewählt, wenn die [**ncryptkreateschutzdescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) -Funktion die als Eingabe bereitgestellte Schutz Beschreibungszeichenfolge analysiert. Der Microsoft-Schlüsselschutz Anbieter wird für Regel Zeichenfolgen ausgewählt, die mit sid, SDDL und local beginnen. Der Microsoft-Client Schlüsselschutz-Anbieter analysiert Regel Zeichenfolgen, die mit webanmelde Informationen beginnen. Weitere Informationen zu Regel Zeichenfolgen finden Sie unter [Schutz Deskriptoren](protection-descriptors.md).

> [!Note]  
> Benutzerdefinierte Anbieter sind zurzeit nicht zulässig. [CNG-DPAPI](cng-dpapi.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CNG-DPAPI](cng-dpapi.md)
</dt> <dt>

[**Ncryptkreateschutzdescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[Schutz Deskriptoren](protection-descriptors.md)
</dt> </dl>

 

 



