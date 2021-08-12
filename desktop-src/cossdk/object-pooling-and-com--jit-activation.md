---
description: Bei der COM+-JIT-Aktivierung kommt es im Wesentlichen zu einer Gefährdung zwischen gierigen Clients und gierigen Servern, um eine optimale Leistung zu erzielen. Clients können Objektverweise beibehalten, während Server die Speicherauslastung genauer verwalten können.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Objektpooling und COM+-JIT-Aktivierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb4a61534d19559c5d3492cd73f99fe65cf837c059d5f58b226d56a6cd301d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306148"
---
# <a name="object-pooling-and-com-jit-activation"></a>Objektpooling und COM+-JIT-Aktivierung

Bei der COM+-JIT-Aktivierung kommt es im Wesentlichen zu einer Gefährdung zwischen gierigen Clients und gierigen Servern, um eine optimale Leistung zu erzielen. Clients können Objektverweise beibehalten, während Server die Speicherauslastung genauer verwalten können.

Sie können dies weiter verfeinern, indem Sie [COM+-Objektpooling](com--object-pooling.md)verwenden. Durch das Pooling von JIT-aktivierten Objekten können Sie eine bestimmte Menge an Arbeitsspeicher für eine bestimmte Anzahl von Objekten reservieren, die im Arbeitsspeicher aktiv sind und sofort wiederverwendet werden können. Dies ist am sinnvollsten, wenn Objekte teuer zu erstellen sind, wie in dem Fall, in dem sie mehrere Ressourcen enthalten.

Durch das Pooling von JIT-aktivierten Objekten auf diese Weise können Sie die folgenden Vorteile erzielen:

-   Die Reaktivierungszeiten von Objekten wurden erheblich beschleunigt.
-   Wiederverwendung von ressourcenintensiven Ressourcen, die die Objekte enthalten.
-   Genauere Steuerung des Arbeitsspeichers und der Ressourcennutzung für die in einem Pool zusammengefassten Objekte.
-   Beibehaltung der Administrativen Flexibilität, damit Ihre Anwendung skaliert werden kann, um verfügbare Ressourcen zu nutzen und sich an sich ändernde Leistungsanforderungen anzupassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+ Just-in-Time-Aktivierungskonzepte](com--just-in-time-activation-concepts.md)
</dt> <dt>

[COM+-Objektpooling](com--object-pooling.md)
</dt> <dt>

[Aktivieren der JIT-Aktivierung für eine Komponente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Transaktionen und COM+-JIT-Aktivierung](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



