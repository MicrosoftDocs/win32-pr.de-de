---
description: Die COMAdmin-Objekte bieten ein einfaches Objektmodell, das Ihnen Zugriff auf den COM+-Katalog bietet.
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: Übersicht über die COMAdmin-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad382fcfab6e53a2eb8bfec9914a070d8a78e6ef2a29253005c324c8df8257e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070390"
---
# <a name="overview-of-the-comadmin-objects"></a>Übersicht über die COMAdmin-Objekte

Die COMAdmin-Objekte bieten ein einfaches Objektmodell, das Ihnen Zugriff auf den COM+-Katalog bietet. Dabei dienen sie dazu, alle Funktionen zu modellieren, die vom Verwaltungstool für Komponentendienste bereitgestellt werden. Bei jeder Art von COM+-Verwaltung interagieren Sie mit dem COM+-Katalog. Eine Beschreibung des Katalogs finden Sie unter [Zugreifen auf den COM+-Katalog.](accessing-the-com--catalog.md)

Die Informationen, die Sie entweder über das Component Services-Verwaltungstool oder mithilfe der COMAdmin-Objekte erhalten, sind ähnlich strukturiert, und die Aktionen, die Sie in beiden Kontexten ausführen, sind analog. Die grundlegende Korrelation zwischen der Verwendung des Komponentendienste-Snap-Ins und der programmgesteuerten Verwaltung ist, dass Ordner in der Konsolenstruktur des Snap-Ins Sammlungen im COM+-Katalog entsprechen. Dies bedeutet, dass jeder Ordner im Snap-In Elemente aller Art enthält. **COM+-Anwendungen** enthalten z. B. installierte COM+-Anwendungen– jede Sammlung im COM+-Katalog enthält Elemente einer einheitlichen Art. Ebenso wie jedes Element in einem Ordner Eigenschaften aufweist, die Sie auf einem Eigenschaftenblatt festlegen können, macht jedes Element in einer Auflistung Eigenschaften verfügbar, die Sie festlegen können.

Damit Sie Objekte innerhalb dieser Struktur konfigurieren können, bieten ihnen die COMAdmin-Objekte die folgenden Möglichkeiten:

-   Zugreifen auf den COM+-Katalog
-   Zugreifen auf Sammlungen im Katalog
-   Zugreifen auf Elemente in Sammlungen
-   Zugreifen auf Eigenschaften für die Elemente in den Sammlungen

Zur Unterstützung dieser Aktionen stellt die COMAdmin-Bibliothek die folgenden drei Klassen zur Verfügung:

-   [**COMAdminCatalog**](comadmincatalog.md), das den Katalog selbst darstellt.
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md), das eine beliebige Auflistung darstellt.
-   [**COMAdminCatalogObject**](comadmincatalogobject.md), das jedes Element in einer Auflistung darstellt.

Eine vollständige Beschreibung dieser Klassen finden Sie unter [Zusammenfassungsbeschreibung der COMAdmin-Klassen](summary-description-of-the-comadmin-classes.md) in diesem Abschnitt.

Eine schnelle Vorstellung von typischen Aktionen, die Sie in der programmgesteuerten Verwaltung ausführen, finden Sie unter [Einführungsbeispiel mit dem COM+-Verwaltungskatalog.](introductory-example-using-the-com--administration-catalog.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Verwaltungsvorgänge innerhalb von Transaktionen](com--administration-operations-within-transactions.md)
</dt> <dt>

[Behandeln von COM+-Verwaltungsfehlern](handling-com--administration-errors.md)
</dt> <dt>

[Einführendes Beispiel mit dem COM+-Verwaltungskatalog](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Abrufen von Sammlungen im COM+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Festlegen von Eigenschaften und Speichern von Änderungen am COM+-Katalog](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



