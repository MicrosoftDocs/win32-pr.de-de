---
description: Der Windows Installer speichert alle Informationen zur Installation in einer relationalen Datenbank. Sie können diese Datenbank und somit die Installation mithilfe von Transformationen und Zusammenführungen ändern.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Zusammenführungen und Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9779cd901df349b80dba84f056104c316810f8a3f67b19cdd4622dd68480ce1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012978"
---
# <a name="merges-and-transforms"></a>Zusammenführungen und Transformationen

Der Windows Installer speichert alle Informationen zur Installation in einer relationalen Datenbank. Sie können diese Datenbank und somit die Installation mithilfe von Transformationen und Zusammenführungen ändern.

## <a name="transforms"></a>Transformationen

Eine [Datenbanktransformation](database-transforms.md) fügt Elemente in der ursprünglichen Datenbank hinzu oder ersetzt sie. Eine Transformation kann beispielsweise den gesamten Text in der Benutzeroberfläche einer Anwendung von Französisch in Englisch ändern.

Zu den primären Verwendungsmöglichkeiten für Transformationen gehören:

-   Anpassung der Basisinstallationspakete für bestimmte Benutzergruppen.

    Transformationen können verwendet werden, um die verschiedenen Anpassungen eines einzelnen Basispakets zu kapseln, die für verschiedene Benutzergruppen erforderlich sind. Dies ist beispielsweise in Organisationen nützlich, in denen die Finanz- und Personalsupportabteilungen unterschiedliche Installationen eines bestimmten Produkts benötigen. Das Basispaket eines Produkts kann für alle Benutzer an einem administrativen Installationspunkt verfügbar sein, wobei die entsprechenden Anpassungen separat an jede Benutzergruppe verteilt werden.

-   Sprachübergreifende Synchronisierung von Anwendungen.

    Transformationen sind nützlich, um Pakete, die an weit getrennten Speicherorten erstellt werden, während der Erstellung synchronisiert zu halten. Wenn ein Upgrade beispielsweise zuerst für eine englische Version einer Anwendung entwickelt wird, die in Englisch und Französisch vorhanden ist, kann eine Transformation auf die aktualisierte englische Version angewendet werden, die sie in eine aktualisierte französische Version konvertiert.

    Mehrere Transformationen können auf ein Basispaket angewendet und dann während der Installation gleichzeitig angewendet werden. Dies erweitert die Funktionen des Installationsprogramms zum Erstellen benutzerdefinierter Pakete und bietet einen Mechanismus zum effizienten Zuweisen der am besten geeigneten Installationen zu verschiedenen Benutzergruppen.

-   Patchen von Anwendungen.

    Transformationen können verwendet werden, um eine kleinere Korrektur auf eine Anwendung anzuwenden, die kein größeres Upgrade erforderlich macht. Weitere Informationen zu Patches finden Sie unter [Patchpakete.](patch-packages.md)

## <a name="merges"></a>Merges

Eine Zusammenführung kombiniert zwei Datenbanken in einer Datenbank und fügt Informationen hinzu, anstatt sie zu ersetzen. Wenn die gleichen Informationen in beiden Datenbanken vorhanden sind, tritt ein Mergekonflikt auf. Zusammenführungen sind für Entwicklungsteams nützlich, da sie es ermöglichen, eine große Anwendung in Teile zu unterteilen, die später neu kombiniert werden können. Beispielsweise können die Datenbankelemente für die Installation einer neuen Komponente separat entwickelt und später mit der Hauptinstallationsdatenbank zusammengeführt werden. Weitere Informationen finden Sie unter [Merge Modules](merge-modules.md).

Ein Entwicklungsteam kann einen Mergevorgang wie folgt anwenden:

1.  Trennen Sie sie in Gruppen, und arbeiten Sie gleichzeitig an verschiedenen Komponenten einer großen Anwendung.
2.  Jede Entwicklungsgruppe füllt dann eine Datenbank mit Installationsinformationen für ihre eigene Komponente auf, ohne sich um die anderen Komponenten der Anwendung kümmern zu müssen.
3.  Nach Abschluss der Entwicklung einer Komponente kann die Datenbank dieser Komponente mit der Hauptinstallationsdatenbank für die gesamte Anwendung zusammengeführt werden.

 

 



