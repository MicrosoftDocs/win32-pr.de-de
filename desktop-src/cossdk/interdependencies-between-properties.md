---
description: Abhängigkeiten zwischen Eigenschaften
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Abhängigkeiten zwischen Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb039db26ee06868da0b1832e1a3af2692ac47cde73bf7fe5c2e934916c4f4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547672"
---
# <a name="interdependencies-between-properties"></a>Abhängigkeiten zwischen Eigenschaften

Wenn Sie Eigenschaften festlegen, erzwingt der COM+-Katalog eine gewisse Parallelitätslogik, um sicherzustellen, dass Sie Elemente auf sinnvolle Weise konfigurieren. Diese Logik kann auf zwei Arten implementiert werden:

-   **Abhängigkeiten:** Es kann sein, dass Sie einige Änderungen nicht vornehmen können, da eine andere Eigenschaft von einer bestimmten Einstellung für eine Eigenschaft abhängt, die Sie festlegen möchten. Wenn beispielsweise eine Komponente mit dem Attribut Transaktionen erforderlich festgelegt ist und Sie dann versuchen, die Synchronisierungseinstellung in Keine zu ändern, wird beim Versuch, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) aufrufen, ein Fehler generiert, da Transaktionen von der Synchronisierung abhängen.
-   **Nebenwirkungen.** Einige Eigenschaften können für Sie geändert werden, ohne dass Sie sie explizit festlegen. Wenn Sie beispielsweise eine Komponente mit dem Attribut Transaktionen erforderlich festlegen, wird Synchronisierung auch auf Erforderlich festgelegt. Dies ist tatsächlich die Kehrseite von Abhängigkeiten– eine Eigenschaft hat Vorrang vor einer anderen, und ihre Abhängigkeit wird ausgedrückt, indem zuerst die sekundäre Eigenschaft und dann Änderungen an ihr blockiert werden.

In der Liste der Eigenschaften, die von Elementen in einer Sammlung verfügbar gemacht werden, die alle in [COM+-Verwaltungssammlungen](com--administration-collections.md)aufgeführt sind, werden die Abhängigkeiten und Nebeneffekte für jede Eigenschaft angegeben. Wenn Sie COM+-Anwendungen und -Komponenten konfigurieren, sollten Sie wissen, welche Einschränkungen für Konfigurationen gelten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abrufen und Festlegen von Eigenschaften](getting-and-setting-properties.md)
</dt> <dt>

[Abfragen verfügbarer Eigenschaften](querying-for-available-properties.md)
</dt> <dt>

[Speichern oder Verwerfen von Änderungen](saving-or-discarding-changes.md)
</dt> </dl>

 

 



