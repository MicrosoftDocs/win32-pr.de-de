---
description: Bei einem geringfügigen Upgrade werden zahlreiche Ressourcen geändert.
ms.assetid: 74c962f9-93cd-40ed-a8fe-141ccac79d79
title: Kleinere Upgrades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833bb46e2cafe0545f83c0ed0f8ff8aba00f0695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867287"
---
# <a name="minor-upgrades"></a>Kleinere Upgrades

Bei einem geringfügigen Upgrade werden zahlreiche Ressourcen geändert. Keine der Änderungen kann das Ändern von [**ProductCode**](productcode.md)erfordern. Ein Update erfordert ein [großes Upgrade](major-upgrades.md) , um **ProductCode** zu ändern. Ein kleineres Upgrade kann verwendet werden, um neue Features und Komponenten hinzuzufügen, die Funktionskomponenten Struktur jedoch nicht neu zu organisieren. Kleinere Upgrades bieten eine Produktdifferenzierung, ohne tatsächlich ein anderes Produkt zu definieren. Ein typisches kleines Upgrade umfasst alle Korrekturen in früheren kleinen Updates, die in einem Patch zusammengefasst sind. Ein kleineres Upgrade wird auch als Service Pack Update (SP) bezeichnet. Weitere Informationen dazu, welche Updates das Ändern von **ProductCode** nicht erfordern, finden Sie [unter Ändern des Produktcodes](changing-the-product-code.md).

Bei einem geringfügigen Upgrade wird die [**ProductVersion**](productversion.md) -Eigenschaft geändert. Das Ändern der Produktversion der Anwendung bedeutet, dass die verschiedenen Updates über eine Bestellung verfügen. Wenn beispielsweise ein Patch zum Aktualisieren von v 9,0 auf v 9,1 vorhanden war und ein anderer Patch zum Patchen von v 9,1 bis v 9,2 vorhanden war, kann das Installationsprogramm die richtige Reihenfolge erzwingen, indem die Produktversion vor der Anwendung des Patches überprüft wird. Dadurch wird auch verhindert, dass der Patch v 9,1 to v 9,2 auf v 9,0 angewendet wird. Bei Patches wird diese Reihenfolge durch die Produktversion – Validierungs Bits erzwungen, die in den im [Patchpaket](patch-packages.md)enthaltenen Transformationen festgelegt sind.

Ein kleineres Upgrade und ein kleines Update unterscheiden sich insofern, als das kleinere Upgrade den Paket Code und die Produktversion ändert. Informationen zu den Arten von Updates, die von einem kleinen Update oder einem geringfügigen Upgrade behandelt werden können, finden Sie unter [kleine Updates](small-updates.md) . Kleinere Upgrades werden als vollständiges Produkt Installationspaket oder als [Patchpaket](patch-packages.md)ausgeliefert. Bei einem geringfügigen Upgrade kann jedoch keine andere Volumebezeichnung für die neue Version verwendet werden.

Informationen zum Anwenden eines geringfügigen Upgrades finden Sie in den folgenden Themen:

-   [Anwenden von kleinen Updates durch Patchen der lokalen Installation des Produkts](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [Anwenden von kleinen Updates durch Neuinstallation des Produkts](applying-small-updates-by-reinstalling-the-product.md)
-   [Anwenden von kleinen Updates durch Patchen eines administrativen Abbilds](applying-small-updates-by-patching-an-administrative-image.md)

 

 



