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
# <a name="mixed-mode-serialization-of-context-handles"></a><span data-ttu-id="2762a-106">Serialisierung im gemischten Modus von Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="2762a-106">Mixed Mode Serialization of Context Handles</span></span>

<span data-ttu-id="2762a-107">Ab Windows XP kann eine einzelne Schnittstelle sowohl serialisierte als auch nicht serialisierte Kontext Handles aufnehmen, sodass eine Methode in einer Schnittstelle ausschließlich auf ein Kontext Handle (serialisiert) zugreifen kann, während andere Methoden auf dieses Kontext Handle im freigegebenen Modus zugreifen (nicht serialisiert).</span><span class="sxs-lookup"><span data-stu-id="2762a-107">Starting with Windows XP, a single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="2762a-108">Weitere Informationen zu Kontext Handles finden Sie unter den folgenden Attributen:</span><span class="sxs-lookup"><span data-stu-id="2762a-108">For more information about context handles, see the following attributes:</span></span>

-   [<span data-ttu-id="2762a-109">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="2762a-109">**context\_handle**</span></span>](context-handle.md)
-   [<span data-ttu-id="2762a-110">**Kontext \_ handle- \_ Serialisierung**</span><span class="sxs-lookup"><span data-stu-id="2762a-110">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
-   [<span data-ttu-id="2762a-111">**Kontext \_ handle \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="2762a-111">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)

<span data-ttu-id="2762a-112">Die Zugriffs Funktionen für serialisierte und freigegebene Modi sind mit Lese-/schreibsperrungs-Mechanismen vergleichbar. Methoden, die ein serialisiertes Kontext Handle verwenden, sind exklusive Benutzer (Writer), während Methoden, die ein nicht serialisiertes Kontext Handle verwenden, freigegebene Benutzer (Reader) sind.</span><span class="sxs-lookup"><span data-stu-id="2762a-112">Serialized and shared mode access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="2762a-113">Methoden, die den Zustand eines Kontext Handles zerstören oder ändern, müssen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2762a-113">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="2762a-114">Methoden, die den Zustand eines Kontext Handles nicht ändern, wie z. b. die Methoden, die einfach aus einem Kontext Handle lesen, können nicht serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2762a-114">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="2762a-115">Die Verwendung eines Kontext Handles im gemischten Modus kann die Skalierbarkeit eines Servers erheblich verbessern, insbesondere dann, wenn mehrere Threads gleichzeitige Aufrufe desselben Kontext Handles durchführen.</span><span class="sxs-lookup"><span data-stu-id="2762a-115">Using a context handle in mixed mode can substantially improve the scalability of a server, especially when multiple threads make simultaneous calls to the same context handle.</span></span>

<span data-ttu-id="2762a-116">RPC erzwingt keine "Schreibsperre" für Methoden, die ein Kontext Handle im freigegebenen Modus verwenden. das bedeutet, dass Anwendungen sicherstellen müssen, dass Kontext Handles im gemeinsam genutzten Modus nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2762a-116">RPC does not enforce "write lock" on methods using a context handle in shared mode, which means applications must ensure that shared mode context handles are not modified.</span></span> <span data-ttu-id="2762a-117">Die Änderung eines Kontext Handles, das im freigegebenen Modus verwendet wird, kann zu geringfügigen Beschädigungen von Kontext Handle-Inhalten führen, die nicht debuggt werden können.</span><span class="sxs-lookup"><span data-stu-id="2762a-117">Modification of a context handle used in shared mode can result in subtle corruptions of context handle contents, which are impossible to debug.</span></span>

<span data-ttu-id="2762a-118">Das Ändern der Serialisierungslogik eines Kontext Handles wirkt sich nur auf den Server aus.</span><span class="sxs-lookup"><span data-stu-id="2762a-118">Changing the serialization logic of a context handle affects only the server.</span></span> <span data-ttu-id="2762a-119">Außerdem wirkt sich das Ändern der Serialisierungslogik eines Kontext Handles nicht auf das Wire-Format aus. aus diesem Grund haben Änderungen an der Serialisierungslogik auf einem Server keinen Einfluss auf die Funktion vorhandener Clients, mit dem Server zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="2762a-119">Also, changing the serialization logic of a context handle does not affect the wire format, and therefore, changes to serialization logic on a server do not affect existing clients' capability to interact with the server.</span></span>

<span data-ttu-id="2762a-120">Es wird nicht empfohlen, nur nicht serialisierte Kontext Handles zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2762a-120">Using only nonserialized context handles is not recommended.</span></span> <span data-ttu-id="2762a-121">Server, die nicht serialisierte Handles verwenden, sollten zum serialisierten Zugriff für die Methode wechseln, die das Kontext Handle schließt.</span><span class="sxs-lookup"><span data-stu-id="2762a-121">Servers that use nonserialized handles are should switch to serialized access for the method that closes the context handle.</span></span>

<span data-ttu-id="2762a-122">Kontext Handles, die \[ out \] -only sind, werden in der Regel von Erstellungs Methoden verwendet und erfordern keine Serialisierung.</span><span class="sxs-lookup"><span data-stu-id="2762a-122">Context handles that are \[out\]-only are typically used by creation methods, and do not require any serialization.</span></span> <span data-ttu-id="2762a-123">Daher wird ein beliebiges serialisierungsattribut, das auf reine \[ out \] -Kontext Handles angewendet wird, wie z. b. das Verarbeiten von [**Kontext \_ \_**](context-handle-serialize.md) Handles oder das [**Kontext \_ handle \_ noserialize**](context-handle-noserialize.md), von RPC ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2762a-123">Therefore, any serialization attribute applied to \[out\]-only context handles, such as [**context\_handle\_serialize**](context-handle-serialize.md) or [**context\_handle\_noserialize**](context-handle-noserialize.md), is ignored by RPC.</span></span>

> [!Note]  
> <span data-ttu-id="2762a-124">Erstellungs Methoden werden implizit serialisiert.</span><span class="sxs-lookup"><span data-stu-id="2762a-124">Creation methods are implicitly serialized.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2762a-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2762a-125">Examples</span></span>

<span data-ttu-id="2762a-126">In den folgenden zwei Beispielen wird gezeigt, wie die Serialisierung im gemischten Modus von Kontext Handles aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="2762a-126">The following two examples show how to enable mixed mode serialization of context handles.</span></span>

<span data-ttu-id="2762a-127">Das erste Beispiel zeigt die Vorgehensweise in der IDL-Datei:</span><span class="sxs-lookup"><span data-stu-id="2762a-127">The first example shows how to do so in the IDL file:</span></span>

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

<span data-ttu-id="2762a-128">Im zweiten Beispiel wird gezeigt, wie Sie die Serialisierung im gemischten Modus von Kontext Handles in der ACF-Datei aktivieren:</span><span class="sxs-lookup"><span data-stu-id="2762a-128">The second example shows how to enable mixed mode serialization of context handles in the ACF file:</span></span>

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a><span data-ttu-id="2762a-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2762a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2762a-130">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="2762a-130">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="2762a-131">**Kontext \_ handle- \_ Serialisierung**</span><span class="sxs-lookup"><span data-stu-id="2762a-131">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="2762a-132">**Kontext \_ handle \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="2762a-132">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> </dl>

 

 




