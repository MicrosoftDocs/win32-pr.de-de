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

Die COM+-JIT-Aktivierung ist eng an automatische Transaktionen gebunden. Wenn Sie eine Komponente so konfigurieren, dass sie eine Transaktion erfordert oder eine neue Transaktion erfordert, wird die JIT-Aktivierung automatisch aktiviert. Die beiden Features funktionieren natürlich in Verbindung. Transaktionale, JIT-aktivierte Komponenten haben die folgenden Merkmale:

-   Staatenlosigkeit. Sie würden weder einen Zustand besitzen, der die Transaktionsisolation verletzen würde, noch den Zustand, der bei der Objektdeaktivierung verloren gehen würde.

-   Schnelle Verwendung. Das kanonische Verwendungsmuster für ein Objekt, das In einer automatischen Transaktion arbeitet, besteht in der Durchführung einer kleinen Arbeitseinheit, der Abstimmung und dem Beenden.

    > [!Note]  
    > Die Möglichkeiten, wie Sie in COM+-Transaktionen abstimmen und signalisieren, dass die JIT-Aktivierung erfolgt, sind ebenfalls eng miteinander verknüpft. Weitere Informationen finden Sie unter [Setting the Done Bit](setting-the-done-bit.md).

     

-   Wiederholte Verwendung. Wenn transaktionale Aufgaben ordnungsgemäß aufgebrochen werden, verwenden Clients immer wieder die gleichen Objekte, um wenig atomische Aufgaben durchzuführen.

-   Bei Commit oder Abbruch deaktiviert. In COM+ werden alle Objekte innerhalb der Transaktionsgrenze deaktiviert, wenn ein Commit oder Abbruch der Transaktion ausgeführt wird.

In Verbindung mit COM+-Transaktionskomponenten dient die JIT-Aktivierung als eine große Leistungssteigerung, da der Kanal geöffnet wird, da Clients langlebige Verweise auf Transaktionsobjekte enthalten. Als weitere Verbesserungen können Sie die Transaktionsobjekte in einem Pool zusammenzuspeichern, um die in ihnen gespeicherten Ressourcen wiederzuverwenden, die Reaktivierungszeit von Objekten zu beschleunigen und genau zu verwalten, wie Sie Speicherressourcen für bestimmte Objekte verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der COM+-Just-In-Time-Aktivierung](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Aktivieren der JIT-Aktivierung für eine Komponente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Objektpooling und COM+-JIT-Aktivierung](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



