---
description: Mergemodule stellen eine Standardmethode bereit, mit der Entwickler freigegebene Windows Installer Komponenten und Setup Logik für Ihre Anwendungen bereitstellen.
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: Mergemodule
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218344"
---
# <a name="merge-modules"></a>Mergemodule

Mergemodule stellen eine Standardmethode bereit, mit der Entwickler freigegebene Windows Installer [*Komponenten*](c-gly.md) und Setup Logik für Ihre Anwendungen bereitstellen. Mergemodule werden verwendet, um freigegebenen Code, Dateien, Ressourcen, Registrierungseinträge und Setup Logik als einzelne Verbund Datei an Anwendungen zu übermitteln. Entwickler, die neue Mergemodule erstellen oder vorhandene Mergemodule verwenden, sollten den in diesem Abschnitt beschriebenen Standard befolgen.

Ein Mergemodul ähnelt der Struktur einer vereinfachten Windows Installer [*. msi-Datei*](m-gly.md). Allerdings kann ein Mergemodul nicht allein installiert werden, sondern es muss mithilfe eines Merge-Tools in einem Installationspaket zusammengeführt werden. Entwickler, die Mergemodule verwenden möchten, müssen eines der frei verteilten mergetools (z. b. Mergemod.dll) abrufen oder ein Mergetool von einem unabhängigen Softwarehersteller erwerben. Entwickler können neue Mergemodule erstellen, indem Sie viele derselben Software Tools verwenden, die zum Erstellen eines Windows Installer Installationspakets verwendet werden, z. b. den Datenbanktabellen-Editor, der mit dem Windows Installer SDK bereitgestellt wird.

Wenn ein Mergemodul in die MSI-Datei einer Anwendung zusammengeführt wird, werden alle Informationen und Ressourcen, die für die Installation der vom Mergemodul gelieferten Komponenten erforderlich sind, in die MSI-Datei der Anwendung integriert. Das Mergemodul ist dann nicht mehr erforderlich, um diese Komponenten zu installieren, und das Mergemodul muss für einen Benutzer nicht verfügbar sein. Da alle Informationen, die zum Installieren der Komponenten erforderlich sind, als einzelne Datei bereitgestellt werden, können durch die Verwendung von Mergemodulen viele Instanzen von Versions Konflikten, fehlende Registrierungseinträge und nicht ordnungsgemäß installierte Dateien eliminiert werden.

Weitere Informationen zu Mergemodulen finden Sie unter:

-   [Informationen zu Mergemodulen](about-merge-modules.md)
-   [Verwenden von Mergemodulen](using-merge-modules.md)
-   [Modul Verweis zusammenführen](merge-module-reference.md)

 

 



