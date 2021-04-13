---
description: Die COMAdmin-Objekte bieten ein einfaches Objektmodell, das Ihnen den Zugriff auf den com+-Katalog ermöglicht.
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: Übersicht über die COMAdmin-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22837cbe0548b623463234d1a03d17288eba2149
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127789"
---
# <a name="overview-of-the-comadmin-objects"></a>Übersicht über die COMAdmin-Objekte

Die COMAdmin-Objekte bieten ein einfaches Objektmodell, das Ihnen den Zugriff auf den com+-Katalog ermöglicht. Auf diese Weise werden alle Funktionen des Verwaltungs Programms Komponenten Dienste modelliert. Jedes Mal, wenn Sie eine com+-Verwaltung durchführen, interagieren Sie mit dem com+-Katalog. Eine Beschreibung des Katalogs finden Sie unter [zugreifen auf den com+-Katalog](accessing-the-com--catalog.md).

Die Informationen, die Sie entweder über das Verwaltungs Programmkomponenten Dienste oder mithilfe der COMAdmin-Objekte erhalten, sind ähnlich strukturiert, und die Aktionen, die Sie in einem der beiden Kontext ausführen, sind analog. Die grundlegende Korrelation zwischen der Verwendung des Komponenten Dienste-Snap-Ins und der programmgesteuerten Verwaltung besteht darin, dass Ordner in der Konsolen Struktur des Snap-Ins den Sammlungen im com+-Katalog entsprechen. Das heißt, genauso wie jeder Ordner im Snap-in Elemente enthält alle Elemente. Beispielsweise enthält **com+-Anwendungen** installierte COM+-Anwendungen – jede Sammlung im com+-Katalog enthält Elemente mit einheitlicher Art. Ebenso wie jedes Element in einem Ordner über Eigenschaften verfügt, die Sie für ein Eigenschaften Blatt festlegen können, werden von jedem Element in einer Sammlung Eigenschaften verfügbar gemacht, die Sie festlegen können.

Damit Sie Objekte innerhalb dieser Struktur konfigurieren können, bieten die COMAdmin-Objekte Ihnen die Möglichkeit, die folgenden Aufgaben durchzuführen:

-   Zugreifen auf den com+-Katalog
-   Zugreifen auf Auflistungen im Katalog
-   Zugreifen auf Elemente in Auflistungen
-   Zugreifen auf Eigenschaften für die Elemente in den Auflistungen

Zur Unterstützung dieser Aktionen bietet die COMAdmin-Bibliothek die folgenden drei Klassen:

-   [**Comadmincatalog**](comadmincatalog.md), das den Katalog selbst darstellt.
-   [**Comadmincatalogcollection**](comadmincatalogcollection.md), die eine beliebige Sammlung darstellt.
-   [**COMAdminCatalogObject**](comadmincatalogobject.md), das jedes Element in einer Sammlung darstellt.

Ausführlichere Beschreibungen dieser Klassen finden Sie unter [Zusammenfassungs Beschreibung der COMAdmin-Klassen](summary-description-of-the-comadmin-classes.md) in diesem Abschnitt.

Einen kurzen Überblick über typische Aktionen, die Sie in der programmgesteuerten Verwaltung durchführen, finden Sie unter [Einführ Endes Beispiel mithilfe des com+-Verwaltungs Katalogs](introductory-example-using-the-com--administration-catalog.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Verwaltungsvorgänge in Transaktionen](com--administration-operations-within-transactions.md)
</dt> <dt>

[Behandeln von com+-Verwaltungsfehlern](handling-com--administration-errors.md)
</dt> <dt>

[Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Abrufen von Auflistungen im com+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Festlegen von Eigenschaften und Speichern von Änderungen am com+-Katalog](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



