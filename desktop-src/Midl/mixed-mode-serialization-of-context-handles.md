---
title: Serialisierung im gemischten Modus von Kontext Handles
description: In Microsoft Windows XP kann eine einzelne Schnittstelle sowohl serialisierte als auch nicht serialisierte Kontext Handles aufnehmen, die als "im gemischten Modus" bezeichnete Serialisierung bezeichnet werden.
ms.assetid: b52c1d6f-cdc5-4597-a36e-bb957e4aab01
keywords:
- Mittel l-sprach Verweis-Mittel l, Serialisierung im gemischten Modus von Kontext Handles
- Kontext Handles (Mitte)
- serialisierungsmittell im gemischten Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0922b53bfc7ba2e30ad8df0764e3cf9a36f0f723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856076"
---
# <a name="mixed-mode-serialization-of-context-handles"></a>Serialisierung im gemischten Modus von Kontext Handles

Ab Windows XP kann eine einzelne Schnittstelle sowohl serialisierte als auch nicht serialisierte Kontext Handles aufnehmen, sodass eine Methode in einer Schnittstelle ausschließlich auf ein Kontext Handle (serialisiert) zugreifen kann, während andere Methoden auf dieses Kontext Handle im freigegebenen Modus zugreifen (nicht serialisiert). Weitere Informationen zu Kontext Handles finden Sie unter den folgenden Attributen:

-   [**Kontext \_ handle**](context-handle.md)
-   [**Kontext \_ handle- \_ Serialisierung**](context-handle-serialize.md)
-   [**Kontext \_ handle \_ noserialize**](context-handle-noserialize.md)

Die Zugriffs Funktionen für serialisierte und freigegebene Modi sind mit Lese-/schreibsperrungs-Mechanismen vergleichbar. Methoden, die ein serialisiertes Kontext Handle verwenden, sind exklusive Benutzer (Writer), während Methoden, die ein nicht serialisiertes Kontext Handle verwenden, freigegebene Benutzer (Reader) sind. Methoden, die den Zustand eines Kontext Handles zerstören oder ändern, müssen serialisiert werden. Methoden, die den Zustand eines Kontext Handles nicht ändern, wie z. b. die Methoden, die einfach aus einem Kontext Handle lesen, können nicht serialisiert werden. Die Verwendung eines Kontext Handles im gemischten Modus kann die Skalierbarkeit eines Servers erheblich verbessern, insbesondere dann, wenn mehrere Threads gleichzeitige Aufrufe desselben Kontext Handles durchführen.

RPC erzwingt keine "Schreibsperre" für Methoden, die ein Kontext Handle im freigegebenen Modus verwenden. das bedeutet, dass Anwendungen sicherstellen müssen, dass Kontext Handles im gemeinsam genutzten Modus nicht geändert werden. Die Änderung eines Kontext Handles, das im freigegebenen Modus verwendet wird, kann zu geringfügigen Beschädigungen von Kontext Handle-Inhalten führen, die nicht debuggt werden können.

Das Ändern der Serialisierungslogik eines Kontext Handles wirkt sich nur auf den Server aus. Außerdem wirkt sich das Ändern der Serialisierungslogik eines Kontext Handles nicht auf das Wire-Format aus. aus diesem Grund haben Änderungen an der Serialisierungslogik auf einem Server keinen Einfluss auf die Funktion vorhandener Clients, mit dem Server zu interagieren.

Es wird nicht empfohlen, nur nicht serialisierte Kontext Handles zu verwenden. Server, die nicht serialisierte Handles verwenden, sollten zum serialisierten Zugriff für die Methode wechseln, die das Kontext Handle schließt.

Kontext Handles, die \[ out \] -only sind, werden in der Regel von Erstellungs Methoden verwendet und erfordern keine Serialisierung. Daher wird ein beliebiges serialisierungsattribut, das auf reine \[ out \] -Kontext Handles angewendet wird, wie z. b. das Verarbeiten von [**Kontext \_ \_**](context-handle-serialize.md) Handles oder das [**Kontext \_ handle \_ noserialize**](context-handle-noserialize.md), von RPC ignoriert.

> [!Note]  
> Erstellungs Methoden werden implizit serialisiert.

 

## <a name="examples"></a>Beispiele

In den folgenden zwei Beispielen wird gezeigt, wie die Serialisierung im gemischten Modus von Kontext Handles aktiviert wird.

Das erste Beispiel zeigt die Vorgehensweise in der IDL-Datei:

``` syntax
typedef [context_handle] void *TestContextHandleExclusive;
typedef [context_handle] TestContextHandleExclusive TestContextHandleShared;

void
UseShared(...
          [in] TestContextHandleShared *Ctx,
          ...);

void
UseExclusive(...
             [in, out] TestContextHandleExclusive *Ctx,
             ...);
```

Im zweiten Beispiel wird gezeigt, wie Sie die Serialisierung im gemischten Modus von Kontext Handles in der ACF-Datei aktivieren:

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Kontext \_ handle**](context-handle.md)
</dt> <dt>

[**Kontext \_ handle- \_ Serialisierung**](context-handle-serialize.md)
</dt> <dt>

[**Kontext \_ handle \_ noserialize**](context-handle-noserialize.md)
</dt> </dl>

 

 




