---
description: Der Windows Installer kann eine Administrative Installation einer Anwendung oder eines Produkts in einem Netzwerk für die Verwendung durch eine Arbeitsgruppe ausführen.
ms.assetid: 5840cfab-a127-4b1f-a7af-a2d8e2786928
title: Administratorinstallation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26968b6b81c1c2aafedfd74151b139f61062baa29c44b04977a119b14ab1a8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381850"
---
# <a name="administrative-installation"></a>Administratorinstallation

Der Windows Installer kann eine Administrative Installation einer Anwendung oder eines Produkts in einem Netzwerk für die Verwendung durch eine Arbeitsgruppe ausführen. Bei einer Administratorinstallation wird ein Quellimage der Anwendung im Netzwerk installiert, das einem Quellimage auf einer CD-ROM ähnelt. Benutzer in einer Arbeitsgruppe, die Zugriff auf dieses Administratorimage haben, können das Produkt dann aus dieser Quelle installieren. Ein Benutzer muss das Produkt zunächst aus dem Netzwerk installieren, um die Anwendung auszuführen. Der Benutzer kann bei der Installation von der Quelle ausführen, und der Installer verwendet den Großteil der Produktdatei direkt aus dem Netzwerk.

Administratoren können eine Administratorinstallation über die Befehlszeile ausführen, indem sie die [Befehlszeilenoption](command-line-options.md)/a verwenden.

Die [ADMIN-Aktion](admin-action.md) ist die Aktion der obersten Ebene, die zum Initiieren einer Administratorinstallation verwendet wird. Wenn diese Aktion ausgeführt wird, ruft das Installationsprogramm die Aktionen in den Tabellen [AdminExecuteSequence](adminexecutesequence-table.md) und [AdminUISequence](adminuisequence-table.md) auf, um die Administratorinstallation durchzuführen.

Die [**AdminProperties-Eigenschaft**](adminproperties.md) ist eine durch Semikolons getrennte Liste von Eigenschaften, die zum Zeitpunkt einer Administratorinstallation festgelegt werden. Das Installationsprogramm verwendet diese Eigenschaften während einer Installation der Anwendung nach der Verwaltung aus dem Administratorimage.

Benutzer, die keinen kontinuierlichen Zugriff auf das Netzwerk haben, können eine Anwendung über ein Administratorimage installieren und müssen sich dann manchmal auf Medien wie CD-ROM-Datenträger als Sicherungsquelle verlassen. In diesen Fällen muss die Länge der Dateinamen im administrativen Image und auf den Medien übereinstimmen. Beide müssen lange Dateinamen oder beide kurze Dateinamen verwenden. Beispielsweise könnte eine CD-ROM, die nur kurze Dateinamen unterstützt, sowohl das ursprüngliche Medium für die Installation des Administrativen Images als auch eine Sicherungsquelle bereitstellen.

Wenn die [**SHORTFILENAMES-Eigenschaft**](shortfilenames.md) während einer Administratorinstallation festgelegt wird, muss diese Eigenschaft möglicherweise erneut von einem Benutzer festgelegt werden, der anschließend einen Patch auf das Administrative Image anwendet. Wenn Windows Installer zum Anwenden des Patches verwendet wird, legt das Installationsprogramm automatisch die **SHORTFILENAMES-Eigenschaft** fest, wenn das Administrative Image kurze Dateinamen verwendet.

Wenn ein Administrator ein Paket mit der [**Word Count Summary-Eigenschaft**](word-count-summary.md) 2 oder 3 verwendet, um eine Administratorinstallation durchzuführen, können Benutzer des Administrativen Images nicht automatisch aus der ursprünglichen Medienquelle neu installieren. Wenn das Administratorimage nicht mehr verfügbar ist, können Benutzer, die über das Administratorimage installiert haben, nicht auf die ursprünglichen Medien zurückgesetzt werden.

Die Anwendung von Transformationen während der Erstellung eines [*administrativen*](t-gly.md) Images hat keine gültigen Auswirkungen. Um einer Arbeitsgruppe eine angepasste Version eines Produkts zur Verfügung zu stellen, wenden Sie die Transformation während der Installation des Produkts aus dem Administratorimage an.

Während einer Administratorinstallation erstellt das Installationsprogramm ein Quellimage für alle Features im Produkt, mit Ausnahme der Features mit 0 (0) in der Spalte Ebene der [Featuretabelle](feature-table.md).

 

 



