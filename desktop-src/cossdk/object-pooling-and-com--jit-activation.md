---
description: Die com+-JIT-Aktivierung stellt im Wesentlichen einen Kompromiss zwischen gierigen Clients und gierigen Servern dar, um eine optimale Leistung zu erzielen. Clients erhalten Objekt Verweise, während Server die Speicherauslastung genauer verwalten können.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Objekt Pooling und com+-JIT-Aktivierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8042d838aaaae62eace6f61a8fe1aa820e17d079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393222"
---
# <a name="object-pooling-and-com-jit-activation"></a>Objekt Pooling und com+-JIT-Aktivierung

Die com+-JIT-Aktivierung stellt im Wesentlichen einen Kompromiss zwischen gierigen Clients und gierigen Servern dar, um eine optimale Leistung zu erzielen. Clients erhalten Objekt Verweise, während Server die Speicherauslastung genauer verwalten können.

Sie können dies mithilfe des [com+-Objekt Pooling](com--object-pooling.md)weiter verfeinern. Durch das Pooling von Objekten, die JIT-aktiviert sind, können Sie eine bestimmte Menge an Arbeitsspeicher für eine bestimmte Anzahl von Objekten im Arbeitsspeicher bereitstellen, die sofort wieder verwendet werden können. Dies ist am sinnvollsten, wenn Objekte zu erstellen sind, wie in dem Fall, in dem Sie mehrere Ressourcen enthalten.

Wenn Sie JIT-aktivierte Objekte auf diese Weise bündeln, können Sie die folgenden Vorteile erzielen:

-   Sehr beschleunigte Reaktivierungs Zeiten für Objekte.
-   Wiederverwendung kostspieliger Ressourcen, die von den Objekten gehalten werden.
-   Genauere Steuerung der Arbeitsspeicher-und Ressourcenverwendung für die in einem Pool zusammengefassten Objekte.
-   Beibehaltung der administrativen Flexibilität, damit Ihre Anwendung skaliert werden kann, um verfügbare Ressourcen zu verwenden und sich an geänderte Leistungsanforderungen anzupassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte für die Just-in-Time-Aktivierung in com+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Com+-Objekt Pooling](com--object-pooling.md)
</dt> <dt>

[Aktivieren der JIT-Aktivierung für eine Komponente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Transaktionen und com+-JIT-Aktivierung](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



