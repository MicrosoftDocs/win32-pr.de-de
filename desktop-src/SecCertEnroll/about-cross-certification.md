---
description: Die Kreuzzertifizierung ermöglicht es Entitäten in einer Public Key-Infrastruktur (PKI), Entitäten in einer anderen PKI zu vertrauen.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Zertifizierungsübergreifend
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644e5326f9d3b9f7cbe87290c044dea7f401f8a888fa3904afa162118a98d89b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904544"
---
# <a name="cross-certification"></a>Zertifizierungsübergreifend

Die Kreuzzertifizierung ermöglicht es Entitäten in einer Public Key-Infrastruktur (PKI), Entitäten in einer anderen PKI zu vertrauen. Diese gegenseitige Vertrauensstellung wird in der Regel durch eine zertifizierungsübergreifende Vereinbarung zwischen den Zertifizierungsstellen (Certification Authorities, CAs) in jeder PKI unterstützt. Die Vereinbarung legt die Zuständigkeiten und die Haftung der einzelnen Parteien fest.

Eine gegenseitige Vertrauensstellung zwischen zwei Zertifizierungsstellen erfordert, dass jede Zertifizierungsstelle ein Zertifikat für die andere ausstellen muss, um die Beziehung in beide Richtungen herzustellen. Der Vertrauenspfad ist nicht hierarchisch (keiner der übergeordneten Zertifizierungsstellen ist der anderen untergeordnet), obwohl es sich bei den separaten PKIs möglicherweise um Zertifikathierarchien handelt. Nachdem zwei Zertifizierungsstellen die Vertrauensbedingungen und ausgestellten Zertifikate eingerichtet und angegeben haben, können Entitäten innerhalb der separaten PKIs gemäß den in den Zertifikaten angegebenen Richtlinien interagieren.

![Zertifizierungsübergreifendes Diagramm](images/cross-certification.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertrauensstellungsmodelle](about-trust-models.md)
</dt> </dl>

 

 



