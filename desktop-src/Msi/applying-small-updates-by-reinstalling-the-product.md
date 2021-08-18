---
description: Ein kleines Update kann auf eine Anwendung angewendet werden, indem die Anwendung vollständig oder teilweise über die Befehlszeile oder über ein Programm neu installiert wird.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Anwenden kleiner Updates durch Neuinstallation des Produkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb128ec3b62b3f81e8a1f9762bda715fa21e010fa4c16d16c8ca377aa4c5ce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145853"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a>Anwenden kleiner Updates durch Neuinstallation des Produkts

Ein kleines Update kann auf eine Anwendung angewendet werden, indem die Anwendung vollständig oder teilweise über die Befehlszeile oder über ein Programm neu installiert wird.

**So können Sie das kleine Update über die Befehlszeile an aktuelle Benutzer (dies ist eine vollständige Neuinstallation) weiterleiten**

1.  Verwenden Sie in der Befehlszeile entweder **msiexec \[ /fvomus** _path to updated .msi file_ oder *_\]_* **msiexec /I \[** path to updated .msi _file_ *_\] REINSTALL=ALL REINSTALLMODE=vomus_*.
2.  Die aktualisierte .msi Datei wird auf dem Computer des Benutzers zwischengespeichert. Beachten Sie, dass es dem Benutzer nicht möglich ist, das Produkt mithilfe von Software zu installieren, da sich die aktualisierte .msi Datei noch nicht auf dem Computer des Benutzers befindet.

**So über ein Programm ein kleines Update an aktuelle Benutzer (dies ist eine vollständige Neuinstallation)**

1.  Rufen Sie in einem Programm [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) auf, und geben Sie REINSTALLMODE \_ PACKAGE, REINSTALLMODE \_ FILEOLDERVERSION, REINSTALLMODE \_ MACHINEDATA, REINSTALLMODE \_ USERDATA und REINSTALLMODE \_ SHORTCUT an.
2.  Die aktualisierte .msi Datei wird auf dem Computer des Benutzers zwischengespeichert.

Die folgende Methode startet eine Neuinstallation nur der Features oder Komponenten, die von dem kleinen Update betroffen sind.

**So übertragen Sie ein kleines Update an aktuelle Benutzer (dies ist eine teilreinstallation)**

1.  Rufen Sie eine Liste der Namen der Features und Komponenten ab, die von dem kleinen Update betroffen sind.
2.  Verwenden Sie an der Eingabeaufforderung **msiexec /I \[** _path to updated .msi file_ *_\] REINSTALL= \[_* Feature _list \]_ **REINSTALLMODE=vomus**.
3.  Die aktualisierte .msi Datei wird auf dem Computer des Benutzers zwischengespeichert.

 

 



