---
description: Abhängigkeiten zwischen Eigenschaften
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Abhängigkeiten zwischen Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df8015c3fc49e35f5079315f6c056f680ebcc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958420"
---
# <a name="interdependencies-between-properties"></a>Abhängigkeiten zwischen Eigenschaften

Wenn Sie Eigenschaften festlegen, erzwingt der com+-Katalog einige Konsistenz Logik, um sicherzustellen, dass Sie Elemente auf sinnvolle Weise konfigurieren. Diese Logik kann auf zwei Arten implementiert werden, wie im folgenden dargestellt:

-   **Abhängigkeiten:** Sie werden möglicherweise daran gehindert, Änderungen vorzunehmen, weil eine andere Eigenschaft von einer bestimmten Einstellung für eine Eigenschaft abhängt, die Sie festlegen möchten. Wenn eine Komponente z. b. mit den erforderlichen Attribut Transaktionen festgelegt ist und Sie dann versuchen, die Synchronisierungs Einstellung in keine zu ändern, wird beim Versuch, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) aufzurufen, ein Fehler generiert, da die Transaktionen von der Synchronisierung abhängen.
-   **Nebeneffekte.** Einige Eigenschaften werden möglicherweise geändert, ohne dass Sie explizit festgelegt werden. Wenn Sie z. b. eine Komponente mit den erforderlichen Attribut Transaktionen festgelegt haben, wird die Synchronisierung auch auf Required festgelegt. Dies ist wirklich die Kehrseite der Abhängigkeiten – eine Eigenschaft hat Vorrang vor einer anderen Eigenschaft, und ihre Abhängigkeit wird durch das erste Festlegen der sekundären Eigenschaft und das anschließende Blockieren von Änderungen an der Eigenschaft ausgedrückt.

In der Liste der Eigenschaften, die von Elementen in einer Sammlung verfügbar gemacht werden und die in [com+-Administrations Sammlungen](com--administration-collections.md)aufgeführt sind, werden die Abhängigkeiten und Nebeneffekte für jede Eigenschaft angegeben. Wenn Sie com+-Anwendungen und-Komponenten konfigurieren, sollten Sie wissen, welche Einschränkungen für Konfigurationen gelten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften werden erhalten und festgelegt](getting-and-setting-properties.md)
</dt> <dt>

[Abfragen von verfügbaren Eigenschaften](querying-for-available-properties.md)
</dt> <dt>

[Speichern oder Verwerfen von Änderungen](saving-or-discarding-changes.md)
</dt> </dl>

 

 



