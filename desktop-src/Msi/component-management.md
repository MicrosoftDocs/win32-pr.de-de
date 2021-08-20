---
description: Der Windows Installer reduziert die Gesamtbetriebskosten (TCO) Ihrer Anwendungen, indem er die Fähigkeit Ihrer Kunden erhöht, Anwendungskomponenten während des Setups und der Laufzeit zu verwalten und zu verwalten.
ms.assetid: fbb139e3-c81b-44fc-9e92-bada0be02862
title: Verwaltung von Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a818e6ceab0ed793ded2bdd0034d9fe8355d16fbbea1d5c78d521f4682b7c373
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144814"
---
# <a name="component-management"></a>Verwaltung von Komponenten

Der Windows Installer reduziert die Gesamtbetriebskosten (TCO) Ihrer Anwendungen, indem er die Fähigkeit Ihrer Kunden erhöht, Anwendungskomponenten während des Setups und der Laufzeit zu verwalten und zu verwalten. Die Installationsdatenbank verfolgt nach, welche Anwendungen eine bestimmte Komponente erfordern, welche Dateien die einzelnen Komponenten umfassen, wo jede Datei auf dem System installiert ist und wo sich Komponentenquellen befinden. Dadurch können Entwickler Pakete erstellen, die die folgenden Vorteile bieten:

-   Erhöhte Resilienz von Anwendungen. Verwenden Sie das Installationsprogramm, um beschädigte Komponenten zu erkennen und neu zu installieren, ohne das Setup erneut ausführen zu müssen. Das Installationsprogramm überprüft den Pfad einer Komponente zur Laufzeit. Dadurch werden Anwendungen von Abhängigkeiten von statischen Dateipfaden frei, die sich häufig zwischen Computern unterscheiden und auf fehlende Komponenten verweisen können. Weitere Informationen finden Sie unter [Resilienz.](resiliency.md)
-   Installation bei Bedarf. Dieser Featuresatz wird während des Setups nicht installiert, sondern in der Datenbank angegeben, die just-in-time für die zukünftige Verwendung durch die Anwendung installiert werden soll. Benutzer müssen das Setup nicht erneut ausführen. Weitere Informationen finden Sie unter [Installation On-Demand](installation-on-demand.md).
-   Ankündigung von Verknüpfungen zu Features, Anwendungen oder ganzen Produkten auf der Benutzeroberfläche. Benutzer können diese bei Bedarf mithilfe der Tastenkombinationen installieren. Benutzer können bei Bedarf auch Features, Anwendungen oder ganze Produkte entfernen. Weitere Informationen finden Sie unter [Advertisement](advertisement.md).
-   Anpassung der Installation. Ein Administrator kann Transformationen auf die Datenbank anwenden, die die Installation für eine bestimmte Gruppe von Benutzern anpassen. Weitere Informationen finden Sie unter [Anpassung](customization.md).
-   Einfachere Bereitstellung von Anwendungsupdates. Verwenden Sie das Installationsprogramm, um Ihre Produkte zu aktualisieren. Weitere Informationen finden Sie unter [Patchen und Aktualisieren von](patching-and-upgrades.md).
-   Featureverknüpfungsanzeige. Das Installationsprogramm zeigt Verknüpfungen zu Features an, die lokal mit Verknüpfungen zu Features ausgeführt werden, die remote ausgeführt werden. Da die Installationsdatenbank den Ausführungskontext der einzelnen Features angibt, können benutzern nach Bedarf sichtbar äquivalente Einstiegspunkte angezeigt werden.
-   Behalten Sie Nutzungsmetriken für Features bei. Entwickler können ein Installationspaket bereitstellen, das die Nutzungsanzahl eines Features für alle Clientanwendungen bei behält und Komponenten entfernt, die nicht verwendet werden.
-   Integrieren von Installationen. Entwickler können die Komponentenverwaltungsfunktionen des Installationsprogramms in ihre Anwendungen integrieren, indem sie ein Installationspaket erstellen und die [Installerfunktionen](installer-functions.md) in ihrem Anwendungscode verwenden. Die folgende Abbildung veranschaulicht eine Anwendung, die die Installation eines Features an fordert.

    ![-Anwendung, die die Featureinstallation an fordert. ](images/over1.png)

 

 



