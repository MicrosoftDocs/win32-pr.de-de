---
description: Eine Administratorinstallation erstellt ein Quellimage einer Anwendung oder eines Produkts in einem Netzwerk.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Anwenden kleiner Updates durch Patchen eines administrativen Images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02c8e3eb606dc92c60a86dd8e3216cbc99603200a87e5ee5dda0983fb7ad34d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559160"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a>Anwenden kleiner Updates durch Patchen eines administrativen Images

Eine [Administratorinstallation](administrative-installation.md) erstellt ein Quellimage einer Anwendung oder eines Produkts in einem Netzwerk. Benutzer in einer Arbeitsgruppe, die Zugriff auf dieses Administrative Image haben, können das Produkt aus dieser Quelle installieren. Das Aktualisieren der Anwendung für diese Arbeitsgruppe erfolgt in zwei Schritten:

-   Zunächst kann der kleine Updatepatch auf das Administratorimage angewendet werden.
-   Zweitens müssen die Änderungen im kleinen Update an die Benutzer weitergegeben werden.

**So wenden Sie einen kleinen Updatepatch auf ein Administratorimage an**

1.  Rufen Sie das kleine Update in Form eines [Patchpakets ab.](patch-packages.md) Beispiel: das kleine Update mit dem Namen Patch.msp.
2.  Rufen Sie den Pfad zum Administratorimage ab.
3.  Verwenden Sie in der Befehlszeile Folgendes:

    **msiexec /a** *\[ path to administrative image \] .msi file* **/p** *patch.msp*

4.  Dadurch werden die Anwendungsdateien und die .msi Datei des Administratorimages aktualisiert. Eine Liste der Optionen, die mit Msiexec.exe verwendet werden können, finden Sie unter [Befehlszeilenoptionen.](command-line-options.md) Windows Das Installationsprogramm bestimmt automatisch, ob das Administrative Image kurze Dateinamen verwendet, und legt die [**SHORTFILENAMES-Eigenschaft**](shortfilenames.md) fest.
5.  Das resultierende Administratorimage entspricht dem, das von einer Administratorinstallation mithilfe einer vollständigen CD-ROM erstellt wird, die das Update enthält. Wenn neue Benutzer die Anwendung aus dieser Quelle installieren, erhalten sie die aktualisierte Anwendung.

**So übertragen Sie das kleine Update an die Arbeitsgruppe**

-   Mitglieder der Arbeitsgruppe erhalten die Änderungen, indem sie die Anwendung mithilfe des unter [Anwenden kleiner Updates durch Erneutes Installieren des Produkts](applying-small-updates-by-reinstalling-the-product.md)beschriebenen Verfahrens aus dem Administratorimage neu installieren.

 

 



