---
description: Der Produktcode ist eine GUID, bei der es sich um die Prinzipal Identifizierung einer Anwendung oder eines Produkts handelt.
ms.assetid: 6fbad59b-27b7-4ac1-bad5-8a608c7b270f
title: Produkt Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edca03d54dcd14068e89b2314b729e672b0c631c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217468"
---
# <a name="product-codes"></a>Produkt Codes

Der Produktcode ist eine GUID, bei der es sich um die Prinzipal Identifizierung einer Anwendung oder eines Produkts handelt. Weitere Informationen finden Sie unter der [**ProductCode**](productcode.md) -Eigenschaft. Wenn an einem Produkt bedeutende Änderungen vorgenommen werden, sollte der Produktcode ebenfalls geändert werden, um dies widerzuspiegeln. Es ist jedoch nicht erforderlich, dass der Produktcode geändert wird, wenn die Änderungen am Produkt relativ gering sind.

Die 32-Bit-und 64-Bit-Versionen des Pakets einer Anwendung müssen über unterschiedliche Produktcodes verfügen. Wenn eine 32-Bit-Komponente einer Anwendung in eine 64-Bit-Komponente neu kompiliert wird, muss ein neuer Produktcode zugewiesen werden.

Wenn ein Server, der in der [PublishComponent-Tabelle](publishcomponent-table.md) verfügbar gemacht wird, von 32-Bits auf 64 Bit neu kompiliert wird, muss die GUID in dieser Tabelle möglicherweise ebenfalls geändert werden, damit 32-Bit-und 64-Bit-Clients die geeignete qualifizierte Komponenten Kategorie identifizieren können. In diesem Fall muss der Produktcode ebenfalls geändert werden.

Beachten Sie, dass Buchstaben in Produktcode-GUIDs Großbuchstaben sein müssen. Dienstprogramme wie GUIDGEN generieren GUIDs, die Kleinbuchstaben enthalten. Die Kleinbuchstaben in diesen GUIDs müssen in Großbuchstaben geändert werden, damit Sie als Produktcode oder Paketcode verwendet werden können. Weitere Informationen finden Sie unter [Ändern des Produktcodes](changing-the-product-code.md).

Der Paket Code ist eine GUID, die ein bestimmtes Windows Installer [*Paket*](p-gly.md)identifiziert. Der Paket Code ordnet eine MSI-Datei einer Anwendung oder einem Produkt zu und kann auch für die Überprüfung von Quellen verwendet werden. Die Produkt-und Paket Codes sind nicht austauschbar. Keine zwei nonidentical. msi-Dateien sollten jemals denselben Paketcode aufweisen. Obwohl es üblich ist, eine Anwendung zu liefern, die denselben Paketcode und Produktcode aufweist, können sich die beiden Werte beim Aktualisieren der Anwendung unterscheiden. Weitere Informationen finden Sie unter [Paket Codes](package-codes.md).

 

 



