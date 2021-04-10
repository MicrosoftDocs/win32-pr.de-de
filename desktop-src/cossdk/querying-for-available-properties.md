---
description: Abfragen von verfügbaren Eigenschaften
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Abfragen von verfügbaren Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127401"
---
# <a name="querying-for-available-properties"></a>Abfragen von verfügbaren Eigenschaften

Wenn Sie ein allgemeines Verwaltungs Tool schreiben, müssen Sie höchstwahrscheinlich Routinen zum Festlegen von Eigenschaften mit vollständiger Generalität schreiben. Um dies zu unterstützen, gibt es eine Funktion, die es Ihnen ermöglicht, die Eigenschaften, die für die Elemente in einer bestimmten Sammlung verfügbar sind, dynamisch abzufragen.

Die [**PropertyInfo**](propertyinfo.md) -Auflistung ist in jeder Auflistung verfügbar, die Sie möglicherweise halten. Die **PropertyInfo** -Auflistung enthält ein Element für jede verfügbare Eigenschaft. Sie können diese Elemente durchlaufen, um zu bestimmen, ob eine bestimmte Eigenschaft verfügbar ist.

Sie können die [**PropertyInfo**](propertyinfo.md) -Auflistung von einer beliebigen Auflistung mit der [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) -Methode für das [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt erhalten, wobei der zweite Parameter leer bleibt, wo Sie normalerweise die Schlüsseleigenschaft eines übergeordneten Elements angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften werden erhalten und festgelegt](getting-and-setting-properties.md)
</dt> <dt>

[Abhängigkeiten zwischen Eigenschaften](interdependencies-between-properties.md)
</dt> <dt>

[Speichern oder Verwerfen von Änderungen](saving-or-discarding-changes.md)
</dt> </dl>

 

 



