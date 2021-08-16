---
description: Abrufen und Festlegen von Eigenschaften
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Abrufen und Festlegen von Eigenschaften (Komponentendienste)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805d98463e1f9b8f08c1018b49554c95e2735bfa7ea6dca21d90243eb324df49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306755"
---
# <a name="getting-and-setting-properties-component-services"></a>Abrufen und Festlegen von Eigenschaften (Komponentendienste)

Bevor Sie bestimmte Eigenschaften lesen oder schreiben können, die von einem Element in einer Sammlung verfügbar gemacht werden, müssen Sie die folgenden Schritte ausführen:

1.  Rufen Sie die Auflistung ab.
2.  Füllen Sie die Sammlung auf, um Daten aus dem COM+-Katalog einlesen zu können.
3.  Rufen Sie das bestimmte Element in der Auflistung ab, das es mit einem -Objekt aus der [**COMAdminCatalogObject-Klasse**](comadmincatalogobject.md) darstellt.

Ein Beispiel, das diese Schritte veranschaulicht, finden Sie unter [Navigieren in der COM+-Sammlungshierarchie.](navigating-the-com--collection-hierarchy.md)

Da die jeweiligen verfügbar gemachten Eigenschaften je nach dem, was das Element darstellt, variieren können. Das heißt, ein Element, das eine Komponente darstellt, verfügt über andere Eigenschaften als eine, die eine COM+-Anwendung darstellt. Legen Sie eine dieser Eigenschaften mithilfe einer einzelnen generischen Eigenschaft, der Value-Eigenschaft, für [**COMAdminCatalogObject fest.**](comadmincatalogobject.md)

Mit der Value-Eigenschaft können Sie eine bestimmte benannte Eigenschaft abrufen oder festlegen, die von einem Element verfügbar gemacht wird, einen Wert für eine benannte Eigenschaft beim Abrufen zurückgeben und beim Festlegen einen Namen und einen Wert verwenden.

Es werden keine Änderungen am COM+-Katalog aufgezeichnet, bis Sie Änderungen explizit mithilfe der [**SaveChanges-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) im [**COMAdminCatalogCollection-Objekt**](comadmincatalogcollection.md) speichern. Ausstehende Änderungen für alle Eigenschaften aller Elemente in einer bestimmten Auflistung werden alle auf einmal gespeichert. Weitere Informationen finden Sie unter [Speichern oder Verwerfen von Änderungen.](saving-or-discarding-changes.md)

Nicht alle Änderungen, die Sie vornehmen, werden akzeptiert. Der COM+-Katalog erzwingt eine gewisse Parallelitätslogik, um sicherzustellen, dass Sie die Dinge auf sinnvolle Weise konfigurieren. Wenn Sie darüber hinaus einige Eigenschaften ändern, ändern sich andere möglicherweise automatisch durch dieselbe Parallelitätslogik. Diese Auswirkungen werden beim Versuch, Änderungen zu speichern, deutlich.

> [!Note]  
> Es ist möglich, dass Sie mit einem anderen Writer für den COM+-Katalog in Einem-Zusammenhang sind. Zwischen den Aufrufen [**von Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) und [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) für eine bestimmte Sammlung ist keine Sperre für diese Daten im Katalog verfügbar. Es kann sein, dass mehrere Parteien gleichzeitig Elemente in einer bestimmten Sammlung konfigurieren und sich beim Speichern von Änderungen einen Konflikt damit machen können. Dies bedeutet, dass eine andere Person die Einstellungen für ein Objekt vor oder nach der Ausführung ändern kann, indem sie entweder eine Art von Programm mithilfe der COMAdmin-Objekte oder das Verwaltungstool komponentendienste lokal oder remote ausführen. Die allgemeine Regel beim Schreiben von Objekten im Katalog ist, dass alle Eigenschaften eines Objekts gleichzeitig geschrieben werden. Das heißt, der letzte Writer gewinnt – das Objekt wird im Katalog genau so gespeichert, wie es vom letzten Writer konfiguriert wurde.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abhängigkeiten zwischen Eigenschaften](interdependencies-between-properties.md)
</dt> <dt>

[Abfragen verfügbarer Eigenschaften](querying-for-available-properties.md)
</dt> <dt>

[Speichern oder Verwerfen von Änderungen](saving-or-discarding-changes.md)
</dt> </dl>

 

 



