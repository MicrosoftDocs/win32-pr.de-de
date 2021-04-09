---
description: Bei einer administrativen Installation wird ein Quell Abbild einer Anwendung oder eines Produkts in einem Netzwerk erstellt.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Anwenden von kleinen Updates durch Patchen eines administrativen Abbilds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dad22d91e101d79d2bf6ecc0efc8ea9358eda2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959534"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a>Anwenden von kleinen Updates durch Patchen eines administrativen Abbilds

Bei einer [administrativen Installation](administrative-installation.md) wird ein Quell Abbild einer Anwendung oder eines Produkts in einem Netzwerk erstellt. Benutzer in einer Arbeitsgruppe, die Zugriff auf dieses administrative image haben, können das Produkt aus dieser Quelle installieren. Das Aktualisieren der Anwendung für diese Arbeitsgruppe erfolgt in zwei Schritten:

-   Zuerst kann der Patch für kleine Updates auf das administrative Abbild angewendet werden.
-   Zweitens müssen die Änderungen am kleinen Update an die Benutzer weitergegeben werden.

**So wenden Sie einen kleinen Update Patch auf ein administratives Image an**

1.  Abrufen des kleinen Updates in Form eines [Patchpakets](patch-packages.md) Beispielsweise das kleine Update mit dem Namen Patch. msp.
2.  Abrufen des Pfads zum administrativen Image.
3.  Verwenden Sie in der Befehlszeile Folgendes:

    **msiexec/a** *\[ Pfad zur \] Datei "administrativer Image. msi* " **/p** *Patch. msp*

4.  Dadurch werden die Anwendungs Dateien und die MSI-Datei des administrativen Abbilds aktualisiert. Eine Liste der Optionen, die mit Msiexec.exe verwendet werden können, finden Sie unter [Befehlszeilenoptionen](command-line-options.md). Windows Installer ermittelt automatisch, ob das administrative image kurze Dateinamen verwendet, und legt die [**shortfileames**](shortfilenames.md) -Eigenschaft fest.
5.  Das resultierende administrative image ist identisch mit dem, das von einer administrativen Installation mithilfe einer vollständigen Produkt-CD-ROM erstellt wurde, die das Update enthält. Wenn neue Benutzer die Anwendung aus dieser Quelle installieren, erhalten Sie die aktualisierte Anwendung.

**So verteilen Sie das kleine Update an die Arbeitsgruppe**

-   Mitglieder der Arbeitsgruppe erhalten die Änderungen, indem Sie die Anwendung über das administrative image neu installieren. verwenden Sie hierzu das unter [Anwenden von kleinen Updates durch Neuinstallieren des Produkts](applying-small-updates-by-reinstalling-the-product.md)beschriebene Verfahren.

 

 



