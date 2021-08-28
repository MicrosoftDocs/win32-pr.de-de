---
title: Serialisierung von Kontexthandles im gemischten Modus
description: In Microsoft Windows XP kann eine einzelne Schnittstelle sowohl serialisierte als auch nicht serialisierte Kontexthandles aufnehmen, die als Serialisierung im gemischten Modus bezeichnet wird.
ms.assetid: b52c1d6f-cdc5-4597-a36e-bb957e4aab01
keywords:
- MIDL-Sprachreferenz MIDL , Serialisierung von Kontexthandles im gemischten Modus
- Context handles MIDL (Kontexthandles MIDL)
- MIDL-Serialisierung im gemischten Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aaa35f02a939a50e2484ace29630783ee219d6313d7538cba54b1f54cd83007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787430"
---
# <a name="mixed-mode-serialization-of-context-handles"></a>Serialisierung von Kontexthandles im gemischten Modus

Ab Windows XP kann eine einzelne Schnittstelle sowohl serialisierte als auch nicht serialisierte Kontexthandles aufnehmen, sodass eine Methode auf einer Schnittstelle ausschließlich (serialisiert) auf ein Kontexthandle zugreifen kann, während andere Methoden auf dieses Kontexthandle im freigegebenen Modus (nicht serialisiert) zugreifen. Weitere Informationen zu Kontexthandles finden Sie in den folgenden Attributen:

-   [**Kontexthand \_ handle**](context-handle.md)
-   [**Context \_ Handle \_ serialize**](context-handle-serialize.md)
-   [**context \_ handle \_ noserialize**](context-handle-noserialize.md)

Zugriffsfunktionen im serialisierten modus und im gemeinsam genutzten Modus sind mit Lese-/Schreibsperrmechanismen vergleichbar. -Methoden, die ein serialisiertes Kontexthandle verwenden, sind exklusive Benutzer (Writer), während Methoden, die ein nicht serialisiertes Kontexthandle verwenden, freigegebene Benutzer (Reader) sind. Methoden, die den Zustand eines Kontexthandpunkts zerstören oder ändern, müssen serialisiert werden. Methoden, die den Zustand eines Kontexthandles nicht ändern, z. B. methoden, die einfach aus einem Kontexthandle lesen, können nicht serialisiert werden. Die Verwendung eines Kontexthandlings im gemischten Modus kann die Skalierbarkeit eines Servers erheblich verbessern, insbesondere wenn mehrere Threads gleichzeitig Aufrufe desselben Kontexthandlings ausführen.

RPC erzwingt keine Schreibsperre für Methoden, die ein Kontexthandles im freigegebenen Modus verwenden. Das bedeutet, dass Anwendungen sicherstellen müssen, dass Kontexthandles im freigegebenen Modus nicht geändert werden. Die Änderung eines kontextigen Handles, das im freigegebenen Modus verwendet wird, kann zu feinen Beschädigungen von Kontexthandpunktinhalten führen, die nicht debuggt werden können.

Das Ändern der Serialisierungslogik eines Kontexthandpunkts wirkt sich nur auf den Server aus. Außerdem wirkt sich das Ändern der Serialisierungslogik eines Kontexthandpunkts nicht auf das Wire-Format aus. Änderungen an der Serialisierungslogik auf einem Server wirken sich daher nicht auf die Fähigkeit vorhandener Clients aus, mit dem Server zu interagieren.

Es wird nicht empfohlen, nur nicht-lokalisierte Kontexthandles zu verwenden. Server, die nicht serialisierte Handles verwenden, sollten zum serialisierten Zugriff für die Methode wechseln, die das Kontexthandle schließt.

Kontexthandles, die nur out sind, werden in der Regel von Erstellungsmethoden verwendet und erfordern \[ \] keine Serialisierung. Daher wird jedes Serialisierungsattribut, das auf out-only-Kontexthandles angewendet wird, z. B. context \[ handle \] [**\_ \_ serialize**](context-handle-serialize.md) oder [**context handle \_ \_ noserialize,**](context-handle-noserialize.md)von RPC ignoriert.

> [!Note]  
> Erstellungsmethoden werden implizit serialisiert.

 

## <a name="examples"></a>Beispiele

In den folgenden beiden Beispielen wird gezeigt, wie die Serialisierung von Kontexthandles im gemischten Modus aktiviert wird.

Das erste Beispiel zeigt dies in der IDL-Datei:

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

Das zweite Beispiel zeigt, wie die Serialisierung von Kontexthandles im gemischten Modus in der ACF-Datei aktiviert wird:

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Kontexthand \_ handle**](context-handle.md)
</dt> <dt>

[**Context \_ Handle \_ serialize**](context-handle-serialize.md)
</dt> <dt>

[**context \_ handle \_ noserialize**](context-handle-noserialize.md)
</dt> </dl>

 

 




