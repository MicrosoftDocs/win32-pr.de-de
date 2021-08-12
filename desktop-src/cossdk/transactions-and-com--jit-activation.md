---
description: Transaktionen und COM+-JIT-Aktivierung
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Transaktionen und COM+-JIT-Aktivierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2b496f46652dc8ab9f6d573e712a0aa83575cac0adbb86a7dc4cfa88b565ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546047"
---
# <a name="transactions-and-com-jit-activation"></a>Transaktionen und COM+-JIT-Aktivierung

Die COM+-JIT-Aktivierung ist eng an automatische Transaktionen gebunden. Wenn Sie eine Komponente so konfigurieren, dass sie eine Transaktion oder eine neue Transaktion erfordert, wird die JIT-Aktivierung automatisch aktiviert. Die beiden Features funktionieren natürlich in Verbindung. Transaktionale, JIT-aktivierte Komponenten haben die folgenden Merkmale:

-   Staatenlosigkeit. Sie würden weder einen Zustand speichern, der gegen die Transaktionsisolation verstoßen würde, noch den Zustand, der bei der Objektdeaktivierung verloren geht.

-   Schnelle Verwendung. Das kanonische Verwendungsmuster für ein Objekt, das Arbeit in einer automatischen Transaktion ausführt, besteht darin, eine kleine Arbeitseinheit auszuführen, abzustimmen und zu beenden.

    > [!Note]  
    > Die Methoden, mit denen Sie für COM+-Transaktionen abstimmen und die JiT-Aktivierung signalisieren, sind ebenfalls eng miteinander verbunden. Weitere Informationen finden Sie unter [Festlegen von Done Bit](setting-the-done-bit.md).

     

-   Wiederholte Verwendung. Wenn Transaktionsaufgaben ordnungsgemäß aufgeteilt werden, verwenden Clients immer wieder dieselben Objekte, um kleine Unausdinge der atomaren Arbeit auszuführen.

-   Deaktiviert beim Commit oder Abbruch. In COM+ werden alle Objekte innerhalb der Transaktionsgrenze deaktiviert, wenn die Transaktion committet oder abgebrochen wird.

In Verbindung mit COM+-Transaktionskomponenten stellt die JIT-Aktivierung eine große Leistungssteigerung dar, indem der Kanal geöffnet bleibt, da Clients langlebige Verweise auf Transaktionsobjekte enthalten. Als weitere Verbesserungen können Sie die Transaktionsobjekte in einem Pool zusammensetzen, um die darin enthaltenen Ressourcen wiederzuverwenden, die Reaktivierungszeit von Objekten zu beschleunigen und genau zu verwalten, wie Sie Speicherressourcen für bestimmte Objekte verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+ Just-in-Time-Aktivierungskonzepte](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Aktivieren der JIT-Aktivierung für eine Komponente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Objektpooling und COM+-JIT-Aktivierung](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



