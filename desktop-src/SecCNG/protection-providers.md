---
description: Ab Windows 8 hat Microsoft damit begonnen, die Anbieter zu verteilen, mit denen Sie verschlüsselte Geheimnisse und Nachrichten sicher computerübergreifend freigeben können.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Schutzanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fe4c688eec734a7c32d1a85eaec2d9ebf132834a5970802cecb2639240e7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907191"
---
# <a name="protection-providers"></a>Schutzanbieter

Ab Windows 8 hat Microsoft damit begonnen, die Anbieter zu verteilen, mit denen Sie verschlüsselte Geheimnisse und Nachrichten sicher computerübergreifend freigeben können. Derzeit gibt es zwei wichtige Schutzanbieter. Mit dem Microsoft Key Protection-Anbieter können Sie Inhalte für eine Gruppe in einer Active Directory-Gesamtstruktur schützen. Mit dem Microsoft Client Key Protection-Anbieter können Sie Inhalte mit einer Reihe von Webanmeldeinformationen schützen.

Die richtige Schutzvorrichtung, die verwendet werden soll, wird automatisch für Sie ausgewählt, wenn die [**NCryptCreateProtectionDescriptor-Funktion**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) die schutzdeskriptor-Regelzeichenfolge analysiert, die Sie als Eingabe angeben. Der Microsoft Key Protection-Anbieter wird für Regelzeichenfolgen ausgewählt, die mit SID, SDDL und LOCAL beginnen. Der Microsoft Client Key Protection-Anbieter analysiert Regelzeichenfolgen, die mit WEBCREDENTIALS beginnen. Weitere Informationen zu Regelzeichenfolgen finden Sie unter [Schutzdeskriptoren.](protection-descriptors.md)

> [!Note]  
> Benutzerdefinierte Anbieter sind derzeit nicht zulässig. [CNG DPAPI](cng-dpapi.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[Schutzdeskriptoren](protection-descriptors.md)
</dt> </dl>

 

 



