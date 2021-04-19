---
description: Der Windows Installer speichert alle Informationen zur Installation in einer relationalen Datenbank. Sie können diese Datenbank und somit die Installation mithilfe von Transformationen und Zusammenführungen ändern.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Zusammenführungen und Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec6314e81afb5afa9d74346b64fe3129ba5ed30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349694"
---
# <a name="merges-and-transforms"></a>Zusammenführungen und Transformationen

Der Windows Installer speichert alle Informationen zur Installation in einer relationalen Datenbank. Sie können diese Datenbank und somit die Installation mithilfe von Transformationen und Zusammenführungen ändern.

## <a name="transforms"></a>Transformationen

Eine [Daten Bank Transformation](database-transforms.md) fügt Elemente in der ursprünglichen Datenbank hinzu oder ersetzt Sie. Eine Transformation kann z. b. den gesamten Text in der Benutzeroberfläche einer Anwendung von Französisch in Englisch ändern.

Zu den Haupt Verwendungsmöglichkeiten von Transformationen gehören:

-   Anpassung der Basis Installationspakete für bestimmte Gruppen von Benutzern.

    Transformationen können verwendet werden, um die verschiedenen Anpassungen eines einzelnen Basispakets zu kapseln, die von verschiedenen Benutzergruppen benötigt werden. Dies ist z. b. in Organisationen hilfreich, in denen die Support Abteilung für Finanzabteilung und Personal verschiedene Installationen eines bestimmten Produkts erfordert. Das Basispaket eines Produkts kann allen Benutzern an einem administrativen Installations Punkt zur Verfügung gestellt werden, wobei die entsprechenden Anpassungen separat an jede Benutzergruppe verteilt werden.

-   Sprachübergreifende Synchronisierung von Anwendungen.

    Transformationen sind nützlich, um Pakete, die an weit verbreiteten Positionen erstellt wurden, während der Erstellung synchronisiert zu halten. Wenn beispielsweise ein Upgrade zuerst für eine englische Version einer Anwendung entwickelt wird, die auf Englisch und Französisch vorhanden ist, kann eine Transformation auf die aktualisierte englische Version angewendet werden, die Sie in eine aktualisierte französische Version konvertiert.

    Mehrere Transformationen können auf ein Basispaket angewendet und dann während der Installation dynamisch angewendet werden. Dies erweitert die Funktionen des Installers zum Erstellen von benutzerdefinierten Paketen und bietet einen Mechanismus, mit dem die am besten geeigneten Installationen den verschiedenen Benutzergruppen effizient zugewiesen werden können.

-   Patchen von Anwendungen.

    Transformationen können verwendet werden, um eine geringfügige Korrektur für eine Anwendung anzuwenden, die kein großes Upgrade rechtfertigt. Weitere Informationen zu Patches finden Sie unter [Patch-Pakete](patch-packages.md).

## <a name="merges"></a>Merges

Ein Merge kombiniert zwei Datenbanken zu einer Datenbank und fügt Informationen hinzu, anstatt Sie zu ersetzen. Wenn die gleichen Informationen in beiden Datenbanken vorhanden sind, tritt ein Mergekonflikt auf. Zusammenführungen sind für Entwicklungsteams nützlich, da Sie es ermöglichen, eine große Anwendung in Teile zu unterteilen, die später erneut kombiniert werden können. Beispielsweise können die Datenbankelemente für die Installation einer neuen Komponente separat und später in der Haupt Installations Datenbank zusammengeführt werden. Weitere Informationen finden Sie unter zusammen [führen von Modulen](merge-modules.md).

Ein Entwicklungsteam kann einen Zusammenarbeits Vorgang folgendermaßen anwenden:

1.  Trennen Sie die Gruppen, und arbeiten Sie gleichzeitig an verschiedenen Komponenten einer großen Anwendung.
2.  Jede Entwicklungsgruppe füllt dann eine Datenbank mit Installationsinformationen für die eigene Komponente auf, ohne dass Sie sich mit den anderen Komponenten der Anwendung beschäftigt.
3.  Nachdem die Entwicklung einer Komponente vollständig ist, kann die Datenbank dieser Komponente in der Haupt Installations Datenbank für die gesamte Anwendung zusammengeführt werden.

 

 



