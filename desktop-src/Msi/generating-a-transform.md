---
description: Das folgende Verfahren beschreibt ein Szenario zum Generieren einer Transformation, die ein Feature dauerhaft ausblendet.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Generieren einer Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df605dd01a494089d2e6ecd38c8b3c6d03ecb5d6335e2348682e1af16f79faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635988"
---
# <a name="generating-a-transform"></a>Generieren einer Transformation

Das folgende Verfahren beschreibt ein Szenario zum Generieren einer Transformation, die ein Feature dauerhaft ausblendet.

**So blenden Sie ein Produktfeature dauerhaft aus**

1.  Kopieren Sie das ursprüngliche Installationspaket.
2.  Ändern Sie die Kopie, indem Sie den Wert der Spalte Anzeigen in der [Tabelle Feature auf](feature-table.md) 0 (null) festlegen. Dies gibt an, dass das Feature verborgen wird.
3.  Erstellen Sie eine Transformation vom ursprünglichen Installationspaket zu den neuen Installationspaketen, indem [**Sie MsiDatabaseGenerateTransform aufrufen.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)
4.  Erstellen Sie die Zusammenfassungsinformationen in der Transformation, indem Sie [**MsiCreateTransformSummaryInfo aufrufen.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

Die Transformation kann dann während der Installation angewendet werden. Weitere Informationen finden Sie unter [Anwenden von Transformationen.](applying-transforms.md)

 

 



