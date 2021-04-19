---
description: Ressourcen, die für die Anpassung einer Anwendung benötigt werden, z. b. Unternehmens Vorlagen, können mit der Anwendung bereitgestellt werden, indem eine Transformation mit dem Installationspaket der Anwendung eingeschlossen wird.
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: Verwenden von Transformationen zum Hinzufügen von Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c11fac7ad65601286fb550abd950bf5ac49af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356175"
---
# <a name="using-transforms-to-add-resources"></a>Verwenden von Transformationen zum Hinzufügen von Ressourcen

Ressourcen, die für die Anpassung einer Anwendung benötigt werden, z. b. Unternehmens Vorlagen, können mit der Anwendung bereitgestellt werden, indem eine Transformation mit dem Installationspaket der Anwendung eingeschlossen wird. Beim Bereitstellen von Ressourcen, wie z. b. Dateien, Registrierungs Schlüsseln oder Verknüpfungen, mithilfe einer Transformation müssen folgende Regeln befolgt werden.

-   Die Transformation sollte der Installations Datenbank eine oder mehrere neue Komponenten hinzufügen, um die zusätzlichen Ressourcen zu enthalten. Die Transformation sollte einer Komponente, die bereits in der Installation vorhanden ist, keine Ressourcen hinzufügen.
-   Die Transformation sollte der Installations Datenbank eine oder mehrere neue Funktionen hinzufügen, um diese neuen Komponenten zu enthalten. Diese neuen Features sollten nicht die übergeordneten Elemente vorhandener Funktionen sein, aber es können auch neue über-und untergeordnete Funktionen integriert werden. Neuen Features sollten Namen zugewiesen werden, die für alle anderen Transformationen für dieses Produkt eindeutig sind. Zwei Transformationen sollten dem Produkt, das in der featurespalte der [Featuretabelle](feature-table.md) mit dem gleichen Namen aufgeführt ist und verschiedene Komponenten oder Ressourcen enthält, nie eine Funktion hinzufügen.

 

 



