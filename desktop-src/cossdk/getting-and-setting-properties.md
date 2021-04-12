---
description: Eigenschaften werden erhalten und festgelegt
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Festlegen und Festlegen von Eigenschaften (Komponenten Dienste)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151b08293cd32a35cd27bdba4dd3a37cdebfa4f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483446"
---
# <a name="getting-and-setting-properties-component-services"></a>Festlegen und Festlegen von Eigenschaften (Komponenten Dienste)

Bevor Sie bestimmte Eigenschaften lesen oder schreiben können, die von einem Element in einer Sammlung verfügbar gemacht werden, müssen Sie die folgenden Schritte ausführen:

1.  Rufen Sie die-Auflistung ab.
2.  Füllen Sie die Sammlung aus, um Daten aus dem com+-Katalog einzulesen.
3.  Rufen Sie das spezifische Element in der Auflistung ab, das es mit einem Objekt aus der [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse darstellt.

Ein Beispiel, das diese Schritte veranschaulicht, finden Sie unter [Navigieren in der com+](navigating-the-com--collection-hierarchy.md)-Auflistungs Hierarchie.

Da die jeweils verfügbaren Eigenschaften variieren können, hängt davon ab, was das Element darstellt. Das heißt, ein Element, das eine Komponente darstellt, verfügt über andere Eigenschaften als eine, die eine COM+-Anwendung darstellt. Legen Sie eine dieser Eigenschaften mithilfe einer einzelnen generischen Eigenschaft (der Wert-Eigenschaft) für [**COMAdminCatalogObject**](comadmincatalogobject.md)fest.

Die Value-Eigenschaft ermöglicht es Ihnen, eine bestimmte benannte Eigenschaft, die von einem Element verfügbar gemacht wird, zu erhalten oder festzulegen, bei der Erstellung einen Wert für eine benannte Eigenschaft zurückzugeben und beim Festlegen einen Namen und einen Wert zu nehmen.

Es werden erst dann Änderungen im com+-Katalog aufgezeichnet, wenn Sie die Änderungen mithilfe der [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) -Methode für das [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt explizit speichern. Ausstehende Änderungen für alle Eigenschaften in allen Elementen in einer bestimmten Sammlung werden gleichzeitig gespeichert. Weitere Informationen finden Sie unter [Speichern oder Verwerfen von Änderungen](saving-or-discarding-changes.md).

Nicht alle Änderungen, die Sie vornehmen, werden akzeptiert. Der com+-Katalog erzwingt eine gewisse Konsistenz Logik, um sicherzustellen, dass Sie die Dinge auf sinnvolle Weise konfigurieren. Wenn Sie einige Eigenschaften ändern, können sich außerdem andere automatisch durch die gleiche Konsistenz Logik ändern. Diese Effekte werden angezeigt, wenn Sie versuchen, Änderungen zu speichern.

> [!Note]  
> Es ist möglich, dass Sie mit einem anderen Writer im com+-Katalog in Konflikt stehen. Zwischen Aufrufen von "Auffüllen [**" und "**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) " für eine bestimmte Sammlung verfügen Sie nicht über eine Sperre für diese Daten im Katalog. Mehrere Parteien können gleichzeitig Elemente in einer bestimmten Sammlung konfigurieren und können Konflikte aufweisen, wenn Sie Änderungen speichern. Dies bedeutet, dass eine andere Person die Einstellungen eines Objekts vor oder nach dem Ausführen ändern kann, entweder mithilfe der COMAdmin-Objekte oder mithilfe des Verwaltungs Programms Komponenten Dienste entweder lokal oder Remote. Die allgemeine Regel, bei der Objekte im Katalog geschrieben werden, besteht darin, dass alle Eigenschaften eines Objekts gleichzeitig geschrieben werden. Das heißt, der letzte Writer gewinnt – das Objekt wird im Katalog genau so gespeichert, wie es vom letzten Writer konfiguriert wurde.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abhängigkeiten zwischen Eigenschaften](interdependencies-between-properties.md)
</dt> <dt>

[Abfragen von verfügbaren Eigenschaften](querying-for-available-properties.md)
</dt> <dt>

[Speichern oder Verwerfen von Änderungen](saving-or-discarding-changes.md)
</dt> </dl>

 

 



