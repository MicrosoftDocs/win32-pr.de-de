---
description: Jedes Element in einer Auflistung macht Eigenschaften verfügbar.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Bearbeiten von Eigenschaften im com+-Katalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed2bade8886fe08bb7ed1ece179b35677569f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748273"
---
# <a name="editing-properties-in-the-com-catalog"></a>Bearbeiten von Eigenschaften im com+-Katalog

Jedes Element in einer Auflistung macht Eigenschaften verfügbar. Diese Eigenschaften dienen zum Speichern von Konfigurationsdaten für jedes Element, das das Element darstellt. Diese Eigenschaften werden im Verwaltungs Programmkomponenten Dienste auf einer Eigenschaften Seite angezeigt, auf die Sie zugreifen können, indem Sie mit der rechten Maustaste auf ein Element in einem Ordner klicken.

Da die Elemente in einer bestimmten Auflistung alle dieselbe Art darstellen, machen diese Elemente einen Satz von Eigenschaften verfügbar, der in der gesamten Auflistung konsistent ist. Beispielsweise macht die [**Anwendungs**](applications.md) Auflistung eine Name-Eigenschaft, eine AppID-Eigenschaft usw. verfügbar. Dies entspricht der Art und Weise, wie die einzelnen Anwendungen im Verwaltungs Programmkomponenten Dienste eine einheitlich strukturierte Eigenschaften Seite für die Anwendung bereitstellen. Eine Liste der Eigenschaften, die für die **Anwendungs** Sammlung verfügbar sind, finden Sie unter **Anwendungen**. Eine Liste der Eigenschaften, die für die [**Komponenten**](components.md) Auflistung verfügbar sind, finden Sie unter **Komponenten**.

Eine umfassende Liste der Eigenschaften, die von Elementen in jeder Sammlung verfügbar gemacht werden, finden Sie unter [com+-Verwaltungs Sammlungen](com--administration-collections.md).

Sie stellen ein Element in einer Auflistung dar, indem Sie ein Objekt verwenden, das aus der [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse erstellt wurde. Mit diesem Objekt können Sie alle Eigenschaften, die vom Element verfügbar gemacht werden, festlegen und erhalten. Beim Festlegen von Eigenschaften ist es auch möglich, dass Sie mit einem anderen Writer mit dem com+-Katalog in Konflikt stehen. Weitere Informationen finden Sie unter " [erhalten und Festlegen von Eigenschaften](getting-and-setting-properties.md)".

Nachdem Sie die Eigenschaften festgelegt haben, wird tatsächlich ein Commit für die Änderungen ausgeführt, bis Sie die Änderungen explizit speichern. Weitere Informationen finden Sie unter [Speichern oder Verwerfen von Änderungen](saving-or-discarding-changes.md).

Wenn Sie Änderungen speichern, erzwingt der com+-Katalog einige Konfigurations Logik, um sicherzustellen, dass keine inkompatiblen Konfigurationen festgelegt werden. Außerdem werden einige Eigenschaften geändert, wenn Sie bestimmte andere Eigenschaften explizit ändern. Weitere Informationen finden Sie unter Abhängigkeiten [zwischen Eigenschaften](interdependencies-between-properties.md).

Außerdem verfügt com+ über eine Funktion, mit der Sie dynamisch Abfragen können, um festzustellen, welche Eigenschaften für die Elemente in einer bestimmten Sammlung verfügbar sind. Weitere Informationen finden Sie unter [Abfragen von verfügbaren Eigenschaften](querying-for-available-properties.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Verwaltungsvorgänge in Transaktionen](com--administration-operations-within-transactions.md)
</dt> <dt>

[Behandeln von com+-Verwaltungsfehlern](handling-com--administration-errors.md)
</dt> <dt>

[Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Abrufen von Auflistungen im com+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



