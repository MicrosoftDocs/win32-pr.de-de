---
title: Die STGMEDIUM-Struktur
description: Die STGMEDIUM-Struktur
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da0adc98b5d774754bd2cbbccb415092d6498684a60189d6346afac82bd270a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992270"
---
# <a name="the-stgmedium-structure"></a>Die STGMEDIUM-Struktur

Ebenso wie die [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) eine Erweiterung des Formatbezeichners der Windows-Zwischenablage ist, ist die [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) eine Verbesserung des globalen Speicherhandles, das zum Übertragen der Daten verwendet wird. Die **STGMEDIUM-Struktur** enthält einen Member, tymed , der das zu verwendende Medium angibt, und eine Union, die Zeiger und ein Handle zum Abrufen des in **tymed** angegebenen **Mediums enthält.**

Die [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) ermöglicht es Datenquellen und Consumers, das effizienteste Austauschmedium pro Rendering zu wählen. Wenn die Daten so groß sind, dass sie auf dem Datenträger aufbewahrt werden sollen, kann die Datenquelle ein datenträgerbasiertes Medium im bevorzugten Format angeben und nur dann globalen Arbeitsspeicher als Sicherung verwenden, wenn dies das einzige Medium ist, das der Consumer versteht. Die Möglichkeit, das beste Medium als Standard für den Austausch zu verwenden, verbessert die Gesamtleistung des Datenaustauschs zwischen Anwendungen. Wenn sich einige der zu übertragenden Daten beispielsweise bereits auf dem Datenträger befindet, kann die Quellanwendung sie verschieben oder in ein neues Ziel kopieren, entweder in derselben Anwendung oder in einer anderen Anwendung, ohne die Daten zuerst in den globalen Arbeitsspeicher laden zu müssen. Am empfangenden Ende muss der Consumer der Daten diese nicht auf den Datenträger zurückschreiben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenformate und Übertragungsmedien](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




