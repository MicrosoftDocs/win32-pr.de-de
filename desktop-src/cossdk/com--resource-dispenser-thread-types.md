---
description: Com+-ressourcendispenser-Thread Typen
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: Com+-ressourcendispenser-Thread Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393009"
---
# <a name="com-resource-dispenser-thread-types"></a>Com+-ressourcendispenser-Thread Typen

Aufrufe eines com+-Ressourcen Verteilers können aus einem der folgenden Thread Typen stammen:

-   Apartment Thread (STA)
-   Freier Thread (MTA)
-   Nicht-com-Thread (Anwendung oder der Garbage Collector-Thread des [Dispenser-Managers](com--dispenser-manager.md) )

Wenn ein Ressourcen Verteiler kein COM-Objekt ist, muss es in der Lage sein, Aufrufe zu verarbeiten, die von einem beliebigen Thread empfangen werden. Wenn ein Ressourcen Verteiler ein COM-Objekt ist, sollte das COM-Objekt mit einem Threading Modell von **beidem** registriert werden. Dies ermöglicht es STA-oder MTA-Threads, den Ressourcen Verteiler ohne Thread Wechsel zu erstellen und zu verwenden.

Wenn ein Ressourcen Verteiler ein anderes com-Objekt erstellt und verwendet (z. b. einen Out-of-Process-Ressourcen-Manager), muss der Ressourcen Verteiler möglicherweise mehrere Proxys für dieses andere COM-Objekt verwalten und sicherstellen, dass Aufrufe des Objekts mithilfe des entsprechenden Proxys für den aufrufenden Thread durchgeführt werden. Wenn der Ressourcen Spender dieses Objekt erstellt, Marshalls und speichert es den Verweis. Vor dem erneuten Aufrufen des Objekts muss das Marshalling durchlaufen werden, um einen Proxy für den aufrufenden Thread zu erstellen.

Es ist möglicherweise effizienter, diese Thread bezogenen Proxys zwischenzuspeichern, indem eine Zuordnung von der Thread-ID zu einem Proxy Zeiger beibehalten wird. Diese Zuordnung wird erweitert, wenn im Prozess neue Threads verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte des com+-Ressourcen Verteilers](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



