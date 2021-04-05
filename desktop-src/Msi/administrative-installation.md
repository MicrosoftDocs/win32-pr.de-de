---
description: Der Windows Installer kann eine administrative Installation einer Anwendung oder eines Produkts in einem Netzwerk ausführen, das von einer Arbeitsgruppe verwendet werden kann.
ms.assetid: 5840cfab-a127-4b1f-a7af-a2d8e2786928
title: Administrative Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3958bdc81ee43cd1a36e0d464f3e77032b4c2d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042158"
---
# <a name="administrative-installation"></a>Administrative Installation

Der Windows Installer kann eine administrative Installation einer Anwendung oder eines Produkts in einem Netzwerk ausführen, das von einer Arbeitsgruppe verwendet werden kann. Bei einer administrativen Installation wird ein Quell Abbild der Anwendung auf dem Netzwerk installiert, das einem Quell Abbild auf einer CD-ROM ähnelt. Benutzer in einer Arbeitsgruppe, die Zugriff auf dieses administrative image haben, können dann das Produkt aus dieser Quelle installieren. Ein Benutzer muss zuerst das Produkt aus dem Netzwerk installieren, um die Anwendung auszuführen. Der Benutzer kann auswählen, ob er bei der Installation von der Quelle ausgeführt wird, und das Installationsprogramm verwendet den größten Teil der Produktdatei direkt aus dem Netzwerk.

Administratoren können eine administrative Installation über die Befehlszeile ausführen, indem Sie die [Befehlszeilenoption](command-line-options.md)/a verwenden.

Die [Administrator Aktion](admin-action.md) ist die Aktion der obersten Ebene, mit der eine administrative Installation initiiert wird. Wenn diese Aktion ausgeführt wird, ruft das Installationsprogramm die Aktionen in den Tabellen " [AdminExecuteSequence](adminexecutesequence-table.md) " und " [AdminUISequence](adminuisequence-table.md) " auf, um die administrative Installation durchzuführen.

Die [**adminproperties**](adminproperties.md) -Eigenschaft ist eine durch Semikolons getrennte Liste der Eigenschaften, die zum Zeitpunkt der Installation der-Verwaltung festgelegt werden. Das Installationsprogramm verwendet diese Eigenschaften während einer Installation der Anwendung nach der Verwaltung über das administrative image.

Benutzer, die keinen kontinuierlichen Zugriff auf das Netzwerk haben, können eine Anwendung von einem Administrator Abbild installieren und sich dann manchmal auf Medien wie CD-ROM-Datenträgern als Sicherungs Quelle verlassen. In diesen Fällen muss die Länge der Dateinamen im administrativen Image und auf dem Medium Stimmen. Beide müssen lange Dateinamen verwenden, oder beide müssen kurze Dateinamen verwenden. Beispielsweise könnte eine CD-ROM, die nur kurze Dateinamen unterstützt, sowohl die ursprünglichen Medien für die Installation des administrativen Abbilds als auch eine Sicherungs Quelle bereitstellen.

Wenn die Eigenschaft [**shortfile Ames**](shortfilenames.md) während einer administrativen Installation festgelegt wird, muss diese Eigenschaft möglicherweise erneut von einem Benutzer festgelegt werden, der anschließend einen Patch auf das administrative image anwendet. Wenn Sie Windows Installer zum Anwenden des Patches verwenden, legt das Installationsprogramm automatisch die **shortfileames** -Eigenschaft fest, wenn das administrative image kurze Dateinamen verwendet.

Wenn ein Administrator ein Paket mit der Eigenschaft " [**Anzahl der Wort Zählung**](word-count-summary.md) " 2 oder 3 verwendet, um eine administrative Installation durchzuführen, können Benutzer des administrativen Abbilds aus der ursprünglichen Medienquelle nicht automatisch neu installieren. Wenn das administrative image nicht mehr verfügbar ist, können Benutzer, die über das administrative Abbild installiert haben, nicht auf die ursprünglichen Medien zurückkehren.

Die Anwendung von [*Transformationen*](t-gly.md) während der Erstellung eines administrativen Abbilds hat keine gültige Auswirkung. Wenn Sie einer Arbeitsgruppe eine angepasste Version eines Produkts zur Verfügung stellen möchten, wenden Sie die Transformation während der Installation des Produkts aus dem administrativen Image an.

Während einer administrativen Installation erstellt das Installationsprogramm ein Quell Abbild für alle Features im Produkt, ausgenommen diese Features mit 0 in der Spalte Ebene der [Featuretabelle](feature-table.md).

 

 



