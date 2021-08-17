---
description: Der Produktcode ist eine GUID, die die Hauptidentifikation einer Anwendung oder eines Produkts ist.
ms.assetid: 6fbad59b-27b7-4ac1-bad5-8a608c7b270f
title: Produktcodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2afe0c96e78d14bc989d4acdc7195d374b82466c4b345a999df7085468587e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145373"
---
# <a name="product-codes"></a>Produktcodes

Der Produktcode ist eine GUID, die die Hauptidentifikation einer Anwendung oder eines Produkts ist. Weitere Informationen finden Sie in der [**ProductCode-Eigenschaft.**](productcode.md) Wenn erhebliche Änderungen an einem Produkt vorgenommen werden, sollte auch der Produktcode geändert werden, um dies widerzuspiegeln. Es ist jedoch nicht erforderlich, dass der Produktcode geändert wird, wenn die Änderungen am Produkt relativ geringfügig sind.

Die 32-Bit- und 64-Bit-Versionen des Pakets einer Anwendung müssen unterschiedliche Produktcodes aufweisen. Wenn eine 32-Bit-Komponente einer Anwendung in eine 64-Bit-Komponente neu kompiliert wird, muss ein neuer Produktcode zugewiesen werden.

Wenn ein in der [PublishComponent-Tabelle](publishcomponent-table.md) verfügbar gemachter Server von 32 Bits in 64 Bits neu kompiliert wird, muss die GUID in dieser Tabelle möglicherweise auch geändert werden, damit 32-Bit- und 64-Bit-Clients die entsprechende qualifizierte Komponentenkategorie identifizieren können. In diesem Fall muss auch der Produktcode geändert werden.

Beachten Sie, dass Buchstaben in Produktcode-GUIDs groß geschrieben werden müssen. Hilfsprogramme wie GUIDGEN generieren GUIDs mit Kleinbuchstaben. Die Kleinbuchstaben in diesen GUIDs müssen in Großbuchstaben geändert werden, um als Produktcode oder Paketcode verwendet zu werden. Weitere Informationen finden Sie unter [Ändern des Produktcodes.](changing-the-product-code.md)

Der Paketcode ist eine GUID, die einen bestimmten Windows [*Installer-Paket*](p-gly.md)identifiziert. Der Paketcode ordnet einer Anwendung oder einem Produkt eine .msi-Datei zu und kann auch für die Überprüfung von Quellen verwendet werden. Die Produkt- und Paketcodes sind nicht austauschbar. Keine zwei nichtidentischen .msi Dateien sollten jemals den gleichen Paketcode aufweisen. Obwohl es üblich ist, eine Anwendung mit dem gleichen Paketcode und Produktcode zu versenden, können die beiden Werte abweichen, wenn die Anwendung aktualisiert wird. Weitere Informationen finden Sie unter [Paketcodes.](package-codes.md)

 

 



