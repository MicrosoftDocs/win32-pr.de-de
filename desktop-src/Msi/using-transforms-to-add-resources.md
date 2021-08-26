---
description: Ressourcen, die für die Anpassung einer Anwendung erforderlich sind, z. B. Unternehmensvorlagen, können mit der Anwendung bereitgestellt werden, indem eine Transformation mit dem Installationspaket der Anwendung bereitgestellt wird.
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: Verwenden von Transformationen zum Hinzufügen von Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2999371079ac57d0e44800c9374d496db6eb400864fed3422d88f2b03731724
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038990"
---
# <a name="using-transforms-to-add-resources"></a>Verwenden von Transformationen zum Hinzufügen von Ressourcen

Ressourcen, die für die Anpassung einer Anwendung erforderlich sind, z. B. Unternehmensvorlagen, können mit der Anwendung bereitgestellt werden, indem eine Transformation mit dem Installationspaket der Anwendung bereitgestellt wird. Die folgenden Regeln sollten beim Bereitstellen von Ressourcen wie Dateien, Registrierungsschlüsseln oder Verknüpfungen mithilfe einer Transformation befolgt werden.

-   Die Transformation sollte der Installationsdatenbank eine oder mehrere neue Komponenten hinzufügen, um die zusätzlichen Ressourcen zu enthalten. Die Transformation sollte einer Komponente, die bereits in der Installation vorhanden ist, keine Ressourcen hinzufügen.
-   Die Transformation sollte der Installationsdatenbank ein oder mehrere neue Features hinzufügen, um diese neuen Komponenten zu enthalten. Diese neuen Features sollten nicht die übergeordneten Elemente vorhandener Features sein, aber neue übergeordnete und untergeordnete Features können zusammen eingeführt werden. Neuen Features sollten Namen gegeben werden, die für alle anderen Transformationen für dieses Produkt eindeutig sind. Keine zwei Transformationen sollten diesem Produkt jemals ein Feature hinzufügen, das den gleichen Namen hat, der in der Spalte Feature der Tabelle [Feature](feature-table.md) aufgeführt ist und verschiedene Komponenten oder Ressourcen enthält.

 

 



