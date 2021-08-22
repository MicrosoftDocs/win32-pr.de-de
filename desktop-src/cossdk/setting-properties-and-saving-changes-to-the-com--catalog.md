---
description: Jedes Element in einer Auflistung macht Eigenschaften verfügbar.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Bearbeiten von Eigenschaften im COM+-Katalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ace2809fef4510a9c89b5faf31df555cb76426a06dd445aff9438c0d19e887
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546228"
---
# <a name="editing-properties-in-the-com-catalog"></a>Bearbeiten von Eigenschaften im COM+-Katalog

Jedes Element in einer Auflistung macht Eigenschaften verfügbar. Diese Eigenschaften dienen dazu, Konfigurationsdaten für jedes Element zu enthalten, das das Element darstellt. Im Verwaltungstool Komponentendienste werden diese Eigenschaften auf einer Eigenschaftenseite angezeigt, auf die Sie zugreifen, indem Sie mit der rechten Maustaste auf ein Element in einem Ordner klicken.

Da die Elemente in einer bestimmten Auflistung alle dieselbe Art von Objekten darstellen, machen diese Elemente einen Satz von Eigenschaften verfügbar, der in der gesamten Auflistung konsistent ist. Beispielsweise macht die [**Anwendungssammlung**](applications.md) eine Name-Eigenschaft, eine AppID-Eigenschaft usw. verfügbar. Dies entspricht der Art und Weise, in der jede Anwendung im Component Services-Verwaltungstool über eine konsistent strukturierte Eigenschaftenseite verfügt. Eine Liste der Eigenschaften, die für die Anwendungssammlung **verfügbar** sind, finden Sie unter **Anwendungen**. Eine Liste der Eigenschaften, die für die [**Components-Auflistung verfügbar**](components.md) sind, finden Sie unter **Komponenten**.

Eine vollständige Liste der Eigenschaften, die von Elementen in jeder Sammlung verfügbar gemacht werden, finden Sie unter [COM+-Verwaltungssammlungen.](com--administration-collections.md)

Sie stellen ein Element in einer Auflistung dar, indem Sie ein -Objekt verwenden, das aus der [**COMAdminCatalogObject-Klasse erstellt**](comadmincatalogobject.md) wurde. Mit diesem Objekt können Sie alle Eigenschaften festlegen und erhalten, die vom Element verfügbar gemacht werden. Beim Festlegen von Eigenschaften ist es auch möglich, dass Sie mit einem anderen Writer für den COM+-Katalog in Kontakt kommen. Weitere Informationen finden Sie unter [Getting and Setting Properties (Abrufen und Festlegen von Eigenschaften).](getting-and-setting-properties.md)

Nachdem Sie Eigenschaften festgelegt haben, werden keine Änderungen tatsächlich vorgenommen, bis Sie die Änderungen explizit speichern. Weitere Informationen finden Sie unter [Speichern oder Verwerfen von Änderungen.](saving-or-discarding-changes.md)

Wenn Sie Änderungen speichern, erzwingt der COM+-Katalog konfigurationslogik, um sicherzustellen, dass Sie keine Inkompatiblen Konfigurationen festlegen. Außerdem werden einige Eigenschaften für Sie geändert, wenn Sie bestimmte andere Eigenschaften explizit ändern. Weitere Informationen finden Sie unter [Interdependencies Between Properties](interdependencies-between-properties.md).

Darüber hinaus bietet COM+ eine Funktion, mit der Sie dynamisch abfragen können, um zu sehen, welche Eigenschaften für die Elemente in einer bestimmten Sammlung verfügbar sind. Weitere Informationen finden Sie unter [Abfragen von verfügbaren Eigenschaften.](querying-for-available-properties.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Verwaltungsvorgänge innerhalb von Transaktionen](com--administration-operations-within-transactions.md)
</dt> <dt>

[Behandeln von COM+-Verwaltungsfehlern](handling-com--administration-errors.md)
</dt> <dt>

[Einführendes Beispiel mit dem COM+-Verwaltungskatalog](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Abrufen von Sammlungen im COM+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



