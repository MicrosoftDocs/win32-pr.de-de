---
description: Transaktionen und com+-JIT-Aktivierung
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Transaktionen und com+-JIT-Aktivierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281691ebc9c8d5c654ea6ff0c3035d7e285f62c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861551"
---
# <a name="transactions-and-com-jit-activation"></a>Transaktionen und com+-JIT-Aktivierung

Die com+-JIT-Aktivierung ist eng an automatische Transaktionen gebunden. Wenn Sie eine Komponente so konfigurieren, dass eine Transaktion erforderlich ist oder eine neue Transaktion erforderlich ist, wird die JIT-Aktivierung ebenfalls automatisch aktiviert. Die beiden Features funktionieren natürlich in Verbindung. Transaktionale, von JIT aktivierte Komponenten haben die folgenden Merkmale:

-   Zustands losigkeit. Der Zustand, der gegen die Transaktions Isolation verstoßen würde, wird nicht aufrechterhalten, und Sie würden den Zustand anhalten, der bei der Objekt-decoaktivierung verloren geht.

-   Schnelle Verwendung. Das kanonische Verwendungs Muster für ein Objekt, das in einer automatischen Transaktion funktioniert, besteht darin, eine kleine Arbeitseinheit auszuführen, abzustimmen und zu beenden.

    > [!Note]  
    > Die Methoden, die Sie in com+-Transaktionen und Signal-doneness für die JIT-Aktivierung abstimmen, sind ebenfalls eng miteinander verbunden. Weitere Informationen finden Sie unter [Festlegen des done-Bits](setting-the-done-bit.md).

     

-   Wiederholte Verwendung. Wenn die Transaktionsarbeit ordnungsgemäß untergliedert ist, verwenden Clients immer wieder dieselben Objekte, um wenig atomarische Arbeiten auszuführen.

-   Bei Commit oder Abbruch deaktiviert. In com+ werden alle Objekte innerhalb der Transaktionsgrenze deaktiviert, wenn die Transaktion ausgeführt wird oder abgebrochen wird.

In Verbindung mit den com+-Transaktions Komponenten ist die JIT-Aktivierung eine große Leistungssteigerung, da der Kanal geöffnet bleibt, da Clients langlebige Verweise auf Transaktions Objekte enthalten. Als weitere Verbesserungen können Sie festlegen, dass die Transaktions Objekte in den Pool eingereihlt werden, um die darin verwendeten Ressourcen wiederzuverwenden, die Reaktivierungs Zeit des Objekts zu beschleunigen und die Arbeitsspeicher Ressourcen für bestimmte Objekte genau zu verwalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte für die Just-in-Time-Aktivierung in com+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Aktivieren der JIT-Aktivierung für eine Komponente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Objekt Pooling und com+-JIT-Aktivierung](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



