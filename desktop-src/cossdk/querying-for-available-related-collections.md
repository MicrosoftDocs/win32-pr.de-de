---
description: Abfragen von verfügbaren verwandten Sammlungen
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: Abfragen von verfügbaren verwandten Sammlungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0203df5bb7b5bf89396d5687dc28b19e9b183d56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342319"
---
# <a name="querying-for-available-related-collections"></a>Abfragen von verfügbaren verwandten Sammlungen

Wenn Sie ein allgemeines Verwaltungs Tool schreiben, ist es wahrscheinlich, dass Sie Routinen für die Navigation in der gesamten Sammlungs Hierarchie schreiben müssen. Um dies zu unterstützen, verfügt com+ über eine Funktion, die es Ihnen ermöglicht, die verknüpften Auflistungen, die in einer bestimmten Sammlung verfügbar sind, dynamisch abzufragen

Die [**relatedcollectioninfo**](relatedcollectioninfo.md) -Auflistung ist in jeder Auflistung verfügbar, die Sie möglicherweise beibehalten, und enthält ein Element für jede verfügbare verknüpfte Auflistung. Sie können diese Elemente durchlaufen, um zu bestimmen, ob eine bestimmte Sammlung verfügbar ist.

Sie können die [**relatedcollectioninfo**](relatedcollectioninfo.md) -Auflistung aus einer beliebigen Auflistung mit der [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) -Methode für das [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt erhalten, wobei der zweite Parameter leer bleibt, wo Sie normalerweise die Schlüsseleigenschaft eines übergeordneten Elements angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Navigieren in der com+-Sammlungs Hierarchie](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Com+-Sammlungen werden aufgefüllt.](populating-com--collections.md)
</dt> <dt>

[Abrufen von Auflistungen im com+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



