---
description: Im folgenden Verfahren wird ein Szenario zum Generieren einer Transformation beschrieben, die eine Funktion dauerhaft verbirgt.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Erstellen einer Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0543ae74f71155e6fcd504ebee677558f21bbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042541"
---
# <a name="generating-a-transform"></a>Erstellen einer Transformation

Im folgenden Verfahren wird ein Szenario zum Generieren einer Transformation beschrieben, die eine Funktion dauerhaft verbirgt.

**So blenden Sie eine Produkt Funktion dauerhaft aus**

1.  Kopieren Sie das ursprüngliche Installationspaket.
2.  Ändern Sie die Kopie, indem Sie den Wert der Anzeige Spalte in der [Featuretabelle](feature-table.md) auf NULL festlegen. Dies gibt das Ausblenden des Features an.
3.  Erstellen Sie eine Transformation vom ursprünglichen Installationspaket zu den neuen Installationspaketen, indem Sie [**msidatabasegeneratetransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)aufrufen.
4.  Erstellen Sie die Zusammenfassungs Informationen in der Transformation, indem Sie [**msicreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)aufrufen.

Die Transformation kann dann während der Installation angewendet werden. Weitere Informationen finden Sie unter [Anwenden von Transformationen](applying-transforms.md).

 

 



