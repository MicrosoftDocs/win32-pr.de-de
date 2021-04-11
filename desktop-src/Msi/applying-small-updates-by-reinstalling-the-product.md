---
description: Ein kleines Update kann auf eine Anwendung angewendet werden, indem die Anwendung vollständig oder teilweise von der Befehlszeile oder von einem Programm neu installiert wird.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Anwenden von kleinen Updates durch Neuinstallation des Produkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959532"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a>Anwenden von kleinen Updates durch Neuinstallation des Produkts

Ein kleines Update kann auf eine Anwendung angewendet werden, indem die Anwendung vollständig oder teilweise von der Befehlszeile oder von einem Programm neu installiert wird.

**So verteilen Sie das kleine Update über die Befehlszeile an die aktuellen Benutzer (Hierbei handelt es sich um eine komplette Neuinstallation)**

1.  Verwenden Sie in der Befehlszeile einen der folgenden Befehle: **msiexec/fvomus \[** _path to aktualisierte MSI-Datei_ *_\]_* oder **msiexec/I \[** _path to aktualisierte. msi file_ *_\] REINSTALL = ALL REINSTALLMODE = vomus_*.
2.  Die aktualisierte MSI-Datei wird auf dem Computer des Benutzers zwischengespeichert. Beachten Sie, dass der Benutzer das Produkt nicht mithilfe der Option "Software" erneut installieren kann, da sich die aktualisierte MSI-Datei noch nicht auf dem Computer des Benutzers befindet.

**So verteilen Sie ein kleines Update von einem Programm an die aktuellen Benutzer (Dies ist eine komplette Neuinstallation)**

1.  Geben Sie in einem Programm [**msireinstallproduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) ein, und geben Sie REINSTALLMODE \_ Package, REINSTALLMODE \_ fileolderversion, REINSTALLMODE \_ MachineData, REINSTALLMODE \_ UserData und REINSTALLMODE \_ Shortcut an.
2.  Die aktualisierte MSI-Datei wird auf dem Computer des Benutzers zwischengespeichert.

Mit der folgenden Methode wird eine Neuinstallation der Features oder Komponenten gestartet, die vom kleinen Update betroffen sind.

**So übertragen Sie ein kleines Update an die aktuellen Benutzer (Hierbei handelt es sich um eine partielle Neuinstallation)**

1.  Abrufen einer Liste der Namen von Features und Komponenten, die von dem kleinen Update betroffen sind.
2.  Geben Sie an der Eingabeaufforderung Folgendes ein: **msiexec/I \[** _path to aktualisierte. msi file_ *_\] REINSTALL = \[_*_Feature List \]_ **REINSTALLMODE = vomus**.
3.  Die aktualisierte MSI-Datei wird auf dem Computer des Benutzers zwischengespeichert.

 

 



